---
description: Verwenden des \_ Befehls Codes für die Verwendung von SIO-Multicast \_ Bereich zum Angeben des Bereichs, in dem der Multicast auftreten soll.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: SIO_MULTICAST_SCOPE ioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d1fd6f2bea76d095ea88d66c0ac029fb9168ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364109"
---
# <a name="sio_multicast_scope-ioctl"></a><span data-ttu-id="af106-103">Bereich für die SIO- \_ Multicast- \_ ioctl</span><span class="sxs-lookup"><span data-stu-id="af106-103">SIO\_MULTICAST\_SCOPE Ioctl</span></span>

<span data-ttu-id="af106-104">Wenn Multicasting verwendet wird, ist es in der Regel erforderlich, den Bereich anzugeben, in dem der Multicast auftreten soll.</span><span class="sxs-lookup"><span data-stu-id="af106-104">When multicasting is employed, it is usually necessary to specify the scope over which the multicast should occur.</span></span> <span data-ttu-id="af106-105">Der Gültigkeitsbereich ist so definiert, dass es sich um die Anzahl der weitergeleiteten Netzwerksegmente handelt.</span><span class="sxs-lookup"><span data-stu-id="af106-105">Here scope is defined to be the number of routed network segments to be covered.</span></span> <span data-ttu-id="af106-106">Der \_ \_ Befehls Code für die Verwendung von "sio Multicast Scope" für " [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) " wird zur Steuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="af106-106">The SIO\_MULTICAST\_SCOPE command code for [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) is used to control this.</span></span> <span data-ttu-id="af106-107">Ein Bereich von 0 (null) gibt an, dass die Multicast Übertragung nicht bei der Übertragung platziert würde, sondern über Sockets innerhalb des lokalen Hosts verteilt werden könnte.</span><span class="sxs-lookup"><span data-stu-id="af106-107">A scope of zero would indicate that the multicast transmission would not be placed on the wire but could be disseminated across sockets within the local host.</span></span> <span data-ttu-id="af106-108">Ein Bereichs Wert von 1 (Standardwert) gibt an, dass die Übertragung in das Netzwerk übertragen wird, ohne Router zu überschreiten.</span><span class="sxs-lookup"><span data-stu-id="af106-108">A scope value of one (the default) indicates that the transmission will be placed on the wire, but will not cross any routers.</span></span> <span data-ttu-id="af106-109">Höhere Bereichs Werte bestimmen die Anzahl von Routern, die möglicherweise überschritten werden.</span><span class="sxs-lookup"><span data-stu-id="af106-109">Higher scope values determine the number of routers that may be crossed.</span></span> <span data-ttu-id="af106-110">Beachten Sie, dass dies dem Time-to-Live (TTL)-Parameter in IP-Multicasting entspricht.</span><span class="sxs-lookup"><span data-stu-id="af106-110">Note that this corresponds to the time-to-live (TTL) parameter in IP multicasting.</span></span>

 

 
