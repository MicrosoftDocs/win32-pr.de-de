---
description: 'Msvm_CollectedCollections-Klasse: Ordnet die Msvm \_ VirtualSystemCollection den enthaltenen Msvm \_ ComputerSystem-Objekten zu.'
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
ms.openlocfilehash: 83719d364fac22923d68206c8cfe7d37adad5edb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112128"
---
# <a name="msvm_collectedcollections-class"></a><span data-ttu-id="045e9-103">Msvm \_ CollectedCollections-Klasse</span><span class="sxs-lookup"><span data-stu-id="045e9-103">Msvm\_CollectedCollections class</span></span>

<span data-ttu-id="045e9-104">Ordnet die [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) den enthaltenen [**Msvm \_ ComputerSystem-Objekten**](msvm-computersystem.md) zu.</span><span class="sxs-lookup"><span data-stu-id="045e9-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="045e9-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="045e9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="045e9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="045e9-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a><span data-ttu-id="045e9-107">Member</span><span class="sxs-lookup"><span data-stu-id="045e9-107">Members</span></span>

<span data-ttu-id="045e9-108">Die **Msvm \_ CollectedCollections-Klasse** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="045e9-108">The **Msvm\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="045e9-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="045e9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="045e9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="045e9-110">Properties</span></span>

<span data-ttu-id="045e9-111">Die **Msvm \_ CollectedCollections-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="045e9-111">The **Msvm\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="045e9-112">**Sammlung**</span><span class="sxs-lookup"><span data-stu-id="045e9-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="045e9-113">Datentyp: **Msvm \_ ManagementCollection**</span><span class="sxs-lookup"><span data-stu-id="045e9-113">Data type: **Msvm\_ManagementCollection**</span></span>
</dt> <dt>

<span data-ttu-id="045e9-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="045e9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="045e9-115">Qualifizierer: [**Aggregieren,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="045e9-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="045e9-116">Ein [**Msvm \_ ManagementCollection-Gruppierungsobjekt**](msvm-managementcollection.md) oder ein Bag-Objekt, das die Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="045e9-116">An [**Msvm\_ManagementCollection**](msvm-managementcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="045e9-117">**Member**</span><span class="sxs-lookup"><span data-stu-id="045e9-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="045e9-118">Datentyp: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="045e9-118">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="045e9-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="045e9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="045e9-120">Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="045e9-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="045e9-121">Eine [**\_ CIM-CollectionOfMSEs,**](cim-collectionofmses.md) die die Elemente der Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="045e9-121">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="045e9-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="045e9-122">Requirements</span></span>



| <span data-ttu-id="045e9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="045e9-123">Requirement</span></span> | <span data-ttu-id="045e9-124">Wert</span><span class="sxs-lookup"><span data-stu-id="045e9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="045e9-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="045e9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="045e9-126">nur Windows 10 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="045e9-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="045e9-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="045e9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="045e9-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="045e9-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="045e9-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="045e9-129">Namespace</span></span><br/>                | <span data-ttu-id="045e9-130">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="045e9-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="045e9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="045e9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="045e9-132"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="045e9-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="045e9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="045e9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="045e9-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="045e9-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="045e9-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="045e9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="045e9-136">**CIM \_ CollectedMSEs**</span><span class="sxs-lookup"><span data-stu-id="045e9-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

