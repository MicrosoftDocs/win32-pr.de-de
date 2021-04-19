---
description: Die linecalltreatment- \_ Konstanten Listen Behandlungen für Aufrufe auf, die nicht beantwortet werden oder angehalten sind. Mit Ausnahme der grundlegenden Parameter Validierung ist die aufrufsbehandlung ein geradliniges Pass-Through von TAPI zum Dienstanbieter.
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: LINECALLTREATMENT_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25a19b5db4525550047c468b496cce2363f6ee2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373980"
---
# <a name="linecalltreatment_-constants"></a><span data-ttu-id="72d0e-104">Linecalltreatment- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="72d0e-104">LINECALLTREATMENT\_ Constants</span></span>

<span data-ttu-id="72d0e-105">Die **linecalltreatment \_** -Konstanten Listen Behandlungen für Aufrufe auf, die nicht beantwortet werden oder angehalten sind.</span><span class="sxs-lookup"><span data-stu-id="72d0e-105">The **LINECALLTREATMENT\_** constants list treatments for calls that are unanswered or on hold.</span></span> <span data-ttu-id="72d0e-106">Mit Ausnahme der grundlegenden Parameter Validierung ist die aufrufsbehandlung ein geradliniges Pass-Through von TAPI zum Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="72d0e-106">Except for basic parameter validation, call treatment is a straight pass-through by TAPI to the service provider.</span></span>

<dl> <dt>

<span data-ttu-id="72d0e-107"><span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**linecalltreatment \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="72d0e-107"><span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="72d0e-108">Wenn der-Rückruf nicht aktiv mit einem Gerät (Angebot oder OnHold) verbunden ist, hört die Partei das ausgelastete Signal.</span><span class="sxs-lookup"><span data-stu-id="72d0e-108">When the call is not actively connected to a device (offering or onhold), the party hears busy signal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="72d0e-109"><span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**linecalltreatment- \_ Musik**</span><span class="sxs-lookup"><span data-stu-id="72d0e-109"><span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**LINECALLTREATMENT\_MUSIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="72d0e-110">Wenn der-Befehl nicht aktiv mit einem Gerät (Angebot oder OnHold) verbunden ist, hört die Partei Musik.</span><span class="sxs-lookup"><span data-stu-id="72d0e-110">When the call is not actively connected to a device (offering or onhold), the party hears music.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="72d0e-111"><span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**linecalltreatment- \_ Rollback**</span><span class="sxs-lookup"><span data-stu-id="72d0e-111"><span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="72d0e-112">Wenn der-Befehl nicht aktiv mit einem Gerät (Angebot oder OnHold) verbunden ist, hört die Partei den ringbackton.</span><span class="sxs-lookup"><span data-stu-id="72d0e-112">When the call is not actively connected to a device (offering or onhold), the party hears ringback tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="72d0e-113"><span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**Ruhe Behandlung in linecalltreatment \_**</span><span class="sxs-lookup"><span data-stu-id="72d0e-113"><span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**LINECALLTREATMENT\_SILENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="72d0e-114">Wenn der-Befehl nicht aktiv mit einem Gerät (Angebot oder OnHold) verbunden ist, hört die Partei Ruhe.</span><span class="sxs-lookup"><span data-stu-id="72d0e-114">When the call is not actively connected to a device (offering or onhold), the party hears silence.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72d0e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72d0e-115">Remarks</span></span>

<span data-ttu-id="72d0e-116">Der Wert 0x00000000 ist reserviert, um anzugeben, dass der Dienstanbieter keine aufrufsbehandlungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="72d0e-116">The value 0x00000000 is reserved to indicate that the service provider does not support call treatments.</span></span> <span data-ttu-id="72d0e-117">Werte im Bereich 0x00000005 bei der bis 0x000000ff sind für zukünftige Definitionen reserviert.</span><span class="sxs-lookup"><span data-stu-id="72d0e-117">Values in the range 0x00000005 through 0x000000FF are reserved for future definition.</span></span> <span data-ttu-id="72d0e-118">Werte im Bereich 0x00000100 bis 0xffffffff sind für die Zuweisung durch Dienstanbieter reserviert und können die Identifizierung bestimmter musikalischer oder aufgezeichneter Ankündigungen einschließen.</span><span class="sxs-lookup"><span data-stu-id="72d0e-118">Values in the range 0x00000100 through 0xFFFFFFFF are reserved for assignment by service providers, and may include identification of specific musical selections or recorded announcements.</span></span>

## <a name="requirements"></a><span data-ttu-id="72d0e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72d0e-119">Requirements</span></span>



| <span data-ttu-id="72d0e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72d0e-120">Requirement</span></span> | <span data-ttu-id="72d0e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="72d0e-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="72d0e-122">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="72d0e-122">TAPI version</span></span><br/> | <span data-ttu-id="72d0e-123">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="72d0e-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="72d0e-124">Header</span><span class="sxs-lookup"><span data-stu-id="72d0e-124">Header</span></span><br/>       | <dl> <span data-ttu-id="72d0e-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="72d0e-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




