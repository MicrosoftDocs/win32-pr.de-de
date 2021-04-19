---
description: Stellt eine generische Zuordnung zwischen einer Auflistung verwalteter Systemelemente und den Membern der Auflistung dar.
ms.assetid: c9e2bbca-67be-41f2-a94c-cf4eaf5f4694
title: CIM_CollectedMSEs-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdf5c5d682f1b6e1b47b64100b3e00f5f79cebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373198"
---
# <a name="cim_collectedmses-class-hyper-v-management"></a><span data-ttu-id="6dd63-103">CIM_CollectedMSEs-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="6dd63-103">CIM_CollectedMSEs class (Hyper-V management)</span></span>

<span data-ttu-id="6dd63-104">Stellt eine generische Zuordnung zwischen einer Auflistung verwalteter Systemelemente und den Membern der Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="6dd63-104">Represents a generic association between a collection of managed system elements and the members of the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dd63-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dd63-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectedMSEs : CIM_MemberOfCollection
{
  CIM_CollectionOfMSEs     REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="6dd63-106">Member</span><span class="sxs-lookup"><span data-stu-id="6dd63-106">Members</span></span>

<span data-ttu-id="6dd63-107">Die **CIM \_ collectedmses** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6dd63-107">The **CIM\_CollectedMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="6dd63-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6dd63-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6dd63-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6dd63-109">Properties</span></span>

<span data-ttu-id="6dd63-110">Die **CIM \_ collectedmses** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6dd63-110">The **CIM\_CollectedMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6dd63-111">**Sammlung**</span><span class="sxs-lookup"><span data-stu-id="6dd63-111">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dd63-112">Datentyp: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="6dd63-112">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="6dd63-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6dd63-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dd63-114">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="6dd63-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="6dd63-115">Die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="6dd63-115">The collection.</span></span>

</dd> <dt>

<span data-ttu-id="6dd63-116">**Member**</span><span class="sxs-lookup"><span data-stu-id="6dd63-116">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dd63-117">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="6dd63-117">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="6dd63-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6dd63-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dd63-119">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="6dd63-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="6dd63-120">Die Member der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="6dd63-120">The members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6dd63-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6dd63-121">Requirements</span></span>



| <span data-ttu-id="6dd63-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6dd63-122">Requirement</span></span> | <span data-ttu-id="6dd63-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6dd63-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd63-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6dd63-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6dd63-125">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6dd63-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6dd63-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6dd63-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6dd63-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6dd63-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6dd63-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="6dd63-128">Namespace</span></span><br/>                | <span data-ttu-id="6dd63-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6dd63-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6dd63-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6dd63-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6dd63-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6dd63-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6dd63-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6dd63-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dd63-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6dd63-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6dd63-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6dd63-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dd63-135">**CIM- \_ mitgliedfassungs Sammlung**</span><span class="sxs-lookup"><span data-stu-id="6dd63-135">**CIM\_MemberOfCollection**</span></span>](cim-memberofcollection.md)
</dt> </dl>

 

