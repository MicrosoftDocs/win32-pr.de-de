---
title: Synchrone Vorgänge
description: Wenn "rasdial" als synchroner Vorgang aufgerufen wird, gibt die Funktion erst dann zurück, wenn die Verbindung hergestellt wurde oder ein Fehler auftritt.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2463e3112c3faac4d7601023ea73f0182e2d5b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037446"
---
# <a name="synchronous-operations"></a><span data-ttu-id="46b9b-103">Synchrone Vorgänge</span><span class="sxs-lookup"><span data-stu-id="46b9b-103">Synchronous Operations</span></span>

<span data-ttu-id="46b9b-104">Wenn " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " als synchroner Vorgang aufgerufen wird, gibt die Funktion erst dann zurück, wenn die Verbindung hergestellt wurde oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="46b9b-104">When [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) is invoked as a synchronous operation, the function does not return until the connection has been established or an error occurs.</span></span> <span data-ttu-id="46b9b-105">Der synchrone Modus ist eine einfache Möglichkeit für einen RAS-Client, eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="46b9b-105">Synchronous mode provides a simple way for a RAS client to establish a connection.</span></span> <span data-ttu-id="46b9b-106">Der Client kann einfach " **rasdial**" aufrufen, warten, bis die Funktion zurückgegeben wird, und dann die Funktion " [**rasgetconnectstatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) " aufrufen, um zu bestimmen, ob der Verbindungsvorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="46b9b-106">The client can simply call **RasDial**, wait for the function to return, and then call the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to determine whether the connection operation was successful.</span></span> <span data-ttu-id="46b9b-107">Nachdem die Verbindung hergestellt wurde, kann die Client Anwendung beendet werden, ohne dass die Verbindung unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="46b9b-107">Once the connection has been established, the client application can terminate without breaking the connection.</span></span> <span data-ttu-id="46b9b-108">Wenn ein Fehler auftritt, muss die Client Anwendung [den Verbindungsvorgang](disconnecting.md) beenden, bevor Sie beendet wird.</span><span class="sxs-lookup"><span data-stu-id="46b9b-108">If an error occurs, the client application must [shut down the connection operation](disconnecting.md) before terminating.</span></span>

<span data-ttu-id="46b9b-109">Der Nachteil des synchronen Modus besteht darin, dass der Client keine Status Benachrichtigungen empfängt, während der Verbindungsvorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="46b9b-109">The disadvantage of synchronous mode is that the client does not receive progress notifications as the connection operation proceeds.</span></span> <span data-ttu-id="46b9b-110">Um diese fehlende Fortschritts Benachrichtigung zu umgehen, kann ein Client im synchronen Modus einen separaten Thread verwenden, der " [**rasgetconnectstatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) " aufruft, um den aktuellen Status abzurufen und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="46b9b-110">As a workaround for this lack of progress notifications, a synchronous mode client can use a separate thread that calls [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) to poll for and display the current state.</span></span> <span data-ttu-id="46b9b-111">Für RAS-Clients, die Statusinformationen empfangen möchten, empfiehlt es sich jedoch, den Vorgang [**asynchron**](/windows/desktop/api/Ras/nf-ras-rasdiala) aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="46b9b-111">However, for RAS clients that want to receive progress information, the preferred technique is to invoke [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) asynchronously.</span></span>

 

 




