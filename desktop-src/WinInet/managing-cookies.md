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
# <a name="managing-cookies"></a>Verwalten von Cookies

Unter dem HTTP-Protokoll werden von einem Server oder einem Skript Cookies verwendet, um Zustandsinformationen auf der Client Arbeitsstation beizubehalten. Die WinInet-Funktionen haben zu diesem Zweck eine persistente Cookie-Datenbank implementiert. Sie können verwendet werden, um Cookies in der cookiedatenbank festzulegen und auf Cookies zuzugreifen. Weitere Informationen finden Sie unter [http-Cookies](http-cookies.md).

Die Funktionen [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) und [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) können zum Verwalten von Cookies verwendet werden.

## <a name="using-cookie-functions"></a>Verwenden von Cookie-Funktionen

Mit den folgenden Funktionen kann eine Anwendung Cookies in der cookiedatenbank erstellen oder abrufen.



| Funktion                                       | BESCHREIBUNG                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) | Ruft Cookies für die angegebene URL und alle übergeordneten URLs ab. |
| [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) | Legt ein Cookie für die angegebene URL fest.                              |



 

Beachten Sie, dass diese Funktionen keinen [**Internet Open**](/windows/desktop/api/Wininet/nf-wininet-internetopena)-aufrufbedarf erfordern. Cookies, die ein Ablaufdatum aufweisen, werden im lokalen Benutzerkonto unter Benutzer \\ Benutzername " \\ AppData \\ Roaming \\ Microsoft \\ Windows \\ Cookies-Verzeichnis" und Benutzer \\ "Benutzername" \\ AppData \\ Roaming \\ \\ von Microsoft Windows \\ Cookies Low-Directory für Anwendungen gespeichert, die mit \\ niedrigen Berechtigungen ausgeführt werden. Cookies, die kein Ablaufdatum aufweisen, werden im Arbeitsspeicher gespeichert und sind nur für den Prozess verfügbar, in dem Sie erstellt wurden.

Wie im Thema [http-Cookies](http-cookies.md) erwähnt, gibt die [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) -Funktion keine Cookies zurück, die vom Server als nicht skriptfähig gekennzeichnet wurden, mit dem Attribut "HttpOnly" im Set-Cookie-Header.

### <a name="getting-a-cookie"></a>Ein Cookie wird erhalten.

[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) gibt die Cookies für die angegebene URL und alle übergeordneten URLs zurück.

Im folgenden Beispiel wird ein Aufrufen von [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea)veranschaulicht.


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



### <a name="setting-a-cookie"></a>Festlegen eines Cookies

[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) wird verwendet, um ein Cookie für die angegebene URL festzulegen. [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) kann sowohl persistente als auch Sitzungs Cookies erstellen.

Persistente Cookies haben ein Ablaufdatum. Diese Cookies werden im lokalen Benutzerkonto unter Benutzer \\ Benutzername " \\ AppData \\ Roaming \\ Microsoft \\ Windows \\ Cookies-Verzeichnis" und Benutzer \\ "Benutzername" \\ AppData \\ Roaming \\ Microsoft \\ Windows \\ Cookies \\ Low Directory für Anwendungen, die mit niedrigen Berechtigungen ausgeführt werden, gespeichert.

Sitzungs Cookies werden im Arbeitsspeicher gespeichert, und nur der Prozess, der Sie erstellt hat, kann darauf zugegriffen werden.

Die Daten für das Cookie sollten folgendes Format aufweisen:

``` syntax
NAME=VALUE
```

Für das Ablaufdatum muss das Format wie folgt lauten:

``` syntax
DAY, DD-MMM-YYYY HH:MM:SS GMT
```

Day ist die drei buchstabige Abkürzung für den Wochentag. dd ist der Tag des Monats, mmm ist die drei buchstabige Abkürzung für den Monat, yyyy ist das Jahr, und hh: mm: SS ist die Uhrzeit des Tages in der militärischen Zeit.

Im folgenden Beispiel werden zwei Aufrufe von [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea)veranschaulicht. Der erste-Befehl erstellt ein Sitzungs Cookie, das zweite erstellt ein dauerhaftes Cookie.


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
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 