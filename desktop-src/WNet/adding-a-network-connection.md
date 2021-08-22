---
title: Hinzufügen einer Netzwerkverbindung
description: Um eine Verbindung mit einer Netzwerkressource herzustellen, die von einer NETRESOURCE-Struktur beschrieben wird, kann eine Anwendung die Funktion WNetAddConnection2, WNetAddConnection3 oder WNetUseConnection aufrufen.
ms.assetid: 0dab9eed-9019-4075-833b-324e5caee257
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8298216ab277c5f0ec4a0db8c4d6d1b6c592a8b643e6c30de96731ae2a32632b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053388"
---
# <a name="adding-a-network-connection"></a>Hinzufügen einer Netzwerkverbindung

Um eine Verbindung mit einer Netzwerkressource herzustellen, die von einer [**NETRESOURCE-Struktur**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) beschrieben wird, kann eine Anwendung [**die Funktion WNetAddConnection2,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)oder [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) aufrufen. Im folgenden Beispiel wird die Verwendung der **WNetAddConnection2-Funktion** veranschaulicht.

Das Codebeispiel ruft die **WNetAddConnection2-Funktion** auf und gibt an, dass das System das Benutzerprofil mit den Informationen aktualisieren soll, wodurch eine "gespeicherte" oder dauerhafte Verbindung erstellt wird. Im Beispiel wird ein anwendungsdefiniertes Fehlerhandler zum Verarbeiten von Fehlern und die [**TextOut-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-textouta) zum Drucken aufrufen.


```C++
DWORD dwResult; 
NETRESOURCE nr; 
//
// Call the WNetAddConnection2 function to make the connection,
//   specifying a persistent connection.
//
dwResult = WNetAddConnection2(&nr, // NETRESOURCE from enumeration 
    (LPSTR) NULL,                  // no password 
    (LPSTR) NULL,                  // logged-in user 
    CONNECT_UPDATE_PROFILE);       // update profile with connect information 
 
// Process errors.
//  The local device is already connected to a network resource.
//
if (dwResult == ERROR_ALREADY_ASSIGNED) 
{ 
    printf("Already connected to specified resource.\n"); 
    return dwResult; 
} 
 
//  An entry for the local device already exists in the user profile.
//
else if (dwResult == ERROR_DEVICE_ALREADY_REMEMBERED) 
{ 
    printf("Attempted reassignment of remembered device.\n"); 
    return dwResult; 
} 
else if(dwResult != NO_ERROR) 
{ 
    //
    // Call an application-defined error handler.
    //
    printf("WNetAddConnection2 failed.\n"); 
    return dwResult; 
} 
 
//
// Otherwise, report a successful connection.
//
printf("Connected to the specified resource.\n"); 
```



Die [**WNetAddConnection-Funktion**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) wird aus Gründen der Kompatibilität mit früheren Versionen von Windows für Arbeitsgruppen unterstützt. Neue Anwendungen sollten die [**WNetAddConnection2-Funktion**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) oder die [**WNetAddConnection3-Funktion**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) aufrufen.

Weitere Informationen zur Verwendung eines anwendungsdefinierte Fehlerhandlers finden Sie unter [Abrufen von Netzwerkfehlern.](retrieving-network-errors.md)

 

 