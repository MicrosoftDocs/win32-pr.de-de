---
title: Falsche Schnittstellen Warnungs Rückrufe
description: Nachdem die Kernel Weiterleitung Multicast Daten von einer bestimmten Quelle auf der falschen Oberfläche empfangen hat, wird der Multicast-Gruppen-Manager benachrichtigt.
ms.assetid: 7b20625e-286b-4c4f-8452-4d21563fd030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12906d836ca994e90347ea78cf22e50f8f2f00d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713913"
---
# <a name="wrong-interface-alert-callbacks"></a><span data-ttu-id="0804c-103">Falsche Schnittstellen Warnungs Rückrufe</span><span class="sxs-lookup"><span data-stu-id="0804c-103">Wrong Interface Alert Callbacks</span></span>

<span data-ttu-id="0804c-104">Nachdem die Kernel Weiterleitung Multicast Daten von einer bestimmten Quelle auf der falschen Oberfläche empfangen hat, wird der Multicast-Gruppen-Manager benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="0804c-104">After the kernel forwarder receives multicast data from a specific source on the wrong interface, it notifies the multicast group manager.</span></span> <span data-ttu-id="0804c-105">Der Multicast-Gruppen-Manager ruft dann den falschen pmgm-Rückruf auf, [**\_ Wenn der \_ \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) zum Routing Protokoll gehört, das die Schnittstelle besitzt, auf der die Daten fälschlicherweise eintreffen.</span><span class="sxs-lookup"><span data-stu-id="0804c-105">The multicast group manager then invokes the [**PMGM\_WRONG\_IF\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) callback to the routing protocol that owns the interface on which the data incorrectly arrived.</span></span>

> [!Note]  
> <span data-ttu-id="0804c-106">Dieser Rückruf ist in dieser Version der MGM-API zurzeit nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="0804c-106">This callback is not currently implemented in this version of the MGM API.</span></span>

 

 

 




