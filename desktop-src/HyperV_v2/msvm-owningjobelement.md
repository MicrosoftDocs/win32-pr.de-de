---
description: Stellt eine Zuordnung zwischen einem Auftrag und dem verwalteten Element dar, das für die Erstellung des Auftrags zuständig ist.
ms.assetid: 1a100c7e-7e17-47dd-b730-c05c5e4dccda
title: Msvm_OwningJobElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_OwningJobElement
- Msvm_OwningJobElement.OwningElement
- Msvm_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 34aa6f390d21a37421e09f30f9a775784717be9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366275"
---
# <a name="msvm_owningjobelement-class"></a><span data-ttu-id="13e6e-103">MSVM \_ owningjobelements-Klasse</span><span class="sxs-lookup"><span data-stu-id="13e6e-103">Msvm\_OwningJobElement class</span></span>

<span data-ttu-id="13e6e-104">Stellt eine Zuordnung zwischen einem Auftrag und dem verwalteten Element dar, das für die Erstellung des Auftrags zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="13e6e-104">Represents an association between a job and the managed element responsible for the creation of the job.</span></span>

<span data-ttu-id="13e6e-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="13e6e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="13e6e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="13e6e-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_OwningJobElement : CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  Msvm_ConcreteJob   REF OwnedElement;
};
```

## <a name="members"></a><span data-ttu-id="13e6e-107">Member</span><span class="sxs-lookup"><span data-stu-id="13e6e-107">Members</span></span>

<span data-ttu-id="13e6e-108">Die **MSVM \_ owningjobelements** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="13e6e-108">The **Msvm\_OwningJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="13e6e-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13e6e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13e6e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13e6e-110">Properties</span></span>

<span data-ttu-id="13e6e-111">Die **MSVM \_ owningjobelements** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="13e6e-111">The **Msvm\_OwningJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13e6e-112">**Owdelta-Element**</span><span class="sxs-lookup"><span data-stu-id="13e6e-112">**OwnedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13e6e-113">Datentyp: **[ **MSVM \_ concretejob**](msvm-concretejob.md)**</span><span class="sxs-lookup"><span data-stu-id="13e6e-113">Data type: **[**Msvm\_ConcreteJob**](msvm-concretejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="13e6e-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="13e6e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13e6e-115">Der Auftrag, der vom verwalteten Element erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="13e6e-115">The job created by the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="13e6e-116">**OwningElement**</span><span class="sxs-lookup"><span data-stu-id="13e6e-116">**OwningElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13e6e-117">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="13e6e-117">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="13e6e-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="13e6e-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13e6e-119">Das verwaltete Element, das für die Erstellung des Auftrags zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="13e6e-119">The managed element responsible for the creation of the job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13e6e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13e6e-120">Requirements</span></span>



| <span data-ttu-id="13e6e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13e6e-121">Requirement</span></span> | <span data-ttu-id="13e6e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="13e6e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13e6e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13e6e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="13e6e-124">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13e6e-124">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="13e6e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13e6e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="13e6e-126">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13e6e-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13e6e-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="13e6e-127">Namespace</span></span><br/>                | <span data-ttu-id="13e6e-128">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="13e6e-128">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="13e6e-129">MOF</span><span class="sxs-lookup"><span data-stu-id="13e6e-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13e6e-130"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="13e6e-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13e6e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="13e6e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13e6e-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13e6e-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

