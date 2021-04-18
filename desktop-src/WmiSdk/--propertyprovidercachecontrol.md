---
description: Steuert den Cache, wenn ein Eigenschaften Anbieter entladen wird.
ms.assetid: 8fc7de7a-889c-4d53-97ea-a676879de1d3
ms.tgt_platform: multiple
title: __PropertyProviderCacheControl-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderCacheControl
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d153049a9635b4b77a1ad09ca0ee64835b9bcfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216324"
---
# <a name="__propertyprovidercachecontrol-class"></a><span data-ttu-id="c0b6d-103">\_\_Propertyprovidercachecontrol-Klasse</span><span class="sxs-lookup"><span data-stu-id="c0b6d-103">\_\_PropertyProviderCacheControl class</span></span>

<span data-ttu-id="c0b6d-104">Die **\_ \_ propertyprovidercachecontrol** -Klasse steuert den Cache, wenn ein Eigenschaften Anbieter entladen wird.</span><span class="sxs-lookup"><span data-stu-id="c0b6d-104">The **\_\_PropertyProviderCacheControl** class controls the cache when a property provider is unloaded.</span></span> <span data-ttu-id="c0b6d-105">Diese Klasse ist nur im \\ Root-Namespace vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c0b6d-105">This class exists only in the \\root namespace.</span></span>

<span data-ttu-id="c0b6d-106">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c0b6d-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c0b6d-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c0b6d-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b6d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0b6d-108">Syntax</span></span>

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="c0b6d-109">Member</span><span class="sxs-lookup"><span data-stu-id="c0b6d-109">Members</span></span>

<span data-ttu-id="c0b6d-110">Die **\_ \_ propertyprovidercachecontrol** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c0b6d-110">The **\_\_PropertyProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="c0b6d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0b6d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0b6d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0b6d-112">Properties</span></span>

<span data-ttu-id="c0b6d-113">Die **\_ \_ propertyprovidercachecontrol** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c0b6d-113">The **\_\_PropertyProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0b6d-114">**Clearafter**</span><span class="sxs-lookup"><span data-stu-id="c0b6d-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0b6d-115">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c0b6d-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c0b6d-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c0b6d-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c0b6d-117">Das Zeitintervall nach der Freigabe eines Eigenschaften Anbieters durch WMI.</span><span class="sxs-lookup"><span data-stu-id="c0b6d-117">Time interval after WMI releases a property provider.</span></span> <span data-ttu-id="c0b6d-118">Die Uhrzeit liegt im Intervall Format vor.</span><span class="sxs-lookup"><span data-stu-id="c0b6d-118">The time is in the interval format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0b6d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0b6d-119">Remarks</span></span>

<span data-ttu-id="c0b6d-120">Die **\_ \_ propertyprovidercachecontrol** -Klasse wird von [**\_ \_ CacheControl**](--cachecontrol.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c0b6d-120">The **\_\_PropertyProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="c0b6d-121">Weitere Informationen finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c0b6d-121">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b6d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0b6d-122">Requirements</span></span>



| <span data-ttu-id="c0b6d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0b6d-123">Requirement</span></span> | <span data-ttu-id="c0b6d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c0b6d-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c0b6d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0b6d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c0b6d-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0b6d-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c0b6d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0b6d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c0b6d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0b6d-128">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c0b6d-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0b6d-129">Namespace</span></span><br/>                | <span data-ttu-id="c0b6d-130">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="c0b6d-130">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c0b6d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0b6d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b6d-132">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="c0b6d-132">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




