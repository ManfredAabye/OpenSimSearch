# Diverse Tests

[Search]

	; This line is optional and shows the default.
	Module = "OpenSimSearch"
	; The SearchURL is important. It must be correct or search won't work.
	; Change the URL to point to the query.php file on your own web server
	;SearchURL = "http://192.168.0.1/query.php"
	SearchURL = "http://${Const|BaseHostname/oswebinterface/query.php"


[SimulatorFeatures]

    ;# {SearchServerURI} {} {URL of the search server} {}
    ;; Optional. If given this serves the same purpose as the grid wide
    ;; [LoginServices] SearchURL setting and will override that where
    ;; supported by viewers.
    SearchServerURI = "${Const|BaseURL}:${Const|PublicPort}/oswebinterface/searchservice.php";

    ;# {DestinationGuideURI} {} {URL of the destination guide} {}
    ;; Optional. If given this serves the same purpose as the grid wide
    ;; [LoginServices] DestinationGuide setting and will override that where
    ;; supported by viewers.
    DestinationGuideURI = "${Const|BaseURL}/oswebinterface/guide.php"
