.PHONY: angular
angular:
	# Test Angular2 build
	cp package.json-angular2 package.json
	rm -rf node_modules
	npm install
	if [ ! -e node_modules ]; then mkdir node_modules; fi
	if [ ! -e node_modules/xlsx ]; then cd node_modules; ln -s ../../../ xlsx; cd -; fi
	npm run build

	# Test Angular4 build
	cp package.json-angular4 package.json
	rm -rf node_modules
	npm install
	if [ ! -e node_modules ]; then mkdir node_modules; fi
	if [ ! -e node_modules/xlsx ]; then cd node_modules; ln -s ../../../ xlsx; cd -; fi
	npm run build

	# Test Angular5 build
	cp package.json-angular5 package.json
	rm -rf node_modules
	npm install
	if [ ! -e node_modules ]; then mkdir node_modules; fi
	if [ ! -e node_modules/xlsx ]; then cd node_modules; ln -s ../../../ xlsx; cd -; fi
	npm run build

.PHONY: ionic
ionic:
	bash ./ionic.sh

.PHONY: ios android browser
ios android browser: ionic
	cd SheetJSIonic; ionic cordova emulate $@ </dev/null; cd -

