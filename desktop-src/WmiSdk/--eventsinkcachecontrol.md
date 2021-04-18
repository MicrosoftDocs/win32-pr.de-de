---
description: Wird verwendet, um zu bestimmen, wann WMI einen Ereignisconsumeranbieter iwbemunboundobjectsink-Zeiger freigibt.
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: __EventSinkCacheControl-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventSinkCacheControl
- Root.__EventSinkCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 9d20e64fed1ee6ba5622d5e6a342a60485f53d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352298"
---
# <a name="__eventsinkcachecontrol-class"></a><span data-ttu-id="5034a-103">\_\_EventSink Cache econtrol-Klasse</span><span class="sxs-lookup"><span data-stu-id="5034a-103">\_\_EventSinkCacheControl class</span></span>

<span data-ttu-id="5034a-104">Die **\_ \_ EventSink Cache econtrol** -System Klasse wird verwendet, um zu bestimmen, wann WMI den [**iwbemunboundobjectsink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) -Zeiger eines Ereignis Verbraucher Anbieters freigibt.</span><span class="sxs-lookup"><span data-stu-id="5034a-104">The **\_\_EventSinkCacheControl** system class is used to determine when WMI releases an event consumer provider's [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) pointer.</span></span> <span data-ttu-id="5034a-105">Die **\_ \_ EventSink Cache econtrol** -Klasse ist eine Singleton-Klasse.</span><span class="sxs-lookup"><span data-stu-id="5034a-105">The **\_\_EventSinkCacheControl** class is a singleton class.</span></span> <span data-ttu-id="5034a-106">Sie befindet sich nur im \\ Root-Namespace.</span><span class="sxs-lookup"><span data-stu-id="5034a-106">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="5034a-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="5034a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5034a-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5034a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5034a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5034a-109">Syntax</span></span>

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="5034a-110">Member</span><span class="sxs-lookup"><span data-stu-id="5034a-110">Members</span></span>

<span data-ttu-id="5034a-111">Die **\_ \_ EventSink Cache econtrol** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5034a-111">The **\_\_EventSinkCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="5034a-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5034a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5034a-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5034a-113">Properties</span></span>

<span data-ttu-id="5034a-114">Die **\_ \_ EventSink Cache econtrol** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5034a-114">The **\_\_EventSinkCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5034a-115">**Clearafter**</span><span class="sxs-lookup"><span data-stu-id="5034a-115">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5034a-116">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="5034a-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5034a-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5034a-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5034a-118">Das Zeitintervall, nach dem WMI einen Ereignis Anbieter freigibt.</span><span class="sxs-lookup"><span data-stu-id="5034a-118">Time interval after which WMI releases an event provider.</span></span> <span data-ttu-id="5034a-119">Es kann bis zu einem doppelten Intervall dauern, bis der Anbieter entladen wurde.</span><span class="sxs-lookup"><span data-stu-id="5034a-119">It can take up to twice the interval specified to unload the provider.</span></span> <span data-ttu-id="5034a-120">Die Uhrzeit liegt im [Intervall Format](interval-format.md)vor.</span><span class="sxs-lookup"><span data-stu-id="5034a-120">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5034a-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5034a-121">Remarks</span></span>

<span data-ttu-id="5034a-122">Die **\_ \_ EventSink Cache econtrol** -Klasse ist von [**\_ \_ CacheControl**](--cachecontrol.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5034a-122">The **\_\_EventSinkCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="5034a-123">Weitere Informationen zum Verwenden dieser Klasse finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5034a-123">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5034a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5034a-124">Requirements</span></span>



| <span data-ttu-id="5034a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5034a-125">Requirement</span></span> | <span data-ttu-id="5034a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5034a-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5034a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5034a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5034a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5034a-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5034a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5034a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5034a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5034a-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5034a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="5034a-131">Namespace</span></span><br/>                | <span data-ttu-id="5034a-132">Root</span><span class="sxs-lookup"><span data-stu-id="5034a-132">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="5034a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5034a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5034a-134">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="5034a-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




