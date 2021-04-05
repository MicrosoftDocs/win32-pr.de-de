---
description: Ordnet die MSVM \_ referencepointcollection den enthaltenen MSVM \_ virtualsystemreferencepoint-Objekten zu.
ms.assetid: 826125c3-0a89-4573-ac28-88588eac248d
title: Msvm_CollectedReferencePoints-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedReferencePoints
- Msvm_CollectedReferencePoints.Collection
- Msvm_CollectedReferencePoints.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4891d4ec4c613c92c3b5d5a090f2683bfc77dc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753024"
---
# <a name="msvm_collectedreferencepoints-class"></a><span data-ttu-id="5b74b-103">MSVM \_ collectedreferencepoints-Klasse</span><span class="sxs-lookup"><span data-stu-id="5b74b-103">Msvm\_CollectedReferencePoints class</span></span>

<span data-ttu-id="5b74b-104">Ordnet die [**MSVM \_ referencepointcollection**](msvm-referencepointcollection.md) den enthaltenen [**MSVM \_ virtualsystemreferencepoint**](msvm-virtualsystemreferencepoint.md) -Objekten zu.</span><span class="sxs-lookup"><span data-stu-id="5b74b-104">Associates the [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) to the contained [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) objects.</span></span>

<span data-ttu-id="5b74b-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5b74b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b74b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b74b-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedReferencePoints : CIM_CollectedMSEs
{
  Msvm_ReferencePointCollection    REF Collection;
  Msvm_VirtualSystemReferencePoint REF Member;
};
```

## <a name="members"></a><span data-ttu-id="5b74b-107">Member</span><span class="sxs-lookup"><span data-stu-id="5b74b-107">Members</span></span>

<span data-ttu-id="5b74b-108">Die **MSVM \_ collectedreferencepoints** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5b74b-108">The **Msvm\_CollectedReferencePoints** class has these types of members:</span></span>

-   [<span data-ttu-id="5b74b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b74b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b74b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b74b-110">Properties</span></span>

<span data-ttu-id="5b74b-111">Die **MSVM \_ collectedreferencepoints** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5b74b-111">The **Msvm\_CollectedReferencePoints** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b74b-112">**Sammlung**</span><span class="sxs-lookup"><span data-stu-id="5b74b-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b74b-113">Datentyp: **MSVM \_ referencepointcollection**</span><span class="sxs-lookup"><span data-stu-id="5b74b-113">Data type: **Msvm\_ReferencePointCollection**</span></span>
</dt> <dt>

<span data-ttu-id="5b74b-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b74b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b74b-115">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="5b74b-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="5b74b-116">Eine [**MSVM- \_ referencepointcollection**](msvm-referencepointcollection.md) -Gruppierung oder ein "Bag"-Objekt, das die Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="5b74b-116">An [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="5b74b-117">**Member**</span><span class="sxs-lookup"><span data-stu-id="5b74b-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b74b-118">Datentyp: **MSVM \_ virtualsystemreferencepoint**</span><span class="sxs-lookup"><span data-stu-id="5b74b-118">Data type: **Msvm\_VirtualSystemReferencePoint**</span></span>
</dt> <dt>

<span data-ttu-id="5b74b-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5b74b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b74b-120">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="5b74b-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="5b74b-121">Ein [**MSVM \_ virtualsystemreferencepoint**](msvm-virtualsystemreferencepoint.md) , der die Member der Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="5b74b-121">An [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b74b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b74b-122">Requirements</span></span>



| <span data-ttu-id="5b74b-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b74b-123">Requirement</span></span> | <span data-ttu-id="5b74b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5b74b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b74b-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b74b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5b74b-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b74b-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5b74b-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b74b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5b74b-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5b74b-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5b74b-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b74b-129">Namespace</span></span><br/>                | <span data-ttu-id="5b74b-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5b74b-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5b74b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5b74b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b74b-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5b74b-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b74b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5b74b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b74b-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5b74b-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5b74b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b74b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b74b-136">**CIM \_ collectedmses**</span><span class="sxs-lookup"><span data-stu-id="5b74b-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

