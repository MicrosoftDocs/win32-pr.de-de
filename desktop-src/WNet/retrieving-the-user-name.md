---
title: Abrufen des Benutzernamens
description: Zum Abrufen des Namens des Benutzers, der entweder einem lokalen Gerät zugeordnet ist, das mit einer Netzwerkressource oder mit dem Namen eines Netzwerks verbunden ist, kann eine Anwendung die wnetgetuser-Funktion aufrufen.
ms.assetid: aed410af-d5f0-4389-882b-5b4338b5f900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0aeb8df11187828be0865d6b73e08325f2e0e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209298"
---
# <a name="retrieving-the-user-name"></a><span data-ttu-id="1362b-103">Abrufen des Benutzernamens</span><span class="sxs-lookup"><span data-stu-id="1362b-103">Retrieving the User Name</span></span>

<span data-ttu-id="1362b-104">Zum Abrufen des Namens des Benutzers, der entweder einem lokalen Gerät zugeordnet ist, das mit einer Netzwerkressource oder mit dem Namen eines Netzwerks verbunden ist, kann eine Anwendung die [**wnetgetuser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1362b-104">To retrieve the name of the user associated either with a local device connected to a network resource or with the name of a network, an application can call the [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) function.</span></span>

<span data-ttu-id="1362b-105">Im folgenden Beispiel wird der Gerätename verwendet, um den Namen des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1362b-105">The following example uses the device name to retrieve the name of the user.</span></span> <span data-ttu-id="1362b-106">Das Beispiel ruft einen Anwendungs definierten Fehlerhandler zum Verarbeiten von Fehlern und die [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) -Funktion zum Drucken auf.</span><span class="sxs-lookup"><span data-stu-id="1362b-106">The sample calls an application-defined error handler to process errors, and the [**TextOut**](/windows/desktop/api/wingdi/nf-wingdi-textouta) function for printing.</span></span>


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



<span data-ttu-id="1362b-107">Weitere Informationen zum Verwenden eines Anwendungs definierten Fehler Handlers finden Sie unter [Abrufen von Netzwerkfehlern](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="1362b-107">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 