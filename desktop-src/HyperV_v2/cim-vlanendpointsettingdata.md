---
description: Stellt Konfigurationsdaten für einen VLAN-Endpunkt dar.
ms.assetid: 5ef3cc55-cf27-40b4-9e94-2e2b42ca41c5
title: CIM_VLANEndpointSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpointSettingData
- CIM_VLANEndpointSettingData.PruneEligibleVLANList
- CIM_VLANEndpointSettingData.NativeVLAN
- CIM_VLANEndpointSettingData.DefaultVLAN
- CIM_VLANEndpointSettingData.TrunkedVLANList
- CIM_VLANEndpointSettingData.AccessVLAN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a510c4195c538ab9735e7544acec2c88beeaa1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869280"
---
# <a name="cim_vlanendpointsettingdata-class"></a><span data-ttu-id="13c2d-103">CIM- \_ vlanendpointsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="13c2d-103">CIM\_VLANEndpointSettingData class</span></span>

<span data-ttu-id="13c2d-104">Stellt Konfigurationsdaten für einen VLAN-Endpunkt dar.</span><span class="sxs-lookup"><span data-stu-id="13c2d-104">Represents configuration data for a VLAN endpoint.</span></span>

## <a name="syntax"></a><span data-ttu-id="13c2d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13c2d-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.11.0"), UMLPackagePath("CIM::Network::VLAN")]
class CIM_VLANEndpointSettingData : CIM_SettingData
{
  uint16 PruneEligibleVLANList[];
  uint16 NativeVLAN;
  uint16 DefaultVLAN;
  uint16 TrunkedVLANList[];
  uint16 AccessVLAN;
};
```

## <a name="members"></a><span data-ttu-id="13c2d-106">Member</span><span class="sxs-lookup"><span data-stu-id="13c2d-106">Members</span></span>

<span data-ttu-id="13c2d-107">Die **CIM- \_ vlanendpointsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="13c2d-107">The **CIM\_VLANEndpointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="13c2d-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13c2d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13c2d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13c2d-109">Properties</span></span>

<span data-ttu-id="13c2d-110">Die **CIM- \_ vlanendpointsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="13c2d-110">The **CIM\_VLANEndpointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13c2d-111">**AccessVLAN**</span><span class="sxs-lookup"><span data-stu-id="13c2d-111">**AccessVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c2d-112">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13c2d-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13c2d-113">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="13c2d-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="13c2d-114">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ vlanendpoint**](cim-vlanendpoint.md)".**Operationalendpointmode**")</span><span class="sxs-lookup"><span data-stu-id="13c2d-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="13c2d-115">Das Access-VLAN für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="13c2d-115">The access VLAN for the endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="13c2d-116">**Defaultvlan**</span><span class="sxs-lookup"><span data-stu-id="13c2d-116">**DefaultVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c2d-117">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13c2d-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13c2d-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="13c2d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13c2d-119">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ vlanendpoint**](cim-vlanendpoint.md)".**Operationalendpointmode**")</span><span class="sxs-lookup"><span data-stu-id="13c2d-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="13c2d-120">Der Standardwert für das native VLAN auf dem trunk Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="13c2d-120">The default value for the native VLAN on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="13c2d-121">Diese Eigenschaft wird nur verwendet, wenn der VLAN-Endpunkt im trunkingmodus betrieben wird, der in der **operationalendpointmode** -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="13c2d-121">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="13c2d-122">**Nativevlan**</span><span class="sxs-lookup"><span data-stu-id="13c2d-122">**NativeVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c2d-123">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13c2d-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13c2d-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="13c2d-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="13c2d-125">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ vlanendpoint**](cim-vlanendpoint.md)".**Operationalendpointmode**")</span><span class="sxs-lookup"><span data-stu-id="13c2d-125">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="13c2d-126">Die VLAN-ID, die verwendet wird, um nicht markierten Datenverkehr zu markieren, der auf dem trunk Endpunkt empfangen wurde</span><span class="sxs-lookup"><span data-stu-id="13c2d-126">The VLAN ID that is used to tag untagged traffic received on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="13c2d-127">Diese Eigenschaft wird nur verwendet, wenn der VLAN-Endpunkt im trunkingmodus betrieben wird, der in der **switchendpointmode** -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="13c2d-127">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **SwitchEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="13c2d-128">**Pruneeligiblevlanlist**</span><span class="sxs-lookup"><span data-stu-id="13c2d-128">**PruneEligibleVLANList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c2d-129">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="13c2d-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="13c2d-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="13c2d-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="13c2d-131">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ vlanendpoint**](cim-vlanendpoint.md)".**Operationalendpointmode**")</span><span class="sxs-lookup"><span data-stu-id="13c2d-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="13c2d-132">Ein Array, das IDs von VLANs enthält, die vom System aus dem trunk Endpunkt entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="13c2d-132">An array that contains IDs of VLANs that the system may remove from the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="13c2d-133">Diese Eigenschaft wird nur verwendet, wenn der VLAN-Endpunkt im trunkingmodus betrieben wird, der in der **operationalendpointmode** -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="13c2d-133">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="13c2d-134">**TrunkedVLANList**</span><span class="sxs-lookup"><span data-stu-id="13c2d-134">**TrunkedVLANList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c2d-135">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="13c2d-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="13c2d-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="13c2d-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="13c2d-137">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ vlanendpoint**](cim-vlanendpoint.md)".**Operationalendpointmode**")</span><span class="sxs-lookup"><span data-stu-id="13c2d-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="13c2d-138">Ein Array, das IDs von VLAN-Endpunkten mit aktiviertem Trunking enthält.</span><span class="sxs-lookup"><span data-stu-id="13c2d-138">An array that contains IDs of VLAN endpoints with trunking enabled.</span></span>

> [!Note]  
> <span data-ttu-id="13c2d-139">Diese Eigenschaft wird nur verwendet, wenn der VLAN-Endpunkt im trunkingmodus betrieben wird, der in der **operationalendpointmode** -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="13c2d-139">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13c2d-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13c2d-140">Requirements</span></span>



| <span data-ttu-id="13c2d-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13c2d-141">Requirement</span></span> | <span data-ttu-id="13c2d-142">Wert</span><span class="sxs-lookup"><span data-stu-id="13c2d-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c2d-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13c2d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="13c2d-144">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="13c2d-144">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="13c2d-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13c2d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="13c2d-146">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="13c2d-146">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="13c2d-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="13c2d-147">Namespace</span></span><br/>                | <span data-ttu-id="13c2d-148">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="13c2d-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="13c2d-149">MOF</span><span class="sxs-lookup"><span data-stu-id="13c2d-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13c2d-150"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="13c2d-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13c2d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="13c2d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13c2d-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13c2d-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13c2d-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13c2d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c2d-154">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="13c2d-154">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

