---
description: Wenn die Kommunikation des Clients mit einem beliebigen Server abgeschlossen ist oder die zusätzlichen Anmelde Informationen, die an die AcquireCredentialsHandle-Funktion weitergegeben wurden, nicht mehr verwendet werden, muss der Client die freecredentialshandle-Funktion aufrufen.
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: Beenden einer SSPI-Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1fdc51ba1c31ae4ac8abb52c6d4c4372a9d161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750929"
---
# <a name="ending-an-sspi-session"></a><span data-ttu-id="a4f06-103">Beenden einer SSPI-Sitzung</span><span class="sxs-lookup"><span data-stu-id="a4f06-103">Ending an SSPI Session</span></span>

<span data-ttu-id="a4f06-104">Nachdem die Kommunikation zwischen Client und Server abgeschlossen ist, wird die [**Delta Context**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) -Funktion von beiden Seiten mit den entsprechenden Kontext Handles aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a4f06-104">After the client and server have finished communicating, both sides call the [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) function with their respective context handles.</span></span> <span data-ttu-id="a4f06-105">Wenn die Kommunikation des Clients mit einem beliebigen Server abgeschlossen ist oder die zusätzlichen Anmelde Informationen, die an die [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Funktion weitergegeben wurden, nicht mehr verwendet werden, muss der Client die [**freecredentialshandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a4f06-105">When the client has finished communicating with any server or has finished using the additional credentials passed to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function, the client must call the [**FreeCredentialsHandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) function.</span></span> <span data-ttu-id="a4f06-106">Wenn der Server zum Herunterfahren und vor dem Entladen der dll bereit ist, muss der Server " **Delta Context**" aufruft.</span><span class="sxs-lookup"><span data-stu-id="a4f06-106">When the server is ready to shut down and before unloading the DLL, the server must call **DeleteSecurityContext**.</span></span>

 

 
