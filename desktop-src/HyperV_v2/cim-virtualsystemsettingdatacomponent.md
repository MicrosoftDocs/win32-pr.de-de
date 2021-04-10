---
description: Stellt einen Teil einer Beziehung zwischen einer CIM \_ -virtualsystemsettingdata-Instanz und einem Satz von CIM \_ resourcezucationsettingdata-Instanzen dar.
ms.assetid: 4f167517-079e-4b5f-885a-741ac1d1dc71
title: CIM_VirtualSystemSettingDataComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingDataComponent
- CIM_VirtualSystemSettingDataComponent.GroupComponent
- CIM_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afbd7ab192c65e99f4479e5380e57dc78c8a0a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132000"
---
# <a name="cim_virtualsystemsettingdatacomponent-class"></a><span data-ttu-id="5ff17-103">CIM \_ virtualsystemsettingdatacomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="5ff17-103">CIM\_VirtualSystemSettingDataComponent class</span></span>

<span data-ttu-id="5ff17-104">Stellt einen Teil einer Beziehung zwischen einer [**CIM- \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Instanz und einem Satz von [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) -Instanzen dar.</span><span class="sxs-lookup"><span data-stu-id="5ff17-104">Represents a portion of a relationship between a [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) instance and a set of [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ff17-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ff17-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingDataComponent : CIM_Component
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="5ff17-106">Member</span><span class="sxs-lookup"><span data-stu-id="5ff17-106">Members</span></span>

<span data-ttu-id="5ff17-107">Die **CIM- \_ virtualsystemsettingdatacomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5ff17-107">The **CIM\_VirtualSystemSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="5ff17-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5ff17-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ff17-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5ff17-109">Properties</span></span>

<span data-ttu-id="5ff17-110">Die **CIM- \_ virtualsystemsettingdatacomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5ff17-110">The **CIM\_VirtualSystemSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ff17-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="5ff17-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ff17-112">Datentyp: **CIM \_ virtualsystemsettingdata**</span><span class="sxs-lookup"><span data-stu-id="5ff17-112">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="5ff17-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5ff17-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ff17-114">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="5ff17-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="5ff17-115">Ein Verweis auf das [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Objekt der obersten Ebene der virtuellen Systemkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="5ff17-115">A reference to the top-level [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) object of the virtual system configuration.</span></span>

</dd> <dt>

<span data-ttu-id="5ff17-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="5ff17-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ff17-117">Datentyp: **CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="5ff17-117">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="5ff17-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5ff17-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ff17-119">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="5ff17-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="5ff17-120">Ein Verweis auf das [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) -Objekt, das einen Teil der Konfiguration des virtuellen Systems darstellt.</span><span class="sxs-lookup"><span data-stu-id="5ff17-120">A reference the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) object that represents a part of the virtual system configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ff17-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ff17-121">Requirements</span></span>



| <span data-ttu-id="5ff17-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ff17-122">Requirement</span></span> | <span data-ttu-id="5ff17-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5ff17-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ff17-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ff17-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5ff17-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5ff17-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5ff17-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ff17-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5ff17-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ff17-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5ff17-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ff17-128">Namespace</span></span><br/>                | <span data-ttu-id="5ff17-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5ff17-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5ff17-130">MOF</span><span class="sxs-lookup"><span data-stu-id="5ff17-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ff17-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5ff17-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ff17-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5ff17-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ff17-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5ff17-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5ff17-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ff17-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ff17-135">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="5ff17-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

