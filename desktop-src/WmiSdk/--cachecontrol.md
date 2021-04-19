---
description: Class ist die abstrakte Basisklasse für Klassen, mit denen bestimmt wird, wann WMI ein Component Object Model (com)-Objekt freigeben soll.
ms.assetid: 32631610-8c0e-4f04-b0b2-62e5f8e23ef4
ms.tgt_platform: multiple
title: __CacheControl-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CacheControl
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: fe5358630a7ac5eb48751135d39c2fd998196bf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373132"
---
# <a name="__cachecontrol-class"></a><span data-ttu-id="29f3a-103">\_\_CacheControl-Klasse</span><span class="sxs-lookup"><span data-stu-id="29f3a-103">\_\_CacheControl class</span></span>

<span data-ttu-id="29f3a-104">Die **\_ \_ CacheControl** -System Klasse ist die abstrakte Basisklasse für Klassen, mit denen bestimmt wird, wann WMI ein Component Object Model (com)-Objekt freigeben soll.</span><span class="sxs-lookup"><span data-stu-id="29f3a-104">The **\_\_CacheControl** system class is the abstract base class for classes that are used to determine when WMI should release a Component Object Model (COM) object.</span></span> <span data-ttu-id="29f3a-105">Instanzen dieser Klasse werden nie erstellt.</span><span class="sxs-lookup"><span data-stu-id="29f3a-105">Instances of this class are never created.</span></span> <span data-ttu-id="29f3a-106">Die **\_ \_ CacheControl** -Klasse befindet sich nur im Root-Namespace.</span><span class="sxs-lookup"><span data-stu-id="29f3a-106">The **\_\_CacheControl** class is located only in the root namespace.</span></span> <span data-ttu-id="29f3a-107">Weitere Informationen zum Verwenden dieser Klasse finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="29f3a-107">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

<span data-ttu-id="29f3a-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="29f3a-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="29f3a-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="29f3a-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="29f3a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="29f3a-110">Syntax</span></span>

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a><span data-ttu-id="29f3a-111">Member</span><span class="sxs-lookup"><span data-stu-id="29f3a-111">Members</span></span>

<span data-ttu-id="29f3a-112">Die **\_ \_ CacheControl** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="29f3a-112">The **\_\_CacheControl** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="29f3a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29f3a-113">Remarks</span></span>

<span data-ttu-id="29f3a-114">Die **\_ \_ CacheControl** -Klasse wird von [**\_ \_ systemclass**](--systemclass.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="29f3a-114">The **\_\_CacheControl** class is derived from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29f3a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29f3a-115">Requirements</span></span>



| <span data-ttu-id="29f3a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29f3a-116">Requirement</span></span> | <span data-ttu-id="29f3a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="29f3a-117">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="29f3a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29f3a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="29f3a-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29f3a-119">Windows Vista</span></span><br/>       |
| <span data-ttu-id="29f3a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29f3a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="29f3a-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29f3a-121">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="29f3a-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="29f3a-122">Namespace</span></span><br/>                | <span data-ttu-id="29f3a-123">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="29f3a-123">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="29f3a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29f3a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29f3a-125">**\_\_System Class**</span><span class="sxs-lookup"><span data-stu-id="29f3a-125">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="29f3a-126">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="29f3a-126">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="29f3a-127">**\_\_Eventconsumerprovidercachecontrol**</span><span class="sxs-lookup"><span data-stu-id="29f3a-127">**\_\_EventConsumerProviderCacheControl**</span></span>](--eventconsumerprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="29f3a-128">**\_\_Eventprovidercachecontrol**</span><span class="sxs-lookup"><span data-stu-id="29f3a-128">**\_\_EventProviderCacheControl**</span></span>](--eventprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="29f3a-129">**\_\_EventSink Cache econtrol**</span><span class="sxs-lookup"><span data-stu-id="29f3a-129">**\_\_EventSinkCacheControl**</span></span>](--eventsinkcachecontrol.md)
</dt> <dt>

[<span data-ttu-id="29f3a-130">**\_\_Objectprovidercachecontrol**</span><span class="sxs-lookup"><span data-stu-id="29f3a-130">**\_\_ObjectProviderCacheControl**</span></span>](--objectprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="29f3a-131">\_\_Propertyprovidercachecontrol</span><span class="sxs-lookup"><span data-stu-id="29f3a-131">\_\_PropertyProviderCacheControl</span></span>](--propertyprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="29f3a-132">Entladen eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="29f3a-132">Unloading a Provider</span></span>](unloading-a-provider.md)
</dt> </dl>

 

