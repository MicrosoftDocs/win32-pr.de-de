---
description: Stellt ein Aggregat Ereignis aus mehreren einzelnen systeminternen oder extrinsischen Ereignissen dar.
ms.assetid: 99afa390-01fe-4a13-ba21-27587470f111
ms.tgt_platform: multiple
title: __AggregateEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AggregateEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f93a962e57452ac555214e42f00af8ac8a4ea3db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349652"
---
# <a name="__aggregateevent-class"></a><span data-ttu-id="4d9ac-103">\_\_Aggregateevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="4d9ac-103">\_\_AggregateEvent class</span></span>

<span data-ttu-id="4d9ac-104">Die **\_ \_ aggregateevent** -System Klasse stellt ein Aggregat Ereignis aus mehreren einzelnen systeminternen oder extrinsischen Ereignissen dar.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-104">The **\_\_AggregateEvent** system class represents an aggregate event of several individual intrinsic or extrinsic events.</span></span> <span data-ttu-id="4d9ac-105">WMI generiert eine Instanz von **\_ \_ aggregateevent** anstelle eines [**\_ \_ Ereignisses**](--event.md) , wenn sich Consumer bei der [Group within](group-clause.md) -Klausel in der Ereignis Abfrage registrieren.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-105">WMI generates an instance of **\_\_AggregateEvent** rather than [**\_\_Event**](--event.md) when consumers register with the [GROUP WITHIN](group-clause.md) clause in their event query.</span></span>

<span data-ttu-id="4d9ac-106">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4d9ac-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d9ac-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d9ac-108">Syntax</span></span>

``` syntax
class __AggregateEvent : __IndicationRelated
{
  uint32 NumberOfEvents;
  object Representative;
};
```

## <a name="members"></a><span data-ttu-id="4d9ac-109">Member</span><span class="sxs-lookup"><span data-stu-id="4d9ac-109">Members</span></span>

<span data-ttu-id="4d9ac-110">Die **\_ \_ aggregateevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4d9ac-110">The **\_\_AggregateEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="4d9ac-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d9ac-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d9ac-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d9ac-112">Properties</span></span>

<span data-ttu-id="4d9ac-113">Die **\_ \_ aggregateevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-113">The **\_\_AggregateEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d9ac-114">**NumberOfEvents**</span><span class="sxs-lookup"><span data-stu-id="4d9ac-114">**NumberOfEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d9ac-115">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d9ac-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d9ac-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d9ac-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d9ac-117">Anzahl der Ereignisse kombiniert, um dieses einzelne Zusammenfassungs Ereignis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-117">Number of events combined to produce this single summary event.</span></span>

</dd> <dt>

<span data-ttu-id="4d9ac-118">**Representative**</span><span class="sxs-lookup"><span data-stu-id="4d9ac-118">**Representative**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d9ac-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="4d9ac-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="4d9ac-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4d9ac-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d9ac-121">Kopie eines der Ereignisse, die innerhalb des Aggregations Intervalls übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-121">Copy of one of the events delivered within the aggregation interval.</span></span> <span data-ttu-id="4d9ac-122">Wenn ein Consumer z. b. für Registrierungsschlüssel-Änderungs Ereignisse vom Registrierungs Ereignis Anbieter registriert ist, würde der **repräsentative** eine Instanz der **RegistryKeyChangeEvent** -Klasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-122">For example, if a consumer has registered for registry key change events from the Registry Event provider, **Representative** would hold an instance of the **RegistryKeyChangeEvent** class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d9ac-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d9ac-123">Remarks</span></span>

<span data-ttu-id="4d9ac-124">Die **\_ \_ aggregateevent** -Klasse wird von " [**\_ \_ indicationrelated**](--indicationrelated.md)" abgeleitet, die keine Eigenschaften hat.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-124">The **\_\_AggregateEvent** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

<span data-ttu-id="4d9ac-125">Ereignis Anbieter generieren niemals Aggregat Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-125">Event providers never generate aggregate events.</span></span> <span data-ttu-id="4d9ac-126">Die Group within-Klausel muss bei der Verarbeitung von Ereignis Abfragen ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="4d9ac-126">They must ignore the GROUP WITHIN clause in their processing of event queries.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d9ac-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d9ac-127">Requirements</span></span>



| <span data-ttu-id="4d9ac-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d9ac-128">Requirement</span></span> | <span data-ttu-id="4d9ac-129">Wert</span><span class="sxs-lookup"><span data-stu-id="4d9ac-129">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4d9ac-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d9ac-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4d9ac-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d9ac-131">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4d9ac-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d9ac-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4d9ac-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d9ac-133">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4d9ac-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="4d9ac-134">Namespace</span></span><br/>                | <span data-ttu-id="4d9ac-135">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="4d9ac-135">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4d9ac-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d9ac-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d9ac-137">**\_\_Indicationrelated**</span><span class="sxs-lookup"><span data-stu-id="4d9ac-137">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="4d9ac-138">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="4d9ac-138">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="4d9ac-139">Abfragen mit WQL</span><span class="sxs-lookup"><span data-stu-id="4d9ac-139">Querying with WQL</span></span>](querying-with-wql.md)
</dt> </dl>

 

