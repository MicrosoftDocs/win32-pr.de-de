---
description: In diesem Abschnitt wird veranschaulicht, wie Sie ein Skript schreiben, das das WinHttpRequest-Objekt verwendet, um auf Daten von einem Server zu zugreifen, für den eine HTTP-Authentifizierung erforderlich ist.
ms.assetid: 9e46777c-4d79-4f9b-9b31-1280ed1e3289
title: Authentifizierung mithilfe eines Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81e2dec50ccf765239bbbd1d6a71c8f8fb2be0e4f70f2db5717b0072f0b62d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052098"
---
# <a name="authentication-using-script"></a>Authentifizierung mithilfe eines Skripts

In diesem Abschnitt wird veranschaulicht, wie Sie ein Skript schreiben, das das [**WinHttpRequest-Objekt**](winhttprequest.md) verwendet, um auf Daten von einem Server zu zugreifen, für den eine HTTP-Authentifizierung erforderlich ist.

-   [Voraussetzungen und Anforderungen](#prerequisites-and-requirements)
-   [Zugreifen auf eine Website mit Authentifizierung](#accessing-a-web-site-with-authentication)
-   [Überprüfen der Statuscodes](#checking-the-status-codes)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites-and-requirements"></a>Voraussetzungen und Anforderungen

Zusätzlich zu den Kenntnissen zu Microsoft JScript erfordert dieses Beispiel Folgendes:

-   Die aktuelle Version des Microsoft Windows Software Development Kit (SDK).
-   Das Proxykonfigurationstool zum Einrichten der Proxyeinstellungen für Microsoft Windows HTTP Services (WinHTTP), wenn Ihre Verbindung mit dem Internet über einen Proxyserver hergestellt wird. Weitere [Proxycfg.exe finden Sie unterProxycfg.exe Proxykonfigurationstool.](proxycfg-exe--a-proxy-configuration-tool.md)
-   Vertrautheit mit [Netzwerkterminologie und](network-terminology.md) -konzepten.

## <a name="accessing-a-web-site-with-authentication"></a>Zugreifen auf eine Website mit Authentifizierung

**Gehen Sie wie folgt vor, um ein Skript zu erstellen, das die Authentifizierung veranschaulicht:**

1.  Öffnen Sie einen Text-Editor wie Microsoft Editor.
2.  Kopieren Sie den folgenden Code in den Text-Editor, nachdem Sie "authenticationSite" durch den entsprechenden Text ersetzt haben, um die URL einer Website anzugeben, die \[ \] HTTP-Authentifizierung erfordert.

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
4.  Geben Sie an einer Eingabeaufforderung "cscript Auth.js" ein, und drücken Sie die EINGABETASTE.

Sie verfügen nun über ein Programm, das eine Ressource auf zwei verschiedene Arten an fordert. Die erste Methode fordert die Ressource an, ohne Anmeldeinformationen anzugeben. Der Statuscode 401 wird zurückgegeben, um anzugeben, dass der Server eine Authentifizierung erfordert. Die Antwortheader werden ebenfalls angezeigt und sollten in etwa wie folgt aussehen:

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

Obwohl die Antwort darauf hinweist, dass der Zugriff auf die Ressource verweigert wurde, gibt sie dennoch mehrere Header zurück, die einige Informationen zur Ressource bereitstellen. Der Header "WWW-Authenticate" gibt an, dass der Server eine Authentifizierung für diese Ressource erfordert. Wenn es einen Header mit dem Namen "Proxy-Authenticate" gibt, bedeutet dies, dass der Proxyserver eine Authentifizierung erfordert. Jeder Authentifizierungsheader enthält ein verfügbares Authentifizierungsschema und manchmal einen Bereich. Beim Bereichswert wird die Kleinschreibung beachtet, und es wird eine Gruppe von Servern oder Proxys definiert, für die die gleichen Anmeldeinformationen akzeptiert werden sollen.

Es gibt zwei Header mit dem Namen "WWW-Authenticate", die angeben, dass mehrere Authentifizierungsschemas unterstützt werden. Wenn Sie die [**GetResponseHeader-Methode**](iwinhttprequest-getresponseheader.md) aufrufen, um "WWW-Authenticate"-Header zu suchen, gibt die Methode nur den Inhalt des ersten Headers dieses Namens zurück. In diesem Fall wird der Wert "NTLM" zurückgegeben. Um sicherzustellen, dass alle Vorkommen eines Headers verarbeitet werden, verwenden Sie stattdessen die [**GetAllResponseHeaders-Methode.**](iwinhttprequest-getallresponseheaders.md)

Der zweite Methodenaufruf fordert dieselbe Ressource an, stellt jedoch zunächst Authentifizierungsanmeldeinformationen durch Aufrufen der [**SetCredentials-Methode**](iwinhttprequest-setcredentials.md) zur Verfügung. Der folgende Codeabschnitt zeigt, wie diese Methode verwendet wird.


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



Diese Methode legt den Benutzernamen auf "UserName" und das Kennwort auf "Password" fest und gibt an, dass die Autorisierungsanmeldeinformationen für den Ressourcenserver gelten. Authentifizierungsanmeldeinformationen können auch an einen Proxy gesendet werden.

Wenn Anmeldeinformationen angegeben werden, gibt der Server den Statuscode 200 zurück, der angibt, dass das Dokument abgerufen werden kann.

## <a name="checking-the-status-codes"></a>Überprüfen der Statuscodes

Das vorherige Beispiel ist anweisungsbeweisig, erfordert jedoch, dass der Benutzer explizit Anmeldeinformationen anfordert. Eine Anwendung, die Anmeldeinformationen bei Bedarf und keine Anmeldeinformationen ankn gibt, wenn sie nicht erforderlich ist, ist nützlicher. Um eine Funktion zu implementieren, die dies tut, müssen Sie Das Beispiel ändern, um den Statuscode zu untersuchen, der mit der Antwort zurückgegeben wird.

Eine vollständige Liste der möglichen Statuscodes sowie Beschreibungen finden Sie unter [**HTTP-Statuscodes**](http-status-codes.md). In diesem Beispiel sollte jedoch nur einer von drei Codes auftreten. Der Statuscode 200 gibt an, dass eine Ressource verfügbar ist und mit der Antwort gesendet wird. Der Statuscode 401 gibt an, dass der Server eine Authentifizierung erfordert. Der Statuscode 407 gibt an, dass der Proxy eine Authentifizierung erfordert.

Ändern Sie das Beispiel, das Sie im letzten Abschnitt erstellt haben, indem Sie die Funktion "getText2" durch den folgenden Code ersetzen (ersetzen Sie "authenticationSite" durch Ihren eigenen Text, um die URL einer Website angibt, die HTTP-Authentifizierung \[ \] erfordert):


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



Speichern Sie die Datei erneut, und führen Sie sie aus. Die zweite Methode ruft das Dokument weiterhin ab, stellt jedoch nur bei Bedarf Anmeldeinformationen zurEntspricht. Die Funktion "getText2" führt die [**Open-**](iwinhttprequest-open.md) und [**Send-Methoden**](iwinhttprequest-send.md) so aus, als wäre keine Authentifizierung erforderlich. Der Status wird mit der [**Status-Eigenschaft**](iwinhttprequest-status.md) abgerufen, und eine switch-Anweisung antwortet auf den resultierenden Statuscode. Wenn der Status 401 (Server erfordert Authentifizierung) oder 407 (Proxy erfordert Authentifizierung) ist, wird die [**Open-Methode**](iwinhttprequest-open.md) erneut ausgeführt. Darauf folgt die [**SetCredentials-Methode,**](iwinhttprequest-setcredentials.md) mit der der Benutzername und das Kennwort festgelegt werden. Der Code schleife dann zurück zur [**Send-Methode.**](iwinhttprequest-send.md) Wenn die Ressource nach drei Versuchen nicht erfolgreich abgerufen werden kann, beendet die Funktion die Ausführung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Authentifizierung in WinHTTP](authentication-in-winhttp.md)
</dt> <dt>

[WinHttpRequest](winhttprequest.md)
</dt> <dt>

[**Setcredentials**](iwinhttprequest-setcredentials.md)
</dt> <dt>

[HTTP/1.1-Anforderung für Kommentare (RFC 2616)](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



