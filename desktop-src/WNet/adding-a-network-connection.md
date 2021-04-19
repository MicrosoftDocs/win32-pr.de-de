---
title: Hinzufügen einer Netzwerkverbindung
description: Zum Herstellen einer Verbindung mit einer Netzwerkressource, die durch eine Struktur vom Typ "nettresource" beschrieben wird, kann eine Anwendung die WNetAddConnection2-, WNetAddConnection3-oder wnettuseconnetction-Funktion aufrufen.
ms.assetid: 0dab9eed-9019-4075-833b-324e5caee257
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476e03193b919f17a2060e415db5e7ea60c8364e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338479"
---
# <a name="adding-a-network-connection"></a>Hinzufügen einer Netzwerkverbindung

Zum Herstellen einer Verbindung mit einer Netzwerkressource, die durch eine Struktur vom Typ " [**nettresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) " beschrieben wird, kann eine Anwendung die [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a)-, [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)-oder [**wnettuseconnetction**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona) -Funktion aufrufen. Im folgenden Beispiel wird die Verwendung der **WNetAddConnection2** -Funktion veranschaulicht.

Das Codebeispiel ruft die **WNetAddConnection2** -Funktion auf, wobei angegeben wird, dass das System das Profil des Benutzers mit den Informationen aktualisieren soll, indem eine "gespeicherte" oder eine persistente Verbindung erstellt wird. Das Beispiel ruft einen Anwendungs definierten Fehlerhandler zum Verarbeiten von Fehlern und die [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) -Funktion zum Drucken auf.


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



Die Funktion " [**wnetaddconnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) " wird für die Kompatibilität mit früheren Versionen von Windows für Arbeitsgruppen unterstützt. Neue Anwendungen sollten die [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) -Funktion oder die [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) -Funktion aufzurufen.

Weitere Informationen zum Verwenden eines Anwendungs definierten Fehler Handlers finden Sie unter [Abrufen von Netzwerkfehlern](retrieving-network-errors.md).

 

 