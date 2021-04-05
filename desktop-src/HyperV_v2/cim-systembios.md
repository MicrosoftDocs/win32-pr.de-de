---
description: Ordnet ein BIOS einem Computersystem zu.
ms.assetid: a06af789-75c8-4d58-8a25-572dcf1091e2
title: CIM_SystemBIOS-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemBIOS
- CIM_SystemBIOS.GroupComponent
- CIM_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: faa3130544fdb97bdf216fa266bc9e8cfe1815bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042075"
---
# <a name="cim_systembios-class"></a><span data-ttu-id="4338a-103">CIM- \_ Systembios-Klasse</span><span class="sxs-lookup"><span data-stu-id="4338a-103">CIM\_SystemBIOS class</span></span>

<span data-ttu-id="4338a-104">Ordnet ein BIOS einem Computersystem zu.</span><span class="sxs-lookup"><span data-stu-id="4338a-104">Associates a BIOS with a computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4338a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4338a-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_SystemBIOS : CIM_SystemComponent
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_BIOSElement    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="4338a-106">Member</span><span class="sxs-lookup"><span data-stu-id="4338a-106">Members</span></span>

<span data-ttu-id="4338a-107">Die **CIM- \_ Systembios** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4338a-107">The **CIM\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="4338a-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4338a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4338a-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4338a-109">Properties</span></span>

<span data-ttu-id="4338a-110">Die **CIM- \_ Systembios** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4338a-110">The **CIM\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4338a-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4338a-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4338a-112">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="4338a-112">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="4338a-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4338a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4338a-114">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="4338a-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4338a-115">Das Computersystem, das über das BIOS gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="4338a-115">The computer system that boots from the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="4338a-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4338a-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4338a-117">Datentyp: **CIM \_ bioselements**</span><span class="sxs-lookup"><span data-stu-id="4338a-117">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="4338a-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4338a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4338a-119">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="4338a-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4338a-120">Das BIOS.</span><span class="sxs-lookup"><span data-stu-id="4338a-120">The BIOS.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4338a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4338a-121">Requirements</span></span>



| <span data-ttu-id="4338a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4338a-122">Requirement</span></span> | <span data-ttu-id="4338a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4338a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4338a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4338a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4338a-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4338a-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4338a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4338a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4338a-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4338a-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4338a-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="4338a-128">Namespace</span></span><br/>                | <span data-ttu-id="4338a-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4338a-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4338a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4338a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4338a-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4338a-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4338a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4338a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4338a-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4338a-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4338a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4338a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4338a-135">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="4338a-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

