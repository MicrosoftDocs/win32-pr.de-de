---
description: 'SystemConfig_V0_Power-Klasse: Diese Klasse ist die Ereignistypklasse für Energiekonfigurationsereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
ms.assetid: b3391435-dac0-4c48-b788-eb4d4a7aa635
title: SystemConfig_V0_Power-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Power
- SystemConfig_V0_Power.s1
- SystemConfig_V0_Power.s2
- SystemConfig_V0_Power.s3
- SystemConfig_V0_Power.s4
- SystemConfig_V0_Power.s5
- SystemConfig_V0_Power.Pad1
- SystemConfig_V0_Power.Pad2
- SystemConfig_V0_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab268e719374906e149dc9c1b733487f986e8308
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105938"
---
# <a name="systemconfig_v0_power-class"></a><span data-ttu-id="365ca-104">SystemConfig \_ V0 \_ Power-Klasse</span><span class="sxs-lookup"><span data-stu-id="365ca-104">SystemConfig\_V0\_Power class</span></span>

<span data-ttu-id="365ca-105">Diese Klasse ist die Ereignistypklasse für Energiekonfigurationsereignisse.</span><span class="sxs-lookup"><span data-stu-id="365ca-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="365ca-106">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="365ca-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="365ca-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="365ca-107">Syntax</span></span>

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_V0_Power : SystemConfig_V0
{
  boolean s1;
  boolean s2;
  boolean s3;
  boolean s4;
  boolean s5;
  uint8   Pad1;
  uint8   Pad2;
  uint8   Pad3;
};
```

## <a name="members"></a><span data-ttu-id="365ca-108">Member</span><span class="sxs-lookup"><span data-stu-id="365ca-108">Members</span></span>

<span data-ttu-id="365ca-109">Die **SystemConfig \_ V0 \_ Power-Klasse** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="365ca-109">The **SystemConfig\_V0\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="365ca-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="365ca-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="365ca-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="365ca-111">Properties</span></span>

<span data-ttu-id="365ca-112">Die **SystemConfig \_ V0 \_ Power-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="365ca-112">The **SystemConfig\_V0\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="365ca-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="365ca-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="365ca-114">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="365ca-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="365ca-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="365ca-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="365ca-116">Qualifizierer: WmiDataId(6)</span><span class="sxs-lookup"><span data-stu-id="365ca-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="365ca-117">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="365ca-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="365ca-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="365ca-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="365ca-119">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="365ca-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="365ca-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="365ca-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="365ca-121">Qualifizierer: WmiDataId(7)</span><span class="sxs-lookup"><span data-stu-id="365ca-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="365ca-122">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="365ca-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="365ca-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="365ca-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="365ca-124">Datentyp: **uint8**</span><span class="sxs-lookup"><span data-stu-id="365ca-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="365ca-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="365ca-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="365ca-126">Qualifizierer: WmiDataId(8)</span><span class="sxs-lookup"><span data-stu-id="365ca-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="365ca-127">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="365ca-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="365ca-128">s1</span><span class="sxs-lookup"><span data-stu-id="365ca-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="365ca-129">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="365ca-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="365ca-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="365ca-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="365ca-131">Qualifizierer: WmiDataId(1)</span><span class="sxs-lookup"><span data-stu-id="365ca-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="365ca-132">True gibt an, dass das System den Standbyzustand S1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="365ca-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="365ca-133">s2</span><span class="sxs-lookup"><span data-stu-id="365ca-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="365ca-134">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="365ca-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="365ca-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="365ca-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="365ca-136">Qualifizierer: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="365ca-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="365ca-137">True gibt an, dass das System den Ruhezustand S2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="365ca-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="365ca-138">s3</span><span class="sxs-lookup"><span data-stu-id="365ca-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="365ca-139">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="365ca-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="365ca-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="365ca-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="365ca-141">Qualifizierer: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="365ca-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="365ca-142">True gibt an, dass das System den Ruhezustand S3 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="365ca-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="365ca-143">s4</span><span class="sxs-lookup"><span data-stu-id="365ca-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="365ca-144">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="365ca-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="365ca-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="365ca-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="365ca-146">Qualifizierer: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="365ca-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="365ca-147">True gibt an, dass das System den Ruhezustand S4 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="365ca-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="365ca-148">s5</span><span class="sxs-lookup"><span data-stu-id="365ca-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="365ca-149">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="365ca-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="365ca-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="365ca-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="365ca-151">Qualifizierer: WmiDataId(5)</span><span class="sxs-lookup"><span data-stu-id="365ca-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="365ca-152">True gibt an, dass das System den Ruhezustand S5 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="365ca-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="365ca-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="365ca-153">Requirements</span></span>



| <span data-ttu-id="365ca-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="365ca-154">Requirement</span></span> | <span data-ttu-id="365ca-155">Wert</span><span class="sxs-lookup"><span data-stu-id="365ca-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="365ca-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="365ca-156">Minimum supported client</span></span><br/> | <span data-ttu-id="365ca-157">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="365ca-157">None supported</span></span><br/>                            |
| <span data-ttu-id="365ca-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="365ca-158">Minimum supported server</span></span><br/> | <span data-ttu-id="365ca-159">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="365ca-159">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="365ca-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="365ca-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="365ca-161">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="365ca-161">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




