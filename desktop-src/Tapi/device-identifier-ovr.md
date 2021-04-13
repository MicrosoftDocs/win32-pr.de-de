---
description: Eine Geräte-ID ist ein Anwendungs unabhängiger Bezeichner für ein bestimmtes Kommunikationsgerät.
ms.assetid: c7ca72a6-97fa-441f-92ce-a4c77a53765c
title: Gerätebezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb9c88820ecfe26d3ecd971489d709a34af10f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529078"
---
# <a name="device-identifier"></a><span data-ttu-id="422f5-103">Gerätebezeichner</span><span class="sxs-lookup"><span data-stu-id="422f5-103">Device Identifier</span></span>

<span data-ttu-id="422f5-104">Eine *Geräte-ID* ist ein Anwendungs unabhängiger Bezeichner für ein bestimmtes Kommunikationsgerät.</span><span class="sxs-lookup"><span data-stu-id="422f5-104">A *device ID* is an application-independent identifier for a specific communications device.</span></span> <span data-ttu-id="422f5-105">Dies ist in der Regel nur erforderlich, wenn eine TAPI-Anwendung einen Teil der Verarbeitung an eine Kommunikationssitzung an die Funktionen einer anderen API übergeben muss.</span><span class="sxs-lookup"><span data-stu-id="422f5-105">It is typically needed only when a TAPI application needs to hand off part of the processing involving in a communications session to the functions of a different API.</span></span> <span data-ttu-id="422f5-106">TAPI 2,2-Anwendungen können z. b. möglicherweise nicht direkt auf einen Medienstrom zugreifen und können die Wave-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="422f5-106">For example, TAPI 2.2 applications may be unable to directly access a media stream and might use the Wave API.</span></span>

<span data-ttu-id="422f5-107">**TAPI 2. x:** Siehe [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).</span><span class="sxs-lookup"><span data-stu-id="422f5-107">**TAPI 2.x:** See [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="422f5-108">**TAPI 3. x:** Siehe [**itaddresscapability:: get \_ addresscapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*addresscap* festgelegt auf den **AC \_ PERMANENTDEVICEID** Member of [**Address \_ Capability**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).</span><span class="sxs-lookup"><span data-stu-id="422f5-108">**TAPI 3.x:** See [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* set to the **AC\_PERMANENTDEVICEID** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).</span></span>

 

 
