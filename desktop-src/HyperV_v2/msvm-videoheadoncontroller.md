---
description: Ordnet einen Video Kopf dem Videocontroller zu, der ihn enthält.
ms.assetid: D072DF7C-D55B-4203-9FE5-B395D1EC1632
title: Msvm_VideoHeadOnController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHeadOnController
- Msvm_VideoHeadOnController.Antecedent
- Msvm_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11065c7b7a9e23b786697c3d4f0dbd63e67d6b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131520"
---
# <a name="msvm_videoheadoncontroller-class"></a><span data-ttu-id="33463-103">MSVM \_ videoheadoncontroller-Klasse</span><span class="sxs-lookup"><span data-stu-id="33463-103">Msvm\_VideoHeadOnController class</span></span>

<span data-ttu-id="33463-104">Ordnet einen Video Kopf dem Videocontroller zu, der ihn enthält.</span><span class="sxs-lookup"><span data-stu-id="33463-104">Associates a video head with the video controller that includes it.</span></span>

<span data-ttu-id="33463-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="33463-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="33463-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="33463-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHeadOnController : CIM_VideoHeadOnController
{
  CIM_DisplayController REF Antecedent;
  Msvm_VideoHead        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="33463-107">Member</span><span class="sxs-lookup"><span data-stu-id="33463-107">Members</span></span>

<span data-ttu-id="33463-108">Die **MSVM \_ videoheadoncontroller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="33463-108">The **Msvm\_VideoHeadOnController** class has these types of members:</span></span>

-   [<span data-ttu-id="33463-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="33463-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33463-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="33463-110">Properties</span></span>

<span data-ttu-id="33463-111">Die **MSVM \_ videoheadoncontroller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="33463-111">The **Msvm\_VideoHeadOnController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33463-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="33463-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33463-113">Datentyp: **[ **CIM \_ Display Controller**](/previous-versions//cc136810(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="33463-113">Data type: **[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="33463-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="33463-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33463-115">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="33463-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="33463-116">Der Videocontroller, der den Kopf enthält.</span><span class="sxs-lookup"><span data-stu-id="33463-116">The video controller that includes the head.</span></span>

</dd> <dt>

<span data-ttu-id="33463-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="33463-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33463-118">Datentyp: **[ **MSVM \_ videohead**](msvm-videohead.md)**</span><span class="sxs-lookup"><span data-stu-id="33463-118">Data type: **[**Msvm\_VideoHead**](msvm-videohead.md)**</span></span>
</dt> <dt>

<span data-ttu-id="33463-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="33463-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33463-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="33463-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="33463-121">Die Kopfzeile des Videogeräts.</span><span class="sxs-lookup"><span data-stu-id="33463-121">The head on the video device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33463-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33463-122">Remarks</span></span>

<span data-ttu-id="33463-123">Der Zugriff auf die **MSVM \_ videoheadoncontroller** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="33463-123">Access to the **Msvm\_VideoHeadOnController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="33463-124">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="33463-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="33463-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33463-125">Requirements</span></span>



| <span data-ttu-id="33463-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33463-126">Requirement</span></span> | <span data-ttu-id="33463-127">Wert</span><span class="sxs-lookup"><span data-stu-id="33463-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33463-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33463-128">Minimum supported client</span></span><br/> | <span data-ttu-id="33463-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33463-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="33463-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33463-130">Minimum supported server</span></span><br/> | <span data-ttu-id="33463-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33463-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33463-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="33463-132">Namespace</span></span><br/>                | <span data-ttu-id="33463-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="33463-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="33463-134">MOF</span><span class="sxs-lookup"><span data-stu-id="33463-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33463-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="33463-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="33463-136">DLL</span><span class="sxs-lookup"><span data-stu-id="33463-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33463-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="33463-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="33463-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33463-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33463-139">**CIM- \_ videoheadoncontroller**</span><span class="sxs-lookup"><span data-stu-id="33463-139">**CIM\_VideoHeadOnController**</span></span>](cim-videoheadoncontroller.md)
</dt> <dt>

<span data-ttu-id="33463-140">[**CIM- \_ videoheadoncontroller**](/previous-versions//cc136950(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33463-140">[**CIM\_VideoHeadOnController**](/previous-versions//cc136950(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="33463-141">Video Klassen</span><span class="sxs-lookup"><span data-stu-id="33463-141">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

