---
description: Stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und einem logischen Gerät dar, von dem es implementiert wird.
ms.assetid: 40c8111a-d439-4c0f-805e-9c10d7182eb4
title: CIM_DeviceSAPImplementation-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Antecedent
- CIM_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e32676077cccd5c7e17fa551e904079f457b8d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354538"
---
# <a name="cim_devicesapimplementation-class-hyper-v-management"></a><span data-ttu-id="c525c-103">CIM_DeviceSAPImplementation-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="c525c-103">CIM_DeviceSAPImplementation class (Hyper-V management)</span></span>

<span data-ttu-id="c525c-104">Stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und einem logischen Gerät dar, von dem es implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="c525c-104">Represents an association between a service access point (SAP) and a logical device that implements it.</span></span>

## <a name="syntax"></a><span data-ttu-id="c525c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c525c-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c525c-106">Member</span><span class="sxs-lookup"><span data-stu-id="c525c-106">Members</span></span>

<span data-ttu-id="c525c-107">Die CIM-Klasse " **\_ devicesapimplementation** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c525c-107">The **CIM\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="c525c-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c525c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c525c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c525c-109">Properties</span></span>

<span data-ttu-id="c525c-110">Die CIM-Klasse " **\_ devicesapimplementation** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c525c-110">The **CIM\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c525c-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="c525c-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c525c-112">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="c525c-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="c525c-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c525c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c525c-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="c525c-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c525c-115">Das logische Gerät.</span><span class="sxs-lookup"><span data-stu-id="c525c-115">The logical device.</span></span>

</dd> <dt>

<span data-ttu-id="c525c-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="c525c-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c525c-117">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="c525c-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="c525c-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c525c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c525c-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="c525c-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c525c-120">Das vom logischen Gerät implementierte SAP.</span><span class="sxs-lookup"><span data-stu-id="c525c-120">The SAP implemented by the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c525c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c525c-121">Requirements</span></span>



| <span data-ttu-id="c525c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c525c-122">Requirement</span></span> | <span data-ttu-id="c525c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c525c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c525c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c525c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c525c-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c525c-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c525c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c525c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c525c-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c525c-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c525c-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="c525c-128">Namespace</span></span><br/>                | <span data-ttu-id="c525c-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c525c-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c525c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="c525c-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c525c-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c525c-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c525c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c525c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c525c-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c525c-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c525c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c525c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c525c-135">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="c525c-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

