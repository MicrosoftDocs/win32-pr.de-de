---
description: Die Microsoft Windows HTTP-Dienste (WinHTTP) machen einen Satz von C/C++-Funktionen verfügbar, die Ihrer Anwendung den Zugriff auf http-Ressourcen im Web ermöglichen. Dieses Thema bietet einen Überblick darüber, wie diese Funktionen für die Interaktion mit einem HTTP-Server verwendet werden.
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: Übersicht über WinHTTP-Sitzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98dc8116dff75f279b87cb5f5ee6af607034176f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129257"
---
# <a name="winhttp-sessions-overview"></a>Übersicht über WinHTTP-Sitzungen

Die Microsoft Windows HTTP-Dienste (WinHTTP) machen einen Satz von C/C++-Funktionen verfügbar, die Ihrer Anwendung den Zugriff auf http-Ressourcen im Web ermöglichen. Dieses Thema bietet einen Überblick darüber, wie diese Funktionen für die Interaktion mit einem HTTP-Server verwendet werden.

-   [Verwenden der WinHTTP-API für den Zugriff auf das Web](#using-the-winhttp-api-to-access-the-web)
-   [Initialisieren von WinHTTP](#initializing-winhttp)
-   [Öffnen einer Anforderung](#opening-a-request)
-   [Anforderungs Header werden hinzugefügt](#adding-request-headers)
-   [Senden einer Anforderung](#sending-a-request)
-   [Veröffentlichen von Daten auf dem Server](#posting-data-to-the-server)
-   [Informationen zu einer Anforderung erhalten](#getting-information-about-a-request)
-   [Herunterladen von Ressourcen aus dem Web](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a>Verwenden der WinHTTP-API für den Zugriff auf das Web

Das folgende Diagramm zeigt die Reihenfolge, in der WinHTTP-Funktionen in der Regel bei der Interaktion mit einem HTTP-Server aufgerufen werden. Die schattierten Felder stellen Funktionen dar, die ein [hinternethandle](hinternet-handles-in-winhttp.md) generieren, während die einfachen Felder Funktionen darstellen, die diese Handles verwenden.

![Funktionen zum Erstellen von Handles](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a>Initialisieren von WinHTTP

Vor der Interaktion mit einem Server muss WinHTTP durch Aufrufen von [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)initialisiert werden. [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) erstellt einen Sitzungs Kontext, um Details zur HTTP-Sitzung beizubehalten, und gibt ein Sitzungs Handle zurück. Mithilfe dieses Handles kann die [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) -Funktion einen HTTP-oder Secure Hypertext Transfer Protocol (HTTPS)-Zielserver angeben.

> [!Note]  
> Ein [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) -Aufrufe führt nicht zu einer tatsächlichen Verbindung mit dem HTTP-Server, bis eine Anforderung für eine bestimmte Ressource erfolgt.

 

## <a name="opening-a-request"></a>Öffnen einer Anforderung

Die [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) -Funktion öffnet eine HTTP-Anforderung für eine bestimmte Ressource und gibt ein [HINTERNET](hinternet-handles-in-winhttp.md) -Handle zurück, das von den anderen HTTP-Funktionen verwendet werden kann. [**Winhttpopanrequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) sendet die Anforderung nicht an den Server, wenn Sie aufgerufen wird. Die [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) -Funktion stellt tatsächlich eine Verbindung über das Netzwerk her und sendet die Anforderung.

Das folgende Beispiel zeigt einen Beispiel Aufrufe von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) , der die Standardoptionen verwendet.

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a>Anforderungs Header werden hinzugefügt

Mit der [**winhttpadressquestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) -Funktion kann eine Anwendung zusätzliche freiformat-Anforderungs Header an das HTTP-Anforderungs handle anfügen. Es ist für die Verwendung durch anspruchsvolle Anwendungen vorgesehen, die eine genaue Kontrolle über die an den HTTP-Server gesendeten Anforderungen erfordern.

Die [**winhttpadressquestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) -Funktion erfordert ein von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstelltes HTTP-Anforderungs handle, eine Zeichenfolge, die die Header, die Länge der Header und alle Modifizierer enthält.

Die folgenden modifiziererer können mit [**winhttpadressquestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)verwendet werden.



| Modifizierer                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WinHTTP- \_ adressq- \_ Flag \_ Hinzufügen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | Fügt den Header hinzu, wenn er nicht vorhanden ist. Wird mit dem [**WinHTTP- \_ adressq- \_ Flag \_ ersetzen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)verwendet.                                                                                                                                                                                                               |
| [**WinHTTP- \_ adressq- \_ Flag \_ Add, \_ Wenn \_ neu**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | Fügt den Header nur hinzu, wenn er nicht bereits vorhanden ist. Andernfalls wird ein Fehler zurückgegeben.                                                                                                                                                                                                                                                           |
| [**WinHTTP- \_ adressq- \_ Flag \_ COALESCE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | Führt Header desselben Namens zusammen.                                                                                                                                                                                                                                                                                                              |
| [**WinHTTP- \_ adressq- \_ Flag \_ COALESCE \_ mit \_ Komma**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | Führt mit einem Komma Header desselben Namens zusammen. Das Hinzufügen von "Accept: Text/ \* " gefolgt von "Accept: Audio/ \* " mit diesem Flag bildet z. b. den einzelnen Header "Accept: Text/ \* , Audio/ \* " und bewirkt, dass der erste Header zusammengeführt wird. Es liegt an der aufrufenden Anwendung, ein zusammenhängendes Schema in Bezug auf zusammengeführte/separate Header sicherzustellen. |
| [**WinHTTP- \_ adressq- \_ Flag \_ COALESCE \_ mit \_ Semikolon**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | Führt mit einem Semikolon Header desselben Namens zusammen.                                                                                                                                                                                                                                                                                            |
| [**WinHTTP- \_ adressq- \_ Flag \_ ersetzen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | Ersetzt oder entfernt einen Header. Wenn der Header Wert leer ist und der Header gefunden wird, wird er entfernt. Wenn der Header Wert nicht leer ist, wird der Header Wert ersetzt.                                                                                                                                                                            |



 

## <a name="sending-a-request"></a>Senden einer Anforderung

Die [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) -Funktion stellt eine Verbindung mit dem Server her und sendet die Anforderung an die angegebene Site. Diese Funktion erfordert ein [hinternethandle](hinternet-handles-in-winhttp.md) , das von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt wurde. [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) kann auch zusätzliche Header oder optionale Informationen senden. Die optionalen Informationen werden im Allgemeinen für Vorgänge verwendet, die Informationen auf dem Server schreiben, z. b. Put und Post.

Nachdem die Funktion " [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) " die Anforderung gesendet hat, kann die Anwendung die Funktionen " [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) " und " [**winhttpquerydataavailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) " im [HINTERNET](hinternet-handles-in-winhttp.md) -Handle verwenden, um die Ressourcen des Servers herunterzuladen.

## <a name="posting-data-to-the-server"></a>Veröffentlichen von Daten auf dem Server

Zum Bereitstellen von Daten auf einem Server muss das [*http-Verb*](glossary.md) im [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) -Befehl entweder Post oder Put lauten. Wenn " [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) " aufgerufen wird, sollte der Parameter " *dwtotallength* " auf die Größe der Daten in Byte festgelegt werden. Verwenden Sie dann [**winhttpschreitedata**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) , um die Daten an den Server zu senden.

Alternativ können Sie den *lpoptional* -Parameter von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) auf die Adresse eines Puffers festlegen, der Daten enthält, die an den Server gesendet werden sollen. Wenn Sie dieses Verfahren verwenden, müssen Sie die Parameter " *dwoptionallength* " und " *dwtotallength* " von " [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) " auf die Größe der Daten festlegen, die gesendet werden. Wenn Sie [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) auf diese Weise aufrufen, entfällt die Notwendigkeit, [**winhttpschreitedata**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)aufzurufen.

## <a name="getting-information-about-a-request"></a>Informationen zu einer Anforderung erhalten

Die Funktion [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) ermöglicht einer Anwendung das Abrufen von Informationen zu einer HTTP-Anforderung. Die Funktion erfordert ein [hinternethandle](hinternet-handles-in-winhttp.md) , das von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), einem Wert auf Informationsebene und einer Pufferlänge erstellt wurde. [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) akzeptiert auch einen Puffer, in dem die Informationen gespeichert sind, sowie einen NULL basierten Header Index, der mehrere Header mit demselben Namen auflistet.

Verwenden Sie einen der auf der Seite [**abfrageinfoflags**](query-info-flags.md) gefundenen Werte auf Informationsebene mit einem-Modifizierer, um das Format zu steuern, in dem die Informationen im *lpvbuffer* -Parameter von [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)gespeichert werden.

## <a name="downloading-resources-from-the-web"></a>Herunterladen von Ressourcen aus dem Web

Nachdem Sie eine Anforderung mit der [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) -Funktion geöffnet, Sie mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)an den Server gesendet und das Anforderungs Handle für den Empfang einer Antwort mit [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)vorbereitet haben, kann die Anwendung die Funktionen [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) und [**winhttpquerydataavailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) zum Herunterladen der Ressource vom HTTP-Server verwenden.

Der folgende Beispielcode zeigt, wie Sie eine Ressource mit einer sicheren Transaktions Semantik herunterladen. Der Beispielcode initialisiert die WinHTTP-API (Application Programming Interface), wählt einen HTTPS-Zielserver aus und öffnet dann eine Anforderung für diese sichere Ressource. [**Winhttpquerydataavailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) wird mit dem Anforderungs Handle verwendet, um zu bestimmen, wie viele Daten heruntergeladen werden können, und anschließend wird [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) verwendet, um diese Daten zu lesen. Dieser Vorgang wird wiederholt, bis das gesamte Dokument abgerufen und angezeigt wird.


```C++
  DWORD dwSize = 0;
  DWORD dwDownloaded = 0;
  LPSTR pszOutBuffer;
  BOOL  bResults = FALSE;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTPS_PORT, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                   NULL, WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                   WINHTTP_FLAG_SECURE );

  // Send a request.
  if( hRequest )
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS, 0,
                                   WINHTTP_NO_REQUEST_DATA, 0, 
                                   0, 0 );


  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL );

  // Keep checking for data until there is nothing left.
  if( bResults )
  {
    do 
    {
      // Check for available data.
      dwSize = 0;
      if( !WinHttpQueryDataAvailable( hRequest, &dwSize ) )
        printf( "Error %u in WinHttpQueryDataAvailable.\n",
                GetLastError( ) );

      // Allocate space for the buffer.
      pszOutBuffer = new char[dwSize+1];
      if( !pszOutBuffer )
      {
        printf( "Out of memory\n" );
        dwSize=0;
      }
      else
      {
        // Read the data.
        ZeroMemory( pszOutBuffer, dwSize+1 );

        if( !WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                              dwSize, &dwDownloaded ) )
          printf( "Error %u in WinHttpReadData.\n", GetLastError( ) );
        else
          printf( "%s", pszOutBuffer );

        // Free the memory allocated to the buffer.
        delete [] pszOutBuffer;
      }
    } while( dwSize > 0 );
  }


  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
```



 

 



