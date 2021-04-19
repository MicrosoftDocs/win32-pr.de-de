---
description: Stellt Einstellungen für die Zuordnung des Ethernet-Ports dar, zusätzlich zu den Einstellungen, die von der CIM- \_ Ethernetport-Klasse bereitgestellt werden. Diese Einstellungen werden verwendet, um spezifische Informationen für die Ressource bereitzustellen.
ms.assetid: f59ebaf1-60dd-49bd-b48e-d7a6c2650909
title: CIM_EthernetPortAllocationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPortAllocationSettingData
- CIM_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- CIM_EthernetPortAllocationSettingData.OtherEndpointMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e77b4387f77e88ceaff273b8be72a354c989e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338954"
---
# <a name="cim_ethernetportallocationsettingdata-class"></a><span data-ttu-id="7b5cf-104">CIM- \_ ethernetportationscationsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="7b5cf-104">CIM\_EthernetPortAllocationSettingData class</span></span>

<span data-ttu-id="7b5cf-105">Stellt Einstellungen für die Zuordnung des Ethernet-Ports dar, zusätzlich zu den Einstellungen, die von der [**CIM- \_ Ethernetport**](cim-ethernetport.md) -Klasse bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7b5cf-105">Represents settings for the allocation of the ethernet port, in addition to the settings provided by the [**CIM\_EthernetPort**](cim-ethernetport.md) class.</span></span> <span data-ttu-id="7b5cf-106">Diese Einstellungen werden verwendet, um spezifische Informationen für die Ressource bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7b5cf-106">These settings are used to provide information specific to the resource itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b5cf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b5cf-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_EthernetPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint16 DesiredVLANEndpointMode;
  string OtherEndpointMode;
};
```

## <a name="members"></a><span data-ttu-id="7b5cf-108">Member</span><span class="sxs-lookup"><span data-stu-id="7b5cf-108">Members</span></span>

<span data-ttu-id="7b5cf-109">Die CIM-Klasse " **\_ ethernetportzugewiesene cationsettingdata** " enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7b5cf-109">The **CIM\_EthernetPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7b5cf-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b5cf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b5cf-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b5cf-111">Properties</span></span>

<span data-ttu-id="7b5cf-112">Die CIM-Klasse " **\_ ethernetportzugewiesene cationsettingdata** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7b5cf-112">The **CIM\_EthernetPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b5cf-113">**Desiredvlanendpointmode**</span><span class="sxs-lookup"><span data-stu-id="7b5cf-113">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b5cf-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b5cf-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b5cf-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7b5cf-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b5cf-116">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ vlanendpoint**](cim-vlanendpoint.md)".**Operationalendpointmode**","**CIM \_ vlanendpoint**.**"Desiredendpointmode**", "**CIM \_ ethernetportzuweisung cationsettingdata**".**Otherendpointmode**")</span><span class="sxs-lookup"><span data-stu-id="7b5cf-116">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**", "**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_EthernetPortAllocationSettingData**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="7b5cf-117">Der angeforderte VLAN-Modus.</span><span class="sxs-lookup"><span data-stu-id="7b5cf-117">The requested VLAN mode.</span></span> <span data-ttu-id="7b5cf-118">Diese Eigenschaft wird verwendet, um den ursprünglichen **operationalendpointmode** -Eigenschafts Wert in der Instanz von **CIM \_ vlanendpoint** festzulegen, die dem Ethernet-Port zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7b5cf-118">This property is used to set the initial **OperationalEndpointMode** property value in the instance of **CIM\_VLANEndpoint** associated with the ethernet port.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7b5cf-119">**DMTF reserviert** (0)</span><span class="sxs-lookup"><span data-stu-id="7b5cf-119">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7b5cf-120">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7b5cf-120">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="7b5cf-121">**Zugriff** (2)</span><span class="sxs-lookup"><span data-stu-id="7b5cf-121">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="7b5cf-122">**Dynamisches Auto** (3)</span><span class="sxs-lookup"><span data-stu-id="7b5cf-122">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="7b5cf-123">**Dynamisch erwünscht** (4)</span><span class="sxs-lookup"><span data-stu-id="7b5cf-123">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="7b5cf-124">**Trunk** (5)</span><span class="sxs-lookup"><span data-stu-id="7b5cf-124">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="7b5cf-125">**Dot1Q Tunnel** (6)</span><span class="sxs-lookup"><span data-stu-id="7b5cf-125">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7b5cf-126">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="7b5cf-126">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7b5cf-127">**Anbieter reserviert** (0X8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="7b5cf-127">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7b5cf-128">**Otherendpointmode**</span><span class="sxs-lookup"><span data-stu-id="7b5cf-128">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b5cf-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7b5cf-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b5cf-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7b5cf-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b5cf-131">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ethernetportzuweisung-Daten**.**Desiredvlanendpointmode**")</span><span class="sxs-lookup"><span data-stu-id="7b5cf-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="7b5cf-132">Der Typ des VLAN-Endpunkt Modells, das von diesem VLAN-Endpunkt unterstützt wird, wenn der Wert der Mode-Eigenschaft auf "1" (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7b5cf-132">The type of VLAN endpoint model that is supported by this VLAN endpoint, when the value of the mode property is set to "1" (Other).</span></span> <span data-ttu-id="7b5cf-133">Diese Eigenschaft sollte auf **null** festgelegt werden, wenn die Mode-Eigenschaft einen anderen Wert als "1" hat.</span><span class="sxs-lookup"><span data-stu-id="7b5cf-133">This property should be set to **NULL** when the mode property is any value other than "1".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b5cf-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b5cf-134">Requirements</span></span>



| <span data-ttu-id="7b5cf-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b5cf-135">Requirement</span></span> | <span data-ttu-id="7b5cf-136">Wert</span><span class="sxs-lookup"><span data-stu-id="7b5cf-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b5cf-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b5cf-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7b5cf-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7b5cf-138">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7b5cf-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b5cf-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7b5cf-140">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b5cf-140">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7b5cf-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b5cf-141">Namespace</span></span><br/>                | <span data-ttu-id="7b5cf-142">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7b5cf-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7b5cf-143">MOF</span><span class="sxs-lookup"><span data-stu-id="7b5cf-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b5cf-144"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7b5cf-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b5cf-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7b5cf-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b5cf-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7b5cf-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7b5cf-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b5cf-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b5cf-148">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="7b5cf-148">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

