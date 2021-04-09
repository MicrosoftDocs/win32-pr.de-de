---
description: Stellt eine Beziehung dar, in der ein verwaltetes Element ein Member von ist und durch eine Auflistung aggregiert wird.
ms.assetid: 324284fa-ece6-41df-9891-040a7561dce4
title: CIM_MemberOfCollection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemberOfCollection
- CIM_MemberOfCollection.Collection
- CIM_MemberOfCollection.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9bcebfb08cbbc0cb18e00f1b0e5e2646ca086faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042551"
---
# <a name="cim_memberofcollection-class"></a><span data-ttu-id="15fe1-103">CIM- \_ mitgliedfassungs Klasse</span><span class="sxs-lookup"><span data-stu-id="15fe1-103">CIM\_MemberOfCollection class</span></span>

<span data-ttu-id="15fe1-104">Stellt eine Beziehung dar, in der ein verwaltetes Element ein Member von ist und durch eine Auflistung aggregiert wird.</span><span class="sxs-lookup"><span data-stu-id="15fe1-104">Represents a relationship in which a managed element is a member of and is aggregated by a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="15fe1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15fe1-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_MemberOfCollection
{
  CIM_Collection     REF Collection;
  CIM_ManagedElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="15fe1-106">Member</span><span class="sxs-lookup"><span data-stu-id="15fe1-106">Members</span></span>

<span data-ttu-id="15fe1-107">Die **CIM- \_ mitgliedfassungs** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="15fe1-107">The **CIM\_MemberOfCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="15fe1-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15fe1-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15fe1-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15fe1-109">Properties</span></span>

<span data-ttu-id="15fe1-110">Die **CIM- \_ Mitgliedschafts** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="15fe1-110">The **CIM\_MemberOfCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15fe1-111">**Sammlung**</span><span class="sxs-lookup"><span data-stu-id="15fe1-111">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15fe1-112">Datentyp: **CIM \_** -Auflistung</span><span class="sxs-lookup"><span data-stu-id="15fe1-112">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="15fe1-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="15fe1-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15fe1-114">Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregat**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="15fe1-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="15fe1-115">Die Auflistung, die Elemente aggregiert.</span><span class="sxs-lookup"><span data-stu-id="15fe1-115">The collection that aggregates members.</span></span>

</dd> <dt>

<span data-ttu-id="15fe1-116">**Member**</span><span class="sxs-lookup"><span data-stu-id="15fe1-116">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15fe1-117">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="15fe1-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="15fe1-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="15fe1-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15fe1-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="15fe1-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="15fe1-120">Der Member der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="15fe1-120">The member of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15fe1-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15fe1-121">Requirements</span></span>



| <span data-ttu-id="15fe1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15fe1-122">Requirement</span></span> | <span data-ttu-id="15fe1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="15fe1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15fe1-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15fe1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="15fe1-125">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15fe1-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="15fe1-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15fe1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="15fe1-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="15fe1-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="15fe1-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="15fe1-128">Namespace</span></span><br/>                | <span data-ttu-id="15fe1-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="15fe1-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="15fe1-130">MOF</span><span class="sxs-lookup"><span data-stu-id="15fe1-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15fe1-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="15fe1-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15fe1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="15fe1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15fe1-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15fe1-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

