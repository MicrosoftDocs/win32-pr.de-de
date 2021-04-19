---
description: Stellt eine Zuordnung zwischen einem Port oder einem Verbindungspunkt und einem Gerät dar.
ms.assetid: b35e741a-7110-4e48-a132-d436f4fbf038
title: CIM_PortOnDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PortOnDevice
- CIM_PortOnDevice.Antecedent
- CIM_PortOnDevice.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76d8500daaa5db1746efa347e5dd10eb70a82234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363821"
---
# <a name="cim_portondevice-class"></a><span data-ttu-id="8b0d4-103">CIM- \_ portondevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="8b0d4-103">CIM\_PortOnDevice class</span></span>

<span data-ttu-id="8b0d4-104">Stellt eine Zuordnung zwischen einem Port oder einem Verbindungspunkt und einem Gerät dar.</span><span class="sxs-lookup"><span data-stu-id="8b0d4-104">Represents an association between a port or connection point and a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b0d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b0d4-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_PortOnDevice : CIM_HostedDependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="8b0d4-106">Member</span><span class="sxs-lookup"><span data-stu-id="8b0d4-106">Members</span></span>

<span data-ttu-id="8b0d4-107">Die **CIM- \_ portondevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8b0d4-107">The **CIM\_PortOnDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="8b0d4-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b0d4-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b0d4-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b0d4-109">Properties</span></span>

<span data-ttu-id="8b0d4-110">Die **CIM- \_ portondevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8b0d4-110">The **CIM\_PortOnDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b0d4-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="8b0d4-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b0d4-112">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="8b0d4-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="8b0d4-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b0d4-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b0d4-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="8b0d4-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8b0d4-115">Das Gerät, das den Port enthält.</span><span class="sxs-lookup"><span data-stu-id="8b0d4-115">The device that includes the port.</span></span>

</dd> <dt>

<span data-ttu-id="8b0d4-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="8b0d4-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b0d4-117">Datentyp: **CIM \_ logicalport**</span><span class="sxs-lookup"><span data-stu-id="8b0d4-117">Data type: **CIM\_LogicalPort**</span></span>
</dt> <dt>

<span data-ttu-id="8b0d4-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b0d4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b0d4-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="8b0d4-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8b0d4-120">Der Port auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="8b0d4-120">The port on the device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b0d4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b0d4-121">Requirements</span></span>



| <span data-ttu-id="8b0d4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b0d4-122">Requirement</span></span> | <span data-ttu-id="8b0d4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="8b0d4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b0d4-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b0d4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8b0d4-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8b0d4-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8b0d4-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b0d4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8b0d4-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b0d4-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8b0d4-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b0d4-128">Namespace</span></span><br/>                | <span data-ttu-id="8b0d4-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8b0d4-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8b0d4-130">MOF</span><span class="sxs-lookup"><span data-stu-id="8b0d4-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b0d4-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8b0d4-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b0d4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8b0d4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b0d4-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b0d4-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8b0d4-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b0d4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b0d4-135">**CIM- \_ hubabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="8b0d4-135">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

