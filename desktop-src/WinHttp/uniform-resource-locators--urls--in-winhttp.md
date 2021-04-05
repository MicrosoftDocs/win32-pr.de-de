---
description: Eine URL ist eine kompakte Darstellung der Standort-und Zugriffsmethode für eine Ressource, die sich im Internet befindet.
ms.assetid: 940c414d-274f-475c-a50e-7a0853c3c26b
title: URL (Uniform Resource Locators) in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486ed3b17e2cf205f6ac815e87617a84e0ccc4cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042064"
---
# <a name="uniform-resource-locators-urls-in-winhttp"></a>URL (Uniform Resource Locators) in WinHTTP

Eine URL ist eine kompakte Darstellung der Standort-und Zugriffsmethode für eine Ressource, die sich im Internet befindet. Jede URL besteht aus einem Schema (http, HTTPS, FTP oder Gopher) und einer Schema spezifischen Zeichenfolge. Diese Zeichenfolge kann auch eine Kombination aus Verzeichnispfad, Such Zeichenfolge oder Name der Ressource enthalten. Die Microsoft Windows HTTP-Dienste (WinHTTP) bieten die Möglichkeit, URLs zu erstellen, zu kombinieren, aufzulösen und zu kanonisieren. Weitere Informationen finden Sie unter [RFC 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) und [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [Uniform Resource Identifiers (URI): generische Syntax](https://www.ietf.org/rfc/rfc1738.txt).

## <a name="what-is-a-canonicalized-url"></a>Was ist eine kanonisierte URL?

Die angegebene Syntax und die Semantik von URLs lassen Raum für Variation und Fehler aus. Kanonisierung ist der Prozess, bei dem eine tatsächliche URL in eine korrekte, "kanonische" Standardform normalisiert wird.

Dies umfasst das Codieren einiger Zeichen als "Escapesequenzen". Alphanumerische US-ASCII-Zeichen müssen nicht codiert werden (die Ziffern 0-9, die Großbuchstaben a-z und die Kleinbuchstaben a-z). Die meisten anderen Zeichen müssen mit Escapezeichen versehen werden, einschließlich Steuerzeichen, Leerzeichen, Prozentzeichen, "unsicheren Zeichen" (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ , \] und ') und allen Zeichen mit einem Codepunkt oberhalb von 127.

## <a name="using-the-winhttp-functions-to-handle-urls"></a>Verwenden der WinHTTP-Funktionen zum Verarbeiten von URLs

WinHTTP stellt zwei Funktionen zum Behandeln von URLs bereit. [**Winhttpknackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) trennt eine URL in Ihre Komponenten Teile, und [**winhttpkreateurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) erstellt eine URL aus-Komponenten.

### <a name="separating-urls"></a>Trennen von URLs

Die [**winhttpcrackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) -Funktion trennt eine URL in Ihre Komponenten Teile und gibt die von der [**URL- \_ Komponenten**](/windows/win32/api/winhttp/ns-winhttp-url_components) Struktur, die an die Funktion übergeben wird, aufgeführten Komponenten zurück.

Die Komponenten, die die [**URL- \_ Komponenten**](/windows/win32/api/winhttp/ns-winhttp-url_components) Struktur bilden, sind die Schema Nummer, der Hostname, die Portnummer, der Benutzername, das Kennwort, der URL-Pfad und zusätzliche Informationen, z. b. Suchparameter. Jede Komponente, außer dem Schema und den Portnummern, verfügt über einen Zeichen folgen Member, der die Informationen und einen Member enthält, der die Länge des zeichenfolgenmembers enthält. Das Schema und die Portnummern verfügen nur über einen Member, der den entsprechenden Wert speichert. sowohl das Schema als auch die Portnummern werden bei allen erfolgreichen Aufrufen von " [**winhttpcrackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)" zurückgegeben.

Zum Abrufen des Werts einer bestimmten Komponente in der Struktur der [**URL- \_ Komponenten**](/windows/win32/api/winhttp/ns-winhttp-url_components) muss der Member, der die Zeichen folgen Länge dieser Komponente speichert, auf einen Wert ungleich 0 (null) festgelegt werden. Der Zeichen folgen Member kann entweder ein Zeiger auf einen Puffer oder **null** sein.

Wenn das Zeigermember einen Zeiger auf einen Puffer enthält, muss der Zeichen folgen Längen Member die Größe dieses Puffers enthalten. Die [**winhttpcrackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) -Funktion gibt die Komponenten Informationen als Zeichenfolge im Puffer zurück und speichert die Zeichen folgen Länge im Member der Zeichen folgen Länge.

Wenn das Zeigermember auf **null** festgelegt ist, kann das Zeichen folgen Längen Element auf einen Wert ungleich 0 (null) festgelegt werden. Die [**winhttpknackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) -Funktion speichert einen Zeiger auf das erste Zeichen der URL-Zeichenfolge, die die Komponenten Informationen enthält, und legt die Zeichen folgen Länge auf die Anzahl der Zeichen im verbleibenden Teil der URL-Zeichenfolge fest, die sich auf die Komponente bezieht.

Alle Zeiger Elemente, die auf **null** festgelegt sind, mit einem Element, das nicht NULL ist, zeigen auf den entsprechenden Startpunkt in der URL-Zeichenfolge Die im Längen Element gespeicherte Länge muss verwendet werden, um das Ende der Informationen der einzelnen Komponente zu bestimmen.

Damit die Struktur der [**URL- \_ Komponenten**](/windows/win32/api/winhttp/ns-winhttp-url_components) ordnungsgemäß initialisiert wird, muss der **dwstructsize** -Member auf die Größe der [**URL- \_ Komponenten**](/windows/win32/api/winhttp/ns-winhttp-url_components) Struktur festgelegt werden.

### <a name="creating-urls"></a>Erstellen von URLs

Die [**winhttpkreateurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) -Funktion verwendet die Informationen in der zuvor beschriebenen Struktur der [**URL- \_ Komponenten**](/windows/win32/api/winhttp/ns-winhttp-url_components) , um eine URL zu erstellen.

Für jede erforderliche Komponente sollte das Zeigermember einen Zeiger auf den Puffer enthalten, der die Informationen enthält. Das Längen Element muss auf 0 (null) festgelegt werden, wenn das Zeigermember einen Zeiger auf eine mit NULL endende Zeichenfolge enthält. Das Längen Element muss auf die Länge der Zeichenfolge festgelegt werden, wenn das Zeiger Element einen Zeiger auf eine Zeichenfolge enthält, die nicht mit 0 (null) beendet wird. Das Zeigermember von Komponenten, die nicht erforderlich sind, muss auf **null** festgelegt werden.

### <a name="sample-code"></a>Beispielcode

Der folgende Beispielcode zeigt, wie Sie [**winhttpcrackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) und [**winhttpkreateurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) verwenden, um eine vorhandene URL zu disassemblieren, eine ihrer Komponenten zu ändern und Sie einer neuen URL hinzuzufügen.


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



 

 



