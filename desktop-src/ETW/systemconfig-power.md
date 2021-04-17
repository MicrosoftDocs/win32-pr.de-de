---
description: Diese Klasse ist die Ereignistyp Klasse für Energie Konfigurations Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: d27586451f944ac9c94e9ec2d204035c21f37679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977473"
---
# <a name="systemconfig_power-class"></a><span data-ttu-id="e7445-104">SystemConfig- \_ Power Class</span><span class="sxs-lookup"><span data-stu-id="e7445-104">SystemConfig\_Power class</span></span>

<span data-ttu-id="e7445-105">Diese Klasse ist die Ereignistyp Klasse für Energie Konfigurations Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="e7445-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="e7445-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="e7445-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7445-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7445-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="e7445-108">Member</span><span class="sxs-lookup"><span data-stu-id="e7445-108">Members</span></span>

<span data-ttu-id="e7445-109">Die **System config- \_ Power** Class verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e7445-109">The **SystemConfig\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="e7445-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7445-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7445-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7445-111">Properties</span></span>

<span data-ttu-id="e7445-112">Die **System config- \_ Power** Class verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e7445-112">The **SystemConfig\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7445-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="e7445-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7445-114">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e7445-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e7445-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e7445-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7445-116">Qualifizierer: wmidataid (6)</span><span class="sxs-lookup"><span data-stu-id="e7445-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="e7445-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7445-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e7445-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="e7445-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7445-119">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e7445-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e7445-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e7445-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7445-121">Qualifizierer: wmidataid (7)</span><span class="sxs-lookup"><span data-stu-id="e7445-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="e7445-122">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7445-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e7445-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="e7445-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7445-124">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e7445-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e7445-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e7445-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7445-126">Qualifizierer: wmidataid (8)</span><span class="sxs-lookup"><span data-stu-id="e7445-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="e7445-127">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7445-127">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="e7445-128">s1</span><span class="sxs-lookup"><span data-stu-id="e7445-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7445-129">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e7445-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e7445-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e7445-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7445-131">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="e7445-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="e7445-132">True gibt an, dass das System den Ruhezustand S1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e7445-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="e7445-133">s2</span><span class="sxs-lookup"><span data-stu-id="e7445-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7445-134">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e7445-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e7445-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e7445-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7445-136">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="e7445-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="e7445-137">True gibt an, dass das System den Ruhezustand S2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e7445-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="e7445-138">s3</span><span class="sxs-lookup"><span data-stu-id="e7445-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7445-139">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e7445-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e7445-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e7445-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7445-141">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="e7445-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e7445-142">True gibt an, dass das System den Ruhezustand S3 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e7445-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="e7445-143">verkehrt</span><span class="sxs-lookup"><span data-stu-id="e7445-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7445-144">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e7445-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e7445-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e7445-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7445-146">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="e7445-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="e7445-147">True gibt an, dass das System den Ruhezustand S4 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e7445-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="e7445-148">S5</span><span class="sxs-lookup"><span data-stu-id="e7445-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7445-149">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e7445-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e7445-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e7445-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7445-151">Qualifizierer: wmidataid (5)</span><span class="sxs-lookup"><span data-stu-id="e7445-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="e7445-152">True gibt an, dass das System den Ruhezustand S5 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e7445-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7445-153">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e7445-153">Requirements</span></span>



| <span data-ttu-id="e7445-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7445-154">Requirement</span></span> | <span data-ttu-id="e7445-155">Wert</span><span class="sxs-lookup"><span data-stu-id="e7445-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e7445-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7445-156">Minimum supported client</span></span><br/> | <span data-ttu-id="e7445-157">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7445-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e7445-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7445-158">Minimum supported server</span></span><br/> | <span data-ttu-id="e7445-159">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7445-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7445-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e7445-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7445-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="e7445-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




