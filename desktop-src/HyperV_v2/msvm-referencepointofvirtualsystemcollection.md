---
description: Ordnet die MSVM \_ referencepointcollection den entsprechenden MSVM \_ virtualsystemcollection-Objekten zu.
ms.assetid: 847f1f46-364f-4c91-b9e8-4740d3da1947
title: Msvm_ReferencePointOfVirtualSystemCollection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystemCollection
- Msvm_ReferencePointOfVirtualSystemCollection.Antecedent
- Msvm_ReferencePointOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0919b8666915817d8475908b0305e90ea39e60f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349883"
---
# <a name="msvm_referencepointofvirtualsystemcollection-class"></a><span data-ttu-id="b7646-103">MSVM \_ referencepoinpofvirtualsystemcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="b7646-103">Msvm\_ReferencePointOfVirtualSystemCollection class</span></span>

<span data-ttu-id="b7646-104">Ordnet die [**MSVM \_ referencepointcollection**](msvm-referencepointcollection.md) den entsprechenden [**MSVM \_ virtualsystemcollection**](msvm-virtualsystemcollection.md) -Objekten zu.</span><span class="sxs-lookup"><span data-stu-id="b7646-104">Associates the [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) to the corresponding [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) objects.</span></span>

<span data-ttu-id="b7646-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b7646-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7646-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7646-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b7646-107">Member</span><span class="sxs-lookup"><span data-stu-id="b7646-107">Members</span></span>

<span data-ttu-id="b7646-108">Die **MSVM \_ referencepointofvirtualsystemcollection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b7646-108">The **Msvm\_ReferencePointOfVirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="b7646-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b7646-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7646-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b7646-110">Properties</span></span>

<span data-ttu-id="b7646-111">Die **MSVM \_ referencepoinpofvirtualsystemcollection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b7646-111">The **Msvm\_ReferencePointOfVirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7646-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="b7646-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7646-113">Datentyp: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="b7646-113">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="b7646-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b7646-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7646-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="b7646-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b7646-116">Ein [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) , das das unabhängige Objekt in dieser Zuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="b7646-116">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="b7646-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="b7646-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7646-118">Datentyp: **CIM \_** -Auflistung</span><span class="sxs-lookup"><span data-stu-id="b7646-118">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="b7646-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b7646-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7646-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span><span class="sxs-lookup"><span data-stu-id="b7646-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b7646-121">Eine [**CIM \_**](cim-collection.md) -Auflistung, die das Objekt darstellt, das von dem **Vorgänger** abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="b7646-121">A [**CIM\_Collection**](cim-collection.md) that represents the object that is dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7646-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7646-122">Requirements</span></span>



| <span data-ttu-id="b7646-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7646-123">Requirement</span></span> | <span data-ttu-id="b7646-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b7646-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7646-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7646-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b7646-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7646-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b7646-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7646-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b7646-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b7646-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b7646-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7646-129">Namespace</span></span><br/>                | <span data-ttu-id="b7646-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b7646-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b7646-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b7646-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7646-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b7646-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7646-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b7646-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7646-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b7646-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b7646-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7646-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7646-136">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="b7646-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

