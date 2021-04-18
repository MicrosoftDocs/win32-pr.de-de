---
title: Verwalten von Cookies
description: Unter dem HTTP-Protokoll werden von einem Server oder einem Skript Cookies verwendet, um Zustandsinformationen auf der Client Arbeitsstation beizubehalten.
ms.assetid: c00279cf-9cdc-4caf-8549-af1851edfa25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0418442e961f6f4d3d2bcddb2c607ac9cf7928
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338278"
---
# <a name="managing-cookies"></a><span data-ttu-id="c6511-103">Verwalten von Cookies</span><span class="sxs-lookup"><span data-stu-id="c6511-103">Managing Cookies</span></span>

<span data-ttu-id="c6511-104">Unter dem HTTP-Protokoll werden von einem Server oder einem Skript Cookies verwendet, um Zustandsinformationen auf der Client Arbeitsstation beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="c6511-104">Under the http protocol, a server or a script uses cookies to maintain state information on the client workstation.</span></span> <span data-ttu-id="c6511-105">Die WinInet-Funktionen haben zu diesem Zweck eine persistente Cookie-Datenbank implementiert.</span><span class="sxs-lookup"><span data-stu-id="c6511-105">The WinINet functions have implemented a persistent cookie database for this purpose.</span></span> <span data-ttu-id="c6511-106">Sie können verwendet werden, um Cookies in der cookiedatenbank festzulegen und auf Cookies zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c6511-106">They can be used to set cookies in and access cookies from the cookie database.</span></span> <span data-ttu-id="c6511-107">Weitere Informationen finden Sie unter [http-Cookies](http-cookies.md).</span><span class="sxs-lookup"><span data-stu-id="c6511-107">For more information, see [HTTP Cookies](http-cookies.md).</span></span>

<span data-ttu-id="c6511-108">Die Funktionen [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) und [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) können zum Verwalten von Cookies verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6511-108">The [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) and [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) functions can be used to manage cookies.</span></span>

## <a name="using-cookie-functions"></a><span data-ttu-id="c6511-109">Verwenden von Cookie-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c6511-109">Using Cookie Functions</span></span>

<span data-ttu-id="c6511-110">Mit den folgenden Funktionen kann eine Anwendung Cookies in der cookiedatenbank erstellen oder abrufen.</span><span class="sxs-lookup"><span data-stu-id="c6511-110">The following functions allow an application to create or retrieve cookies in the cookie database.</span></span>



| <span data-ttu-id="c6511-111">Funktion</span><span class="sxs-lookup"><span data-stu-id="c6511-111">Function</span></span>                                       | <span data-ttu-id="c6511-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6511-112">Description</span></span>                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="c6511-113">**InternetGetCookie**</span><span class="sxs-lookup"><span data-stu-id="c6511-113">**InternetGetCookie**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) | <span data-ttu-id="c6511-114">Ruft Cookies für die angegebene URL und alle übergeordneten URLs ab.</span><span class="sxs-lookup"><span data-stu-id="c6511-114">Retrieves cookies for the specified URL and all its parent URLs.</span></span> |
| [<span data-ttu-id="c6511-115">**InternetSetCookie**</span><span class="sxs-lookup"><span data-stu-id="c6511-115">**InternetSetCookie**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) | <span data-ttu-id="c6511-116">Legt ein Cookie für die angegebene URL fest.</span><span class="sxs-lookup"><span data-stu-id="c6511-116">Sets a cookie on the specified URL.</span></span>                              |



 

<span data-ttu-id="c6511-117">Beachten Sie, dass diese Funktionen keinen [**Internet Open**](/windows/desktop/api/Wininet/nf-wininet-internetopena)-aufrufbedarf erfordern.</span><span class="sxs-lookup"><span data-stu-id="c6511-117">Note that these functions do not require a call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="c6511-118">Cookies, die ein Ablaufdatum aufweisen, werden im lokalen Benutzerkonto unter Benutzer \\ Benutzername " \\ AppData \\ Roaming \\ Microsoft \\ Windows \\ Cookies-Verzeichnis" und Benutzer \\ "Benutzername" \\ AppData \\ Roaming \\ \\ von Microsoft Windows \\ Cookies Low-Directory für Anwendungen gespeichert, die mit \\ niedrigen Berechtigungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c6511-118">Cookies that have an expiration date are stored in the local users account under Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies directory, and the Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies\\Low directory for applications running under low privileges.</span></span> <span data-ttu-id="c6511-119">Cookies, die kein Ablaufdatum aufweisen, werden im Arbeitsspeicher gespeichert und sind nur für den Prozess verfügbar, in dem Sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="c6511-119">Cookies that do not have an expiration date are stored in memory and are available only to the process in which they were created.</span></span>

<span data-ttu-id="c6511-120">Wie im Thema [http-Cookies](http-cookies.md) erwähnt, gibt die [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) -Funktion keine Cookies zurück, die vom Server als nicht skriptfähig gekennzeichnet wurden, mit dem Attribut "HttpOnly" im Set-Cookie-Header.</span><span class="sxs-lookup"><span data-stu-id="c6511-120">As noted in the [HTTP Cookies](http-cookies.md) topic, the [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) function does not return cookies that have been marked by the server as non-scriptable with the "HttpOnly" attribute in the Set-Cookie header.</span></span>

### <a name="getting-a-cookie"></a><span data-ttu-id="c6511-121">Ein Cookie wird erhalten.</span><span class="sxs-lookup"><span data-stu-id="c6511-121">Getting a Cookie</span></span>

<span data-ttu-id="c6511-122">[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) gibt die Cookies für die angegebene URL und alle übergeordneten URLs zurück.</span><span class="sxs-lookup"><span data-stu-id="c6511-122">[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) returns the cookies for the specified URL and all its parent URLs.</span></span>

<span data-ttu-id="c6511-123">Im folgenden Beispiel wird ein Aufrufen von [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c6511-123">The following example demonstrates a call to [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).</span></span>


```C++
TCHAR szURL[256];         // buffer to hold the URL
LPTSTR lpszData = NULL;   // buffer to hold the cookie data
DWORD dwSize=0;           // variable to get the buffer size needed

// Insert code to retrieve the URL.

retry:

// The first call to InternetGetCookie will get the required
// buffer size needed to download the cookie data.
if (!InternetGetCookie(szURL, NULL, lpszData, &dwSize))
{
    // Check for an insufficient buffer error.
    if (GetLastError()== ERROR_INSUFFICIENT_BUFFER)
    {
        // Allocate the necessary buffer.
        lpszData = new TCHAR[dwSize];

        // Try the call again.
        goto retry;
    }
    else
    {
        // Insert error handling code.
    }
}
else
{
    // Insert code to display the cookie data.

    // Release the memory allocated for the buffer.
    delete[]lpszData;
}
```



### <a name="setting-a-cookie"></a><span data-ttu-id="c6511-124">Festlegen eines Cookies</span><span class="sxs-lookup"><span data-stu-id="c6511-124">Setting a Cookie</span></span>

<span data-ttu-id="c6511-125">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) wird verwendet, um ein Cookie für die angegebene URL festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c6511-125">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) is used to set a cookie on the specified URL.</span></span> <span data-ttu-id="c6511-126">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) kann sowohl persistente als auch Sitzungs Cookies erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6511-126">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) can create both persistent and session cookies.</span></span>

<span data-ttu-id="c6511-127">Persistente Cookies haben ein Ablaufdatum.</span><span class="sxs-lookup"><span data-stu-id="c6511-127">Persistent cookies have an expiration date.</span></span> <span data-ttu-id="c6511-128">Diese Cookies werden im lokalen Benutzerkonto unter Benutzer \\ Benutzername " \\ AppData \\ Roaming \\ Microsoft \\ Windows \\ Cookies-Verzeichnis" und Benutzer \\ "Benutzername" \\ AppData \\ Roaming \\ Microsoft \\ Windows \\ Cookies \\ Low Directory für Anwendungen, die mit niedrigen Berechtigungen ausgeführt werden, gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c6511-128">These cookies are stored in the local users account under Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies directory, and the Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies\\Low directory for applications running under low privileges.</span></span>

<span data-ttu-id="c6511-129">Sitzungs Cookies werden im Arbeitsspeicher gespeichert, und nur der Prozess, der Sie erstellt hat, kann darauf zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="c6511-129">Session cookies are stored in memory and can be accessed only by the process that created them.</span></span>

<span data-ttu-id="c6511-130">Die Daten für das Cookie sollten folgendes Format aufweisen:</span><span class="sxs-lookup"><span data-stu-id="c6511-130">The data for the cookie should be in the format:</span></span>

``` syntax
NAME=VALUE
```

<span data-ttu-id="c6511-131">Für das Ablaufdatum muss das Format wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="c6511-131">For the expiration date, the format must be:</span></span>

``` syntax
DAY, DD-MMM-YYYY HH:MM:SS GMT
```

<span data-ttu-id="c6511-132">Day ist die drei buchstabige Abkürzung für den Wochentag. dd ist der Tag des Monats, mmm ist die drei buchstabige Abkürzung für den Monat, yyyy ist das Jahr, und hh: mm: SS ist die Uhrzeit des Tages in der militärischen Zeit.</span><span class="sxs-lookup"><span data-stu-id="c6511-132">DAY is the three-letter abbreviation for the day of the week, DD is the day of the month, MMM is the three-letter abbreviation for the month, YYYY is the year, and HH:MM:SS is the time of the day in military time.</span></span>

<span data-ttu-id="c6511-133">Im folgenden Beispiel werden zwei Aufrufe von [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c6511-133">The following example demonstrates two calls to [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea).</span></span> <span data-ttu-id="c6511-134">Der erste-Befehl erstellt ein Sitzungs Cookie, das zweite erstellt ein dauerhaftes Cookie.</span><span class="sxs-lookup"><span data-stu-id="c6511-134">The first call creates a session cookie and the second creates a persistent cookie.</span></span>


```C++
BOOL bReturn;

// Create a session cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
            TEXT("TestData = Test"));

// Create a persistent cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
           TEXT("TestData = Test; expires = Sat,01-Jan-2000 00:00:00 GMT"));

```



> [!Note]  
> <span data-ttu-id="c6511-135">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="c6511-135">WinINet does not support server implementations.</span></span> <span data-ttu-id="c6511-136">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6511-136">In addition, it should not be used from a service.</span></span> <span data-ttu-id="c6511-137">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="c6511-137">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 