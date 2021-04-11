---
description: Eine logische Darstellung eines Netzwerkports auf einem Netzwerkgerät.
ms.assetid: afcfc93d-174e-43b5-a16f-28937b4bf81a
title: CIM_NetworkPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkPort
- CIM_NetworkPort.Speed
- CIM_NetworkPort.OtherNetworkPortType
- CIM_NetworkPort.PortNumber
- CIM_NetworkPort.LinkTechnology
- CIM_NetworkPort.OtherLinkTechnology
- CIM_NetworkPort.PermanentAddress
- CIM_NetworkPort.NetworkAddresses
- CIM_NetworkPort.FullDuplex
- CIM_NetworkPort.AutoSense
- CIM_NetworkPort.SupportedMaximumTransmissionUnit
- CIM_NetworkPort.ActiveMaximumTransmissionUnit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e3ac64b55e17d0526527ebbaca168c3f7b289f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217815"
---
# <a name="cim_networkport-class"></a><span data-ttu-id="6440d-103">CIM- \_ networkport-Klasse</span><span class="sxs-lookup"><span data-stu-id="6440d-103">CIM\_NetworkPort class</span></span>

<span data-ttu-id="6440d-104">Eine logische Darstellung eines Netzwerkports auf einem Netzwerkgerät.</span><span class="sxs-lookup"><span data-stu-id="6440d-104">A logical representation of a network port on a network device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6440d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6440d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_NetworkPort : CIM_LogicalPort
{
  uint64  Speed;
  string  OtherNetworkPortType;
  uint16  PortNumber;
  uint16  LinkTechnology;
  string  OtherLinkTechnology;
  string  PermanentAddress;
  string  NetworkAddresses[];
  boolean FullDuplex;
  boolean AutoSense;
  uint64  SupportedMaximumTransmissionUnit;
  uint64  ActiveMaximumTransmissionUnit;
};
```

## <a name="members"></a><span data-ttu-id="6440d-106">Member</span><span class="sxs-lookup"><span data-stu-id="6440d-106">Members</span></span>

<span data-ttu-id="6440d-107">Die **CIM- \_ networkport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6440d-107">The **CIM\_NetworkPort** class has these types of members:</span></span>

-   [<span data-ttu-id="6440d-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6440d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6440d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6440d-109">Properties</span></span>

<span data-ttu-id="6440d-110">Die **CIM- \_ networkport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6440d-110">The **CIM\_NetworkPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6440d-111">**Activemaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="6440d-111">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6440d-112">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6440d-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6440d-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6440d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6440d-114">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="6440d-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="6440d-115">Die aktive oder ausgehandelte maximale Übertragungseinheit (Maximum Transmission Unit, MTU), die vom Port unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6440d-115">The active or negotiated maximum transmission unit (MTU) that is supported by the port.</span></span>

</dd> <dt>

<span data-ttu-id="6440d-116">**AutoSense**</span><span class="sxs-lookup"><span data-stu-id="6440d-116">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6440d-117">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6440d-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6440d-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6440d-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6440d-119">**true** , wenn der Port die Geschwindigkeit oder andere Kommunikationsmerkmale der angeschlossenen Netzwerk Medien automatisch bestimmen kann. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="6440d-119">**true** if the port can automatically determine the speed or other communications characteristic of the attached network media; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="6440d-120">**Vollduplex**</span><span class="sxs-lookup"><span data-stu-id="6440d-120">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6440d-121">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6440d-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6440d-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6440d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6440d-123">**true** , wenn der Port im Vollduplex Modus betrieben wird. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="6440d-123">**true** if the port is operating in full duplex mode; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="6440d-124">**Linktechnology**</span><span class="sxs-lookup"><span data-stu-id="6440d-124">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6440d-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6440d-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6440d-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6440d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6440d-127">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ networkport**".**Otherlinktechnology**")</span><span class="sxs-lookup"><span data-stu-id="6440d-127">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_NetworkPort**.**OtherLinkTechnology**")</span></span>
</dt> </dl>

<span data-ttu-id="6440d-128">Die vom Port verwendete Link Technologie.</span><span class="sxs-lookup"><span data-stu-id="6440d-128">The link technology used by the port.</span></span> <span data-ttu-id="6440d-129">Wenn der Wert auf "1" festgelegt ist, enthält die **otherlinktechnology** -Eigenschaft eine Beschreibung des linktyps.</span><span class="sxs-lookup"><span data-stu-id="6440d-129">When set to "1" (other), the **OtherLinkTechnology** property contains a description of the link type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6440d-130">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="6440d-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6440d-131">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6440d-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="6440d-132">**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="6440d-132">**Ethernet** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IB"></span><span id="ib"></span>

<span data-ttu-id="6440d-133">**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="6440d-133">**IB** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FC"></span><span id="fc"></span>

<span data-ttu-id="6440d-134">**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="6440d-134">**FC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="6440d-135">**F-di** (5)</span><span class="sxs-lookup"><span data-stu-id="6440d-135">**FDDI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="6440d-136">**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="6440d-136">**ATM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="6440d-137">**TokenRing** (7)</span><span class="sxs-lookup"><span data-stu-id="6440d-137">**Token Ring** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

<span data-ttu-id="6440d-138">**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="6440d-138">**Frame Relay** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="6440d-139">**Infrarot** (9)</span><span class="sxs-lookup"><span data-stu-id="6440d-139">**Infrared** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>

<span data-ttu-id="6440d-140">**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="6440d-140">**BlueTooth** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>

<span data-ttu-id="6440d-141">**Drahtlos LAN** (11)</span><span class="sxs-lookup"><span data-stu-id="6440d-141">**Wireless LAN** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6440d-142">**"Networkaddresses"**</span><span class="sxs-lookup"><span data-stu-id="6440d-142">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6440d-143">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6440d-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6440d-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6440d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6440d-145">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzwerk Adapter 802-Port \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="6440d-145">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="6440d-146">Ein Array, das die Netzwerkadressen für den Port enthält.</span><span class="sxs-lookup"><span data-stu-id="6440d-146">An array that contains the network addresses for the port.</span></span>

</dd> <dt>

<span data-ttu-id="6440d-147">**Otherlinktechnology**</span><span class="sxs-lookup"><span data-stu-id="6440d-147">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6440d-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6440d-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6440d-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6440d-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6440d-150">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ networkport**".**Linktechnology**")</span><span class="sxs-lookup"><span data-stu-id="6440d-150">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_NetworkPort**.**LinkTechnology**")</span></span>
</dt> </dl>

<span data-ttu-id="6440d-151">Die Link Technologie, wenn **linktechnology** auf "1" festgelegt ist, (andere).</span><span class="sxs-lookup"><span data-stu-id="6440d-151">The link technology when **LinkTechnology** is set to "1", (other).</span></span>

</dd> <dt>

<span data-ttu-id="6440d-152">**Othernetworkporttype**</span><span class="sxs-lookup"><span data-stu-id="6440d-152">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6440d-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6440d-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6440d-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6440d-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6440d-155">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ networkport**.**Otherporttype**"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ logicalport**](cim-logicalport.md)".**PortType**")</span><span class="sxs-lookup"><span data-stu-id="6440d-155">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_NetworkPort**.**OtherPortType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalPort**](cim-logicalport.md).**PortType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="6440d-156">Deprecated Description: der Modultyp des Ports, wenn die **portType** -Eigenschaft 1 (Sonstiges) enthält.</span><span class="sxs-lookup"><span data-stu-id="6440d-156">Deprecated description: The module type of the port, when the **PortType** property contains 1 (other).</span></span>

 

<span data-ttu-id="6440d-157">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="6440d-157">This property is deprecated.</span></span> <span data-ttu-id="6440d-158">Stattdessen empfehlen wir die **portType** -Eigenschaft in der [**CIM \_ logicalport**](cim-logicalport.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="6440d-158">Instead, we recommend the **PortType** property in the [**CIM\_LogicalPort**](cim-logicalport.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="6440d-159">**Permanent Address**</span><span class="sxs-lookup"><span data-stu-id="6440d-159">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6440d-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6440d-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6440d-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6440d-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6440d-162">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Netzwerk Adapter 802-Port \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="6440d-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="6440d-163">Die Netzwerkadresse, die in einem Port hart codiert ist.</span><span class="sxs-lookup"><span data-stu-id="6440d-163">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="6440d-164">Die hart codierte Adresse kann mithilfe eines Firmwareupdates oder einer Softwarekonfiguration geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6440d-164">The hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="6440d-165">Wenn diese Änderung vorgenommen wird, sollte diese Eigenschaft gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6440d-165">When this change is made, this property should be updated at the same time.</span></span> <span data-ttu-id="6440d-166">" **Permanentaddress** " sollte leer gelassen werden, wenn die Adresse nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6440d-166">**PermanentAddress** should be left blank if the address doesn't exist.</span></span>

</dd> <dt>

<span data-ttu-id="6440d-167">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="6440d-167">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6440d-168">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6440d-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6440d-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6440d-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6440d-170">Die Portnummer des Netzwerkports.</span><span class="sxs-lookup"><span data-stu-id="6440d-170">The port number of the network port.</span></span> <span data-ttu-id="6440d-171">Netzwerkports sind häufig in Bezug auf ein logisches Modul oder ein Netzwerkelement nummeriert.</span><span class="sxs-lookup"><span data-stu-id="6440d-171">Network ports are often numbered relative to either a logical module or a network element.</span></span>

</dd> <dt>

<span data-ttu-id="6440d-172">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="6440d-172">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6440d-173">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6440d-173">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6440d-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6440d-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6440d-175">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Geschwindigkeit"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| MIB-II. IfSpeed "," MIF. DMTF- \| Netzwerk Adapter 802 Port \| 001,5 "), **Punit** (" Bit/Sekunde ")</span><span class="sxs-lookup"><span data-stu-id="6440d-175">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|MIB-II.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="6440d-176">Die aktuelle Bandbreite des Ports in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="6440d-176">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="6440d-177">Für Ports, die die Bandbreite variieren, oder für diejenigen, bei denen keine genaue Schätzung vorgenommen werden kann, sollte diese Eigenschaft die nominale Bandbreite enthalten.</span><span class="sxs-lookup"><span data-stu-id="6440d-177">For ports that vary in bandwidth, or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="6440d-178">**Supportedmaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="6440d-178">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6440d-179">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6440d-179">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6440d-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6440d-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6440d-181">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="6440d-181">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="6440d-182">Die vom Port unterstützte maximale Übertragungseinheit (MTU).</span><span class="sxs-lookup"><span data-stu-id="6440d-182">The maximum transmission unit (MTU) that is supported by the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6440d-183">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6440d-183">Requirements</span></span>



| <span data-ttu-id="6440d-184">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6440d-184">Requirement</span></span> | <span data-ttu-id="6440d-185">Wert</span><span class="sxs-lookup"><span data-stu-id="6440d-185">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6440d-186">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6440d-186">Minimum supported client</span></span><br/> | <span data-ttu-id="6440d-187">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6440d-187">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6440d-188">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6440d-188">Minimum supported server</span></span><br/> | <span data-ttu-id="6440d-189">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6440d-189">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6440d-190">Namespace</span><span class="sxs-lookup"><span data-stu-id="6440d-190">Namespace</span></span><br/>                | <span data-ttu-id="6440d-191">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6440d-191">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6440d-192">MOF</span><span class="sxs-lookup"><span data-stu-id="6440d-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6440d-193"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6440d-193"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6440d-194">DLL</span><span class="sxs-lookup"><span data-stu-id="6440d-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6440d-195"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6440d-195"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6440d-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6440d-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6440d-197">**CIM \_ logicalport**</span><span class="sxs-lookup"><span data-stu-id="6440d-197">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> </dl>

 

