---
description: Stellt das Vorkommen eines Ereignisses dar, das gelöscht wird. Ein gelöschter Ereignis ist ein Ereignis, das nicht an einen Ereignisconsumer übermittelt wird.
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: __EventDroppedEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventDroppedEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4e9f68328a3c5c455c98e85a65d53156da6eeada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363639"
---
# <a name="__eventdroppedevent-class"></a><span data-ttu-id="e4f9b-104">\_\_Eventdroppedevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="e4f9b-104">\_\_EventDroppedEvent class</span></span>

<span data-ttu-id="e4f9b-105">Die **\_ \_ eventdroppedevent** -System Klasse stellt das Vorkommen eines gelöschten Ereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-105">The **\_\_EventDroppedEvent** system class represents the occurrence of an event that is dropped.</span></span> <span data-ttu-id="e4f9b-106">Ein gelöschter Ereignis ist ein Ereignis, das nicht an einen Ereignisconsumer übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-106">A dropped event is an event that is not delivered to an event consumer.</span></span>

<span data-ttu-id="e4f9b-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e4f9b-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4f9b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4f9b-109">Syntax</span></span>

``` syntax
class __EventDroppedEvent : __SystemEvent
{
  __Event             Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="e4f9b-110">Member</span><span class="sxs-lookup"><span data-stu-id="e4f9b-110">Members</span></span>

<span data-ttu-id="e4f9b-111">Die **\_ \_ eventdroppedevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e4f9b-111">The **\_\_EventDroppedEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="e4f9b-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4f9b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4f9b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4f9b-113">Properties</span></span>

<span data-ttu-id="e4f9b-114">Die **\_ \_ eventdroppedevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-114">The **\_\_EventDroppedEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4f9b-115">**Event**</span><span class="sxs-lookup"><span data-stu-id="e4f9b-115">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4f9b-116">Datentyp: **\_ \_ Ereignis**</span><span class="sxs-lookup"><span data-stu-id="e4f9b-116">Data type: **\_\_Event**</span></span>
</dt> <dt>

<span data-ttu-id="e4f9b-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e4f9b-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4f9b-118">Das Ereignis, das gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-118">Event that is dropped.</span></span>

</dd> <dt>

<span data-ttu-id="e4f9b-119">**Intendidconsumer**</span><span class="sxs-lookup"><span data-stu-id="e4f9b-119">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4f9b-120">Datentyp: **\_ \_ eventconsumer**</span><span class="sxs-lookup"><span data-stu-id="e4f9b-120">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="e4f9b-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e4f9b-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4f9b-122">Verweis auf eine Instanz von [**\_ \_ eventconsumer**](--eventconsumer.md) , die den permanenten Consumer darstellt, den Sie für den Empfang eines Ereignisses identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-122">Reference to an instance of [**\_\_EventConsumer**](--eventconsumer.md) that represents the permanent consumer you identify to receive an event.</span></span> <span data-ttu-id="e4f9b-123">Andere permanente Consumer, die ein Ereignis abonnieren, können weiterhin das Ereignis empfangen.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-123">Different permanent consumers that subscribe to an event can continue to receive the event.</span></span>

</dd> <dt>

<span data-ttu-id="e4f9b-124">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e4f9b-124">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4f9b-125">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="e4f9b-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e4f9b-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e4f9b-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4f9b-127">Deskriptor, der von einem Ereignis Anbieter verwendet wird, um die Benutzer zu ermitteln, die ein Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-127">Descriptor that an event provider uses to determine the users who can receive an event.</span></span> <span data-ttu-id="e4f9b-128">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-128">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4f9b-129">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="e4f9b-129">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4f9b-130">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4f9b-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4f9b-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e4f9b-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4f9b-132">Eindeutiger Wert, der die Uhrzeit angibt, zu der ein Ereignis generiert wird.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-132">Unique value that indicates the time when an event is generated.</span></span> <span data-ttu-id="e4f9b-133">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-133">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="e4f9b-134">Die Informationen liegen im UTC-Format (koordinierte Weltzeit) vor.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-134">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="e4f9b-135">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-135">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="e4f9b-136">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e4f9b-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4f9b-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4f9b-137">Remarks</span></span>

<span data-ttu-id="e4f9b-138">Die **\_ \_ eventdroppedevent** -Klasse wird von System [**\_ \_ Event**](--systemevent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e4f9b-138">The **\_\_EventDroppedEvent** class is derived from [**\_\_SystemEvent**](--systemevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4f9b-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4f9b-139">Requirements</span></span>



| <span data-ttu-id="e4f9b-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4f9b-140">Requirement</span></span> | <span data-ttu-id="e4f9b-141">Wert</span><span class="sxs-lookup"><span data-stu-id="e4f9b-141">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e4f9b-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4f9b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e4f9b-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4f9b-143">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e4f9b-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4f9b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e4f9b-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4f9b-145">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e4f9b-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4f9b-146">Namespace</span></span><br/>                | <span data-ttu-id="e4f9b-147">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="e4f9b-147">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e4f9b-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4f9b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f9b-149">**\_\_System Event**</span><span class="sxs-lookup"><span data-stu-id="e4f9b-149">**\_\_SystemEvent**</span></span>](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[<span data-ttu-id="e4f9b-150">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="e4f9b-150">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

