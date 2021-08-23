---
title: Abrufen des Benutzernamens
description: Um den Namen des Benutzers abzurufen, der entweder einem lokalen Gerät zugeordnet ist, das mit einer Netzwerkressource verbunden ist, oder mit dem Namen eines Netzwerks, kann eine Anwendung die WNetGetUser-Funktion aufrufen.
ms.assetid: aed410af-d5f0-4389-882b-5b4338b5f900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98aeafc849e1a66b373fcb81af46ec47b49644c4b9c753fad480876180a5592a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566478"
---
# <a name="retrieving-the-user-name"></a>Abrufen des Benutzernamens

Um den Namen des Benutzers abzurufen, der entweder einem lokalen Gerät zugeordnet ist, das mit einer Netzwerkressource verbunden ist, oder mit dem Namen eines Netzwerks, kann eine Anwendung die [**WNetGetUser-Funktion**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) aufrufen.

Im folgenden Beispiel wird der Gerätename verwendet, um den Namen des Benutzers abzurufen. Das Beispiel ruft einen anwendungsdefinierten Fehlerhandler auf, um Fehler zu verarbeiten, und die [**TextOut-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-textouta) zum Drucken.


```C++
CHAR szUserName[80]; 
DWORD dwResult, cchBuff = 80; 
 
// Call the WNetGetUser function.
//
dwResult = WNetGetUser("z:", 
    (LPSTR) szUserName, 
    &cchBuff); 
 
// If the call succeeds, print the user name.
//
if(dwResult == NO_ERROR) 
    printf("User name: %s\n", szUserName); 
 
// Handle the error.
//
else 
{ 
    printf("WNetGetUser failed.\n"); 
}
```



Weitere Informationen zur Verwendung eines anwendungsdefinierten Fehlerhandlers finden Sie unter [Retrieving Network Errors](retrieving-network-errors.md).

 

 