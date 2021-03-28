---
description: Diese Klasse ist die Ereignistyp Klasse für IDE-Kanal Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: SystemConfig_IDEChannel-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IDEChannel
- SystemConfig_IDEChannel.TargetId
- SystemConfig_IDEChannel.DeviceType
- SystemConfig_IDEChannel.DeviceTimingMode
- SystemConfig_IDEChannel.LocationInformationLen
- SystemConfig_IDEChannel.LocationInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60cdfcec8f62e6fb96dcedc895d874f01a209430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526381"
---
# <a name="systemconfig_idechannel-class"></a><span data-ttu-id="0c432-104">SystemConfig- \_ idechannel-Klasse</span><span class="sxs-lookup"><span data-stu-id="0c432-104">SystemConfig\_IDEChannel class</span></span>

<span data-ttu-id="0c432-105">Diese Klasse ist die Ereignistyp Klasse für IDE-Kanal Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="0c432-105">This class is the event type class for IDE channel events.</span></span>

<span data-ttu-id="0c432-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="0c432-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c432-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c432-107">Syntax</span></span>

``` syntax
[EventType(23), EventTypeName("IDEChannel")]
class SystemConfig_IDEChannel : SystemConfig
{
  uint32 TargetId;
  uint32 DeviceType;
  uint32 DeviceTimingMode;
  uint32 LocationInformationLen;
  string LocationInformation;
};
```

## <a name="members"></a><span data-ttu-id="0c432-108">Member</span><span class="sxs-lookup"><span data-stu-id="0c432-108">Members</span></span>

<span data-ttu-id="0c432-109">Die **\_ idechannel** -Klasse von SystemConfig verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0c432-109">The **SystemConfig\_IDEChannel** class has these types of members:</span></span>

-   [<span data-ttu-id="0c432-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0c432-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c432-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0c432-111">Properties</span></span>

<span data-ttu-id="0c432-112">Die **\_ idechannel** -Klasse von SystemConfig verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0c432-112">The **SystemConfig\_IDEChannel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c432-113">**Devicetimingmode**</span><span class="sxs-lookup"><span data-stu-id="0c432-113">**DeviceTimingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c432-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c432-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c432-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c432-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c432-116">Qualifizierer: wmidataid (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="0c432-116">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="0c432-117">Der Modus, in dem die IDE funktionieren könnte.</span><span class="sxs-lookup"><span data-stu-id="0c432-117">The mode in which the IDE could function.</span></span> <span data-ttu-id="0c432-118">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="0c432-118">The following are the possible values:</span></span>

-   <span data-ttu-id="0c432-119">Pio \_ MODE0 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0c432-119">PIO\_MODE0 (0x1)</span></span>
-   <span data-ttu-id="0c432-120">Pio \_ MODE1 (0x2)</span><span class="sxs-lookup"><span data-stu-id="0c432-120">PIO\_MODE1 (0x2)</span></span>
-   <span data-ttu-id="0c432-121">Pio \_ Mode2 (0x4)</span><span class="sxs-lookup"><span data-stu-id="0c432-121">PIO\_MODE2 (0x4)</span></span>
-   <span data-ttu-id="0c432-122">Pio \_ MODE3 (0x8)</span><span class="sxs-lookup"><span data-stu-id="0c432-122">PIO\_MODE3 (0x8)</span></span>
-   <span data-ttu-id="0c432-123">Pio \_ MODE4 (0x10)</span><span class="sxs-lookup"><span data-stu-id="0c432-123">PIO\_MODE4 (0x10)</span></span>
-   <span data-ttu-id="0c432-124">Swap- \_ MODE0 (0x20)</span><span class="sxs-lookup"><span data-stu-id="0c432-124">SWDMA\_MODE0 (0x20)</span></span>
-   <span data-ttu-id="0c432-125">MODE1-Datei \_ (0x40)</span><span class="sxs-lookup"><span data-stu-id="0c432-125">SWDMA\_MODE1 (0x40)</span></span>
-   <span data-ttu-id="0c432-126">Swap- \_ Mode2 (0x80)</span><span class="sxs-lookup"><span data-stu-id="0c432-126">SWDMA\_MODE2 (0x80)</span></span>
-   <span data-ttu-id="0c432-127">Mwdma \_ MODE0 (0x100)</span><span class="sxs-lookup"><span data-stu-id="0c432-127">MWDMA\_MODE0 (0x100)</span></span>
-   <span data-ttu-id="0c432-128">Mwdma \_ Mode2 (0x200)</span><span class="sxs-lookup"><span data-stu-id="0c432-128">MWDMA\_MODE2 (0x200)</span></span>
-   <span data-ttu-id="0c432-129">Mwdma \_ MODE3 (0x400)</span><span class="sxs-lookup"><span data-stu-id="0c432-129">MWDMA\_MODE3 (0x400)</span></span>
-   <span data-ttu-id="0c432-130">UDMA \_ MODE0 (0x800)</span><span class="sxs-lookup"><span data-stu-id="0c432-130">UDMA\_MODE0 (0x800)</span></span>
-   <span data-ttu-id="0c432-131">UDMA \_ MODE1 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="0c432-131">UDMA\_MODE1 (0x1000)</span></span>
-   <span data-ttu-id="0c432-132">UDMA \_ Mode2 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="0c432-132">UDMA\_MODE2 (0x2000)</span></span>
-   <span data-ttu-id="0c432-133">UDMA \_ MODE3 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="0c432-133">UDMA\_MODE3 (0x4000)</span></span>
-   <span data-ttu-id="0c432-134">UDMA \_ MODE4 (0X8000)</span><span class="sxs-lookup"><span data-stu-id="0c432-134">UDMA\_MODE4 (0x8000)</span></span>
-   <span data-ttu-id="0c432-135">UDMA \_ MODE5 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="0c432-135">UDMA\_MODE5 (0x10000)</span></span>

</dd> <dt>

<span data-ttu-id="0c432-136">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="0c432-136">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c432-137">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c432-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c432-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c432-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c432-139">Qualifizierer: wmidataid (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="0c432-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="0c432-140">Der Gerätetyp.</span><span class="sxs-lookup"><span data-stu-id="0c432-140">The device type.</span></span> <span data-ttu-id="0c432-141">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="0c432-141">The following are the possible values:</span></span>

-   <span data-ttu-id="0c432-142">ATA (1)</span><span class="sxs-lookup"><span data-stu-id="0c432-142">ATA (1)</span></span>
-   <span data-ttu-id="0c432-143">ATAPI (2)</span><span class="sxs-lookup"><span data-stu-id="0c432-143">ATAPI (2)</span></span>

</dd> <dt>

<span data-ttu-id="0c432-144">**Locationinformation**</span><span class="sxs-lookup"><span data-stu-id="0c432-144">**LocationInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c432-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c432-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c432-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c432-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c432-147">Qualifizierer: wmidataid (5), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="0c432-147">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="0c432-148">Der IDE-Kanal (z. b. primärer Kanal, sekundärer Kanal usw.).</span><span class="sxs-lookup"><span data-stu-id="0c432-148">The IDE channel (for example, Primary Channel, Secondary Channel, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="0c432-149">**Locationinformationlen**</span><span class="sxs-lookup"><span data-stu-id="0c432-149">**LocationInformationLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c432-150">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c432-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c432-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c432-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c432-152">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="0c432-152">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="0c432-153">Länge der **locationinformation** -Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0c432-153">Length of the **LocationInformation** string.</span></span>

</dd> <dt>

<span data-ttu-id="0c432-154">**TargetId**</span><span class="sxs-lookup"><span data-stu-id="0c432-154">**TargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c432-155">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c432-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c432-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c432-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c432-157">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="0c432-157">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="0c432-158">Der Bezeichner des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="0c432-158">The identifier of the disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c432-159">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0c432-159">Requirements</span></span>



| <span data-ttu-id="0c432-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c432-160">Requirement</span></span> | <span data-ttu-id="0c432-161">Wert</span><span class="sxs-lookup"><span data-stu-id="0c432-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0c432-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c432-162">Minimum supported client</span></span><br/> | <span data-ttu-id="0c432-163">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c432-163">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0c432-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c432-164">Minimum supported server</span></span><br/> | <span data-ttu-id="0c432-165">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c432-165">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c432-166">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0c432-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c432-167">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="0c432-167">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




