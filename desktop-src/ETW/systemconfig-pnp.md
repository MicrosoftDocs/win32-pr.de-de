---
description: Diese Klasse ist die Ereignistyp Klasse für PNP-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 01e9a8bb-3f54-4e20-b4db-1b4bba745d4f
title: SystemConfig_PnP-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PnP
- SystemConfig_PnP.IDLength
- SystemConfig_PnP.DescriptionLength
- SystemConfig_PnP.FriendlyNameLength
- SystemConfig_PnP.DeviceID
- SystemConfig_PnP.DeviceDescription
- SystemConfig_PnP.FriendlyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2bd4cdbbec5c61f453a0ef6fae3fef0bd494edac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484667"
---
# <a name="systemconfig_pnp-class"></a><span data-ttu-id="2895b-104">SystemConfig- \_ PnP-Klasse</span><span class="sxs-lookup"><span data-stu-id="2895b-104">SystemConfig\_PnP class</span></span>

<span data-ttu-id="2895b-105">Diese Klasse ist die Ereignistyp Klasse für PNP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="2895b-105">This class is the event type class for PnP events.</span></span>

<span data-ttu-id="2895b-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="2895b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2895b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2895b-107">Syntax</span></span>

``` syntax
[EventType(22), EventTypeName("PnP")]
class SystemConfig_PnP : SystemConfig
{
  uint32 IDLength;
  uint32 DescriptionLength;
  uint32 FriendlyNameLength;
  string DeviceID;
  string DeviceDescription;
  string FriendlyName;
};
```

## <a name="members"></a><span data-ttu-id="2895b-108">Member</span><span class="sxs-lookup"><span data-stu-id="2895b-108">Members</span></span>

<span data-ttu-id="2895b-109">Die " **SystemConfig \_ PnP** "-Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2895b-109">The **SystemConfig\_PnP** class has these types of members:</span></span>

-   [<span data-ttu-id="2895b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2895b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2895b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2895b-111">Properties</span></span>

<span data-ttu-id="2895b-112">Die " **SystemConfig \_ PnP** "-Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2895b-112">The **SystemConfig\_PnP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2895b-113">**Deskriptionlength**</span><span class="sxs-lookup"><span data-stu-id="2895b-113">**DescriptionLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2895b-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2895b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2895b-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2895b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2895b-116">Qualifizierer: wmidataid (2)</span><span class="sxs-lookup"><span data-stu-id="2895b-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="2895b-117">Länge der devicedescription-Zeichenfolge in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2895b-117">Length, in characters, of the DeviceDescription string.</span></span>

</dd> <dt>

<span data-ttu-id="2895b-118">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="2895b-118">**DeviceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2895b-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2895b-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2895b-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2895b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2895b-121">Qualifizierer: wmidataid (5), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="2895b-121">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="2895b-122">Die Beschreibung des PNP-Geräts.</span><span class="sxs-lookup"><span data-stu-id="2895b-122">Description of the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="2895b-123">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2895b-123">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2895b-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2895b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2895b-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2895b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2895b-126">Qualifizierer: wmidataid (4), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="2895b-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="2895b-127">Identifiziert das PNP-Gerät.</span><span class="sxs-lookup"><span data-stu-id="2895b-127">Identifies the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="2895b-128">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="2895b-128">**FriendlyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2895b-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2895b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2895b-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2895b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2895b-131">Qualifizierer: wmidataid (6), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="2895b-131">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="2895b-132">Der Name des PNP-Geräts, der in einer Benutzeroberfläche verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2895b-132">Name of the PnP device to use in a user interface.</span></span>

</dd> <dt>

<span data-ttu-id="2895b-133">**Friendlynamelength**</span><span class="sxs-lookup"><span data-stu-id="2895b-133">**FriendlyNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2895b-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2895b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2895b-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2895b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2895b-136">Qualifizierer: wmidataid (3)</span><span class="sxs-lookup"><span data-stu-id="2895b-136">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="2895b-137">Länge der FriendlyName-Zeichenfolge in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2895b-137">Length, in characters, of the FriendlyName string.</span></span>

</dd> <dt>

<span data-ttu-id="2895b-138">**Idlength**</span><span class="sxs-lookup"><span data-stu-id="2895b-138">**IDLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2895b-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2895b-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2895b-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2895b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2895b-141">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="2895b-141">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="2895b-142">Länge in Zeichen der Zeichenfolge "enviceid".</span><span class="sxs-lookup"><span data-stu-id="2895b-142">Length, in characters, of the DeviceID string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2895b-143">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2895b-143">Requirements</span></span>



| <span data-ttu-id="2895b-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2895b-144">Requirement</span></span> | <span data-ttu-id="2895b-145">Wert</span><span class="sxs-lookup"><span data-stu-id="2895b-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2895b-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2895b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="2895b-147">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2895b-147">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2895b-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2895b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="2895b-149">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2895b-149">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2895b-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2895b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2895b-151">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="2895b-151">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




