---
description: Stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und dem System dar, von dem es gehostet wird.
ms.assetid: 82db71d6-6d14-408e-87e0-fe869e454d4d
title: CIM_HostedAccessPoint-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Antecedent
- CIM_HostedAccessPoint.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0684c2855e7966a0c01d1d9f9bfa0cbd71c2397a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484211"
---
# <a name="cim_hostedaccesspoint-class-hyper-v-management"></a><span data-ttu-id="56a92-103">CIM_HostedAccessPoint-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="56a92-103">CIM_HostedAccessPoint class (Hyper-V management)</span></span>

<span data-ttu-id="56a92-104">Stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und dem System dar, von dem es gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="56a92-104">Represents an association between a service access point (SAP) and the system that hosts it.</span></span> <span data-ttu-id="56a92-105">Ein System kann mehrere Zugriffspunkte hosten.</span><span class="sxs-lookup"><span data-stu-id="56a92-105">A system can host multiple access points.</span></span> <span data-ttu-id="56a92-106">Wenn die Implementierung von SAP modelliert ist, muss Sie von einem Gerät oder einer Software Funktion implementiert werden, die Teil des Systems ist, das SAP hostet.</span><span class="sxs-lookup"><span data-stu-id="56a92-106">If the implementation of the SAP is modeled, it must be implemented by a device or software feature that is part of the system that hosts the SAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="56a92-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56a92-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_HostedAccessPoint : CIM_HostedDependency
{
  CIM_System             REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="56a92-108">Member</span><span class="sxs-lookup"><span data-stu-id="56a92-108">Members</span></span>

<span data-ttu-id="56a92-109">Die CIM-Klasse " **\_ tarstedaccesspoint** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="56a92-109">The **CIM\_HostedAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="56a92-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="56a92-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="56a92-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="56a92-111">Properties</span></span>

<span data-ttu-id="56a92-112">Die CIM-Klasse " **\_ stestedaccesspoint** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="56a92-112">The **CIM\_HostedAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56a92-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="56a92-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56a92-114">Datentyp: **CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="56a92-114">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="56a92-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="56a92-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56a92-116">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="56a92-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="56a92-117">Das Host System.</span><span class="sxs-lookup"><span data-stu-id="56a92-117">The hosting System.</span></span>

</dd> <dt>

<span data-ttu-id="56a92-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="56a92-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56a92-119">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="56a92-119">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="56a92-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="56a92-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56a92-121">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="56a92-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="56a92-122">Die SAPS, die auf dem System gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="56a92-122">The SAPs that are hosted on the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56a92-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56a92-123">Requirements</span></span>



| <span data-ttu-id="56a92-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56a92-124">Requirement</span></span> | <span data-ttu-id="56a92-125">Wert</span><span class="sxs-lookup"><span data-stu-id="56a92-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56a92-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56a92-126">Minimum supported client</span></span><br/> | <span data-ttu-id="56a92-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="56a92-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="56a92-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56a92-128">Minimum supported server</span></span><br/> | <span data-ttu-id="56a92-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="56a92-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="56a92-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="56a92-130">Namespace</span></span><br/>                | <span data-ttu-id="56a92-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="56a92-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="56a92-132">MOF</span><span class="sxs-lookup"><span data-stu-id="56a92-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56a92-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="56a92-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="56a92-134">DLL</span><span class="sxs-lookup"><span data-stu-id="56a92-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56a92-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="56a92-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="56a92-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56a92-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56a92-137">**CIM- \_ hubabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="56a92-137">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

