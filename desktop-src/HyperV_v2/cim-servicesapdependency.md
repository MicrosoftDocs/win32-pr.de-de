---
description: Stellt eine Zuordnung zwischen einem Dienst und einem Dienst Zugriffspunkt (SAP) dar, der dem Dienst Funktionalität bereitstellt.
ms.assetid: 9b82fad2-9731-4e0d-bdb0-d1be13ea20fc
title: CIM_ServiceSAPDependency-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Antecedent
- CIM_ServiceSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d49b63dfb37dfddf009f01122f4aa49af316fa58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349488"
---
# <a name="cim_servicesapdependency-class-hyper-v-management"></a><span data-ttu-id="61835-103">CIM_ServiceSAPDependency-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="61835-103">CIM_ServiceSAPDependency class (Hyper-V management)</span></span>

<span data-ttu-id="61835-104">Stellt eine Zuordnung zwischen einem Dienst und einem Dienst Zugriffspunkt (SAP) dar, der dem Dienst Funktionalität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="61835-104">Represents an association between a service and a service access point (SAP) that provides the service with functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="61835-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="61835-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_Service            REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="61835-106">Member</span><span class="sxs-lookup"><span data-stu-id="61835-106">Members</span></span>

<span data-ttu-id="61835-107">Die **CIM \_ servicesapdepenpklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="61835-107">The **CIM\_ServiceSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="61835-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="61835-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61835-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="61835-109">Properties</span></span>

<span data-ttu-id="61835-110">Die **CIM \_ servicesapdepenpklasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="61835-110">The **CIM\_ServiceSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61835-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="61835-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61835-112">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="61835-112">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="61835-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61835-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61835-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="61835-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="61835-115">Der erforderliche Dienst Zugriffspunkt.</span><span class="sxs-lookup"><span data-stu-id="61835-115">The required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="61835-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="61835-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61835-117">Datentyp: **CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="61835-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="61835-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61835-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61835-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="61835-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="61835-120">Der Dienst, der vom SAP abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="61835-120">The service that is dependent on the SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61835-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61835-121">Requirements</span></span>



| <span data-ttu-id="61835-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61835-122">Requirement</span></span> | <span data-ttu-id="61835-123">Wert</span><span class="sxs-lookup"><span data-stu-id="61835-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61835-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61835-124">Minimum supported client</span></span><br/> | <span data-ttu-id="61835-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="61835-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="61835-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61835-126">Minimum supported server</span></span><br/> | <span data-ttu-id="61835-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="61835-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="61835-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="61835-128">Namespace</span></span><br/>                | <span data-ttu-id="61835-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="61835-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="61835-130">MOF</span><span class="sxs-lookup"><span data-stu-id="61835-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61835-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="61835-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61835-132">DLL</span><span class="sxs-lookup"><span data-stu-id="61835-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61835-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61835-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61835-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61835-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61835-135">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="61835-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

