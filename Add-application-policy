#this is a example for adding new application rules that open MDC required destination, but only include WW and US area.
#!/bin/bash
#chmod +x yourscript.sh
#./your-script.sh

# Variables
RG="your RG name"
FW="your firewall name"
az account set --subscription "your subscription id"

# Variables for Firewall Policy
POLICY_NAME="your azure firewall policy name"
RCG_NAME="DefaultApplicationRuleCollectionGroup" # or your custom group name
COLLECTION_NAME="DefaultRuleCollection" # or your custom collection name

az network firewall policy rule-collection-group collection rule add \
  --resource-group "$RG" \
  --policy-name "$POLICY_NAME" \
  --rule-collection-group-name "$RCG_NAME" \
  --collection-name "$COLLECTION_NAME" \
  --name "allow-ms-security" \
  --rule-type ApplicationRule \
  --source-addresses "*" \
  --protocols "https=443" \
  --target-fqdns \
crl.microsoft.com \
ctldl.windowsupdate.com \
www.microsoft.com \
events.data.microsoft.com \
x.cp.wd.microsoft.com \
cdn.x.cp.wd.microsoft.com \
officecdn-microsoft-com.akamaized.net \
packages.microsoft.com \
unitedstates.x.cp.wd.microsoft.com \
us-v20.events.data.microsoft.com \
winatp-gw-cus.microsoft.com \
winatp-gw-eus.microsoft.com \
winatp-gw-cus3.microsoft.com \
winatp-gw-eus3.microsoft.com \
automatedirstrprdcus.blob.core.windows.net \
automatedirstrprdeus.blob.core.windows.net \
automatedirstrprdcus3.blob.core.windows.net \
automatedirstrprdeus3.blob.core.windows.net \
ussus1eastprod.blob.core.windows.net \
ussus2eastprod.blob.core.windows.net \
ussus3eastprod.blob.core.windows.net \
ussus4eastprod.blob.core.windows.net \
wsus1eastprod.blob.core.windows.net \
wsus2eastprod.blob.core.windows.net \
ussus1westprod.blob.core.windows.net \
ussus2westprod.blob.core.windows.net \
ussus3westprod.blob.core.windows.net \
ussus4westprod.blob.core.windows.net \
wsus1westprod.blob.core.windows.net \
wsus2westprod.blob.core.windows.net \
go.microsoft.com \
definitionupdates.microsoft.com \
*.wdcp.microsoft.com \
*.wd.microsoft.com \
*.events.data.microsoft.com \
*.ecs.office.com \
*.smartscreen-prod.microsoft.com \
*.smartscreen.microsoft.com \
*.endpoint.security.microsoft.com
