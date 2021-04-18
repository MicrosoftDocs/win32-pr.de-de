---
title: Suchen des vollständigen Namens eines Benutzers
description: Computer können in einer Domäne organisiert werden, bei der es sich um eine Sammlung von Computernetzwerk handelt. Der Domänen Administrator unterhält zentralisierte Informationen zu Benutzer-und Gruppenkonten.
ms.assetid: 296ecfd0-1b65-482c-bee1-eff2130cc14e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2daa6bc2bc7d7255e961537c641a999d5a0bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340836"
---
# <a name="looking-up-a-users-full-name"></a>Suchen des vollständigen Namens eines Benutzers

Computer können in einer *Domäne* organisiert werden, bei der es sich um eine Sammlung von Computernetzwerk handelt. Der Domänen Administrator unterhält zentralisierte Informationen zu Benutzer-und Gruppenkonten.

So ermitteln Sie den vollständigen Namen eines Benutzers anhand des Benutzernamens und des Domänen Namens:

-   Konvertieren Sie den Benutzernamen und den Domänen Namen in Unicode, wenn Sie nicht bereits Unicode-Zeichen folgen sind.
-   Suchen Sie den Computernamen des Domänen Controllers (DC), indem Sie [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)aufrufen.
-   Suchen Sie den Benutzernamen auf dem DC-Computer durch Aufrufen von " [**nettusergetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)".
-   Konvertieren Sie den vollständigen Benutzernamen in ANSI, es sei denn, das Programm erwartet die Verwendung von Unicode-Zeichen folgen.

Der folgende Beispielcode ist eine Funktion (getfullname), die einen Benutzernamen und einen Domänen Namen in den ersten beiden Argumenten annimmt und den vollständigen Namen des Benutzers im dritten Argument zurückgibt.


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



 

 




