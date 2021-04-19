---
description: Stellt die Einstellungsdaten für die Port Team Zuordnung dar.
ms.assetid: 7c9a392d-c95e-4b0d-8201-e50adabd21b2
title: Msvm_EthernetSwitchPortTeamMappingSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortTeamMappingSettingData
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterName
- Msvm_EthernetSwitchPortTeamMappingSettingData.NetAdapterDeviceId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f0d7385499dcdf6e84c361de03950a4e78be0a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106371795"
---
# <a name="msvm_ethernetswitchportteammappingsettingdata-class"></a><span data-ttu-id="0abaa-103">MSVM \_ ethernetzwitchportteammappingsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="0abaa-103">Msvm\_EthernetSwitchPortTeamMappingSettingData class</span></span>

<span data-ttu-id="0abaa-104">Stellt die Einstellungsdaten für die Port Team Zuordnung dar.</span><span class="sxs-lookup"><span data-stu-id="0abaa-104">Represents the port team mapping feature setting data.</span></span>

<span data-ttu-id="0abaa-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0abaa-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0abaa-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0abaa-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8D45D4BD-8C18-435C-98A7-D632A7C618FF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Team Mapping Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortTeamMappingSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string NetAdapterName = "";
  string NetAdapterDeviceId = "";
};
```

## <a name="members"></a><span data-ttu-id="0abaa-107">Member</span><span class="sxs-lookup"><span data-stu-id="0abaa-107">Members</span></span>

<span data-ttu-id="0abaa-108">Die **MSVM \_ ethernetzwitchportteammappingsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0abaa-108">The **Msvm\_EthernetSwitchPortTeamMappingSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0abaa-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0abaa-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0abaa-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0abaa-110">Properties</span></span>

<span data-ttu-id="0abaa-111">Die **MSVM \_ ethernetzwitchportteammappingsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0abaa-111">The **Msvm\_EthernetSwitchPortTeamMappingSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0abaa-112">**Netadapterde viceid**</span><span class="sxs-lookup"><span data-stu-id="0abaa-112">**NetAdapterDeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0abaa-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0abaa-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0abaa-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0abaa-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0abaa-115">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0abaa-115">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0abaa-116">Geräte-ID des bevorzugten zugeordneten physischen Adapters.</span><span class="sxs-lookup"><span data-stu-id="0abaa-116">Device ID of the preferred mapped physical adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0abaa-117">**Netadaptername**</span><span class="sxs-lookup"><span data-stu-id="0abaa-117">**NetAdapterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0abaa-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0abaa-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0abaa-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0abaa-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0abaa-120">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0abaa-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0abaa-121">Der Name des bevorzugten zugeordneten physischen Adapters.</span><span class="sxs-lookup"><span data-stu-id="0abaa-121">Name of the preferred mapped physical adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0abaa-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0abaa-122">Requirements</span></span>



| <span data-ttu-id="0abaa-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0abaa-123">Requirement</span></span> | <span data-ttu-id="0abaa-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0abaa-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0abaa-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0abaa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0abaa-126">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0abaa-126">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0abaa-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0abaa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0abaa-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0abaa-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0abaa-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="0abaa-129">Namespace</span></span><br/>                | <span data-ttu-id="0abaa-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0abaa-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0abaa-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0abaa-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0abaa-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0abaa-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0abaa-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0abaa-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0abaa-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0abaa-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0abaa-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0abaa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0abaa-136">**MSVM \_ ethernetzwitchportfeaturesettingdata**</span><span class="sxs-lookup"><span data-stu-id="0abaa-136">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

