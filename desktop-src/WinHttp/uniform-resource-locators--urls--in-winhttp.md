---
description: Eine URL ist eine kompakte Darstellung des Speicherorts und der Zugriffsmethode für eine Ressource im Internet.
ms.assetid: 940c414d-274f-475c-a50e-7a0853c3c26b
title: Uniform Resource Locators (URLs) in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 798d18dd2e3d2095e175904fcc2f3a332d618100174f174510c98780b06a57ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133007"
---
# <a name="uniform-resource-locators-urls-in-winhttp"></a>Uniform Resource Locators (URLs) in WinHTTP

Eine URL ist eine kompakte Darstellung des Speicherorts und der Zugriffsmethode für eine Ressource im Internet. Jede URL besteht aus einem Schema (HTTP, HTTPS, FTP oder Gopher) und einer schemaspezifischen Zeichenfolge. Diese Zeichenfolge kann auch eine Kombination aus einem Verzeichnispfad, einer Suchzeichenfolge oder einem Namen der Ressource enthalten. Die WinHTTP-Funktionen (Microsoft Windows HTTP Services) bieten die Möglichkeit, URLs zu erstellen, zu kombinieren, aufzubrechen und zu kanonisieren. Weitere Informationen finden Sie unter [RFC 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) und [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [Uniform Resource Identifiers (URI): Generische Syntax](https://www.ietf.org/rfc/rfc1738.txt).

## <a name="what-is-a-canonicalized-url"></a>Was ist eine kanonisierte URL?

Die angegebene Syntax und Semantik von URLs lässt Platz für Variationen und Fehler. Kanonisierung ist der Prozess der Normalisierung einer tatsächlichen URL in eine korrekte, standardmäßige, "kanonische" Form.

Dies umfasst das Codieren einiger Zeichen als "Escapesequenzen". Alphanumerische US-ASCII-Zeichen müssen nicht codiert werden (die Ziffern 0 bis 9, die Großbuchstaben A-Z und die Kleinbuchstaben a-z). Die meisten anderen Zeichen müssen mit Escapezeichen markiert werden, einschließlich Steuerzeichen, Leerzeichen, Prozentzeichen, "unsichere Zeichen" ( <, >, ", \# , {, }, \| , , \\ ^, ~, \[ , , und ' ) und alle Zeichen mit einem \] Codepunkt über 127.

## <a name="using-the-winhttp-functions-to-handle-urls"></a>Verwenden der WinHTTP-Funktionen zum Verarbeiten von URLs

WinHTTP stellt zwei Funktionen für die Verarbeitung von URLs bereit. [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) trennt eine URL in seine Komponenten, und [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) erstellt eine URL aus Komponenten.

### <a name="separating-urls"></a>Trennen von URLs

Die [**WinHttpCrackUrl-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) trennt eine URL in ihre Komponententeile und gibt die Komponenten zurück, die durch die [**URL \_ COMPONENTS-Struktur**](/windows/win32/api/winhttp/ns-winhttp-url_components) angegeben werden, die an die Funktion übergeben wird.

Die Komponenten, aus denen sich die [**URL \_ COMPONENTS-Struktur**](/windows/win32/api/winhttp/ns-winhttp-url_components) zusammensetzt, sind Schemanummer, Hostname, Portnummer, Benutzername, Kennwort, URL-Pfad und zusätzliche Informationen wie Suchparameter. Jede Komponente, mit Ausnahme des Schemas und der Portnummern, verfügt über einen Zeichenfolgenmember, der die Informationen enthält, und einen Member, der die Länge des Zeichenfolgenmembers enthält. Das Schema und die Portnummern verfügen nur über ein Element, das den entsprechenden Wert speichert. sowohl das Schema als auch die Portnummern werden bei allen erfolgreichen Aufrufen von [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)zurückgegeben.

Um den Wert einer bestimmten Komponente in der [**URL \_ COMPONENTS-Struktur**](/windows/win32/api/winhttp/ns-winhttp-url_components) abzurufen, muss der Member, der die Zeichenfolgenlänge dieser Komponente speichert, auf einen Wert ungleich 0 (null) festgelegt werden. Der Zeichenfolgenmember kann entweder ein Zeiger auf einen Puffer oder **NULL** sein.

Wenn der Zeigermember einen Zeiger auf einen Puffer enthält, muss der Zeichenfolgenlängenmember die Größe dieses Puffers enthalten. Die [**WinHttpCrackUrl-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) gibt die Komponenteninformationen als Zeichenfolge im Puffer zurück und speichert die Zeichenfolgenlänge im Zeichenfolgenlängenmember.

Wenn der Zeigermember auf **NULL** festgelegt ist, kann der Zeichenfolgenlängenmember auf einen beliebigen Wert ungleich 0 (null) festgelegt werden. Die [**WinHttpCrackUrl-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) speichert einen Zeiger auf das erste Zeichen der URL-Zeichenfolge, die die Komponenteninformationen enthält, und legt die Zeichenfolgenlänge auf die Anzahl der Zeichen im verbleibenden Teil der URL-Zeichenfolge fest, die sich auf die Komponente bezieht.

Alle Zeigermember, die auf **NULL** festgelegt sind, mit einem Memberpunkt ungleich 0 (null) zeigen auf den entsprechenden Startpunkt in der URL-Zeichenfolge. Die im Längenmember gespeicherte Länge muss verwendet werden, um das Ende der Informationen der einzelnen Komponente zu bestimmen.

Um die Initialisierung der [**URL \_ COMPONENTS-Struktur**](/windows/win32/api/winhttp/ns-winhttp-url_components) ordnungsgemäß abzuschließen, muss der **dwStructSize-Member** auf die Größe der [**URL \_ COMPONENTS-Struktur**](/windows/win32/api/winhttp/ns-winhttp-url_components) festgelegt werden.

### <a name="creating-urls"></a>Erstellen von URLs

Die [**WinHttpCreateUrl-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) verwendet die Informationen in der zuvor beschriebenen [**URL \_ COMPONENTS-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-url_components) um eine URL zu erstellen.

Für jede erforderliche Komponente sollte der Zeigermember einen Zeiger auf den Puffer enthalten, der die Informationen enthält. Der Längenmember sollte auf 0 (null) festgelegt werden, wenn der Zeigermember einen Zeiger auf eine auf null endende Zeichenfolge enthält. der Length-Member sollte auf die Zeichenfolgenlänge festgelegt werden, wenn der Zeigermember einen Zeiger auf eine Zeichenfolge enthält, die nicht null terminiert ist. Der Zeigermember aller Komponenten, die nicht erforderlich sind, muss auf **NULL** festgelegt werden.

### <a name="sample-code"></a>Beispielcode

Der folgende Beispielcode zeigt, wie [**Sie winHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) und [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) verwenden, um eine vorhandene URL zu disassemblieren, eine ihrer Komponenten zu ändern und sie in einer neuen URL neu zusammenzusetzen.


```C++
  URL_COMPONENTS urlComp;
  LPCWSTR pwszUrl1 = 
    L"https://search.msn.com/results.asp?RS=CHECKED&FORM=MSNH&v=1&q=wininet";
  DWORD dwUrlLen = 0;

  // Initialize the URL_COMPONENTS structure.
  ZeroMemory(&urlComp, sizeof(urlComp));
  urlComp.dwStructSize = sizeof(urlComp);

  // Set required component lengths to non-zero so that they are cracked.
  urlComp.dwSchemeLength    = (DWORD)-1;
  urlComp.dwHostNameLength  = (DWORD)-1;
  urlComp.dwUrlPathLength   = (DWORD)-1;
  urlComp.dwExtraInfoLength = (DWORD)-1;

  // Crack the URL.
  if( !WinHttpCrackUrl( pwszUrl1, (DWORD)wcslen(pwszUrl1), 0, &urlComp ) )
      printf( "Error %u in WinHttpCrackUrl.\n", GetLastError( ) );
  else
  {
    // Change the search information.  New info is the same length.
    urlComp.lpszExtraInfo = L"?RS=CHECKED&FORM=MSNH&v=1&q=winhttp";

    // Obtain the size of the new URL and allocate memory.
    WinHttpCreateUrl( &urlComp, 0, NULL, &dwUrlLen );
    LPWSTR pwszUrl2 = new WCHAR[dwUrlLen];

    // Create a new URL.
    if( !WinHttpCreateUrl( &urlComp, 0, pwszUrl2, &dwUrlLen ) )
      printf( "Error %u in WinHttpCreateUrl.\n", GetLastError( ) );
    else
    {
      // Show both URLs.
      printf( "Old URL:  %S\nNew URL:  %S\n", pwszUrl1, pwszUrl2 );
    }

    // Free allocated memory.
    delete [] pwszUrl2;
  }
```



 

 



