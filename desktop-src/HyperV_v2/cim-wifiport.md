---
description: Stellt ein Drahtlos Netzwerk Kommunikationsgerät dar, das der IEEE 802,11-Reihe von Spezifikationen entspricht.
ms.assetid: c4e3345f-5c7d-4d1d-9a94-64112d7334ff
title: CIM_WiFiPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiPort
- CIM_WiFiPort.Speed
- CIM_WiFiPort.MaxSpeed
- CIM_WiFiPort.PortType
- CIM_WiFiPort.PermanentAddress
- CIM_WiFiPort.NetworkAddresses
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 098bd0a3795f3e8e0531be5286a65b79d9f6ee0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865779"
---
# <a name="cim_wifiport-class"></a><span data-ttu-id="eee0b-103">CIM- \_ wifport-Klasse</span><span class="sxs-lookup"><span data-stu-id="eee0b-103">CIM\_WiFiPort class</span></span>

<span data-ttu-id="eee0b-104">Stellt ein Drahtlos Netzwerk Kommunikationsgerät dar, das der IEEE 802,11-Reihe von Spezifikationen entspricht.</span><span class="sxs-lookup"><span data-stu-id="eee0b-104">Represents a wireless local area network communications device that conforms to the IEEE 802.11 series of specifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="eee0b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eee0b-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_WiFiPort : CIM_NetworkPort
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint16 PortType;
  string PermanentAddress;
  string NetworkAddresses[];
};
```

## <a name="members"></a><span data-ttu-id="eee0b-106">Member</span><span class="sxs-lookup"><span data-stu-id="eee0b-106">Members</span></span>

<span data-ttu-id="eee0b-107">Die **CIM- \_ wifport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eee0b-107">The **CIM\_WiFiPort** class has these types of members:</span></span>

-   [<span data-ttu-id="eee0b-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eee0b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eee0b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eee0b-109">Properties</span></span>

<span data-ttu-id="eee0b-110">Die **CIM- \_ wifport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eee0b-110">The **CIM\_WiFiPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eee0b-111">**MAXSPEED**</span><span class="sxs-lookup"><span data-stu-id="eee0b-111">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee0b-112">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eee0b-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eee0b-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eee0b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eee0b-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("MAXSPEED")</span><span class="sxs-lookup"><span data-stu-id="eee0b-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxSpeed")</span></span>
</dt> </dl>

<span data-ttu-id="eee0b-115">Die maximal unterstützte Bandbreite in Bits pro Sekunde basierend auf dem Betriebsmodus, der in der **portType** -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="eee0b-115">The maximum supported bandwidth, in bits per second, based on the operating mode specified in the **PortType** property.</span></span> <span data-ttu-id="eee0b-116">**MAXSPEED** ist beispielsweise "11 Millionen", wenn " **portType** " "71" (802.11 b) enthält.</span><span class="sxs-lookup"><span data-stu-id="eee0b-116">For example, **MaxSpeed** is "11000000" if **PortType** contains "71" (802.11b).</span></span>

</dd> <dt>

<span data-ttu-id="eee0b-117">**"Networkaddresses"**</span><span class="sxs-lookup"><span data-stu-id="eee0b-117">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee0b-118">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="eee0b-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eee0b-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eee0b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eee0b-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Netzwerkadressen")</span><span class="sxs-lookup"><span data-stu-id="eee0b-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span></span>
</dt> </dl>

<span data-ttu-id="eee0b-121">Ein Array, das die IEEE 802 EUI-48 Mac-Adressen enthält.</span><span class="sxs-lookup"><span data-stu-id="eee0b-121">An array that contains the IEEE 802 EUI-48 MAC addresses.</span></span> <span data-ttu-id="eee0b-122">Die Mac-Adresse ist als zwölf hexadezimal Ziffern formatiert, wobei jedes Paar einen der sechs Oktette der Mac-Adresse in kanonischer bitreihenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="eee0b-122">The MAC address is formatted as twelve hexadecimal digits, with each pair representing one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="eee0b-123">**Permanent Address**</span><span class="sxs-lookup"><span data-stu-id="eee0b-123">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee0b-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eee0b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eee0b-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eee0b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eee0b-126">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Permanent Address")</span><span class="sxs-lookup"><span data-stu-id="eee0b-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PermanentAddress")</span></span>
</dt> </dl>

<span data-ttu-id="eee0b-127">Die IEEE 802 EUI-48 Mac-Adresse des Ports.</span><span class="sxs-lookup"><span data-stu-id="eee0b-127">The IEEE 802 EUI-48 MAC address of the port.</span></span> <span data-ttu-id="eee0b-128">Die Mac-Adresse ist als zwölf hexadezimal Ziffern formatiert, wobei jedes Paar einen der sechs Oktette der Mac-Adresse in kanonischer bitreihenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="eee0b-128">The MAC address is formatted as twelve hexadecimal digits, with each pair representing one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="eee0b-129">**PortType**</span><span class="sxs-lookup"><span data-stu-id="eee0b-129">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee0b-130">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eee0b-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eee0b-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eee0b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eee0b-132">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span><span class="sxs-lookup"><span data-stu-id="eee0b-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="eee0b-133">Der 802,11-Betriebsmodus, der auf dem Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="eee0b-133">The 802.11 operating mode that is enabled on the port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eee0b-134">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="eee0b-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eee0b-135">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="eee0b-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11a"></span><span id="802.11A"></span>

<span data-ttu-id="eee0b-136">**802.11 a** (70)</span><span class="sxs-lookup"><span data-stu-id="eee0b-136">**802.11a** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11b"></span><span id="802.11B"></span>

<span data-ttu-id="eee0b-137">**802.11 b** (71)</span><span class="sxs-lookup"><span data-stu-id="eee0b-137">**802.11b** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11g"></span><span id="802.11G"></span>

<span data-ttu-id="eee0b-138">**802.11 g** (72)</span><span class="sxs-lookup"><span data-stu-id="eee0b-138">**802.11g** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11n"></span><span id="802.11N"></span>

<span data-ttu-id="eee0b-139">**802.11 n** (73)</span><span class="sxs-lookup"><span data-stu-id="eee0b-139">**802.11n** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="eee0b-140">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="eee0b-140">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="eee0b-141">**Anbieter reserviert** (16000..)</span><span class="sxs-lookup"><span data-stu-id="eee0b-141">**Vendor Reserved** (16000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eee0b-142">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="eee0b-142">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eee0b-143">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eee0b-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eee0b-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eee0b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eee0b-145">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Geschwindigkeit")</span><span class="sxs-lookup"><span data-stu-id="eee0b-145">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed")</span></span>
</dt> </dl>

<span data-ttu-id="eee0b-146">Die Datenrate, mit der die aktuelle ppdu-Protokolldaten Einheit (in Bits pro Sekunde) empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="eee0b-146">The data rate at which the current PPDU (PLCP (Physical Layer Convergence Protocol) Protocol Data Unit) was received, in bits per second.</span></span> <span data-ttu-id="eee0b-147">Dieser Wert wird in den ersten 4 Bits des plcp-Headers in jedem plcp-Frame codiert.</span><span class="sxs-lookup"><span data-stu-id="eee0b-147">This value is encoded in the first 4 bits of the PLCP header in each PLCP frame.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eee0b-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eee0b-148">Requirements</span></span>



| <span data-ttu-id="eee0b-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eee0b-149">Requirement</span></span> | <span data-ttu-id="eee0b-150">Wert</span><span class="sxs-lookup"><span data-stu-id="eee0b-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eee0b-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eee0b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="eee0b-152">Windows 8</span><span class="sxs-lookup"><span data-stu-id="eee0b-152">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="eee0b-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eee0b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="eee0b-154">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eee0b-154">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="eee0b-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="eee0b-155">Namespace</span></span><br/>                | <span data-ttu-id="eee0b-156">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="eee0b-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eee0b-157">MOF</span><span class="sxs-lookup"><span data-stu-id="eee0b-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eee0b-158"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eee0b-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eee0b-159">DLL</span><span class="sxs-lookup"><span data-stu-id="eee0b-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eee0b-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eee0b-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eee0b-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eee0b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eee0b-162">**CIM- \_ Netzwerkport**</span><span class="sxs-lookup"><span data-stu-id="eee0b-162">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

