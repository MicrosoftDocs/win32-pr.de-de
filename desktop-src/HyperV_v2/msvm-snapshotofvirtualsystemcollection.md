---
description: Ordnet die MSVM \_ snapshotcollection den entsprechenden MSVM \_ virtualsystemcollection-Objekten zu.
ms.assetid: 4dbfe21f-e700-4266-aedb-236c57c424f6
title: Msvm_SnapshotOfVirtualSystemCollection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystemCollection
- Msvm_SnapshotOfVirtualSystemCollection.Antecedent
- Msvm_SnapshotOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae3c9c146cea8a8af98f4d3071ee7339d53eb6b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863560"
---
# <a name="msvm_snapshotofvirtualsystemcollection-class"></a><span data-ttu-id="bfbb2-103">MSVM- \_ snapshodessystemcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="bfbb2-103">Msvm\_SnapshotOfVirtualSystemCollection class</span></span>

<span data-ttu-id="bfbb2-104">Ordnet die [**MSVM \_ snapshotcollection**](msvm-snapshotcollection.md) den entsprechenden [**MSVM \_ virtualsystemcollection**](msvm-virtualsystemcollection.md) -Objekten zu.</span><span class="sxs-lookup"><span data-stu-id="bfbb2-104">Associates the [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) to the corresponding [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) objects.</span></span>

<span data-ttu-id="bfbb2-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bfbb2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfbb2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfbb2-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="bfbb2-107">Member</span><span class="sxs-lookup"><span data-stu-id="bfbb2-107">Members</span></span>

<span data-ttu-id="bfbb2-108">Die **MSVM \_ snapshotofvirtualsystemcollection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bfbb2-108">The **Msvm\_SnapshotOfVirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="bfbb2-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bfbb2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bfbb2-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bfbb2-110">Properties</span></span>

<span data-ttu-id="bfbb2-111">Die **MSVM- \_ snapshodessystemcollection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bfbb2-111">The **Msvm\_SnapshotOfVirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bfbb2-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="bfbb2-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfbb2-113">Datentyp: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="bfbb2-113">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="bfbb2-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bfbb2-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfbb2-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="bfbb2-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="bfbb2-116">Ein [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) , das das unabhängige Objekt in dieser Zuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="bfbb2-116">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="bfbb2-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="bfbb2-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfbb2-118">Datentyp: **CIM \_** -Auflistung</span><span class="sxs-lookup"><span data-stu-id="bfbb2-118">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="bfbb2-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bfbb2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfbb2-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span><span class="sxs-lookup"><span data-stu-id="bfbb2-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="bfbb2-121">Eine [**CIM \_**](cim-collection.md) -Auflistung, die das Objekt darstellt, das von dem Vorgänger abhängig ist **.**</span><span class="sxs-lookup"><span data-stu-id="bfbb2-121">A [**CIM\_Collection**](cim-collection.md) that represents the object that is dependent on the **Antecedent.**</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfbb2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfbb2-122">Requirements</span></span>



| <span data-ttu-id="bfbb2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfbb2-123">Requirement</span></span> | <span data-ttu-id="bfbb2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="bfbb2-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfbb2-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfbb2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bfbb2-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfbb2-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="bfbb2-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfbb2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bfbb2-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bfbb2-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bfbb2-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="bfbb2-129">Namespace</span></span><br/>                | <span data-ttu-id="bfbb2-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="bfbb2-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bfbb2-131">MOF</span><span class="sxs-lookup"><span data-stu-id="bfbb2-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfbb2-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bfbb2-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfbb2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="bfbb2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfbb2-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bfbb2-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bfbb2-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfbb2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfbb2-136">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="bfbb2-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

