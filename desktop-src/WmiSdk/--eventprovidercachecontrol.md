---
description: Steuert, wann ein Ereignis Anbieter entladen wird.
ms.assetid: 7f11e521-d0f6-4c3c-8bfe-ceed2d106ed3
ms.tgt_platform: multiple
title: __EventProviderCacheControl-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderCacheControl
- Root.__EventProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: c54ec47b1f67d96816cf24a6b6e0108ee0b1de70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216904"
---
# <a name="__eventprovidercachecontrol-class"></a><span data-ttu-id="0576f-103">\_\_Eventprovidercachecontrol-Klasse</span><span class="sxs-lookup"><span data-stu-id="0576f-103">\_\_EventProviderCacheControl class</span></span>

<span data-ttu-id="0576f-104">Die **\_ \_ eventprovidercachecontrol** -System Klasse steuert, wann ein Ereignis Anbieter entladen wird.</span><span class="sxs-lookup"><span data-stu-id="0576f-104">The **\_\_EventProviderCacheControl** system class controls when an event provider is unloaded.</span></span> <span data-ttu-id="0576f-105">Sie befindet sich nur im \\ Root-Namespace.</span><span class="sxs-lookup"><span data-stu-id="0576f-105">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="0576f-106">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0576f-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0576f-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0576f-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0576f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0576f-108">Syntax</span></span>

``` syntax
[singleton]
class __EventProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="0576f-109">Member</span><span class="sxs-lookup"><span data-stu-id="0576f-109">Members</span></span>

<span data-ttu-id="0576f-110">Die **\_ \_ eventprovidercachecontrol** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0576f-110">The **\_\_EventProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="0576f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0576f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0576f-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0576f-112">Properties</span></span>

<span data-ttu-id="0576f-113">Die **\_ \_ eventprovidercachecontrol** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0576f-113">The **\_\_EventProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0576f-114">**Clearafter**</span><span class="sxs-lookup"><span data-stu-id="0576f-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0576f-115">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0576f-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0576f-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0576f-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0576f-117">Das Zeitintervall, nach dem Windows-Verwaltungsinstrumentation (WMI) einen Ereignis Anbieter freigibt.</span><span class="sxs-lookup"><span data-stu-id="0576f-117">Time interval after Windows Management Instrumentation (WMI) releases an event provider.</span></span> <span data-ttu-id="0576f-118">Die Uhrzeit liegt im [Intervall Format](interval-format.md)vor.</span><span class="sxs-lookup"><span data-stu-id="0576f-118">The time is in [interval format](interval-format.md).</span></span> <span data-ttu-id="0576f-119">Es kann bis zu einem doppelten Intervall dauern, bis der Anbieter entladen wurde.</span><span class="sxs-lookup"><span data-stu-id="0576f-119">It may take up to twice the interval specified to unload the provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0576f-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0576f-120">Remarks</span></span>

<span data-ttu-id="0576f-121">Die **\_ \_ eventprovidercachecontrol** -Klasse ist von [**\_ \_ CacheControl**](--cachecontrol.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0576f-121">The **\_\_EventProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span>

<span data-ttu-id="0576f-122">Weitere Informationen zum Verwenden dieser Klasse finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0576f-122">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0576f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0576f-123">Requirements</span></span>



| <span data-ttu-id="0576f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0576f-124">Requirement</span></span> | <span data-ttu-id="0576f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="0576f-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0576f-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0576f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0576f-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0576f-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0576f-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0576f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0576f-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0576f-129">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="0576f-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="0576f-130">Namespace</span></span><br/>                | <span data-ttu-id="0576f-131">Root</span><span class="sxs-lookup"><span data-stu-id="0576f-131">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="0576f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0576f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0576f-133">**\_\_CacheControl**</span><span class="sxs-lookup"><span data-stu-id="0576f-133">**\_\_CacheControl**</span></span>](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[<span data-ttu-id="0576f-134">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="0576f-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

