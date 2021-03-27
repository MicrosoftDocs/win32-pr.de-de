---
description: Diese Klasse ist die übergeordnete Klasse für Hardware Konfigurations Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 9da1a7ec-89b5-462b-a336-544e4b7adf96
title: SystemConfig_V0-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0
api_type:
- NA
api_location: ''
ms.openlocfilehash: 92d77d1ad3effdd2bf22a7df8112187b27666238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864251"
---
# <a name="systemconfig_v0-class"></a><span data-ttu-id="188dc-104">SystemConfig \_ v0-Klasse</span><span class="sxs-lookup"><span data-stu-id="188dc-104">SystemConfig\_V0 class</span></span>

<span data-ttu-id="188dc-105">Diese Klasse ist die übergeordnete Klasse für Hardware Konfigurations Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="188dc-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="188dc-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="188dc-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="188dc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="188dc-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(0)]
class SystemConfig_V0 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="188dc-108">Member</span><span class="sxs-lookup"><span data-stu-id="188dc-108">Members</span></span>

<span data-ttu-id="188dc-109">Die Klasse " **SystemConfig \_ v0** " definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="188dc-109">The **SystemConfig\_V0** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="188dc-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="188dc-110">Remarks</span></span>

<span data-ttu-id="188dc-111">Informationen zu Hardware Konfigurations Ereignissen unter Windows XP finden Sie in der [**hwconfig**](hwconfig.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="188dc-111">For hardware configuration events on Windows XP, see the [**HWConfig**](hwconfig.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="188dc-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="188dc-112">Requirements</span></span>



| <span data-ttu-id="188dc-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="188dc-113">Requirement</span></span> | <span data-ttu-id="188dc-114">Wert</span><span class="sxs-lookup"><span data-stu-id="188dc-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="188dc-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="188dc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="188dc-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="188dc-116">None supported</span></span><br/>                            |
| <span data-ttu-id="188dc-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="188dc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="188dc-118">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="188dc-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="188dc-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="188dc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="188dc-120">**MSNT \_ systemtrace**</span><span class="sxs-lookup"><span data-stu-id="188dc-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="188dc-121">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="188dc-121">**SystemConfig**</span></span>](systemconfig.md)
</dt> <dt>

[<span data-ttu-id="188dc-122">**SystemConfig \_ v0- \_ CPU**</span><span class="sxs-lookup"><span data-stu-id="188dc-122">**SystemConfig\_V0\_CPU**</span></span>](systemconfig-v0-cpu.md)
</dt> <dt>

[<span data-ttu-id="188dc-123">**SystemConfig \_ v0- \_ logdisk**</span><span class="sxs-lookup"><span data-stu-id="188dc-123">**SystemConfig\_V0\_LogDisk**</span></span>](systemconfig-v0-logdisk.md)
</dt> <dt>

[<span data-ttu-id="188dc-124">**SystemConfig \_ v0- \_ NIC**</span><span class="sxs-lookup"><span data-stu-id="188dc-124">**SystemConfig\_V0\_NIC**</span></span>](systemconfig-v0-nic.md)
</dt> <dt>

[<span data-ttu-id="188dc-125">**SystemConfig \_ v0- \_ phydisk**</span><span class="sxs-lookup"><span data-stu-id="188dc-125">**SystemConfig\_V0\_PhyDisk**</span></span>](systemconfig-v0-phydisk.md)
</dt> <dt>

[<span data-ttu-id="188dc-126">**SystemConfig \_ v0- \_ Strom**</span><span class="sxs-lookup"><span data-stu-id="188dc-126">**SystemConfig\_V0\_Power**</span></span>](systemconfig-v0-power.md)
</dt> <dt>

[<span data-ttu-id="188dc-127">**SystemConfig \_ v0- \_ Dienste**</span><span class="sxs-lookup"><span data-stu-id="188dc-127">**SystemConfig\_V0\_Services**</span></span>](systemconfig-v0-services.md)
</dt> <dt>

[<span data-ttu-id="188dc-128">**System config \_ v0- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="188dc-128">**SystemConfig\_V0\_Video**</span></span>](systemconfig-v0-video.md)
</dt> </dl>

 

 




