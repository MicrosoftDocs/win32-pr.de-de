---
title: Abbrechen einer Netzwerkverbindung
description: Um eine Verbindung mit einer Netzwerkressource abzubrechen, kann eine Anwendung die WNetCancelConnection2-Funktion wie im folgenden Beispiel gezeigt aufruft.
ms.assetid: a1c80222-4986-4c51-86a5-a1caacb4b2fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cc5fb9536a5d073a6c99d8b49a00e3c2771546
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858397"
---
# <a name="canceling-a-network-connection"></a>Abbrechen einer Netzwerkverbindung

Um eine Verbindung mit einer Netzwerkressource abzubrechen, kann eine Anwendung die [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) -Funktion wie im folgenden Beispiel gezeigt aufruft.

Der **WNetCancelConnection2** -aufrufswert gibt an, dass eine Netzwerkverbindung nicht mehr persistent sein sollte. Das Beispiel ruft einen Anwendungs definierten Fehlerhandler zum Verarbeiten von Fehlern und die [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) -Funktion zum Drucken auf.


```C++
DWORD dwResult; 
 
// Call the WNetCancelConnection2 function, specifying
//  that the connection should no longer be a persistent one.
//
dwResult = WNetCancelConnection2("z:", 
    CONNECT_UPDATE_PROFILE, // remove connection from profile 
    FALSE);                 // fail if open files or jobs 
 
// Process errors.
//  The device is not a local redirected device.
//
if (dwResult == ERROR_NOT_CONNECTED) 
{ 
    printf("Drive z: not connected.\n"); 
    return dwResult; 
} 
 
// Call an application-defined error handler.
//
else if(dwResult != NO_ERROR) 
{ 
    printf("WNetCancelConnection2 failed.\n"); 
    return dwResult; 
}
//
// Otherwise, report canceling the connection.
//
printf("Connection closed for z: drive.\n"); 
```



Die [**wnetcancelconnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) -Funktion wird für die Kompatibilität mit früheren Versionen von Windows für Arbeitsgruppen unterstützt. Verwenden Sie für neue Anwendungen [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).

Weitere Informationen zum Verwenden eines Anwendungs definierten Fehler Handlers finden Sie unter [Abrufen von Netzwerkfehlern](retrieving-network-errors.md).

 

 