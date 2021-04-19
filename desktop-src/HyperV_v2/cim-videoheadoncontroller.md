---
description: Ordnet der Grafikkarte, die Sie enthält, einen Video Kopf zu.
ms.assetid: d15f4350-1529-4246-9ea2-8453e52516c6
title: CIM_VideoHeadOnController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHeadOnController
- CIM_VideoHeadOnController.Antecedent
- CIM_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18178e6d9d7f1e684af1d4fe74336e1f2a02eedc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349149"
---
# <a name="cim_videoheadoncontroller-class"></a><span data-ttu-id="93df1-103">CIM- \_ videoheadoncontroller-Klasse</span><span class="sxs-lookup"><span data-stu-id="93df1-103">CIM\_VideoHeadOnController class</span></span>

<span data-ttu-id="93df1-104">Ordnet der Grafikkarte, die Sie enthält, einen Video Kopf zu.</span><span class="sxs-lookup"><span data-stu-id="93df1-104">Associates a video head with the video adapter that contains it.</span></span>

## <a name="syntax"></a><span data-ttu-id="93df1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="93df1-105">Syntax</span></span>

``` syntax
[Association, Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHeadOnController : CIM_HostedDependency
{
  CIM_DisplayController REF Antecedent;
  CIM_VideoHead         REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="93df1-106">Member</span><span class="sxs-lookup"><span data-stu-id="93df1-106">Members</span></span>

<span data-ttu-id="93df1-107">Die **CIM \_ videoheadoncontroller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="93df1-107">The **CIM\_VideoHeadOnController** class has these types of members:</span></span>

-   [<span data-ttu-id="93df1-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93df1-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93df1-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93df1-109">Properties</span></span>

<span data-ttu-id="93df1-110">Die **CIM \_ videoheadoncontroller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="93df1-110">The **CIM\_VideoHeadOnController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93df1-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="93df1-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93df1-112">Datentyp: **CIM \_ Display Controller**</span><span class="sxs-lookup"><span data-stu-id="93df1-112">Data type: **CIM\_DisplayController**</span></span>
</dt> <dt>

<span data-ttu-id="93df1-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93df1-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93df1-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="93df1-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="93df1-115">Die Grafikkarte, die den Kopf enthält.</span><span class="sxs-lookup"><span data-stu-id="93df1-115">The video adapter that includes the head.</span></span>

</dd> <dt>

<span data-ttu-id="93df1-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="93df1-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93df1-117">Datentyp: **CIM- \_ videohead**</span><span class="sxs-lookup"><span data-stu-id="93df1-117">Data type: **CIM\_VideoHead**</span></span>
</dt> <dt>

<span data-ttu-id="93df1-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93df1-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93df1-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="93df1-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="93df1-120">Die Kopfzeile auf der Grafikkarte.</span><span class="sxs-lookup"><span data-stu-id="93df1-120">The head on the video adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93df1-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93df1-121">Requirements</span></span>



| <span data-ttu-id="93df1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93df1-122">Requirement</span></span> | <span data-ttu-id="93df1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="93df1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93df1-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93df1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="93df1-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="93df1-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="93df1-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93df1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="93df1-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93df1-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="93df1-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="93df1-128">Namespace</span></span><br/>                | <span data-ttu-id="93df1-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="93df1-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="93df1-130">MOF</span><span class="sxs-lookup"><span data-stu-id="93df1-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93df1-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="93df1-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93df1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="93df1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93df1-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93df1-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93df1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93df1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93df1-135">**CIM- \_ hubabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="93df1-135">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

