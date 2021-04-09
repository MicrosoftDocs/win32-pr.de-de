---
description: Die Abstraktion eines Ports oder Verbindungs Punkts eines Geräts.
ms.assetid: ee725c64-587b-4e5f-9b1c-7a58902b0631
title: CIM_LogicalPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalPort
- CIM_LogicalPort.Speed
- CIM_LogicalPort.MaxSpeed
- CIM_LogicalPort.RequestedSpeed
- CIM_LogicalPort.UsageRestriction
- CIM_LogicalPort.PortType
- CIM_LogicalPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eeed69e9669048377340cb0ca21e7a2e89f4baff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958685"
---
# <a name="cim_logicalport-class"></a><span data-ttu-id="abb0d-103">CIM \_ logicalport-Klasse</span><span class="sxs-lookup"><span data-stu-id="abb0d-103">CIM\_LogicalPort class</span></span>

<span data-ttu-id="abb0d-104">Die Abstraktion eines Ports oder Verbindungs Punkts eines Geräts.</span><span class="sxs-lookup"><span data-stu-id="abb0d-104">The abstraction of a port or connection point of a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="abb0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="abb0d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_LogicalPort : CIM_LogicalDevice
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint64 RequestedSpeed;
  uint16 UsageRestriction;
  uint16 PortType;
  string OtherPortType;
};
```

## <a name="members"></a><span data-ttu-id="abb0d-106">Member</span><span class="sxs-lookup"><span data-stu-id="abb0d-106">Members</span></span>

<span data-ttu-id="abb0d-107">Die **CIM \_ logicalport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="abb0d-107">The **CIM\_LogicalPort** class has these types of members:</span></span>

-   [<span data-ttu-id="abb0d-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="abb0d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="abb0d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="abb0d-109">Properties</span></span>

<span data-ttu-id="abb0d-110">Die **CIM \_ logicalport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="abb0d-110">The **CIM\_LogicalPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abb0d-111">**MAXSPEED**</span><span class="sxs-lookup"><span data-stu-id="abb0d-111">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abb0d-112">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="abb0d-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="abb0d-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abb0d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abb0d-114">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde"), **Punit** ("Bit/Sekunde")</span><span class="sxs-lookup"><span data-stu-id="abb0d-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="abb0d-115">Die maximale Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="abb0d-115">The maximum bandwidth of the port, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="abb0d-116">**Otherporttype**</span><span class="sxs-lookup"><span data-stu-id="abb0d-116">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abb0d-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="abb0d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abb0d-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abb0d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abb0d-119">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ logicalport**".**PortType**")</span><span class="sxs-lookup"><span data-stu-id="abb0d-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalPort**.**PortType**")</span></span>
</dt> </dl>

<span data-ttu-id="abb0d-120">Beschreibt den Modultyp, wenn " **portType** " auf " **other** " ("1") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="abb0d-120">Describes the type of module, when **PortType** is set to **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="abb0d-121">**PortType**</span><span class="sxs-lookup"><span data-stu-id="abb0d-121">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abb0d-122">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abb0d-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abb0d-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abb0d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abb0d-124">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ networkport**](cim-networkport.md)".**Othernetworkporttype**")</span><span class="sxs-lookup"><span data-stu-id="abb0d-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_NetworkPort**](cim-networkport.md).**OtherNetworkPortType**")</span></span>
</dt> </dl>

<span data-ttu-id="abb0d-125">Der Porttyp.</span><span class="sxs-lookup"><span data-stu-id="abb0d-125">The port type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="abb0d-126">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="abb0d-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="abb0d-127">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="abb0d-127">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="abb0d-128">**Nicht zutreffend** (2)</span><span class="sxs-lookup"><span data-stu-id="abb0d-128">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="abb0d-129">**DMTF reserviert** (3.. 15999)</span><span class="sxs-lookup"><span data-stu-id="abb0d-129">**DMTF Reserved** (3..15999)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="abb0d-130">**Anbieter reserviert** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="abb0d-130">**Vendor Reserved** (16000..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="abb0d-131">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="abb0d-131">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abb0d-132">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="abb0d-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="abb0d-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="abb0d-133">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="abb0d-134">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ logicalport**".**Geschwindigkeit**"), **Punit** (" Bit/Sekunde ")</span><span class="sxs-lookup"><span data-stu-id="abb0d-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalPort**.**Speed**"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="abb0d-135">Die angeforderte Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="abb0d-135">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="abb0d-136">Die tatsächliche Bandbreite wird in der Eigenschaft **Geschwindigkeit** gemeldet.</span><span class="sxs-lookup"><span data-stu-id="abb0d-136">The actual bandwidth is reported in the **Speed** property.</span></span>

</dd> <dt>

<span data-ttu-id="abb0d-137">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="abb0d-137">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abb0d-138">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="abb0d-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="abb0d-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abb0d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abb0d-140">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde"), **Punit** ("Bit/Sekunde")</span><span class="sxs-lookup"><span data-stu-id="abb0d-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="abb0d-141">Die Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="abb0d-141">The bandwidth of the port, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="abb0d-142">**Einsatz Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="abb0d-142">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abb0d-143">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abb0d-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abb0d-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abb0d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abb0d-145">Gibt an, ob der Port auf einen Front-End-oder Back-End-Port beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="abb0d-145">Indicates whether the port is restricted to being a front-end or back-end port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="abb0d-146">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="abb0d-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>

<span data-ttu-id="abb0d-147">**Nur Front-End** (2)</span><span class="sxs-lookup"><span data-stu-id="abb0d-147">**Front-end only** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>

<span data-ttu-id="abb0d-148">**Nur Back-End** (3)</span><span class="sxs-lookup"><span data-stu-id="abb0d-148">**Back-end only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>

<span data-ttu-id="abb0d-149">**Nicht eingeschränkt** (4)</span><span class="sxs-lookup"><span data-stu-id="abb0d-149">**Not restricted** (4)</span></span>


<span data-ttu-id="abb0d-150"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="abb0d-150"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="abb0d-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abb0d-151">Requirements</span></span>



| <span data-ttu-id="abb0d-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abb0d-152">Requirement</span></span> | <span data-ttu-id="abb0d-153">Wert</span><span class="sxs-lookup"><span data-stu-id="abb0d-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abb0d-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abb0d-154">Minimum supported client</span></span><br/> | <span data-ttu-id="abb0d-155">Windows 8</span><span class="sxs-lookup"><span data-stu-id="abb0d-155">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="abb0d-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abb0d-156">Minimum supported server</span></span><br/> | <span data-ttu-id="abb0d-157">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="abb0d-157">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="abb0d-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="abb0d-158">Namespace</span></span><br/>                | <span data-ttu-id="abb0d-159">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="abb0d-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="abb0d-160">MOF</span><span class="sxs-lookup"><span data-stu-id="abb0d-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abb0d-161"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="abb0d-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="abb0d-162">DLL</span><span class="sxs-lookup"><span data-stu-id="abb0d-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abb0d-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="abb0d-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="abb0d-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abb0d-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abb0d-165">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="abb0d-165">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

