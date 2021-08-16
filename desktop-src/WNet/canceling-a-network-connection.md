---
title: Abbrechen einer Netzwerkverbindung
description: Um eine Verbindung mit einer Netzwerkressource abzubricht, kann eine Anwendung die WNetCancelConnection2-Funktion aufrufen, wie im folgenden Beispiel gezeigt.
ms.assetid: a1c80222-4986-4c51-86a5-a1caacb4b2fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbb5c74faa1e1f8b75d0e3b604d89615c6ad1481384a661253ee204dd3ee6081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566920"
---
# <a name="canceling-a-network-connection"></a>Abbrechen einer Netzwerkverbindung

Um eine Verbindung mit einer Netzwerkressource abzubricht, kann eine Anwendung die [**WNetCancelConnection2-Funktion**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) aufrufen, wie im folgenden Beispiel gezeigt.

Der Aufruf von **WNetCancelConnection2** gibt an, dass eine Netzwerkverbindung nicht mehr persistent sein soll. Das Beispiel ruft einen anwendungsdefinierten Fehlerhandler auf, um Fehler zu verarbeiten, und die [**TextOut-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-textouta) zum Drucken.


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



Die [**WNetCancelConnection-Funktion**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) wird aus Kompatibilitäts- und Windows für Arbeitsgruppen unterstützt. Verwenden Sie für neue Anwendungen [**WNetCancelConnection2.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)

Weitere Informationen zur Verwendung eines anwendungsdefinierten Fehlerhandlers finden Sie unter [Retrieving Network Errors](retrieving-network-errors.md).

 

 