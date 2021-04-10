---
description: Stellt eine Zuordnung dar, bei der ein Dienst eine Komponente eines übergeordneten Dienstanbieter ist, die zusammen einen höheren Dienst bilden.
ms.assetid: c629d59d-d9d3-4019-a378-cd1d4d31a5d9
title: CIM_ServiceComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceComponent
- CIM_ServiceComponent.GroupComponent
- CIM_ServiceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2bfb9943685f8568674e696a76df94fda502fcb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214748"
---
# <a name="cim_servicecomponent-class"></a><span data-ttu-id="47b49-103">CIM- \_ ServiceComponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="47b49-103">CIM\_ServiceComponent class</span></span>

<span data-ttu-id="47b49-104">Stellt eine Zuordnung dar, bei der ein Dienst eine Komponente eines übergeordneten Dienstanbieter ist, die zusammen einen höheren Dienst bilden.</span><span class="sxs-lookup"><span data-stu-id="47b49-104">Represents an association in which a service is a component of a parent service, which together, form a higher-level service.</span></span>

## <a name="syntax"></a><span data-ttu-id="47b49-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47b49-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceComponent : CIM_Component
{
  CIM_Service REF GroupComponent;
  CIM_Service REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="47b49-106">Member</span><span class="sxs-lookup"><span data-stu-id="47b49-106">Members</span></span>

<span data-ttu-id="47b49-107">Die **CIM- \_ ServiceComponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="47b49-107">The **CIM\_ServiceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="47b49-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47b49-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47b49-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47b49-109">Properties</span></span>

<span data-ttu-id="47b49-110">Die **CIM- \_ ServiceComponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="47b49-110">The **CIM\_ServiceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47b49-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="47b49-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b49-112">Datentyp: **CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="47b49-112">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="47b49-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47b49-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b49-114">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="47b49-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="47b49-115">Der übergeordnete Dienst.</span><span class="sxs-lookup"><span data-stu-id="47b49-115">The parent service.</span></span>

</dd> <dt>

<span data-ttu-id="47b49-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="47b49-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b49-117">Datentyp: **CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="47b49-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="47b49-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47b49-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b49-119">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="47b49-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="47b49-120">Der Komponenten Dienst.</span><span class="sxs-lookup"><span data-stu-id="47b49-120">The component service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47b49-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47b49-121">Requirements</span></span>



| <span data-ttu-id="47b49-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47b49-122">Requirement</span></span> | <span data-ttu-id="47b49-123">Wert</span><span class="sxs-lookup"><span data-stu-id="47b49-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47b49-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47b49-124">Minimum supported client</span></span><br/> | <span data-ttu-id="47b49-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="47b49-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="47b49-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47b49-126">Minimum supported server</span></span><br/> | <span data-ttu-id="47b49-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="47b49-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="47b49-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="47b49-128">Namespace</span></span><br/>                | <span data-ttu-id="47b49-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="47b49-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="47b49-130">MOF</span><span class="sxs-lookup"><span data-stu-id="47b49-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47b49-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="47b49-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="47b49-132">DLL</span><span class="sxs-lookup"><span data-stu-id="47b49-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47b49-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="47b49-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="47b49-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47b49-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47b49-135">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="47b49-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

