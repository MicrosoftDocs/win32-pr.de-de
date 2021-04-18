---
description: Verknüpft ein System mit einem logischen Gerät, das eine Komponente des Systems ist.
ms.assetid: d5a36f71-5ebe-46e2-aaa9-5d99fa075d31
title: CIM_SystemDevice-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.GroupComponent
- CIM_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b02921e4be0f8aa0cddc194a2ed430e10e115eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343448"
---
# <a name="cim_systemdevice-class-hyper-v-management"></a><span data-ttu-id="c7d57-103">CIM_SystemDevice-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="c7d57-103">CIM_SystemDevice class (Hyper-V management)</span></span>

<span data-ttu-id="c7d57-104">Verknüpft ein System mit einem logischen Gerät, das eine Komponente des Systems ist.</span><span class="sxs-lookup"><span data-stu-id="c7d57-104">Associates a system with a logical device that is a component of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7d57-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7d57-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="c7d57-106">Member</span><span class="sxs-lookup"><span data-stu-id="c7d57-106">Members</span></span>

<span data-ttu-id="c7d57-107">Die **CIM- \_ SystemDevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c7d57-107">The **CIM\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="c7d57-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7d57-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7d57-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7d57-109">Properties</span></span>

<span data-ttu-id="c7d57-110">Die **CIM- \_ SystemDevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c7d57-110">The **CIM\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7d57-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="c7d57-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7d57-112">Datentyp: **CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="c7d57-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="c7d57-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7d57-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7d57-114">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="c7d57-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="c7d57-115">Ein [**CIM- \_ System**](cim-system.md) Verweis auf das übergeordnete System in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="c7d57-115">A [**CIM\_System**](cim-system.md) reference to the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="c7d57-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c7d57-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7d57-117">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="c7d57-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="c7d57-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7d57-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7d57-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("PartComponent"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c7d57-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c7d57-120">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Verweis auf das logische Gerät, das eine Komponente des Systems ist.</span><span class="sxs-lookup"><span data-stu-id="c7d57-120">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) reference to the logical device that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7d57-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7d57-121">Requirements</span></span>



| <span data-ttu-id="c7d57-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7d57-122">Requirement</span></span> | <span data-ttu-id="c7d57-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c7d57-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d57-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7d57-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c7d57-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c7d57-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c7d57-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7d57-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c7d57-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7d57-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c7d57-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7d57-128">Namespace</span></span><br/>                | <span data-ttu-id="c7d57-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c7d57-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c7d57-130">MOF</span><span class="sxs-lookup"><span data-stu-id="c7d57-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7d57-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c7d57-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7d57-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c7d57-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7d57-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7d57-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c7d57-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7d57-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d57-135">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="c7d57-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

