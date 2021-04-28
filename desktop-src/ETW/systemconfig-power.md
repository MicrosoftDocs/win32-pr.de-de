---
description: 'SystemConfig_Power Klasse: Diese Klasse ist die Ereignistypklasse für Energiekonfigurationsereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: 7065b0b0-9a1d-4fce-a494-5762d5efb239
title: SystemConfig_Power-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Power
- SystemConfig_Power.s1
- SystemConfig_Power.s2
- SystemConfig_Power.s3
- SystemConfig_Power.s4
- SystemConfig_Power.s5
- SystemConfig_Power.Pad1
- SystemConfig_Power.Pad2
- SystemConfig_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: d7338faad8c313847ad7db7aaac5d4000abba5be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106068"
---
# <a name="systemconfig_power-class"></a><span data-ttu-id="91065-104">SystemConfig \_ Power Class</span><span class="sxs-lookup"><span data-stu-id="91065-104">SystemConfig\_Power class</span></span>

<span data-ttu-id="91065-105">Diese Klasse ist die Ereignistypklasse für Energiekonfigurationsereignisse.</span><span class="sxs-lookup"><span data-stu-id="91065-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="91065-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="91065-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="91065-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="91065-107">Syntax</span></span>

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_Power : SystemConfig
{
  uint8 s1;
  uint8 s2;
  uint8 s3;
  uint8 s4;
  uint8 s5;
  uint8 Pad1;
  uint8 Pad2;
  uint8 Pad3;
};
```

## <a name="members"></a><span data-ttu-id="91065-108">Member</span><span class="sxs-lookup"><span data-stu-id="91065-108">Members</span></span>

<span data-ttu-id="91065-109">Die **SystemConfig \_ Power-Klasse** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="91065-109">The **SystemConfig\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="91065-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91065-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91065-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91065-111">Properties</span></span>

<span data-ttu-id="91065-112">Die **SystemConfig \_ Power-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="91065-112">The **SystemConfig\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91065-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="91065-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91065-114">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="91065-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="91065-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91065-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91065-116">Qualifizierer: WmiDataId(6)</span><span class="sxs-lookup"><span data-stu-id="91065-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="91065-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="91065-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="91065-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="91065-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91065-119">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="91065-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="91065-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91065-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91065-121">Qualifizierer: WmiDataId(7)</span><span class="sxs-lookup"><span data-stu-id="91065-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="91065-122">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="91065-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="91065-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="91065-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91065-124">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="91065-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="91065-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91065-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91065-126">Qualifizierer: WmiDataId(8)</span><span class="sxs-lookup"><span data-stu-id="91065-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="91065-127">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="91065-127">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="91065-128">s1</span><span class="sxs-lookup"><span data-stu-id="91065-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91065-129">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="91065-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="91065-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91065-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91065-131">Qualifizierer: WmiDataId(1)</span><span class="sxs-lookup"><span data-stu-id="91065-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="91065-132">True gibt an, dass das System den Ruhezustand S1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91065-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="91065-133">s2</span><span class="sxs-lookup"><span data-stu-id="91065-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91065-134">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="91065-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="91065-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91065-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91065-136">Qualifizierer: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="91065-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="91065-137">True gibt an, dass das System den Standbyzustand S2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91065-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="91065-138">s3</span><span class="sxs-lookup"><span data-stu-id="91065-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91065-139">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="91065-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="91065-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91065-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91065-141">Qualifizierer: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="91065-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="91065-142">True gibt an, dass das System den Standbyzustand S3 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91065-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="91065-143">s4</span><span class="sxs-lookup"><span data-stu-id="91065-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91065-144">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="91065-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="91065-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91065-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91065-146">Qualifizierer: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="91065-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="91065-147">True gibt an, dass das System den Standbyzustand S4 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91065-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="91065-148">s5</span><span class="sxs-lookup"><span data-stu-id="91065-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91065-149">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="91065-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="91065-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91065-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91065-151">Qualifizierer: WmiDataId(5)</span><span class="sxs-lookup"><span data-stu-id="91065-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="91065-152">True gibt an, dass das System den Standbyzustand S5 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91065-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91065-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91065-153">Requirements</span></span>



| <span data-ttu-id="91065-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91065-154">Requirement</span></span> | <span data-ttu-id="91065-155">Wert</span><span class="sxs-lookup"><span data-stu-id="91065-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="91065-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91065-156">Minimum supported client</span></span><br/> | <span data-ttu-id="91065-157">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91065-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="91065-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91065-158">Minimum supported server</span></span><br/> | <span data-ttu-id="91065-159">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91065-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91065-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="91065-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91065-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="91065-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




