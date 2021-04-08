---
title: Bewährte Methoden für den Upload
description: Highloads können verschiedene Server Timeout-Bedingungen verursachen. Dies kann wiederum die Last erhöhen, wenn der Client den Vorgang wiederholt.
ms.assetid: 8210f849-2aae-497b-b5dd-af25f6f4b8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95a229ff1e229c41fde8fd377e347f91cf43010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036409"
---
# <a name="upload-best-practices"></a><span data-ttu-id="dc461-103">Bewährte Methoden für den Upload</span><span class="sxs-lookup"><span data-stu-id="dc461-103">Upload Best Practices</span></span>

<span data-ttu-id="dc461-104">Highloads können verschiedene Server Timeout-Bedingungen verursachen. Dies kann wiederum die Last erhöhen, wenn der Client den Vorgang wiederholt.</span><span class="sxs-lookup"><span data-stu-id="dc461-104">Highloads may cause various server timeout conditions, which may in turn increase the load when the client retries.</span></span> <span data-ttu-id="dc461-105">Außerdem verbraucht eine große Anzahl von ausstehenden Verbindungen mehr Server Ressourcen und macht die Situation schlechter.</span><span class="sxs-lookup"><span data-stu-id="dc461-105">Also, a large number of outstanding connections will consume more server resources and make the situation worse.</span></span> <span data-ttu-id="dc461-106">Wenn eine Back-End-APP nicht zur Behandlung von hohen Ladebedingungen geschrieben wird, kann dies zu einem Absturz oder einem anderen Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="dc461-106">On top of that, if backend app is not written to handle high load conditions, it may crash or mal-behave.</span></span> <span data-ttu-id="dc461-107">Die APP muss die folgenden Schritte ausführen, um die Last für das Back-End einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="dc461-107">The app shall perform the following steps to limit the load on the backend.</span></span>

<span data-ttu-id="dc461-108">Wenn die Serveranwendung nicht zur Verarbeitung hoher Volumes geschrieben wird, treten möglicherweise Timeout Bedingungen auf, die wiederum die Last erhöhen, wenn der Client den Vorgang wiederholt.</span><span class="sxs-lookup"><span data-stu-id="dc461-108">If the server application is not written to handle high volumes, timeout conditions may occur, which may in turn increase the load when the client retries.</span></span> <span data-ttu-id="dc461-109">Außerdem verbraucht eine große Anzahl von ausstehenden Verbindungen mehr Server Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="dc461-109">Also, a large number of outstanding connections will consume more server resources.</span></span>

<span data-ttu-id="dc461-110">Testen Sie beim Testen der Serveranwendung mit der höchsten Auslastung.</span><span class="sxs-lookup"><span data-stu-id="dc461-110">When testing your server application, test with highest load possible.</span></span> <span data-ttu-id="dc461-111">Sie sollten mehrere Client Computer verwenden, von denen jeder über mehrere gleichzeitige, Vordergrund-BITS-Aufträge verfügt, und den maximalen Durchsatz beim Back-End messen.</span><span class="sxs-lookup"><span data-stu-id="dc461-111">You should use multiple client machines, each with several concurrent, foreground BITS jobs, and measure the maximum throughput at the backend.</span></span> <span data-ttu-id="dc461-112">Wenn der Durchsatz nicht gemessen werden kann, müssen Sie den Durchsatz schätzen.</span><span class="sxs-lookup"><span data-stu-id="dc461-112">If you cannot measure the throughput, you will have to estimate the throughput.</span></span>

<span data-ttu-id="dc461-113">Die Serveranwendung sollte sich in einer anderen URL als die uploadurl befinden (siehe die BITS-IIS-Eigenschaft, **bitsservernotificationurl**).</span><span class="sxs-lookup"><span data-stu-id="dc461-113">The server application should reside on a different URL from the upload URL (see the BITS IIS property, **BITSServerNotificationURL**).</span></span>

<span data-ttu-id="dc461-114">Es empfiehlt sich, die Last auf dem Anwendungsserver basierend auf bewährten Durchsatz Werten einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="dc461-114">It is good practice to limit the load on the application server based on proven throughput values.</span></span> <span data-ttu-id="dc461-115">Verwenden Sie die IIS-Eigenschaften " **MaxBandwidth** " und " **MaxConnections**", um die Auslastung des Anwendungs Servers einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="dc461-115">You should use the IIS properties, **MaxBandwidth** and **MaxConnections**, to limit the load on the application server.</span></span>

 

 




