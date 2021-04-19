---
description: Steuert, wann ein Klassen-oder Instanzanbieter entladen wird.
ms.assetid: 4cbeb820-8a65-4fab-97f1-2a973b2a4310
ms.tgt_platform: multiple
title: __ObjectProviderCacheControl-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderCacheControl
- Root.__ObjectProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 53cfaa69afead4f436879f128a4d42e50d36fe67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350098"
---
# <a name="__objectprovidercachecontrol-class"></a><span data-ttu-id="64d8c-103">\_\_Objectprovidercachecontrol-Klasse</span><span class="sxs-lookup"><span data-stu-id="64d8c-103">\_\_ObjectProviderCacheControl class</span></span>

<span data-ttu-id="64d8c-104">Die System Klasse **\_ \_ objectprovidercachecontrol** steuert, wann ein Klassen-oder Instanzanbieter entladen wird.</span><span class="sxs-lookup"><span data-stu-id="64d8c-104">The **\_\_ObjectProviderCacheControl** system class controls when a class or instance provider is unloaded.</span></span> <span data-ttu-id="64d8c-105">Sie befindet sich nur im \\ Root-Namespace.</span><span class="sxs-lookup"><span data-stu-id="64d8c-105">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="64d8c-106">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="64d8c-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="64d8c-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="64d8c-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="64d8c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="64d8c-108">Syntax</span></span>

``` syntax
[singleton]
class __ObjectProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="64d8c-109">Member</span><span class="sxs-lookup"><span data-stu-id="64d8c-109">Members</span></span>

<span data-ttu-id="64d8c-110">Die **\_ \_ objectprovidercachecontrol** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="64d8c-110">The **\_\_ObjectProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="64d8c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="64d8c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64d8c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="64d8c-112">Properties</span></span>

<span data-ttu-id="64d8c-113">Die **\_ \_ objectprovidercachecontrol** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="64d8c-113">The **\_\_ObjectProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64d8c-114">**Clearafter**</span><span class="sxs-lookup"><span data-stu-id="64d8c-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64d8c-115">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="64d8c-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="64d8c-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="64d8c-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="64d8c-117">Das Zeitintervall, nach dem WMI eine Instanz, Klasse oder einen Methoden Anbieter freigibt.</span><span class="sxs-lookup"><span data-stu-id="64d8c-117">Time interval after which WMI releases an instance, class, or method provider.</span></span> <span data-ttu-id="64d8c-118">Die Uhrzeit liegt im [Intervall Format](interval-format.md)vor.</span><span class="sxs-lookup"><span data-stu-id="64d8c-118">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64d8c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64d8c-119">Remarks</span></span>

<span data-ttu-id="64d8c-120">Die **\_ \_ objectprovidercachecontrol** -Klasse ist von [**\_ \_ CacheControl**](--cachecontrol.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="64d8c-120">The **\_\_ObjectProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="64d8c-121">Weitere Informationen zum Verwenden dieser Klasse finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="64d8c-121">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64d8c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64d8c-122">Requirements</span></span>



| <span data-ttu-id="64d8c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64d8c-123">Requirement</span></span> | <span data-ttu-id="64d8c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="64d8c-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="64d8c-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64d8c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="64d8c-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64d8c-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="64d8c-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64d8c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="64d8c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64d8c-128">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="64d8c-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="64d8c-129">Namespace</span></span><br/>                | <span data-ttu-id="64d8c-130">Root</span><span class="sxs-lookup"><span data-stu-id="64d8c-130">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="64d8c-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64d8c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d8c-132">**\_\_CacheControl**</span><span class="sxs-lookup"><span data-stu-id="64d8c-132">**\_\_CacheControl**</span></span>](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[<span data-ttu-id="64d8c-133">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="64d8c-133">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="64d8c-134">Empfangen von Ereignissen zu allen Zeitpunkten</span><span class="sxs-lookup"><span data-stu-id="64d8c-134">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

