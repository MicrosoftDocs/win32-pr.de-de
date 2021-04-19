---
description: Stellt die Zuordnung zwischen einer Ansicht und einer-Instanz dar, die die normalisierte Ansicht einer verwalteten Ressource darstellt.
ms.assetid: 9c6eb3d5-7366-4954-9e64-12f889c64114
title: CIM_ElementView-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementView
- CIM_ElementView.Antecedent
- CIM_ElementView.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ffc0e4b69667800b1880cae1a992a207cc95a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363508"
---
# <a name="cim_elementview-class"></a><span data-ttu-id="d3425-103">CIM- \_ elementview-Klasse</span><span class="sxs-lookup"><span data-stu-id="d3425-103">CIM\_ElementView class</span></span>

<span data-ttu-id="d3425-104">Stellt die Zuordnung zwischen einer Ansicht und einer-Instanz dar, die die normalisierte Ansicht einer verwalteten Ressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3425-104">Represents and association between a view, and an instance that represents the normalized view of a managed resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3425-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3425-105">Syntax</span></span>

``` syntax
[Abstract, Association, Experimental, Version("2.21.1"), UMLPackagePath("CIM::Core::CoreElements")]
class CIM_ElementView : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_View           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d3425-106">Member</span><span class="sxs-lookup"><span data-stu-id="d3425-106">Members</span></span>

<span data-ttu-id="d3425-107">Die **CIM- \_ elementview** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d3425-107">The **CIM\_ElementView** class has these types of members:</span></span>

-   [<span data-ttu-id="d3425-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d3425-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d3425-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d3425-109">Properties</span></span>

<span data-ttu-id="d3425-110">Die **CIM- \_ elementview** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d3425-110">The **CIM\_ElementView** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d3425-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="d3425-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3425-112">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="d3425-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d3425-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d3425-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3425-114">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="d3425-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d3425-115">Die-Instanz, die die normalisierte Ansicht der verwalteten Ressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3425-115">The instance that represents the normalized view of the managed resource.</span></span>

</dd> <dt>

<span data-ttu-id="d3425-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="d3425-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3425-117">Datentyp: **CIM- \_ Ansicht**</span><span class="sxs-lookup"><span data-stu-id="d3425-117">Data type: **CIM\_View**</span></span>
</dt> <dt>

<span data-ttu-id="d3425-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d3425-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3425-119">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span><span class="sxs-lookup"><span data-stu-id="d3425-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d3425-120">Die Ansicht, die eine denormalisierte oder Aggregat Ansicht der verwalteten Ressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3425-120">The view that represents a de-normalized or aggregate view of the managed resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3425-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3425-121">Requirements</span></span>



| <span data-ttu-id="d3425-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3425-122">Requirement</span></span> | <span data-ttu-id="d3425-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d3425-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3425-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3425-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d3425-125">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3425-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d3425-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3425-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d3425-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d3425-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d3425-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3425-128">Namespace</span></span><br/>                | <span data-ttu-id="d3425-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d3425-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d3425-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d3425-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3425-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d3425-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3425-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d3425-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3425-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d3425-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d3425-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3425-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3425-135">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="d3425-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

