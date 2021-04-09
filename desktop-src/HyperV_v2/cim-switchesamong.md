---
description: Stellt einen switchdienst dar, mit dem Frames zwischen Switchports gewechselt werden.
ms.assetid: ee2d4831-df00-408c-b350-26d2d1d3e8aa
title: CIM_SwitchesAmong-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchesAmong
- CIM_SwitchesAmong.Antecedent
- CIM_SwitchesAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16a87797b4a138ef79be3d5ea8c6304d2ce4a942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129689"
---
# <a name="cim_switchesamong-class"></a><span data-ttu-id="6e148-103">CIM \_ switchesunter-Klasse</span><span class="sxs-lookup"><span data-stu-id="6e148-103">CIM\_SwitchesAmong class</span></span>

<span data-ttu-id="6e148-104">Stellt einen switchdienst dar, mit dem Frames zwischen Switchports gewechselt werden.</span><span class="sxs-lookup"><span data-stu-id="6e148-104">Represents a switch service, which switches frames between switch ports.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e148-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e148-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchesAmong : CIM_ForwardsAmong
{
  CIM_SwitchPort    REF Antecedent;
  CIM_SwitchService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6e148-106">Member</span><span class="sxs-lookup"><span data-stu-id="6e148-106">Members</span></span>

<span data-ttu-id="6e148-107">Die **CIM \_ Switchesin** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6e148-107">The **CIM\_SwitchesAmong** class has these types of members:</span></span>

-   [<span data-ttu-id="6e148-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e148-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e148-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e148-109">Properties</span></span>

<span data-ttu-id="6e148-110">Die **CIM \_ Switchesin** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6e148-110">The **CIM\_SwitchesAmong** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e148-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="6e148-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e148-112">Datentyp: **CIM \_ Switchport**</span><span class="sxs-lookup"><span data-stu-id="6e148-112">Data type: **CIM\_SwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="6e148-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e148-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e148-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="6e148-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6e148-115">Ein [**CIM- \_ switchportverweis auf den Switchport**](cim-switchport.md) .</span><span class="sxs-lookup"><span data-stu-id="6e148-115">A [**CIM\_SwitchPort**](cim-switchport.md) reference to the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="6e148-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="6e148-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e148-117">Datentyp: **CIM \_ switchservice**</span><span class="sxs-lookup"><span data-stu-id="6e148-117">Data type: **CIM\_SwitchService**</span></span>
</dt> <dt>

<span data-ttu-id="6e148-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e148-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e148-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6e148-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6e148-120">Ein [**CIM \_ switchservice**](cim-switchservice.md) -Verweis auf den Wechseldienst.</span><span class="sxs-lookup"><span data-stu-id="6e148-120">A [**CIM\_SwitchService**](cim-switchservice.md) reference to the switching service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e148-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e148-121">Requirements</span></span>



| <span data-ttu-id="6e148-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e148-122">Requirement</span></span> | <span data-ttu-id="6e148-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6e148-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e148-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e148-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6e148-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6e148-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6e148-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e148-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6e148-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6e148-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6e148-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e148-128">Namespace</span></span><br/>                | <span data-ttu-id="6e148-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6e148-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6e148-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6e148-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e148-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6e148-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e148-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6e148-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e148-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6e148-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6e148-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e148-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e148-135">**CIM \_ forwardsamong**</span><span class="sxs-lookup"><span data-stu-id="6e148-135">**CIM\_ForwardsAmong**</span></span>](cim-forwardsamong.md)
</dt> </dl>

 

