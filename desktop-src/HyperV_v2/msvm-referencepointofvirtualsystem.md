---
description: Ordnet den MSVM \_ virtualsystemreferencepoint den entsprechenden MSVM \_ virtualsystem-Objekten zu.
ms.assetid: 5a9cb099-c0ae-4088-a64c-f2720a6cb9c8
title: Msvm_ReferencePointOfVirtualSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystem
- Msvm_ReferencePointOfVirtualSystem.Antecedent
- Msvm_ReferencePointOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debe1931154c5c7a7868e8ee301daf977076b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756895"
---
# <a name="msvm_referencepointofvirtualsystem-class"></a><span data-ttu-id="5ebe4-103">MSVM \_ referencepoinpofvirtualsystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="5ebe4-103">Msvm\_ReferencePointOfVirtualSystem class</span></span>

<span data-ttu-id="5ebe4-104">Ordnet den [**MSVM \_ virtualsystemreferencepoint**](msvm-virtualsystemreferencepoint.md) den entsprechenden [**MSVM \_ virtualsystem**](msvm-virtualsystemresourcecomponent.md) -Objekten zu.</span><span class="sxs-lookup"><span data-stu-id="5ebe4-104">Associates the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) to the corresponding [**Msvm\_VirtualSystem**](msvm-virtualsystemresourcecomponent.md) objects.</span></span>

<span data-ttu-id="5ebe4-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5ebe4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ebe4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ebe4-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystem : CIM_Dependency
{
  Msvm_ComputerSystem              REF Antecedent;
  Msvm_VirtualSystemReferencePoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5ebe4-107">Member</span><span class="sxs-lookup"><span data-stu-id="5ebe4-107">Members</span></span>

<span data-ttu-id="5ebe4-108">Die **MSVM \_ referencepointofvirtualsystem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5ebe4-108">The **Msvm\_ReferencePointOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="5ebe4-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5ebe4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ebe4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5ebe4-110">Properties</span></span>

<span data-ttu-id="5ebe4-111">Die **MSVM \_ referencepoinpofvirtualsystem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5ebe4-111">The **Msvm\_ReferencePointOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ebe4-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="5ebe4-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ebe4-113">Datentyp: **MSVM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="5ebe4-113">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="5ebe4-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5ebe4-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ebe4-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="5ebe4-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5ebe4-116">Ein [**MSVM- \_ Computersystem**](msvm-computersystem.md) , das das unabhängige Objekt in dieser Zuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="5ebe4-116">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="5ebe4-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="5ebe4-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ebe4-118">Datentyp: **MSVM \_ virtualsystemreferencepoint**</span><span class="sxs-lookup"><span data-stu-id="5ebe4-118">Data type: **Msvm\_VirtualSystemReferencePoint**</span></span>
</dt> <dt>

<span data-ttu-id="5ebe4-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5ebe4-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ebe4-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span><span class="sxs-lookup"><span data-stu-id="5ebe4-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5ebe4-121">Ein [**MSVM \_ virtualsystemreferencepoint**](msvm-virtualsystemreferencepoint.md) , das das Objekt darstellt, das von dem **Vorgänger** abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="5ebe4-121">An [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) that represents the object that is dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ebe4-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ebe4-122">Requirements</span></span>



| <span data-ttu-id="5ebe4-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ebe4-123">Requirement</span></span> | <span data-ttu-id="5ebe4-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5ebe4-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebe4-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ebe4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5ebe4-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ebe4-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5ebe4-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ebe4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5ebe4-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5ebe4-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5ebe4-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ebe4-129">Namespace</span></span><br/>                | <span data-ttu-id="5ebe4-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5ebe4-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5ebe4-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5ebe4-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ebe4-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5ebe4-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ebe4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5ebe4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ebe4-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5ebe4-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5ebe4-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ebe4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ebe4-136">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="5ebe4-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

