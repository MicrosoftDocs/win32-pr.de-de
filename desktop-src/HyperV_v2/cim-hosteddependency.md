---
description: Stellt eine Zuordnung dar, in der ein verwaltetes Element von einem anderen gehostet wird.
ms.assetid: ae8476f7-38a4-4d08-a7dc-21e120d3cbe1
title: CIM_HostedDependency-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedDependency
- CIM_HostedDependency.Antecedent
- CIM_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 551931fd88fac88f85bcc8ffd51423538de3bb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342810"
---
# <a name="cim_hosteddependency-class"></a><span data-ttu-id="4683b-103">CIM-Klasse "- \_ Klassen Abhängigkeiten"</span><span class="sxs-lookup"><span data-stu-id="4683b-103">CIM\_HostedDependency class</span></span>

<span data-ttu-id="4683b-104">Stellt eine Zuordnung dar, in der ein verwaltetes Element von einem anderen gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="4683b-104">Represents an association where a managed element is hosted by another.</span></span>

## <a name="syntax"></a><span data-ttu-id="4683b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4683b-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_HostedDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4683b-106">Member</span><span class="sxs-lookup"><span data-stu-id="4683b-106">Members</span></span>

<span data-ttu-id="4683b-107">Die CIM-Klasse " **\_ husteddependenz** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4683b-107">The **CIM\_HostedDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="4683b-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4683b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4683b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4683b-109">Properties</span></span>

<span data-ttu-id="4683b-110">Die CIM-Klasse " **\_ husteddepend** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4683b-110">The **CIM\_HostedDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4683b-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="4683b-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4683b-112">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="4683b-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="4683b-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4683b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4683b-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="4683b-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4683b-115">Das vom Host verwaltete Element.</span><span class="sxs-lookup"><span data-stu-id="4683b-115">The host managed element.</span></span>

</dd> <dt>

<span data-ttu-id="4683b-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="4683b-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4683b-117">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="4683b-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="4683b-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4683b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4683b-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="4683b-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4683b-120">Das gehostete verwaltete Element.</span><span class="sxs-lookup"><span data-stu-id="4683b-120">The hosted managed element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4683b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4683b-121">Requirements</span></span>



| <span data-ttu-id="4683b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4683b-122">Requirement</span></span> | <span data-ttu-id="4683b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4683b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4683b-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4683b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4683b-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4683b-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4683b-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4683b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4683b-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4683b-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4683b-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="4683b-128">Namespace</span></span><br/>                | <span data-ttu-id="4683b-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4683b-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4683b-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4683b-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4683b-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4683b-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4683b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4683b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4683b-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4683b-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4683b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4683b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4683b-135">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="4683b-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

