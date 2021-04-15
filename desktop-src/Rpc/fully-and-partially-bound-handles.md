---
title: Vollständige und teilweise gebundene Handles
description: Wenn Sie dynamische Endpunkte verwenden, erhalten die Laufzeitbibliotheken Endpunkt Informationen, die Sie benötigen.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc1f434ec53ebcfd992b0090ed9066dce2ec627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471324"
---
# <a name="fully-and-partially-bound-handles"></a><span data-ttu-id="311d6-103">Vollständige und teilweise gebundene Handles</span><span class="sxs-lookup"><span data-stu-id="311d6-103">Fully and Partially Bound Handles</span></span>

<span data-ttu-id="311d6-104">Wenn Sie dynamische Endpunkte verwenden, erhalten die Laufzeitbibliotheken Endpunkt Informationen, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="311d6-104">When you use dynamic endpoints, the run-time libraries obtain endpoint information as they need it.</span></span> <span data-ttu-id="311d6-105">Die-Laufzeitbibliotheken unterscheiden zwischen einem *vollständig gebundenen handle* (eines mit Endpunkt Informationen) und einem *teilweise gebundenen handle* (eines, das keine Endpunkt Informationen enthält).</span><span class="sxs-lookup"><span data-stu-id="311d6-105">The run-time libraries make the distinction between a *fully bound handle* (one that includes endpoint information) and a *partially bound handle* (one that does not include endpoint information).</span></span>

<span data-ttu-id="311d6-106">Die Client Lauf Zeit Bibliothek muss das teilweise gebundene Handle in ein vollständig gebundenes handle konvertieren, bevor der Client an den Server gebunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="311d6-106">The client run-time library must convert the partially bound handle to a fully bound handle before the client can bind to the server.</span></span> <span data-ttu-id="311d6-107">Die Client Lauf Zeit Bibliothek versucht, das teilweise gebundene Handle für die Client Anwendung zu konvertieren, indem die Endpunkt Informationen wie gezeigt erhalten werden:</span><span class="sxs-lookup"><span data-stu-id="311d6-107">The client run-time library tries to convert the partially bound handle for the client application by obtaining the endpoint information as shown:</span></span>

-   <span data-ttu-id="311d6-108">Aus der Schnittstellen Spezifikation des Clients</span><span class="sxs-lookup"><span data-stu-id="311d6-108">From the client's interface specification</span></span>
-   <span data-ttu-id="311d6-109">Von einem Endpunkt Zuordnungsdienst, der auf dem Server ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="311d6-109">From an endpoint-mapping service running on the server</span></span>

<span data-ttu-id="311d6-110">Wenn der Client versucht, ein teilweise gebundenes Handle zu verwenden, wenn die Endpunkt Informationen in der Schnittstellen Spezifikation nicht verfügbar sind und der Endpunkt-Mapper des Servers keine Informationen zum Server Endpunkt hat, verfügt der Client nicht über genügend Informationen, um den Remote Prozedur aufzurufen, und dieser Rückruf schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="311d6-110">If the client tries to use a partially bound handle when the endpoint information is not available in the interface specification and the server's endpoint-mapper does not have information about the server endpoint, the client will not have enough information to make its remote procedure call and that call will fail.</span></span> <span data-ttu-id="311d6-111">Um dies zu verhindern, müssen Sie den Endpunkt in der Endpunkt Zuordnung registrieren, wenn die verteilte Anwendung teilweise gebundene Handles verwendet.</span><span class="sxs-lookup"><span data-stu-id="311d6-111">To prevent this, you must register the endpoint in the endpoint mapper when your distributed application uses partially bound handles.</span></span> <span data-ttu-id="311d6-112">Weitere Informationen zum Endpunkt Mapper finden Sie unter [angeben dynamischer Endpunkte](specifying-endpoints.md).</span><span class="sxs-lookup"><span data-stu-id="311d6-112">For more information about the endpoint mapper, see [Specifying Dynamic Endpoints](specifying-endpoints.md).</span></span>

<span data-ttu-id="311d6-113">Wenn ein Remote Prozedur Rückruf fehlschlägt, kann die Client Anwendung [**rpcbindingreset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) abrufen, um veraltete Endpunkt Informationen zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="311d6-113">When a remote procedure call fails, the client application can call [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) to remove out-of-date endpoint information.</span></span> <span data-ttu-id="311d6-114">Wenn der Client versucht, die Remote Prozedur aufzurufen, versucht die Client Lauf Zeit Bibliothek erneut, das vollständig gebundene Handle in ein teilweise gebundenes Handle zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="311d6-114">When the client tries to call the remote procedure, the client run-time library again tries to convert the fully bound handle to a partially bound handle.</span></span> <span data-ttu-id="311d6-115">Dies ist hilfreich, wenn der Server mit einem anderen dynamischen Endpunkt beendet und neu gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="311d6-115">This is useful when the server has been stopped and restarted using a different dynamic endpoint.</span></span>

 

 




