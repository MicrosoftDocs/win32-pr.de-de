---
title: Suchen des vollständigen Namens eines Benutzers
description: Computer können in einer Domäne organisiert werden, bei der es sich um eine Sammlung von Computernetzwerken handelt. Der Domänenadministrator verwaltet zentralisierte Benutzer- und Gruppenkontoinformationen.
ms.assetid: 296ecfd0-1b65-482c-bee1-eff2130cc14e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdff00483b38ef12355af4dcda4a48d60bf849a8fd5d6829640ae8907e426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012518"
---
# <a name="looking-up-a-users-full-name"></a>Suchen des vollständigen Namens eines Benutzers

Computer können in einer Domäne organisiert *werden,* bei der es sich um eine Sammlung von Computernetzwerken handelt. Der Domänenadministrator verwaltet zentralisierte Benutzer- und Gruppenkontoinformationen.

So suchen Sie den vollständigen Namen eines Benutzers mit dem Benutzernamen und Domänennamen:

-   Konvertieren Sie den Benutzernamen und Domänennamen in Unicode, wenn es sich nicht bereits um Unicode-Zeichenfolgen handelt.
-   Suchen Sie den Computernamen des Domänencontrollers (DC), indem Sie [**NetGetDCName aufrufen.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)
-   Suchen Sie den Benutzernamen auf dem DC-Computer, indem Sie [**NetUserGetInfo aufrufen.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)
-   Konvertieren Sie den vollständigen Benutzernamen in ANSI, es sei denn, das Programm erwartet, dass es mit Unicode-Zeichenfolgen funktioniert.

Der folgende Beispielcode ist eine Funktion (GetFullName), die einen Benutzernamen und einen Domänennamen in den ersten beiden Argumenten verwendet und den vollständigen Namen des Benutzers im dritten Argument zurückgibt.


```C++
#include <windows.h>
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

BOOL GetFullName( char *UserName, char *Domain, char *dest )
{
    WCHAR wszUserName[UNLEN+1];          // Unicode user name
    WCHAR wszDomain[256]; 
    LPBYTE ComputerName;
    
//    struct _SERVER_INFO_100 *si100;  // Server structure
    struct _USER_INFO_2 *ui;         // User structure

// Convert ANSI user name and domain to Unicode

    MultiByteToWideChar( CP_ACP, 0, UserName,
        (int) strlen(UserName)+1, wszUserName, 
        sizeof(wszUserName)/sizeof(WCHAR) );

    MultiByteToWideChar( CP_ACP, 0, Domain,
        (int) strlen(Domain)+1, wszDomain, 
        sizeof(wszDomain)/sizeof(WCHAR) );

// Get the computer name of a DC for the domain.

    NetGetDCName( NULL, wszDomain, &ComputerName );

// Look up the user on the DC.

    if( NetUserGetInfo( (LPWSTR) ComputerName,
        (LPWSTR) &wszUserName, 2, (LPBYTE *) &ui ) )
    {
        wprintf( L"Error getting user information.\n" );
        return( FALSE );
    }

// Convert the Unicode full name to ANSI.

    WideCharToMultiByte( CP_ACP, 0, ui->usri2_full_name, -1,
        dest, 256, NULL, NULL );

    return (TRUE);
}
```



 

 




