---
description: Diese Klasse ist die Ereignistyp Klasse für Interrupt Request (UNQ)-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 9d4692e8-f19f-478c-a003-396722e426c3
title: SystemConfig_IRQ-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IRQ
- SystemConfig_IRQ.IRQAffinity
- SystemConfig_IRQ.IRQNum
- SystemConfig_IRQ.DeviceDescriptionLen
- SystemConfig_IRQ.DeviceDescription
api_type:
- NA
api_location: ''
ms.openlocfilehash: e1dd674c34c06259bc343615c17d165be3f57d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977592"
---
# <a name="systemconfig_irq-class"></a><span data-ttu-id="e2e7a-104">SystemConfig- \_ Klasse "UNQ"</span><span class="sxs-lookup"><span data-stu-id="e2e7a-104">SystemConfig\_IRQ class</span></span>

<span data-ttu-id="e2e7a-105">Diese Klasse ist die Ereignistyp Klasse für Interrupt Request (UNQ)-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="e2e7a-105">This class is the event type class for interrupt request (IRQ) events.</span></span>

<span data-ttu-id="e2e7a-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="e2e7a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e7a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2e7a-107">Syntax</span></span>

``` syntax
[EventType(21), EventTypeName("IRQ")]
class SystemConfig_IRQ : SystemConfig
{
  uint64 IRQAffinity;
  uint32 IRQNum;
  uint32 DeviceDescriptionLen;
  string DeviceDescription;
};
```

## <a name="members"></a><span data-ttu-id="e2e7a-108">Member</span><span class="sxs-lookup"><span data-stu-id="e2e7a-108">Members</span></span>

<span data-ttu-id="e2e7a-109">Die **SystemConfig-Klasse " \_ UNQ** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e2e7a-109">The **SystemConfig\_IRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="e2e7a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2e7a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2e7a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2e7a-111">Properties</span></span>

<span data-ttu-id="e2e7a-112">Die **SystemConfig-Klasse " \_ UNQ** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e2e7a-112">The **SystemConfig\_IRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2e7a-113">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="e2e7a-113">**DeviceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e7a-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2e7a-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2e7a-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2e7a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2e7a-116">Qualifizierer: wmidataid (4), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="e2e7a-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="e2e7a-117">Die Beschreibung des Geräts oder der Software, die die Anforderung sendet.</span><span class="sxs-lookup"><span data-stu-id="e2e7a-117">Description of the device or software making the request.</span></span>

</dd> <dt>

<span data-ttu-id="e2e7a-118">**Devicedescriptionlen**</span><span class="sxs-lookup"><span data-stu-id="e2e7a-118">**DeviceDescriptionLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e7a-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2e7a-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2e7a-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2e7a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2e7a-121">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="e2e7a-121">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e2e7a-122">Länge in Zeichen der Zeichenfolge in **devicedescription**.</span><span class="sxs-lookup"><span data-stu-id="e2e7a-122">Length, in characters, of the string in **DeviceDescription**.</span></span>

</dd> <dt>

<span data-ttu-id="e2e7a-123">**Unqaffinität**</span><span class="sxs-lookup"><span data-stu-id="e2e7a-123">**IRQAffinity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e7a-124">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2e7a-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2e7a-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2e7a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2e7a-126">Qualifizierer: wmidataid (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="e2e7a-126">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="e2e7a-127">UNQ-Affinitäts Maske.</span><span class="sxs-lookup"><span data-stu-id="e2e7a-127">IRQ affinity mask.</span></span> <span data-ttu-id="e2e7a-128">Die Affinitäts Maske identifiziert die spezifischen Prozessoren (oder Gruppen von Prozessoren), die die UNQ empfangen können.</span><span class="sxs-lookup"><span data-stu-id="e2e7a-128">The affinity mask identifies the specific processors (or groups of processors) that can receive the IRQ.</span></span>

</dd> <dt>

<span data-ttu-id="e2e7a-129">**Unqnum**</span><span class="sxs-lookup"><span data-stu-id="e2e7a-129">**IRQNum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e7a-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2e7a-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2e7a-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2e7a-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2e7a-132">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="e2e7a-132">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="e2e7a-133">Die Zeilennummer der Interrupt-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e2e7a-133">Interrupt request line number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2e7a-134">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e2e7a-134">Requirements</span></span>



| <span data-ttu-id="e2e7a-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2e7a-135">Requirement</span></span> | <span data-ttu-id="e2e7a-136">Wert</span><span class="sxs-lookup"><span data-stu-id="e2e7a-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e2e7a-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2e7a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e2e7a-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2e7a-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e2e7a-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2e7a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e2e7a-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2e7a-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2e7a-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e2e7a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e7a-142">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="e2e7a-142">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




