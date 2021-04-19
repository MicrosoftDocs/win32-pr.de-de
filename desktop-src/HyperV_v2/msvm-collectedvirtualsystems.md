---
description: Ordnet die MSVM \_ virtualsystemcollection den enthaltenen MSVM \_ Computersystem-Objekten zu.
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Msvm_CollectedVirtualSystems-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedVirtualSystems
- Msvm_CollectedVirtualSystems.Collection
- Msvm_CollectedVirtualSystems.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0803eda14ffbaf21ee2bf4491bd835123b7191e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366141"
---
# <a name="msvm_collectedvirtualsystems-class"></a><span data-ttu-id="eca20-103">MSVM \_ collectedvirtualsystems-Klasse</span><span class="sxs-lookup"><span data-stu-id="eca20-103">Msvm\_CollectedVirtualSystems class</span></span>

<span data-ttu-id="eca20-104">Ordnet die [**MSVM \_ virtualsystemcollection**](msvm-virtualsystemcollection.md) den enthaltenen [**MSVM \_ Computersystem**](msvm-computersystem.md) -Objekten zu.</span><span class="sxs-lookup"><span data-stu-id="eca20-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="eca20-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eca20-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca20-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="eca20-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a><span data-ttu-id="eca20-107">Member</span><span class="sxs-lookup"><span data-stu-id="eca20-107">Members</span></span>

<span data-ttu-id="eca20-108">Die **MSVM \_ collectedvirtualsystems** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eca20-108">The **Msvm\_CollectedVirtualSystems** class has these types of members:</span></span>

-   [<span data-ttu-id="eca20-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eca20-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eca20-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eca20-110">Properties</span></span>

<span data-ttu-id="eca20-111">Die **MSVM \_ collectedvirtualsystems** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eca20-111">The **Msvm\_CollectedVirtualSystems** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eca20-112">**Sammlung**</span><span class="sxs-lookup"><span data-stu-id="eca20-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eca20-113">Datentyp: **MSVM \_ virtualsystemcollection**</span><span class="sxs-lookup"><span data-stu-id="eca20-113">Data type: **Msvm\_VirtualSystemCollection**</span></span>
</dt> <dt>

<span data-ttu-id="eca20-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eca20-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eca20-115">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="eca20-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="eca20-116">Eine [**MSVM- \_ virtualsystemcollection**](msvm-virtualsystemcollection.md) -Gruppierung oder ein "Bag"-Objekt, das die Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="eca20-116">An [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="eca20-117">**Member**</span><span class="sxs-lookup"><span data-stu-id="eca20-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eca20-118">Datentyp: **MSVM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="eca20-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="eca20-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eca20-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eca20-120">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="eca20-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="eca20-121">Ein [**MSVM \_ Computersystem**](msvm-computersystem.md) -Objekt, das die Member der Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="eca20-121">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) object containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eca20-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eca20-122">Requirements</span></span>



| <span data-ttu-id="eca20-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eca20-123">Requirement</span></span> | <span data-ttu-id="eca20-124">Wert</span><span class="sxs-lookup"><span data-stu-id="eca20-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eca20-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eca20-125">Minimum supported client</span></span><br/> | <span data-ttu-id="eca20-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eca20-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="eca20-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eca20-127">Minimum supported server</span></span><br/> | <span data-ttu-id="eca20-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="eca20-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="eca20-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="eca20-129">Namespace</span></span><br/>                | <span data-ttu-id="eca20-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="eca20-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eca20-131">MOF</span><span class="sxs-lookup"><span data-stu-id="eca20-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eca20-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eca20-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eca20-133">DLL</span><span class="sxs-lookup"><span data-stu-id="eca20-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eca20-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eca20-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eca20-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eca20-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eca20-136">**CIM \_ collectedmses**</span><span class="sxs-lookup"><span data-stu-id="eca20-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

