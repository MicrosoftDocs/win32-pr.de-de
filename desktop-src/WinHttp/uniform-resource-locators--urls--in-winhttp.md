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
# <a name="uniform-resource-locators-urls-in-winhttp"></a><span data-ttu-id="f8eb9-103">URL (Uniform Resource Locators) in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="f8eb9-103">Uniform Resource Locators (URLs) in WinHTTP</span></span>

<span data-ttu-id="f8eb9-104">Eine URL ist eine kompakte Darstellung der Standort-und Zugriffsmethode für eine Ressource, die sich im Internet befindet.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-104">A URL is a compact representation of the location and access method for a resource located on the Internet.</span></span> <span data-ttu-id="f8eb9-105">Jede URL besteht aus einem Schema (http, HTTPS, FTP oder Gopher) und einer Schema spezifischen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-105">Each URL consists of a scheme (HTTP, HTTPS, FTP, or Gopher) and a scheme-specific string.</span></span> <span data-ttu-id="f8eb9-106">Diese Zeichenfolge kann auch eine Kombination aus Verzeichnispfad, Such Zeichenfolge oder Name der Ressource enthalten.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-106">This string can also include a combination of a directory path, search string, or name of the resource.</span></span> <span data-ttu-id="f8eb9-107">Die Microsoft Windows HTTP-Dienste (WinHTTP) bieten die Möglichkeit, URLs zu erstellen, zu kombinieren, aufzulösen und zu kanonisieren.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-107">The Microsoft Windows HTTP Services (WinHTTP) functions provide the ability to create, combine, break down, and canonicalize URLs.</span></span> <span data-ttu-id="f8eb9-108">Weitere Informationen finden Sie unter [RFC 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) und [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [Uniform Resource Identifiers (URI): generische Syntax](https://www.ietf.org/rfc/rfc1738.txt).</span><span class="sxs-lookup"><span data-stu-id="f8eb9-108">For more information, see [RFC 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) and [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [Uniform Resource Identifiers (URI): Generic Syntax](https://www.ietf.org/rfc/rfc1738.txt).</span></span>

## <a name="what-is-a-canonicalized-url"></a><span data-ttu-id="f8eb9-109">Was ist eine kanonisierte URL?</span><span class="sxs-lookup"><span data-stu-id="f8eb9-109">What Is a Canonicalized URL?</span></span>

<span data-ttu-id="f8eb9-110">Die angegebene Syntax und die Semantik von URLs lassen Raum für Variation und Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-110">The specified syntax and semantics of URLs leaves room for variation and error.</span></span> <span data-ttu-id="f8eb9-111">Kanonisierung ist der Prozess, bei dem eine tatsächliche URL in eine korrekte, "kanonische" Standardform normalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-111">Canonicalization is the process of normalizing an actual URL into a correct, standard, "canonical" form.</span></span>

<span data-ttu-id="f8eb9-112">Dies umfasst das Codieren einiger Zeichen als "Escapesequenzen".</span><span class="sxs-lookup"><span data-stu-id="f8eb9-112">This involves coding some characters as "escape sequences."</span></span> <span data-ttu-id="f8eb9-113">Alphanumerische US-ASCII-Zeichen müssen nicht codiert werden (die Ziffern 0-9, die Großbuchstaben a-z und die Kleinbuchstaben a-z).</span><span class="sxs-lookup"><span data-stu-id="f8eb9-113">Alphanumeric US-ASCII characters need not be encoded (the digits 0-9, the capital letters A-Z, and the lowercase letters a-z).</span></span> <span data-ttu-id="f8eb9-114">Die meisten anderen Zeichen müssen mit Escapezeichen versehen werden, einschließlich Steuerzeichen, Leerzeichen, Prozentzeichen, "unsicheren Zeichen" (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ , \] und ') und allen Zeichen mit einem Codepunkt oberhalb von 127.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-114">Most other characters must be escaped, including control characters, the space character, the percent sign, "unsafe characters" ( <, >, ", \#, {, }, \|, \\, ^, ~, \[, \], and ' ), and all characters with a code point above 127.</span></span>

## <a name="using-the-winhttp-functions-to-handle-urls"></a><span data-ttu-id="f8eb9-115">Verwenden der WinHTTP-Funktionen zum Verarbeiten von URLs</span><span class="sxs-lookup"><span data-stu-id="f8eb9-115">Using the WinHTTP Functions to Handle URLs</span></span>

<span data-ttu-id="f8eb9-116">WinHTTP stellt zwei Funktionen zum Behandeln von URLs bereit.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-116">WinHTTP provides two functions for handling URLs.</span></span> <span data-ttu-id="f8eb9-117">[**Winhttpknackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) trennt eine URL in Ihre Komponenten Teile, und [**winhttpkreateurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) erstellt eine URL aus-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-117">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separates a URL into its component parts, and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) creates a URL from components.</span></span>

### <a name="separating-urls"></a><span data-ttu-id="f8eb9-118">Trennen von URLs</span><span class="sxs-lookup"><span data-stu-id="f8eb9-118">Separating URLs</span></span>

<span data-ttu-id="f8eb9-119">Die [**winhttpcrackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) -Funktion trennt eine URL in Ihre Komponenten Teile und gibt die von der [**URL- \_ Komponenten**](/windows/win32/api/winhttp/ns-winhttp-url_components) Struktur, die an die Funktion übergeben wird, aufgeführten Komponenten zurück.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-119">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function separates a URL into its component parts and returns the components indicated by the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure that is passed to the function.</span></span>

<span data-ttu-id="f8eb9-120">Die Komponenten, die die [**URL- \_ Komponenten**](/windows/win32/api/winhttp/ns-winhttp-url_components) Struktur bilden, sind die Schema Nummer, der Hostname, die Portnummer, der Benutzername, das Kennwort, der URL-Pfad und zusätzliche Informationen, z. b. Suchparameter.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-120">The components that make up the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure are the scheme number, host name, port number, user name, password, URL path, and additional information such as search parameters.</span></span> <span data-ttu-id="f8eb9-121">Jede Komponente, außer dem Schema und den Portnummern, verfügt über einen Zeichen folgen Member, der die Informationen und einen Member enthält, der die Länge des zeichenfolgenmembers enthält.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-121">Each component, except the scheme and port numbers, has a string member that holds the information and a member that holds the length of the string member.</span></span> <span data-ttu-id="f8eb9-122">Das Schema und die Portnummern verfügen nur über einen Member, der den entsprechenden Wert speichert. sowohl das Schema als auch die Portnummern werden bei allen erfolgreichen Aufrufen von " [**winhttpcrackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-122">The scheme and port numbers have only a member that stores the corresponding value; both the scheme and port numbers are returned on all successful calls to [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).</span></span>

<span data-ttu-id="f8eb9-123">Zum Abrufen des Werts einer bestimmten Komponente in der Struktur der [**URL- \_ Komponenten**](/windows/win32/api/winhttp/ns-winhttp-url_components) muss der Member, der die Zeichen folgen Länge dieser Komponente speichert, auf einen Wert ungleich 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-123">To retrieve the value of a particular component in the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure, the member that stores the string length of that component must be set to a nonzero value.</span></span> <span data-ttu-id="f8eb9-124">Der Zeichen folgen Member kann entweder ein Zeiger auf einen Puffer oder **null** sein.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-124">The string member can be either a pointer to a buffer or **NULL**.</span></span>

<span data-ttu-id="f8eb9-125">Wenn das Zeigermember einen Zeiger auf einen Puffer enthält, muss der Zeichen folgen Längen Member die Größe dieses Puffers enthalten.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-125">If the pointer member contains a pointer to a buffer, the string length member must contain the size of that buffer.</span></span> <span data-ttu-id="f8eb9-126">Die [**winhttpcrackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) -Funktion gibt die Komponenten Informationen als Zeichenfolge im Puffer zurück und speichert die Zeichen folgen Länge im Member der Zeichen folgen Länge.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-126">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function returns the component information as a string in the buffer and stores the string length in the string length member.</span></span>

<span data-ttu-id="f8eb9-127">Wenn das Zeigermember auf **null** festgelegt ist, kann das Zeichen folgen Längen Element auf einen Wert ungleich 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-127">If the pointer member is set to **NULL**, the string length member can be set to any nonzero value.</span></span> <span data-ttu-id="f8eb9-128">Die [**winhttpknackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) -Funktion speichert einen Zeiger auf das erste Zeichen der URL-Zeichenfolge, die die Komponenten Informationen enthält, und legt die Zeichen folgen Länge auf die Anzahl der Zeichen im verbleibenden Teil der URL-Zeichenfolge fest, die sich auf die Komponente bezieht.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-128">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function stores a pointer to the first character of the URL string that contains the component information and sets the string length to the number of characters in the remaining part of the URL string that pertains to the component.</span></span>

<span data-ttu-id="f8eb9-129">Alle Zeiger Elemente, die auf **null** festgelegt sind, mit einem Element, das nicht NULL ist, zeigen auf den entsprechenden Startpunkt in der URL-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f8eb9-129">All pointer members set to **NULL** with a nonzero length member point to the appropriate starting point in the URL string.</span></span> <span data-ttu-id="f8eb9-130">Die im Längen Element gespeicherte Länge muss verwendet werden, um das Ende der Informationen der einzelnen Komponente zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-130">The length stored in the length member must be used to determine the end of the individual component's information.</span></span>

<span data-ttu-id="f8eb9-131">Damit die Struktur der [**URL- \_ Komponenten**](/windows/win32/api/winhttp/ns-winhttp-url_components) ordnungsgemäß initialisiert wird, muss der **dwstructsize** -Member auf die Größe der [**URL- \_ Komponenten**](/windows/win32/api/winhttp/ns-winhttp-url_components) Struktur festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-131">To finish initializing the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure properly, the **dwStructSize** member must be set to the size of the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure.</span></span>

### <a name="creating-urls"></a><span data-ttu-id="f8eb9-132">Erstellen von URLs</span><span class="sxs-lookup"><span data-stu-id="f8eb9-132">Creating URLs</span></span>

<span data-ttu-id="f8eb9-133">Die [**winhttpkreateurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) -Funktion verwendet die Informationen in der zuvor beschriebenen Struktur der [**URL- \_ Komponenten**](/windows/win32/api/winhttp/ns-winhttp-url_components) , um eine URL zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-133">The [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) function uses the information in the previously described [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure to create a URL.</span></span>

<span data-ttu-id="f8eb9-134">Für jede erforderliche Komponente sollte das Zeigermember einen Zeiger auf den Puffer enthalten, der die Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-134">For each required component, the pointer member should contain a pointer to the buffer that holds the information.</span></span> <span data-ttu-id="f8eb9-135">Das Längen Element muss auf 0 (null) festgelegt werden, wenn das Zeigermember einen Zeiger auf eine mit NULL endende Zeichenfolge enthält. Das Längen Element muss auf die Länge der Zeichenfolge festgelegt werden, wenn das Zeiger Element einen Zeiger auf eine Zeichenfolge enthält, die nicht mit 0 (null) beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-135">The length member should be set to zero if the pointer member contains a pointer to a zero-terminated string; the length member should be set to the string length if the pointer member contains a pointer to a string that is not zero-terminated.</span></span> <span data-ttu-id="f8eb9-136">Das Zeigermember von Komponenten, die nicht erforderlich sind, muss auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-136">The pointer member of any components that are not required must be set to **NULL**.</span></span>

### <a name="sample-code"></a><span data-ttu-id="f8eb9-137">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="f8eb9-137">Sample code</span></span>

<span data-ttu-id="f8eb9-138">Der folgende Beispielcode zeigt, wie Sie [**winhttpcrackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) und [**winhttpkreateurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) verwenden, um eine vorhandene URL zu disassemblieren, eine ihrer Komponenten zu ändern und Sie einer neuen URL hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f8eb9-138">The following sample code shows how to use the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) to disassemble an existing URL, modify one of its components, and reassemble it into a new URL.</span></span>


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



 

 



