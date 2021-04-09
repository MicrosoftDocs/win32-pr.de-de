---
title: IGMP-Rückrufe aktivieren und deaktivieren
description: Der Multicast-Gruppen-Manager verwendet zwei Rückrufe zu IGMP, um Änderungen im Schnittstellen Besitz von IGMP zu einem Routing Protokoll und von einem Routing Protokoll an IGMP zu koordinieren.
ms.assetid: e4b2be85-6c67-4801-9905-eb1990d4bbb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa58e9b65c67ac5946f5f5e54e611565e59d8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858404"
---
# <a name="igmp-enable-and-disable-callbacks"></a><span data-ttu-id="be8ff-103">IGMP-Rückrufe aktivieren und deaktivieren</span><span class="sxs-lookup"><span data-stu-id="be8ff-103">IGMP Enable and Disable Callbacks</span></span>

<span data-ttu-id="be8ff-104">Der Multicast-Gruppen-Manager verwendet zwei Rückrufe zu IGMP, um Änderungen im Schnittstellen Besitz von IGMP zu einem Routing Protokoll und von einem Routing Protokoll an IGMP zu koordinieren.</span><span class="sxs-lookup"><span data-stu-id="be8ff-104">The multicast group manager uses two callbacks to IGMP to coordinate changes in interface ownership from IGMP to a routing protocol, and from a routing protocol to IGMP.</span></span> <span data-ttu-id="be8ff-105">Die Rückrufe ermöglichen es IGMP, auf einer Schnittstelle mit einem anderen Routing Protokoll (z. b. DVMRP) nebeneinander zu existieren.</span><span class="sxs-lookup"><span data-stu-id="be8ff-105">The callbacks enable IGMP to coexist on an interface with another routing protocol, such as DVMRP.</span></span>

<span data-ttu-id="be8ff-106">Nachdem sich der Besitz einer Schnittstelle geändert hat, ruft der Multicast-Gruppen-Manager zunächst den [**pmgm-Rückruf Rückruf " \_ \_ IGMP \_ Deaktivieren**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) " auf.</span><span class="sxs-lookup"><span data-stu-id="be8ff-106">After the ownership of an interface changes, the multicast group manager first invokes the [**PMGM\_DISABLE\_IGMP\_CALLBACK**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) callback.</span></span> <span data-ttu-id="be8ff-107">IGMP muss das Hinzufügen und Löschen von Gruppenmitgliedschaften auf der angegebenen Schnittstelle verhindern, bis der Multicast-Gruppen-Manager den [**pmgm-Rückruf Rückruf " \_ enable \_ IGMP \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) " aufruft.</span><span class="sxs-lookup"><span data-stu-id="be8ff-107">IGMP must stop adding and deleting group memberships on the specified interface until the multicast group manager invokes the [**PMGM\_ENABLE\_IGMP\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) callback.</span></span>

<span data-ttu-id="be8ff-108">Der Multicast-Gruppen-Manager ruft den [**pmgm- \_ Rückruf " \_ IGMP- \_ Rückruf aktivieren**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) " auf, nachdem die Änderung des Schnittstellen Besitzes beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="be8ff-108">The multicast group manager invokes the [**PMGM\_ENABLE\_IGMP\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) callback after the change of interface ownership is complete.</span></span>

 

 