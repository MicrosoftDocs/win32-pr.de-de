---
description: Stellt eine Zuordnung zwischen einem Auftrag und dem verwalteten Element dar, das den Auftrag erstellt hat.
ms.assetid: 08c33a81-0a3f-4545-9812-96a854a7509e
title: CIM_OwningJobElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OwningJobElement
- CIM_OwningJobElement.OwningElement
- CIM_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9d3879104a8f7406ff24dc2f63b79b51eb2fa58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351484"
---
# <a name="cim_owningjobelement-class"></a><span data-ttu-id="e4618-103">CIM \_ owningjobelements-Klasse</span><span class="sxs-lookup"><span data-stu-id="e4618-103">CIM\_OwningJobElement class</span></span>

<span data-ttu-id="e4618-104">Stellt eine Zuordnung zwischen einem Auftrag und dem verwalteten Element dar, das den Auftrag erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="e4618-104">Represents an association between a job and the managed element that created the job.</span></span> <span data-ttu-id="e4618-105">Da ein Auftrag zwischen Systemen verschoben werden kann und das verwaltete Element möglicherweise nicht für die gesamte Dauer des Auftrags vorhanden ist, ist diese Zuordnung in einigen Fällen möglicherweise nicht möglich oder nur für einen Teil des Vorhandenseins des Auftrags vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e4618-105">Since a job might move between systems, and the managed element might not exist for the entire duration of the job, in some cases, this association might not be possible or might only exist for a portion of the existence of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4618-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4618-106">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::System::Processing"), ModelCorrespondence("CIM_Job.Owner"), AMENDMENT]
class CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  CIM_Job            REF OwnedElement;
};
```

## <a name="members"></a><span data-ttu-id="e4618-107">Member</span><span class="sxs-lookup"><span data-stu-id="e4618-107">Members</span></span>

<span data-ttu-id="e4618-108">Die **CIM \_ owningjobelements** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e4618-108">The **CIM\_OwningJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="e4618-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4618-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4618-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4618-110">Properties</span></span>

<span data-ttu-id="e4618-111">Die **CIM \_ owningjobelements** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e4618-111">The **CIM\_OwningJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4618-112">**Owdelta-Element**</span><span class="sxs-lookup"><span data-stu-id="e4618-112">**OwnedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4618-113">Datentyp: **CIM- \_ Auftrag**</span><span class="sxs-lookup"><span data-stu-id="e4618-113">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="e4618-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e4618-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4618-115">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e4618-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e4618-116">Ein Verweis auf den Auftrag, der vom verwalteten Element erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e4618-116">A reference to the job created by the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="e4618-117">**OwningElement**</span><span class="sxs-lookup"><span data-stu-id="e4618-117">**OwningElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4618-118">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="e4618-118">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="e4618-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e4618-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4618-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e4618-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e4618-121">Ein Verweis auf das verwaltete Element, das den Auftrag erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="e4618-121">A reference to the managed element that created the job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4618-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4618-122">Requirements</span></span>



| <span data-ttu-id="e4618-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4618-123">Requirement</span></span> | <span data-ttu-id="e4618-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e4618-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4618-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4618-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e4618-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e4618-126">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e4618-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4618-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e4618-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4618-128">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e4618-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4618-129">Namespace</span></span><br/>                | <span data-ttu-id="e4618-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e4618-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e4618-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e4618-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4618-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e4618-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4618-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e4618-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4618-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e4618-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

