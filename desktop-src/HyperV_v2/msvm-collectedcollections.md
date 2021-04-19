---
description: Ordnet die MSVM \_ virtualsystemcollection den enthaltenen MSVM \_ Computersystem-Objekten zu.
ms.assetid: bbf7713a-b331-4b40-bcb4-3545c26c6f3a
title: Msvm_CollectedCollections-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedCollections
- Msvm_CollectedCollections.Collection
- Msvm_CollectedCollections.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16ec6ad77c44e0a4e9001a0cb77d227573635ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362770"
---
# <a name="msvm_collectedcollections-class"></a><span data-ttu-id="37dbc-103">MSVM \_ collectedcollections-Klasse</span><span class="sxs-lookup"><span data-stu-id="37dbc-103">Msvm\_CollectedCollections class</span></span>

<span data-ttu-id="37dbc-104">Ordnet die [**MSVM \_ virtualsystemcollection**](msvm-virtualsystemcollection.md) den enthaltenen [**MSVM \_ Computersystem**](msvm-computersystem.md) -Objekten zu.</span><span class="sxs-lookup"><span data-stu-id="37dbc-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="37dbc-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="37dbc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37dbc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="37dbc-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a><span data-ttu-id="37dbc-107">Member</span><span class="sxs-lookup"><span data-stu-id="37dbc-107">Members</span></span>

<span data-ttu-id="37dbc-108">Die **MSVM \_ collectedcollections** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="37dbc-108">The **Msvm\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="37dbc-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37dbc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37dbc-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37dbc-110">Properties</span></span>

<span data-ttu-id="37dbc-111">Die **MSVM \_ collectedcollections** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="37dbc-111">The **Msvm\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37dbc-112">**Sammlung**</span><span class="sxs-lookup"><span data-stu-id="37dbc-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37dbc-113">Datentyp: **MSVM \_ managementcollection**</span><span class="sxs-lookup"><span data-stu-id="37dbc-113">Data type: **Msvm\_ManagementCollection**</span></span>
</dt> <dt>

<span data-ttu-id="37dbc-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37dbc-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37dbc-115">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="37dbc-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="37dbc-116">Eine [**MSVM- \_ managementcollection**](msvm-managementcollection.md) -Gruppierung oder ein ' Bag '-Objekt, das die Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="37dbc-116">An [**Msvm\_ManagementCollection**](msvm-managementcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="37dbc-117">**Member**</span><span class="sxs-lookup"><span data-stu-id="37dbc-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37dbc-118">Datentyp: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="37dbc-118">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="37dbc-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="37dbc-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37dbc-120">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="37dbc-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="37dbc-121">Eine [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) , die die Elemente der Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="37dbc-121">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37dbc-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37dbc-122">Requirements</span></span>



| <span data-ttu-id="37dbc-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37dbc-123">Requirement</span></span> | <span data-ttu-id="37dbc-124">Wert</span><span class="sxs-lookup"><span data-stu-id="37dbc-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37dbc-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37dbc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="37dbc-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37dbc-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="37dbc-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37dbc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="37dbc-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="37dbc-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="37dbc-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="37dbc-129">Namespace</span></span><br/>                | <span data-ttu-id="37dbc-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="37dbc-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="37dbc-131">MOF</span><span class="sxs-lookup"><span data-stu-id="37dbc-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37dbc-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="37dbc-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37dbc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="37dbc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37dbc-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37dbc-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37dbc-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37dbc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37dbc-136">**CIM \_ collectedmses**</span><span class="sxs-lookup"><span data-stu-id="37dbc-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

