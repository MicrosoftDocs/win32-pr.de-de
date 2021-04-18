---
description: In diesem Abschnitt wird veranschaulicht, wie Sie ein Skript schreiben, das das WinHttpRequest-Objekt verwendet, um auf Daten von einem Server zuzugreifen, für den HTTP-Authentifizierung
ms.assetid: 9e46777c-4d79-4f9b-9b31-1280ed1e3289
title: Authentifizierung mithilfe eines Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1d33b8042cd1fd15d46e15dfb3624e0d3b4a885b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358484"
---
# <a name="authentication-using-script"></a>Authentifizierung mithilfe eines Skripts

In diesem Abschnitt wird veranschaulicht, wie Sie ein Skript schreiben, das das [**WinHttpRequest**](winhttprequest.md) -Objekt verwendet, um auf Daten von einem Server zuzugreifen, für den HTTP-Authentifizierung

-   [Voraussetzungen und Anforderungen](#prerequisites-and-requirements)
-   [Zugreifen auf eine Website mit Authentifizierung](#accessing-a-web-site-with-authentication)
-   [Überprüfen der Status Codes](#checking-the-status-codes)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites-and-requirements"></a>Voraussetzungen und Anforderungen

Zusätzlich zu den in Microsoft JScript funktionierenden Kenntnissen erfordert dieses Beispiel Folgendes:

-   Die aktuelle Version des Microsoft Windows Software Development Kit (SDK).
-   Das Proxy Konfigurationstool zum Einrichten der Proxy Einstellungen für Microsoft Windows HTTP-Dienste (WinHTTP), wenn die Internetverbindung über einen Proxy Server erfolgt. Weitere Informationen finden Sie [ unterProxycfg.exe, einem Proxy Konfigurations Tool](proxycfg-exe--a-proxy-configuration-tool.md) .
-   Eine Vertrautheit mit der [Netzwerkterminologie](network-terminology.md) und den Konzepten.

## <a name="accessing-a-web-site-with-authentication"></a>Zugreifen auf eine Website mit Authentifizierung

**Gehen Sie folgendermaßen vor, um ein Skript zu erstellen, das die Authentifizierung veranschaulicht:**

1.  Öffnen Sie einen Text-Editor, z. b. Microsoft Notepad.
2.  Kopieren Sie den folgenden Code in den Text-Editor \[ , nachdem Sie "authenticationsite \] " durch den entsprechenden Text ersetzt haben, um die URL einer Website anzugeben, die die HTTP-Authentifizierung erfordert.

    ```VB
    // Load the WinHttpRequest object.
    var WinHttpReq = 
              new ActiveXObject("WinHttp.WinHttpRequest.5.1");

    function getText1( )
    {
      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false;

      // Send a request to the server and wait for a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "No Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText);
      WScript.Echo( WinHttpReq.GetAllResponseHeaders);
      WScript.Echo( );
    };

    function getText2( )
    {
      // HttpRequest SetCredentials flags
      HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;

      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false );

      // Set credentials for server.
      WinHttpReq.SetCredentials( "User Name", 
                                 "Password",
                                 HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

      // It might also be necessary to supply credentials 
      // to the proxy if you connect to the Internet 
      // through a proxy that requires authentication.

      // Send a request to the server and wait for 
      // a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
      WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
      WScript.Echo( );
    };

    getText1( );
    getText2( );
    ```

    

3.  Speichern Sie die Datei als "Auth.js".
4.  Geben Sie an einer Eingabeaufforderung "Cscript Auth.js" ein, und drücken Sie die EINGABETASTE.

Sie verfügen jetzt über ein Programm, das eine Ressource auf zwei verschiedene Arten anfordert. Die erste Methode fordert die Ressource ohne Angabe von Anmelde Informationen an. Der Statuscode 401 wird zurückgegeben, um anzugeben, dass für den Server eine Authentifizierung erforderlich ist. Die Antwortheader werden ebenfalls angezeigt und sollten in etwa wie folgt aussehen:

``` syntax
Connection: Keep-Alive
Content-Length: 0
Date: Fri, 27 Apr 2001 01:47:18 GMT
Content-Type: text/html
Server: Microsoft-IIS/5.0
WWW-Authenticate: NTLM
WWW-Authenticate: Negotiate
Cache-control: private
```

Obwohl die Antwort anzeigt, dass der Zugriff auf die Ressource verweigert wurde, gibt Sie weiterhin mehrere Header zurück, die einige Informationen über die Ressource bereitstellen. Der Header mit dem Namen "www-Authenticate" gibt an, dass der Server eine Authentifizierung für diese Ressource erfordert. Wenn ein Header mit dem Namen "Proxy-Authenticate" vorhanden ist, weist dies darauf hin, dass für den Proxy Server eine Authentifizierung erforderlich ist. Jeder authentifizieren-Header enthält ein verfügbares Authentifizierungsschema und manchmal einen Bereich. Beim Bereichs Wert wird die Groß-/Kleinschreibung beachtet, und es wird eine Gruppe von Servern oder Proxys definiert, für die dieselben Anmelde Informationen akzeptiert werden.

Es gibt zwei Header mit dem Namen "www-Authenticate", die angeben, dass mehrere Authentifizierungs Schemas unterstützt werden. Wenn Sie die [**getrespontsheader**](iwinhttprequest-getresponseheader.md) -Methode für die Suche nach "www-Authenticate"-Headern aufzurufen, gibt die Methode nur den Inhalt des ersten Headers dieses Namens zurück. In diesem Fall wird der Wert "NTLM" zurückgegeben. Um sicherzustellen, dass alle Vorkommen eines Headers verarbeitet werden, verwenden Sie stattdessen die [**getallresponsheaders**](iwinhttprequest-getallresponseheaders.md) -Methode.

Der zweite Methodenaufruf fordert dieselbe Ressource an, gibt jedoch zuerst Anmelde Informationen für die Authentifizierung an, indem die [**setanmelde**](iwinhttprequest-setcredentials.md) -Methode aufgerufen wird. Der folgende Code Abschnitt zeigt, wie diese Methode verwendet wird.


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



Mit dieser Methode wird der Benutzername auf "username" und das Kennwort auf "Password" festgelegt, und es wird angegeben, dass die Anmelde Informationen für die Autorisierung für den Ressourcen Server gelten Anmelde Informationen für die Authentifizierung können auch an einen Proxy gesendet werden.

Wenn Anmelde Informationen angegeben werden, gibt der Server den Statuscode 200 zurück, der angibt, dass das Dokument abgerufen werden kann.

## <a name="checking-the-status-codes"></a>Überprüfen der Status Codes

Das vorherige Beispiel ist Anweisungs basiert, erfordert jedoch, dass der Benutzer explizit Anmelde Informationen bereitstellt. Eine Anwendung, die Anmelde Informationen bei Bedarf bereitstellt und keine Anmelde Informationen bereitstellt, wenn dies nicht erforderlich ist, ist nützlicher. Zum Implementieren eines Features, das dies bewirkt, müssen Sie das Beispiel ändern, um den mit der Antwort zurückgegebenen Statuscode zu untersuchen.

Eine umfassende Liste der möglichen Statuscodes sowie Beschreibungen finden Sie unter http- [**Statuscodes**](http-status-codes.md). In diesem Beispiel sollten Sie jedoch nur einen von drei Codes sehen. Der Statuscode 200 zeigt an, dass eine Ressource verfügbar ist und mit der Antwort gesendet wird. Der Statuscode 401 zeigt an, dass für den Server eine Authentifizierung erforderlich ist. Der Statuscode 407 zeigt an, dass für den Proxy eine Authentifizierung erforderlich ist.

Ändern Sie das Beispiel, das Sie im letzten Abschnitt erstellt haben, indem Sie die Funktion "getText2" durch den folgenden Code ersetzen (ersetzen \[ Sie "authenticationsite \] " durch ihren eigenen Text, und geben Sie die URL einer Website an, die die HTTP-Authentifizierung erfordert):


```VB
function getText2() {
  WScript.Echo( "Credentials: " );

  // HttpRequest SetCredentials flags.
  HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
  HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

  // Specify the target resource.
  var targURL = "https://[authenticationSite]";
  WinHttpReq.open( "GET", targURL, false );

  var Done = false;
  var Attempts = 0;
  do
  {
    // Keep track of the number of request attempts.
    Attempts++;

    // Send a request to the server and wait for a response.
    WinHttpReq.send( );

    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status)
    {
      // A 200 status indicates that the resource was retrieved.
      case 200:
        Done = true;
        break;

      // A 401 status indicates that the server 
      // requires authentication.
      case 401:
        WScript.Echo( "Requires Server UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the server.
        WinHttpReq.SetCredentials( "User Name", 
                             "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        break;

      // A 407 status indicates that the proxy 
      // requires authentication.
      case 407:
        WScript.Echo( "Requires Proxy UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the proxy.
        WinHttpReq.SetCredentials( "User Name", 
                              "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_PROXY );
        break;
    }
  } while( ( !Done ) && ( Attempts < 3 ) );

  // Display the results of the request.
  WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
  WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
  WScript.Echo( );
};
```



Speichern Sie die Datei erneut, und führen Sie Sie aus. Die zweite Methode ruft das Dokument weiterhin ab, stellt jedoch nur bei Bedarf Anmelde Informationen bereit. Die Funktion "getText2" führt die [**Open**](iwinhttprequest-open.md) -Methode und die [**Send**](iwinhttprequest-send.md) -Methode aus, als wäre keine Authentifizierung erforderlich. Der Status wird mit der [**Status**](iwinhttprequest-status.md) -Eigenschaft abgerufen, und eine Switch-Anweisung antwortet auf den resultierenden Statuscode. Wenn der Status 401 (Server erfordert Authentifizierung) oder 407 (Proxy erfordert Authentifizierung) lautet, wird die [**Open**](iwinhttprequest-open.md) -Methode erneut ausgeführt. Danach folgt die [**setanmelde**](iwinhttprequest-setcredentials.md) -Methode, mit der der Benutzername und das Kennwort festgelegt werden. Der Code wird dann zurück zur [**Send**](iwinhttprequest-send.md) -Methode. Wenn die Ressource nach drei versuchen nicht erfolgreich abgerufen werden kann, wird die Ausführung beendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Authentifizierung in WinHTTP](authentication-in-winhttp.md)
</dt> <dt>

[WinHttpRequest](winhttprequest.md)
</dt> <dt>

[**SetCredentials**](iwinhttprequest-setcredentials.md)
</dt> <dt>

[HTTP/1.1-Anforderung für Kommentare (RFC 2616)](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



