---
description: Microsoft Windows HTTP Services (WinHTTP) macht eine Reihe von C/C++-Funktionen verfügbar, mit denen Ihre Anwendung auf HTTP-Ressourcen im Web zugreifen kann. Dieses Thema bietet eine Übersicht darüber, wie diese Funktionen für die Interaktion mit einem HTTP-Server verwendet werden.
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: Übersicht über WinHTTP-Sitzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f7c2a3845b34ac306c1fb8d87441955ab9f4cfe0e1ea250737f62f993cd43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743904"
---
# <a name="winhttp-sessions-overview"></a>Übersicht über WinHTTP-Sitzungen

Microsoft Windows HTTP Services (WinHTTP) macht eine Reihe von C/C++-Funktionen verfügbar, mit denen Ihre Anwendung auf HTTP-Ressourcen im Web zugreifen kann. Dieses Thema bietet eine Übersicht darüber, wie diese Funktionen für die Interaktion mit einem HTTP-Server verwendet werden.

-   [Verwenden der WinHTTP-API für den Webzugriff](#using-the-winhttp-api-to-access-the-web)
-   [Initialisieren von WinHTTP](#initializing-winhttp)
-   [Öffnen einer Anforderung](#opening-a-request)
-   [Hinzufügen von Anforderungsheadern](#adding-request-headers)
-   [Senden einer Anforderung](#sending-a-request)
-   [Bereitstellen von Daten auf dem Server](#posting-data-to-the-server)
-   [Abrufen von Informationen zu einer Anforderung](#getting-information-about-a-request)
-   [Herunterladen von Ressourcen aus dem Web](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a>Verwenden der WinHTTP-API für den Webzugriff

Das folgende Diagramm zeigt die Reihenfolge, in der WinHTTP-Funktionen bei der Interaktion mit einem HTTP-Server normalerweise aufgerufen werden. Die schattierten Felder stellen Funktionen dar, die ein [HINTERNET-Handle](hinternet-handles-in-winhttp.md) generieren, während die einfachen Felder Funktionen darstellen, die diese Handles verwenden.

![Funktionen, die Handles erstellen](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a>Initialisieren von WinHTTP

Vor der Interaktion mit einem Server muss WinHTTP durch Aufrufen von [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)initialisiert werden. [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) erstellt einen Sitzungskontext, um Details zur HTTP-Sitzung zu verwalten, und gibt ein Sitzungshandle zurück. Mit diesem Handle kann die [**WinHttpConnect-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) dann einen HTTP- oder HTTPS-Zielserver (Secure Hypertext Transfer Protocol) angeben.

> [!Note]  
> Ein Aufruf von [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) führt erst dann zu einer tatsächlichen Verbindung mit dem HTTP-Server, wenn eine Anforderung für eine bestimmte Ressource erfolgt.

 

## <a name="opening-a-request"></a>Öffnen einer Anforderung

Die [**WinHttpOpenRequest-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) öffnet eine HTTP-Anforderung für eine bestimmte Ressource und gibt ein [HINTERNET-Handle](hinternet-handles-in-winhttp.md) zurück, das von den anderen HTTP-Funktionen verwendet werden kann. [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) sendet die Anforderung nicht an den Server, wenn sie aufgerufen wird. Die [**WinHttpSendRequest-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) stellt tatsächlich eine Verbindung über das Netzwerk her und sendet die Anforderung.

Das folgende Beispiel zeigt einen Beispielaufruf von [**WinHttpOpenRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) der die Standardoptionen verwendet.

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a>Hinzufügen von Anforderungsheadern

Mit [**der WinHttpAddRequestHeaders-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) kann eine Anwendung zusätzliche Anforderungsheader im Freiformat an das HTTP-Anforderungshandle anfügen. Es ist für die Verwendung durch anspruchsvolle Anwendungen vorgesehen, die eine genaue Kontrolle über die an den HTTP-Server gesendeten Anforderungen erfordern.

Die [**WinHttpAddRequestHeaders-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) erfordert ein http-Anforderungshandle, das von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt wurde, eine Zeichenfolge, die die Header, die Länge der Header und alle Modifizierer enthält.

Die folgenden Modifizierer können mit [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)verwendet werden.



| Modifizierer                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WINHTTP \_ ADDREQ \_ FLAG \_ ADD**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | Fügt den Header hinzu, wenn er nicht vorhanden ist. Wird mit [**WINHTTP \_ ADDREQ \_ FLAG \_ REPLACE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)verwendet.                                                                                                                                                                                                               |
| [**WINHTTP \_ ADDREQ \_ FLAG \_ ADD \_ IF \_ NEW**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | Fügt den Header nur hinzu, wenn er noch nicht vorhanden ist. Andernfalls wird ein Fehler zurückgegeben.                                                                                                                                                                                                                                                           |
| [**WINHTTP \_ ADDREQ \_ FLAG \_ COALESCE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | Führt Header mit dem gleichen Namen zusammen.                                                                                                                                                                                                                                                                                                              |
| [**WINHTTP \_ ADDREQ \_ FLAG \_ COALESCE \_ WITH \_ COMMA**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | Führt Header mit dem gleichen Namen unter Verwendung eines Kommas zusammen. Wenn Sie z. B. "Accept: text/ \* " gefolgt von "Accept: audio/ \* " mit diesem Flag hinzufügen, wird der einzelne Header "Accept: text/ \* , audio/ " \* angezeigt, sodass der erste gefundene Header zusammengeführt wird. Es obliegt der aufrufenden Anwendung, ein einheitliches Schema in Bezug auf zusammengeführte/separate Header sicherzustellen. |
| [**WINHTTP \_ ADDREQ FLAG COALESCE WITH SEMICOLON (ZUSAMMENFÜGEN DES WINHTTP-ADDREQ-FLAGS \_ \_ MIT \_ \_ SEMIKOLON)**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | Führt Header mit dem gleichen Namen mithilfe eines Semikolons zusammen.                                                                                                                                                                                                                                                                                            |
| [**WINHTTP \_ ADDREQ \_ FLAG \_ REPLACE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | Ersetzt oder entfernt einen Header. Wenn der Headerwert leer ist und der Header gefunden wird, wird er entfernt. Wenn der Headerwert nicht leer ist, wird der Headerwert ersetzt.                                                                                                                                                                            |



 

## <a name="sending-a-request"></a>Senden einer Anforderung

Die [**WinHttpSendRequest-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) stellt eine Verbindung mit dem Server her und sendet die Anforderung an den angegebenen Standort. Diese Funktion erfordert ein [HINTERNET-Handle,](hinternet-handles-in-winhttp.md) das von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt wurde. [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) kann auch zusätzliche Header oder optionale Informationen senden. Die optionalen Informationen werden in der Regel für Vorgänge verwendet, die Informationen auf den Server schreiben, z. B. PUT und POST.

Nachdem die [**WinHttpSendRequest-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) die Anforderung gesendet hat, kann die Anwendung die Funktionen [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) und [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) auf dem [HINTERNET-Handle](hinternet-handles-in-winhttp.md) verwenden, um die Ressourcen des Servers herunterzuladen.

## <a name="posting-data-to-the-server"></a>Bereitstellen von Daten auf dem Server

Um Daten an einen Server zu veröffentlichen, muss das [*HTTP-Verb*](glossary.md) im Aufruf von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) entweder POST oder PUT sein. Wenn [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) aufgerufen wird, sollte der *dwTotalLength-Parameter* auf die Größe der Daten in Bytes festgelegt werden. Verwenden Sie dann [**WinHttpWriteData,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) um die Daten auf dem Server zu veröffentlichen.

Alternativ können Sie den *lpOptional-Parameter* von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) auf die Adresse eines Puffers festlegen, der Daten enthält, die an den Server gesendet werden sollen. Wenn Sie diese Technik verwenden, müssen Sie sowohl die *Parameter dwOptionalLength* als auch *dwTotalLength* von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) auf die Größe der bereitgestellten Daten festlegen. Durch das Aufrufen von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) auf diese Weise entfällt die Notwendigkeit, [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)aufzurufen.

## <a name="getting-information-about-a-request"></a>Abrufen von Informationen zu einer Anforderung

Mit [**der WinHttpQueryHeaders-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) kann eine Anwendung Informationen zu einer HTTP-Anforderung abrufen. Die Funktion erfordert ein [HINTERNET-Handle,](hinternet-handles-in-winhttp.md) das von [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellt wurde, einen Informationsebenenwert und eine Pufferlänge. [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) akzeptiert auch einen Puffer, der die Informationen speichert, und einen nullbasierten Headerindex, der mehrere Header mit dem gleichen Namen aufzählt.

Verwenden Sie einen der Werte auf Informationsebene auf der Seite [**Abfrageinformationsflags**](query-info-flags.md) mit einem Modifizierer, um das Format zu steuern, in dem die Informationen im *lpvBuffer-Parameter* von [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)gespeichert werden.

## <a name="downloading-resources-from-the-web"></a>Herunterladen von Ressourcen aus dem Web

Nach dem Öffnen einer Anforderung mit der [**WinHttpOpenRequest-Funktion,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) dem Senden an den Server mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)und dem Vorbereiten des Anforderungshandles für den Empfang einer Antwort mit [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)kann die Anwendung die Funktionen [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) und [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) verwenden, um die Ressource vom HTTP-Server herunterzuladen.

Der folgende Beispielcode zeigt, wie Sie eine Ressource mit sicherer Transaktionssemantik herunterladen. Der Beispielcode initialisiert die WinHTTP-Api (Application Programming Interface), wählt einen HTTPS-Zielserver aus und öffnet dann eine Anforderung für diese sichere Ressource und sendet sie. [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) wird mit dem Anforderungshandle verwendet, um zu bestimmen, wie viele Daten zum Herunterladen verfügbar sind. Anschließend wird [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) zum Lesen dieser Daten verwendet. Dieser Vorgang wird wiederholt, bis das gesamte Dokument abgerufen und angezeigt wurde.


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



 

 



