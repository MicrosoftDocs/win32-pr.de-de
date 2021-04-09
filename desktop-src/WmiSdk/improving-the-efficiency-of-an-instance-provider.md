---
description: Ein WMI-Hochleistungs Anbieter erhöht die Geschwindigkeit, mit der ein WMI-Client Informationen von einem WMI-Instanzanbieter abrufen kann.
ms.assetid: 767a16bb-44b6-4c56-b79b-23241fcc216e
ms.tgt_platform: multiple
title: Verbessern der Effizienz eines Instanzanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fecd0d8a20a3dcccd2878996823a7eb8a7ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866884"
---
# <a name="improving-the-efficiency-of-an-instance-provider"></a><span data-ttu-id="65535-103">Verbessern der Effizienz eines Instanzanbieters</span><span class="sxs-lookup"><span data-stu-id="65535-103">Improving the Efficiency of an Instance Provider</span></span>

<span data-ttu-id="65535-104">Ein WMI-Hochleistungs Anbieter erhöht die Geschwindigkeit, mit der ein WMI-Client Informationen von einem WMI-Instanzanbieter abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="65535-104">A WMI high-performance provider greatly increases the speed at which a WMI client can obtain information from a WMI instance provider.</span></span> <span data-ttu-id="65535-105">Die Haupt Änderung besteht darin, dass ein Hochleistungs Anbieter als Prozess interner Server sowohl für die Client Anwendung als auch für WMI ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65535-105">The main change is that a high-performance provider runs as an in-process server to either the client application or to WMI.</span></span> <span data-ttu-id="65535-106">Wenn Sie den Anbieter innerhalb des Client Prozesses platzieren, können Sie die Interaktion zwischen den beiden beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="65535-106">By placing the provider inside the client process, you can speed up the interaction between the two.</span></span>

<span data-ttu-id="65535-107">Weitere Informationen zum Erstellen eines Hochleistungs Anbieters für den Instanzanbieter finden Sie unter Erstellen eines [Instanzanbieters in einen High-Performance-Anbieter](making-an-instance-provider-into-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="65535-107">For more information about how to make your instance provider a high-performance provider, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md).</span></span>

 

 



