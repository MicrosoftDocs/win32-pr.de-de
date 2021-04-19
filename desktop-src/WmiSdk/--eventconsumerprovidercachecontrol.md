---
description: Bestimmt, wann WMI einen Ereignisconsumeranbieter freigeben soll.
ms.assetid: 93246826-8070-4e05-96f0-f773041ed1d4
ms.tgt_platform: multiple
title: __EventConsumerProviderCacheControl-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderCacheControl
- Root.__EventConsumerProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: f769427c77f6efdf9a521a63f7334d5d27416c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373365"
---
# <a name="__eventconsumerprovidercachecontrol-class"></a><span data-ttu-id="d019e-103">\_\_Eventconsumerprovidercachecontrol-Klasse</span><span class="sxs-lookup"><span data-stu-id="d019e-103">\_\_EventConsumerProviderCacheControl class</span></span>

<span data-ttu-id="d019e-104">Die **\_ \_ eventconsumerprovidercachecontrol** -System Klasse bestimmt, wann WMI einen Ereignisconsumeranbieter freigeben soll.</span><span class="sxs-lookup"><span data-stu-id="d019e-104">The **\_\_EventConsumerProviderCacheControl** system class determines when WMI should release an event consumer provider.</span></span> <span data-ttu-id="d019e-105">Die **\_ \_ eventconsumerprovidercachecontrol** -Klasse ist eine Singleton-Klasse.</span><span class="sxs-lookup"><span data-stu-id="d019e-105">The **\_\_EventConsumerProviderCacheControl** class is a singleton class.</span></span> <span data-ttu-id="d019e-106">Sie befindet sich nur im \\ Root-Namespace.</span><span class="sxs-lookup"><span data-stu-id="d019e-106">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="d019e-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d019e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d019e-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d019e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d019e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d019e-109">Syntax</span></span>

``` syntax
[singleton]
class __EventConsumerProviderCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="d019e-110">Member</span><span class="sxs-lookup"><span data-stu-id="d019e-110">Members</span></span>

<span data-ttu-id="d019e-111">Die **\_ \_ eventconsumerprovidercachecontrol** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d019e-111">The **\_\_EventConsumerProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="d019e-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d019e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d019e-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d019e-113">Properties</span></span>

<span data-ttu-id="d019e-114">Die **\_ \_ eventconsumerprovidercachecontrol** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d019e-114">The **\_\_EventConsumerProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d019e-115">**Clearafter**</span><span class="sxs-lookup"><span data-stu-id="d019e-115">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d019e-116">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d019e-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d019e-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d019e-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d019e-118">Das Zeitintervall, nach dem WMI einen Ereignisconsumeranbieter freigibt.</span><span class="sxs-lookup"><span data-stu-id="d019e-118">Time interval after which WMI releases an event consumer provider.</span></span> <span data-ttu-id="d019e-119">Es kann bis zu einem doppelten Intervall dauern, bis der Anbieter entladen wurde.</span><span class="sxs-lookup"><span data-stu-id="d019e-119">It may take up to twice the interval specified to unload the provider.</span></span> <span data-ttu-id="d019e-120">Die Uhrzeit liegt im [Intervall Format](interval-format.md)vor.</span><span class="sxs-lookup"><span data-stu-id="d019e-120">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d019e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d019e-121">Remarks</span></span>

<span data-ttu-id="d019e-122">Die **\_ \_ eventconsumerprovidercachecontrol** -Klasse ist von [**\_ \_ CacheControl**](--cachecontrol.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d019e-122">The **\_\_EventConsumerProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="d019e-123">Weitere Informationen zum Verwenden dieser Klasse finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d019e-123">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d019e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d019e-124">Requirements</span></span>



| <span data-ttu-id="d019e-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d019e-125">Requirement</span></span> | <span data-ttu-id="d019e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d019e-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d019e-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d019e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d019e-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d019e-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d019e-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d019e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d019e-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d019e-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d019e-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="d019e-131">Namespace</span></span><br/>                | <span data-ttu-id="d019e-132">Root</span><span class="sxs-lookup"><span data-stu-id="d019e-132">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="d019e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d019e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d019e-134">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="d019e-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




