SOL_URL=git@github.com:swimmer-network/bridge-solidity.git
SOL_VERSION="v1.0.0"

fetch-contracts:
	@echo " > \033[32mFetching chainbridge-solidity contracts... \033[0m "
	git clone -b original ${SOL_URL} chainbridge-solidity && cd chainbridge-solidity

compile:
	cd chainbridge-solidity && npm install && npx truffle compile

install: fetch-contracts compile
	@echo " > \033[32mInstalling cb-sol-cli... \033[0m "
	npm link .

clean:
	rm -rf chainbridge-solidity/