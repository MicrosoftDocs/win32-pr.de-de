---
description: 'SystemConfig_V0-Klasse: Diese Klasse ist die übergeordnete Klasse für Hardwarekonfigurationsereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
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
ms.openlocfilehash: 24f0c579f4fb9c947ea02ff677cd433da3103cfc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105908"
---
# <a name="systemconfig_v0-class"></a><span data-ttu-id="88b83-104">SystemConfig \_ V0-Klasse</span><span class="sxs-lookup"><span data-stu-id="88b83-104">SystemConfig\_V0 class</span></span>

<span data-ttu-id="88b83-105">Diese Klasse ist die übergeordnete Klasse für Hardwarekonfigurationsereignisse.</span><span class="sxs-lookup"><span data-stu-id="88b83-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="88b83-106">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="88b83-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="88b83-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="88b83-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(0)]
class SystemConfig_V0 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="88b83-108">Member</span><span class="sxs-lookup"><span data-stu-id="88b83-108">Members</span></span>

<span data-ttu-id="88b83-109">Die **SystemConfig \_ V0-Klasse** definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="88b83-109">The **SystemConfig\_V0** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="88b83-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88b83-110">Remarks</span></span>

<span data-ttu-id="88b83-111">Informationen zu Hardwarekonfigurationsereignissen unter Windows XP finden Sie in der [**HWConfig-Klasse.**](hwconfig.md)</span><span class="sxs-lookup"><span data-stu-id="88b83-111">For hardware configuration events on Windows XP, see the [**HWConfig**](hwconfig.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="88b83-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88b83-112">Requirements</span></span>



| <span data-ttu-id="88b83-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88b83-113">Requirement</span></span> | <span data-ttu-id="88b83-114">Wert</span><span class="sxs-lookup"><span data-stu-id="88b83-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="88b83-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88b83-115">Minimum supported client</span></span><br/> | <span data-ttu-id="88b83-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="88b83-116">None supported</span></span><br/>                            |
| <span data-ttu-id="88b83-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88b83-117">Minimum supported server</span></span><br/> | <span data-ttu-id="88b83-118">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88b83-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88b83-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="88b83-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88b83-120">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="88b83-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="88b83-121">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="88b83-121">**SystemConfig**</span></span>](systemconfig.md)
</dt> <dt>

[<span data-ttu-id="88b83-122">**SystemConfig \_ V0 \_ CPU**</span><span class="sxs-lookup"><span data-stu-id="88b83-122">**SystemConfig\_V0\_CPU**</span></span>](systemconfig-v0-cpu.md)
</dt> <dt>

[<span data-ttu-id="88b83-123">**SystemConfig \_ V0 \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="88b83-123">**SystemConfig\_V0\_LogDisk**</span></span>](systemconfig-v0-logdisk.md)
</dt> <dt>

[<span data-ttu-id="88b83-124">**SystemConfig \_ \_ V0-NIC**</span><span class="sxs-lookup"><span data-stu-id="88b83-124">**SystemConfig\_V0\_NIC**</span></span>](systemconfig-v0-nic.md)
</dt> <dt>

[<span data-ttu-id="88b83-125">**SystemConfig \_ V0 \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="88b83-125">**SystemConfig\_V0\_PhyDisk**</span></span>](systemconfig-v0-phydisk.md)
</dt> <dt>

[<span data-ttu-id="88b83-126">**SystemConfig \_ V0 \_ Power**</span><span class="sxs-lookup"><span data-stu-id="88b83-126">**SystemConfig\_V0\_Power**</span></span>](systemconfig-v0-power.md)
</dt> <dt>

[<span data-ttu-id="88b83-127">**SystemConfig \_ \_ V0-Dienste**</span><span class="sxs-lookup"><span data-stu-id="88b83-127">**SystemConfig\_V0\_Services**</span></span>](systemconfig-v0-services.md)
</dt> <dt>

[<span data-ttu-id="88b83-128">**\_ \_ SystemConfig V0-Video**</span><span class="sxs-lookup"><span data-stu-id="88b83-128">**SystemConfig\_V0\_Video**</span></span>](systemconfig-v0-video.md)
</dt> </dl>

 

 




