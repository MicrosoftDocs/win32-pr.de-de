---
description: Ein Endpunkt auf einem Switch oder einer Endstation, der einem VLAN zugewiesen ist oder Datenverkehr von einem oder mehreren VLANs akzeptiert.
ms.assetid: 20943be3-35c3-4bf5-8f1a-d4095fa6897e
title: CIM_VLANEndpoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpoint
- CIM_VLANEndpoint.DesiredEndpointMode
- CIM_VLANEndpoint.OtherEndpointMode
- CIM_VLANEndpoint.OperationalEndpointMode
- CIM_VLANEndpoint.DesiredVLANTrunkEncapsulation
- CIM_VLANEndpoint.OtherTrunkEncapsulation
- CIM_VLANEndpoint.OperationalVLANTrunkEncapsulation
- CIM_VLANEndpoint.GVRPStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f7b0d1318e4c24ab7381032877d16a8ea83868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128124"
---
# <a name="cim_vlanendpoint-class"></a><span data-ttu-id="4fca2-103">CIM \_ vlanendpoint-Klasse</span><span class="sxs-lookup"><span data-stu-id="4fca2-103">CIM\_VLANEndpoint class</span></span>

<span data-ttu-id="4fca2-104">Ein Endpunkt auf einem Switch oder einer Endstation, der einem VLAN zugewiesen ist oder Datenverkehr von einem oder mehreren VLANs akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="4fca2-104">An endpoint on a switch or end station that is assigned to a VLAN, or accepts traffic from one or more VLANs.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fca2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fca2-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Network::VLAN"), AMENDMENT]
class CIM_VLANEndpoint : CIM_ProtocolEndpoint
{
  uint16 DesiredEndpointMode;
  string OtherEndpointMode;
  uint16 OperationalEndpointMode;
  uint16 DesiredVLANTrunkEncapsulation;
  string OtherTrunkEncapsulation;
  uint16 OperationalVLANTrunkEncapsulation;
  uint16 GVRPStatus;
};
```

## <a name="members"></a><span data-ttu-id="4fca2-106">Member</span><span class="sxs-lookup"><span data-stu-id="4fca2-106">Members</span></span>

<span data-ttu-id="4fca2-107">Die **CIM- \_ vlanendpoint** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4fca2-107">The **CIM\_VLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="4fca2-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4fca2-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4fca2-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4fca2-109">Properties</span></span>

<span data-ttu-id="4fca2-110">Die **CIM- \_ vlanendpoint** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4fca2-110">The **CIM\_VLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4fca2-111">**"Desiredendpointmode"**</span><span class="sxs-lookup"><span data-stu-id="4fca2-111">**DesiredEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fca2-112">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4fca2-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fca2-113">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4fca2-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fca2-114">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ vlanendpoint**".**Operationalendpointmode**","**CIM \_ vlanendpoint**.**Otherendpointmode**")</span><span class="sxs-lookup"><span data-stu-id="4fca2-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OperationalEndpointMode**", "**CIM\_VLANEndpoint**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="4fca2-115">Der angeforderte VLAN-Modus für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="4fca2-115">The requested VLAN mode for the endpoint.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4fca2-116">**DMTF reserviert** (0)</span><span class="sxs-lookup"><span data-stu-id="4fca2-116">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4fca2-117">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="4fca2-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="4fca2-118">**Zugriff** (2)</span><span class="sxs-lookup"><span data-stu-id="4fca2-118">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="4fca2-119">**Dynamisches Auto** (3)</span><span class="sxs-lookup"><span data-stu-id="4fca2-119">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="4fca2-120">**Dynamisch erwünscht** (4)</span><span class="sxs-lookup"><span data-stu-id="4fca2-120">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="4fca2-121">**Trunk** (5)</span><span class="sxs-lookup"><span data-stu-id="4fca2-121">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="4fca2-122">**Dot1Q Tunnel** (6)</span><span class="sxs-lookup"><span data-stu-id="4fca2-122">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4fca2-123">**DMTF reserviert** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="4fca2-123">**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="4fca2-124">**Anbieter reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="4fca2-124">**Vendor Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4fca2-125">**Desiredvlantrunkenkapselung**</span><span class="sxs-lookup"><span data-stu-id="4fca2-125">**DesiredVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fca2-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4fca2-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fca2-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4fca2-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fca2-128">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ vlanendpointfunktionalitäten. supportstrauunkenkapationaushandlung", "**CIM \_ vlanendpoint**.**Operationalvlantrunkenkapselung**","**CIM \_ vlanendpoint**.**Othertrunkenkapselung**")</span><span class="sxs-lookup"><span data-stu-id="4fca2-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VLANEndpointCapabilities.SupportsTrunkEncapsulationNegotiation", "**CIM\_VLANEndpoint**.**OperationalVLANTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**OtherTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="4fca2-129">Der angeforderte VLAN-Kapselungstyp.</span><span class="sxs-lookup"><span data-stu-id="4fca2-129">The requested VLAN encapsulation type.</span></span>

> [!Note]  
> <span data-ttu-id="4fca2-130">Diese Eigenschaft wird nur verwendet, wenn sich der VLAN-Endpunkt im trunkingmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="4fca2-130">This property is only used when the VLAN endpoint is in trunking mode.</span></span>

 

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4fca2-131">**DMTF reserviert** (0)</span><span class="sxs-lookup"><span data-stu-id="4fca2-131">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4fca2-132">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="4fca2-132">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4fca2-133">**Nicht zutreffend** (2)</span><span class="sxs-lookup"><span data-stu-id="4fca2-133">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

<span data-ttu-id="4fca2-134">**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="4fca2-134">**802.1q** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

<span data-ttu-id="4fca2-135">**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="4fca2-135">**Cisco ISL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="4fca2-136">**Aushandeln** (5)</span><span class="sxs-lookup"><span data-stu-id="4fca2-136">**Negotiate** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4fca2-137">**DMTF reserviert** (6.. 32767)</span><span class="sxs-lookup"><span data-stu-id="4fca2-137">**DMTF Reserved** (6..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="4fca2-138">**Anbieter reserviert** (32768..)</span><span class="sxs-lookup"><span data-stu-id="4fca2-138">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4fca2-139">**Gvrpstatus**</span><span class="sxs-lookup"><span data-stu-id="4fca2-139">**GVRPStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fca2-140">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4fca2-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fca2-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fca2-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fca2-142">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ vlanendpoint**".**Operationalendpointmode**, CIM \_ vlanendpointfunktionalitäten. Dot1QTagging ")</span><span class="sxs-lookup"><span data-stu-id="4fca2-142">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OperationalEndpointMode**, CIM\_VLANEndpointCapabilities.Dot1QTagging")</span></span>
</dt> </dl>

<span data-ttu-id="4fca2-143">Gibt an, ob das Garp-VLAN-Registrierungs Protokoll (GVRP) auf dem trunk Endpunkt aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4fca2-143">Indicates whether GARP VLAN Registration Protocol (GVRP) is enabled or disabled on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="4fca2-144">Diese Eigenschaft wird nur verwendet, wenn GVRP vom Endpunkt unterstützt wird und der trunkingmodus aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4fca2-144">This property is only used when GVRP is supported by the endpoint, and trunking mode is enabled.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4fca2-145">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="4fca2-145">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4fca2-146">**Nicht zutreffend** (2)</span><span class="sxs-lookup"><span data-stu-id="4fca2-146">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4fca2-147">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="4fca2-147">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4fca2-148">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="4fca2-148">**Disabled** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4fca2-149">**Operationalendpointmode**</span><span class="sxs-lookup"><span data-stu-id="4fca2-149">**OperationalEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fca2-150">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4fca2-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fca2-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fca2-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fca2-152">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ vlanendpoint**".**Desiredendpointmode**","**CIM \_ vlanendpoint**.**Otherendpointmode**")</span><span class="sxs-lookup"><span data-stu-id="4fca2-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_VLANEndpoint**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="4fca2-153">Der aktuelle VLAN-Modus für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="4fca2-153">The current VLAN mode for the endpoint.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4fca2-154">**DMTF reserviert** (0)</span><span class="sxs-lookup"><span data-stu-id="4fca2-154">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4fca2-155">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="4fca2-155">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="4fca2-156">**Zugriff** (2)</span><span class="sxs-lookup"><span data-stu-id="4fca2-156">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="4fca2-157">**Dynamisches Auto** (3)</span><span class="sxs-lookup"><span data-stu-id="4fca2-157">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="4fca2-158">**Dynamisch erwünscht** (4)</span><span class="sxs-lookup"><span data-stu-id="4fca2-158">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="4fca2-159">**Trunk** (5)</span><span class="sxs-lookup"><span data-stu-id="4fca2-159">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="4fca2-160">**Dot1Q Tunnel** (6)</span><span class="sxs-lookup"><span data-stu-id="4fca2-160">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4fca2-161">**DMTF reserviert** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="4fca2-161">**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="4fca2-162">**Anbieter reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="4fca2-162">**Vendor Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4fca2-163">**Operationalvlantrunkenkapselung**</span><span class="sxs-lookup"><span data-stu-id="4fca2-163">**OperationalVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fca2-164">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4fca2-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fca2-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4fca2-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fca2-166">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ vlanendpoint**".**Othertrunkenkapselung**","**CIM \_ vlanendpoint**.**Desiredvlantrunkenkapselung**")</span><span class="sxs-lookup"><span data-stu-id="4fca2-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OtherTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**DesiredVLANTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="4fca2-167">Der aktuelle VLAN-Kapselungstyp.</span><span class="sxs-lookup"><span data-stu-id="4fca2-167">The current VLAN encapsulation type.</span></span>

> [!Note]  
> <span data-ttu-id="4fca2-168">Diese Eigenschaft wird nur verwendet, wenn sich der VLAN-Endpunkt im trunkingmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="4fca2-168">This property is only used when the VLAN endpoint is in trunking mode.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4fca2-169">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="4fca2-169">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4fca2-170">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="4fca2-170">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4fca2-171">**Nicht zutreffend** (2)</span><span class="sxs-lookup"><span data-stu-id="4fca2-171">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

<span data-ttu-id="4fca2-172">**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="4fca2-172">**802.1q** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

<span data-ttu-id="4fca2-173">**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="4fca2-173">**Cisco ISL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>

<span data-ttu-id="4fca2-174">**Aushandlung** (5)</span><span class="sxs-lookup"><span data-stu-id="4fca2-174">**Negotiating** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4fca2-175">**DMTF reserviert** (6.. 32767)</span><span class="sxs-lookup"><span data-stu-id="4fca2-175">**DMTF Reserved** (6..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="4fca2-176">**Anbieter reserviert** (32768..)</span><span class="sxs-lookup"><span data-stu-id="4fca2-176">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4fca2-177">**Otherendpointmode**</span><span class="sxs-lookup"><span data-stu-id="4fca2-177">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fca2-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4fca2-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fca2-179">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4fca2-179">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fca2-180">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ vlanendpoint**".**Desiredendpointmode**","**CIM \_ vlanendpoint**.**Operationalendpointmode**")</span><span class="sxs-lookup"><span data-stu-id="4fca2-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_VLANEndpoint**.**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="4fca2-181">Der Typ des VLAN-Endpunkt Modells, das von vlanendpoint unterstützt wird, wenn der Wert von " **desiredendpointmode** " auf "1" (sonstige) festgelegt ist. andernfalls **null**.</span><span class="sxs-lookup"><span data-stu-id="4fca2-181">The type of VLAN endpoint model that is supported by the VLANEndpoint when the value of **DesiredEndpointMode** is set to "1" (other); otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4fca2-182">**Othertrunkenkapselung**</span><span class="sxs-lookup"><span data-stu-id="4fca2-182">**OtherTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fca2-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4fca2-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fca2-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4fca2-184">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fca2-185">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ vlanendpoint**".**Desiredvlantrunkenkapselung**","**CIM \_ vlanendpoint**.**Operationalvlantrunkenkapselung**")</span><span class="sxs-lookup"><span data-stu-id="4fca2-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredVLANTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**OperationalVLANTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="4fca2-186">Der Typ der VLAN-Kapselung, der vom VLAN-Endpunkt unterstützt wird, wenn der Wert der Eigenschaft " **desiredvlantrunkenkapselung** " auf 1 (Sonstiges) festgelegt ist. andernfalls **null**.</span><span class="sxs-lookup"><span data-stu-id="4fca2-186">The type of VLAN encapsulation that is supported by the VLAN endpoint when the value of the **DesiredVLANTrunkEncapsulation** property is set to 1 (other); otherwise, **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fca2-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fca2-187">Requirements</span></span>



| <span data-ttu-id="4fca2-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fca2-188">Requirement</span></span> | <span data-ttu-id="4fca2-189">Wert</span><span class="sxs-lookup"><span data-stu-id="4fca2-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fca2-190">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fca2-190">Minimum supported client</span></span><br/> | <span data-ttu-id="4fca2-191">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4fca2-191">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4fca2-192">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fca2-192">Minimum supported server</span></span><br/> | <span data-ttu-id="4fca2-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4fca2-193">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4fca2-194">Namespace</span><span class="sxs-lookup"><span data-stu-id="4fca2-194">Namespace</span></span><br/>                | <span data-ttu-id="4fca2-195">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4fca2-195">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4fca2-196">MOF</span><span class="sxs-lookup"><span data-stu-id="4fca2-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fca2-197"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4fca2-197"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fca2-198">DLL</span><span class="sxs-lookup"><span data-stu-id="4fca2-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fca2-199"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4fca2-199"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4fca2-200">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fca2-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fca2-201">**CIM- \_ protocolendpoint**</span><span class="sxs-lookup"><span data-stu-id="4fca2-201">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

