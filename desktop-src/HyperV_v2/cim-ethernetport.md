---
description: Stellt einen Ethernet-Anschluss dar.
ms.assetid: c9a148c2-cf02-466f-b8ca-b1bf616d75dc
title: CIM_EthernetPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPort
- CIM_EthernetPort.PortType
- CIM_EthernetPort.NetworkAddresses
- CIM_EthernetPort.MaxDataSize
- CIM_EthernetPort.Capabilities
- CIM_EthernetPort.CapabilityDescriptions
- CIM_EthernetPort.EnabledCapabilities
- CIM_EthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a44e93f84178fa2714d3c823735b3d90922e04be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524923"
---
# <a name="cim_ethernetport-class"></a><span data-ttu-id="7540c-103">CIM- \_ Ethernetport-Klasse</span><span class="sxs-lookup"><span data-stu-id="7540c-103">CIM\_EthernetPort class</span></span>

<span data-ttu-id="7540c-104">Stellt einen Ethernet-Anschluss dar.</span><span class="sxs-lookup"><span data-stu-id="7540c-104">Represents an ethernet port.</span></span>

## <a name="syntax"></a><span data-ttu-id="7540c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7540c-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_EthernetPort : CIM_NetworkPort
{
  uint16 PortType;
  string NetworkAddresses[];
  uint32 MaxDataSize;
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint16 EnabledCapabilities[];
  string OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="7540c-106">Member</span><span class="sxs-lookup"><span data-stu-id="7540c-106">Members</span></span>

<span data-ttu-id="7540c-107">Die **CIM- \_ Ethernetport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7540c-107">The **CIM\_EthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="7540c-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7540c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7540c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7540c-109">Properties</span></span>

<span data-ttu-id="7540c-110">Die **CIM- \_ Ethernetport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7540c-110">The **CIM\_EthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7540c-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="7540c-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7540c-112">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7540c-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7540c-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7540c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7540c-114">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Ethernetport**".**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="7540c-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="7540c-115">Die Funktionen des Ethernet-Ports.</span><span class="sxs-lookup"><span data-stu-id="7540c-115">The capabilities of the ethernet port.</span></span>

> [!Note]  
> <span data-ttu-id="7540c-116">Wenn Failover-oder Lasten Ausgleichs Funktionen aktiviert sind, sollte auch ein [**CIM- \_ SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) -Objekt (Failover) oder [**CIM \_ extracapacitygroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) -Objekt (Lasten Ausgleichs Objekt) definiert werden, um die Funktion vollständig zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7540c-116">If failover or load balancing capabilities are enabled, a [**CIM\_SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) or [**CIM\_ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (load balancing) object should also be defined to completely describe the capability.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7540c-117">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7540c-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7540c-118">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7540c-118">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

<span data-ttu-id="7540c-119">**Alertonlan** (2)</span><span class="sxs-lookup"><span data-stu-id="7540c-119">**AlertOnLan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

<span data-ttu-id="7540c-120">**Wake-on-LAN** (3)</span><span class="sxs-lookup"><span data-stu-id="7540c-120">**WakeOnLan** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

<span data-ttu-id="7540c-121">**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="7540c-121">**FailOver** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

<span data-ttu-id="7540c-122">**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="7540c-122">**LoadBalancing** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7540c-123">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="7540c-123">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7540c-124">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="7540c-124">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7540c-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7540c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7540c-126">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Ethernetport**".**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="7540c-126">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="7540c-127">Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen zu allen Features bereitstellt, die im Funktions Array angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7540c-127">An array of free-form strings that provides more detailed explanations for any of the features that are indicated in the Capabilities array.</span></span> <span data-ttu-id="7540c-128">Die Elemente in diesem Array entsprechen den Elementen im Funktions Array.</span><span class="sxs-lookup"><span data-stu-id="7540c-128">The items in this array correspond to the items in the Capabilities array.</span></span>

</dd> <dt>

<span data-ttu-id="7540c-129">**Enabled-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="7540c-129">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7540c-130">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7540c-130">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7540c-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7540c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7540c-132">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Ethernetport**".**Funktionen**","**CIM- \_ Ethernetport**.**Otherenabledfunktionalitäten**")</span><span class="sxs-lookup"><span data-stu-id="7540c-132">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**Capabilities**", "**CIM\_EthernetPort**.**OtherEnabledCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="7540c-133">Gibt an, welche Funktionen im Funktions Array aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="7540c-133">Indicates which capabilities are enabled in the Capabilities array.</span></span> <span data-ttu-id="7540c-134">Die Elemente in diesem Array entsprechen den Elementen im Funktions Array.</span><span class="sxs-lookup"><span data-stu-id="7540c-134">The items in this array correspond to the items in the Capabilities array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7540c-135">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7540c-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7540c-136">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7540c-136">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

<span data-ttu-id="7540c-137">**Alertonlan** (2)</span><span class="sxs-lookup"><span data-stu-id="7540c-137">**AlertOnLan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

<span data-ttu-id="7540c-138">**Wake-on-LAN** (3)</span><span class="sxs-lookup"><span data-stu-id="7540c-138">**WakeOnLan** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

<span data-ttu-id="7540c-139">**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="7540c-139">**FailOver** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

<span data-ttu-id="7540c-140">**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="7540c-140">**LoadBalancing** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7540c-141">**Maxdatasize**</span><span class="sxs-lookup"><span data-stu-id="7540c-141">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7540c-142">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7540c-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7540c-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7540c-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7540c-144">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpPortMaxInfo ")</span><span class="sxs-lookup"><span data-stu-id="7540c-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpPortMaxInfo")</span></span>
</dt> </dl>

<span data-ttu-id="7540c-145">Die maximale Größe des Felds Info (nicht-Mac), das empfangen oder übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="7540c-145">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span>

</dd> <dt>

<span data-ttu-id="7540c-146">**"Networkaddresses"**</span><span class="sxs-lookup"><span data-stu-id="7540c-146">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7540c-147">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="7540c-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7540c-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7540c-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7540c-149">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Netzwerkadressen")</span><span class="sxs-lookup"><span data-stu-id="7540c-149">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span></span>
</dt> </dl>

<span data-ttu-id="7540c-150">Die dem Port zugewiesenen Netzwerkadressen.</span><span class="sxs-lookup"><span data-stu-id="7540c-150">The network addresses assigned to the port.</span></span> <span data-ttu-id="7540c-151">Die Adresse ist ein 802,3-Mac, der als zwölf hexadezimal Ziffern formatiert ist (z. b. "010203040506"), wobei jedes Ziffern Paar eines der sechs Oktette der Mac-Adresse in kanonischer bitreihenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="7540c-151">The address is a 802.3 MAC that is formatted as twelve hexadecimal digits (for example, "010203040506"), where each pair of digits represents one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="7540c-152">**Otherenabled-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="7540c-152">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7540c-153">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="7540c-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7540c-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7540c-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7540c-155">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Ethernetport**".**Enabledfunktionalitäten**")</span><span class="sxs-lookup"><span data-stu-id="7540c-155">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**EnabledCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="7540c-156">Ein Array von Freiform-Zeichen folgen, die Ausführlichere Erläuterungen zu allen **enabledfunktionalitäten** -Array Elementen bereitstellen, die auf 1 (Sonstiges) festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="7540c-156">An array of free-form strings that provide more detailed explanations for any of the **EnabledCapabilities** array items that are set to 1 (Other).</span></span> <span data-ttu-id="7540c-157">Die Elemente in diesem Array entsprechen den Elementen im **enabledfunktionalitäten** -Array.</span><span class="sxs-lookup"><span data-stu-id="7540c-157">The items in this array correspond to the items in the **EnabledCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="7540c-158">**PortType**</span><span class="sxs-lookup"><span data-stu-id="7540c-158">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7540c-159">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7540c-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7540c-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7540c-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7540c-161">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span><span class="sxs-lookup"><span data-stu-id="7540c-161">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="7540c-162">Der Modus, der für den Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7540c-162">The mode that is enabled on the port.</span></span> <span data-ttu-id="7540c-163">Bei Festlegung auf 1 (Sonstiges) beschreibt die **otherporttype** -Eigenschaft den-Modus.</span><span class="sxs-lookup"><span data-stu-id="7540c-163">When set to 1 (Other), the **OtherPortType** property describes the mode.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7540c-164">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7540c-164">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7540c-165">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7540c-165">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="10BaseT"></span><span id="10baset"></span><span id="10BASET"></span>

<span data-ttu-id="7540c-166">**10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="7540c-166">**10BaseT** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>

<span data-ttu-id="7540c-167">**10-100-BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="7540c-167">**10-100BaseT** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>

<span data-ttu-id="7540c-168">**100 BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="7540c-168">**100BaseT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>

<span data-ttu-id="7540c-169">**1000 BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="7540c-169">**1000BaseT** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>

<span data-ttu-id="7540c-170">**2500baset** (54)</span><span class="sxs-lookup"><span data-stu-id="7540c-170">**2500BaseT** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>

<span data-ttu-id="7540c-171">**10gbaset** (55)</span><span class="sxs-lookup"><span data-stu-id="7540c-171">**10GBaseT** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>

<span data-ttu-id="7540c-172">**10GBase-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="7540c-172">**10GBase-CX4** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="100Base-FX"></span><span id="100base-fx"></span><span id="100BASE-FX"></span>

<span data-ttu-id="7540c-173">**100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="7540c-173">**100Base-FX** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>

<span data-ttu-id="7540c-174">**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="7540c-174">**100Base-SX** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>

<span data-ttu-id="7540c-175">**1000 Base-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="7540c-175">**1000Base-SX** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>

<span data-ttu-id="7540c-176">**1000 Base-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="7540c-176">**1000Base-LX** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>

<span data-ttu-id="7540c-177">**1000 Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="7540c-177">**1000Base-CX** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>

<span data-ttu-id="7540c-178">**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="7540c-178">**10GBase-SR** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>

<span data-ttu-id="7540c-179">**10GBase-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="7540c-179">**10GBase-SW** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>

<span data-ttu-id="7540c-180">**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="7540c-180">**10GBase-LX4** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>

<span data-ttu-id="7540c-181">**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="7540c-181">**10GBase-LR** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>

<span data-ttu-id="7540c-182">**10GBase-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="7540c-182">**10GBase-LW** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>

<span data-ttu-id="7540c-183">**10GBase-er** (110)</span><span class="sxs-lookup"><span data-stu-id="7540c-183">**10GBase-ER** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>

<span data-ttu-id="7540c-184">**10GBase-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="7540c-184">**10GBase-EW** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7540c-185">**Anbieter reserviert** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="7540c-185">**Vendor Reserved** (16000..65535)</span></span>


<span data-ttu-id="7540c-186"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7540c-186"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7540c-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7540c-187">Requirements</span></span>



| <span data-ttu-id="7540c-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7540c-188">Requirement</span></span> | <span data-ttu-id="7540c-189">Wert</span><span class="sxs-lookup"><span data-stu-id="7540c-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7540c-190">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7540c-190">Minimum supported client</span></span><br/> | <span data-ttu-id="7540c-191">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7540c-191">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7540c-192">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7540c-192">Minimum supported server</span></span><br/> | <span data-ttu-id="7540c-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7540c-193">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7540c-194">Namespace</span><span class="sxs-lookup"><span data-stu-id="7540c-194">Namespace</span></span><br/>                | <span data-ttu-id="7540c-195">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7540c-195">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7540c-196">MOF</span><span class="sxs-lookup"><span data-stu-id="7540c-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7540c-197"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7540c-197"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7540c-198">DLL</span><span class="sxs-lookup"><span data-stu-id="7540c-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7540c-199"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7540c-199"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7540c-200">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7540c-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7540c-201">**CIM- \_ Netzwerkport**</span><span class="sxs-lookup"><span data-stu-id="7540c-201">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

