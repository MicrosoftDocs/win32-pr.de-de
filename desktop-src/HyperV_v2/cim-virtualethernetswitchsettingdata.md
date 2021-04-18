---
description: Beschreibt die Einstellungsdaten für einen virtuellen Ethernet-Switch.
ms.assetid: 462cff06-5ba6-410a-b091-5c6abab13f03
title: CIM_VirtualEthernetSwitchSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualEthernetSwitchSettingData
- CIM_VirtualEthernetSwitchSettingData.VLANConnection
- CIM_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- CIM_VirtualEthernetSwitchSettingData.MaxNumMACAddress
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64d7053364aebe1fab5739cd75389b1a9343efe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343831"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a><span data-ttu-id="29747-103">CIM \_ virtualethernetzwitchsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="29747-103">CIM\_VirtualEthernetSwitchSettingData class</span></span>

<span data-ttu-id="29747-104">Beschreibt die Einstellungsdaten für einen virtuellen Ethernet-Switch.</span><span class="sxs-lookup"><span data-stu-id="29747-104">Describes settings data for a virtual ethernet switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="29747-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="29747-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualEthernetSwitchSettingData : CIM_VirtualSystemSettingData
{
  string VLANConnection[];
  string AssociatedResourcePool[];
  uint32 MaxNumMACAddress;
};
```

## <a name="members"></a><span data-ttu-id="29747-106">Member</span><span class="sxs-lookup"><span data-stu-id="29747-106">Members</span></span>

<span data-ttu-id="29747-107">Die **CIM- \_ virtualethernetzwitchsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="29747-107">The **CIM\_VirtualEthernetSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="29747-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29747-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29747-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29747-109">Properties</span></span>

<span data-ttu-id="29747-110">Die **CIM- \_ virtualethernetzwitchsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="29747-110">The **CIM\_VirtualEthernetSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29747-111">**Associatedresourcepool**</span><span class="sxs-lookup"><span data-stu-id="29747-111">**AssociatedResourcePool**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29747-112">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="29747-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="29747-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="29747-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29747-114">Ein Array, das die derzeit zugeordneten Host Ressourcenpools enthält, oder, die dem Ethernet-Switch zugeordnet werden sollen, um Ethernet-Verbindungen zwischen dem Ethernet-Switch und einem virtuellen Computer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="29747-114">An array that contains the host resource pools that are currently associated, or to associate with the ethernet switch, in order to allocate ethernet connections between the ethernet switch and a virtual machine.</span></span> <span data-ttu-id="29747-115">Jeder Wert, der nicht NULL ist, muss mit dem **WBEM- \_ URI \_ untypedinstancepath** übereinstimmen, wie in der DMTF-Spezifikation "DSP0207" definiert.</span><span class="sxs-lookup"><span data-stu-id="29747-115">Each non-Null value of this property must conform to **WBEM\_URI\_UntypedInstancePath** as defined in the DMTF "DSP0207" specification.</span></span>

</dd> <dt>

<span data-ttu-id="29747-116">**Maxnummacaddress**</span><span class="sxs-lookup"><span data-stu-id="29747-116">**MaxNumMACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29747-117">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="29747-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="29747-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="29747-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29747-119">Die Anzahl der eindeutigen MAC-Adressen, die der Switch für Mac-Address Learning erlernen kann, wie im IEEE 802,1-Standard definiert.</span><span class="sxs-lookup"><span data-stu-id="29747-119">The number of unique MAC addresses that the switch can learn for MAC address learning, as defined in the IEEE 802.1 standard.</span></span>

</dd> <dt>

<span data-ttu-id="29747-120">**Vlanconnection**</span><span class="sxs-lookup"><span data-stu-id="29747-120">**VLANConnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29747-121">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="29747-121">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="29747-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="29747-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29747-123">Ein Array, das die VLAN-IDs enthält, auf die der Switch zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="29747-123">An array that contains the VLAN IDs that the switch can access.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29747-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29747-124">Requirements</span></span>



| <span data-ttu-id="29747-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29747-125">Requirement</span></span> | <span data-ttu-id="29747-126">Wert</span><span class="sxs-lookup"><span data-stu-id="29747-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29747-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29747-127">Minimum supported client</span></span><br/> | <span data-ttu-id="29747-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="29747-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="29747-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29747-129">Minimum supported server</span></span><br/> | <span data-ttu-id="29747-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29747-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="29747-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="29747-131">Namespace</span></span><br/>                | <span data-ttu-id="29747-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="29747-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="29747-133">MOF</span><span class="sxs-lookup"><span data-stu-id="29747-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29747-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="29747-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="29747-135">DLL</span><span class="sxs-lookup"><span data-stu-id="29747-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29747-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="29747-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="29747-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29747-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29747-138">**CIM \_ virtualsystemsettingdata**</span><span class="sxs-lookup"><span data-stu-id="29747-138">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 




