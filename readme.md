<!--
SPDX-FileCopyrightText: 2021 Open Networking Foundation <info@opennetworking.org>

SPDX-License-Identifier: Apache-2.0
SPDX-License-Identifier: LicenseRef-ONF-Member-Only-1.0
-->

# free5GC Web Console

Prior to building webconsole, install nodejs and yarn package first:
```bash
sudo apt remove cmdtest
sudo apt remove yarn
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update
sudo apt-get install -y nodejs yarn
```

To run free5GC webconsole server. The following steps are to be considered.
```bash
# (In directory: ~/free5gc/webconsole)
cd frontend
yarn install
yarn build
rm -rf ../public
cp -R build ../public
```

### Run the Server
```bash
# (In directory: ~/free5gc/webconsole)
go run server.go
```
