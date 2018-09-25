# xtensysHMRC
Note: where "xtensyslpt02" appears, replace with "localhost" or remote W2O2 server

This project creates a proxy from a mock of the service of the HMRC Import Control System software SOAP API.
	https://www.gov.uk/government/publications/ics-technical-specifications-live-implementation-december-2014

SubmitEntrySummaryDeclaration = Mock service from HSBC compound WSDL
SubmitEntrySummaryDeclarationProxy = Proxy client of the WS02 Proxy service

1) Import the SOAPUI projects;
	http://localhost:8080/ = SOAPUI mocker endpoint
	http://localhost:8280 = WSO2 Proxy endpoint
2) Start either mock service from SubmitEntrySummaryDeclaration to either return a sucsess or error response type for etep 5;
3) In Eclipse import the SubmitEntrySummaryDeclarationESB.zip projects;
4) Link the SubmitEntrySummaryDeclarationESBCompositeApplication to a registered localhost WSO2 server;
5) Run the SOAPUI SubmitEntrySummaryDeclarationProxy test case three times:
	When no mock service is started
	When the error service is started
	When the sucsess service is started
	
