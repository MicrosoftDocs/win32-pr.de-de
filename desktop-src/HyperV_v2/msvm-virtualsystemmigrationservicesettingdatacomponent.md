---
description: Eine Zuordnung, die verwendet wird, um die Netzwerkeinstellungen der virtuellen System Migration des virtuellen System Migrations Dienstanbieter darzustellen.
ms.assetid: 5704dce7-1db3-4049-8c61-58bfa9596766
title: Msvm_VirtualSystemMigrationServiceSettingDataComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingDataComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.GroupComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ba69ebd6cfd50b30923db2ecc87e7e5aeebcaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343645"
---
# <a name="msvm_virtualsystemmigrationservicesettingdatacomponent-class"></a><span data-ttu-id="2bff7-103">MSVM \_ virtualsystemmigrationservicesettingdatacomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="2bff7-103">Msvm\_VirtualSystemMigrationServiceSettingDataComponent class</span></span>

<span data-ttu-id="2bff7-104">Eine Zuordnung, die verwendet wird, um die Netzwerkeinstellungen der virtuellen System Migration des virtuellen System Migrations Dienstanbieter darzustellen.</span><span class="sxs-lookup"><span data-stu-id="2bff7-104">An association used to represent virtual system migration network settings of the virtual system migration service.</span></span>

<span data-ttu-id="2bff7-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2bff7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bff7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bff7-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingDataComponent : CIM_Component
{
  Msvm_VirtualSystemMigrationServiceSettingData REF GroupComponent;
  Msvm_VirtualSystemMigrationNetworkSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="2bff7-107">Member</span><span class="sxs-lookup"><span data-stu-id="2bff7-107">Members</span></span>

<span data-ttu-id="2bff7-108">Die **MSVM \_ virtualsystemmigrationservicesettingdatacomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2bff7-108">The **Msvm\_VirtualSystemMigrationServiceSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="2bff7-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bff7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2bff7-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bff7-110">Properties</span></span>

<span data-ttu-id="2bff7-111">Die **MSVM \_ virtualsystemmigrationservicesettingdatacomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2bff7-111">The **Msvm\_VirtualSystemMigrationServiceSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2bff7-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="2bff7-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bff7-113">Datentyp: **MSVM \_ virtualsystemmigrationservicesettingdata**</span><span class="sxs-lookup"><span data-stu-id="2bff7-113">Data type: **Msvm\_VirtualSystemMigrationServiceSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="2bff7-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bff7-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bff7-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bff7-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bff7-116">Ein Verweis auf eine Instanz der [**MSVM \_ virtualsystemmigrationservicesettingdata**](msvm-virtualsystemmigrationservicesettingdata.md) -Klasse, die die Einstellungen des Migrations dienstanweises darstellt.</span><span class="sxs-lookup"><span data-stu-id="2bff7-116">A reference to an instance of the [**Msvm\_VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) class that represents the migration service settings.</span></span>

</dd> <dt>

<span data-ttu-id="2bff7-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2bff7-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bff7-118">Datentyp: **MSVM \_ virtualsystemmigrationnetworksettingdata**</span><span class="sxs-lookup"><span data-stu-id="2bff7-118">Data type: **Msvm\_VirtualSystemMigrationNetworkSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="2bff7-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bff7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bff7-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="2bff7-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2bff7-121">Ein Verweis auf eine Instanz der [**MSVM \_ virtualsystemmigrationnetworksettingdata**](msvm-virtualsystemmigrationnetworksettingdata.md) -Klasse, die die Migrationsnetzwerk Einstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="2bff7-121">A reference to an instance of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that represents the migration network settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2bff7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bff7-122">Requirements</span></span>



| <span data-ttu-id="2bff7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bff7-123">Requirement</span></span> | <span data-ttu-id="2bff7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2bff7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bff7-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2bff7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2bff7-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bff7-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2bff7-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2bff7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2bff7-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bff7-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2bff7-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="2bff7-129">Namespace</span></span><br/>                | <span data-ttu-id="2bff7-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2bff7-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2bff7-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2bff7-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bff7-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2bff7-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bff7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2bff7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bff7-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2bff7-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

