---
description: Meldet, wenn ein Ereignis aufgrund eines Überlaufs der Übermittlungs Warteschlange gelöscht wird.
ms.assetid: 7cb1ef3b-3b0a-4f72-96de-862022fd6db8
ms.tgt_platform: multiple
title: __EventQueueOverflowEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventQueueOverflowEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 058b03b8a3311aad805f47a04d20e9f1fa8c2477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362918"
---
# <a name="__eventqueueoverflowevent-class"></a><span data-ttu-id="da4f3-103">\_\_Eventqueueoverflowevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="da4f3-103">\_\_EventQueueOverflowEvent class</span></span>

<span data-ttu-id="da4f3-104">Die **\_ \_ eventqueueoverflowevent** -System Klasse meldet, wenn ein Ereignis aufgrund eines Überlaufs der Übermittlungs Warteschlange gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="da4f3-104">The **\_\_EventQueueOverflowEvent** system class reports when an event is dropped as a result of delivery queue overflow.</span></span>

<span data-ttu-id="da4f3-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="da4f3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="da4f3-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="da4f3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="da4f3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="da4f3-107">Syntax</span></span>

``` syntax
class __EventQueueOverflowEvent : __EventDroppedEvent
{
  uint32              CurrentQueueSize;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="da4f3-108">Member</span><span class="sxs-lookup"><span data-stu-id="da4f3-108">Members</span></span>

<span data-ttu-id="da4f3-109">Die **\_ \_ eventqueueoverflowevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="da4f3-109">The **\_\_EventQueueOverflowEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="da4f3-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="da4f3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da4f3-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="da4f3-111">Properties</span></span>

<span data-ttu-id="da4f3-112">Die **\_ \_ eventqueueoverflowevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="da4f3-112">The **\_\_EventQueueOverflowEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da4f3-113">**Currentqueuesize**</span><span class="sxs-lookup"><span data-stu-id="da4f3-113">**CurrentQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da4f3-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da4f3-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da4f3-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da4f3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da4f3-116">Aktuelle Warteschlangen Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="da4f3-116">Current queue size, in bytes.</span></span> <span data-ttu-id="da4f3-117">Diese Eigenschaft ist standardmäßig auf 10 MB für alle Warteschlangen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="da4f3-117">This property defaults to 10 MB for all queues combined.</span></span>

</dd> <dt>

<span data-ttu-id="da4f3-118">**Event**</span><span class="sxs-lookup"><span data-stu-id="da4f3-118">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da4f3-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="da4f3-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="da4f3-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da4f3-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da4f3-121">Interessantes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="da4f3-121">Event of interest.</span></span> <span data-ttu-id="da4f3-122">Diese Eigenschaft wird von [**\_ \_ eventdroppedevent**](--eventdroppedevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da4f3-122">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="da4f3-123">**Intendidconsumer**</span><span class="sxs-lookup"><span data-stu-id="da4f3-123">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da4f3-124">Datentyp: **\_ \_ eventconsumer**</span><span class="sxs-lookup"><span data-stu-id="da4f3-124">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="da4f3-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da4f3-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da4f3-126">Verweis auf den gewünschten Consumer.</span><span class="sxs-lookup"><span data-stu-id="da4f3-126">Reference to the intended consumer.</span></span> <span data-ttu-id="da4f3-127">Diese Eigenschaft wird von [**\_ \_ eventdroppedevent**](--eventdroppedevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da4f3-127">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="da4f3-128">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da4f3-128">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da4f3-129">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="da4f3-129">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="da4f3-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da4f3-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da4f3-131">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="da4f3-131">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="da4f3-132">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da4f3-132">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="da4f3-133">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="da4f3-133">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da4f3-134">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="da4f3-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="da4f3-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da4f3-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da4f3-136">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="da4f3-136">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="da4f3-137">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="da4f3-137">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="da4f3-138">Die Informationen liegen im UTC-Format (koordinierte Weltzeit) vor.</span><span class="sxs-lookup"><span data-stu-id="da4f3-138">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="da4f3-139">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da4f3-139">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="da4f3-140">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="da4f3-140">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da4f3-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da4f3-141">Remarks</span></span>

<span data-ttu-id="da4f3-142">Nur Benutzer mit Administratorrechten können dieses Ereignis empfangen.</span><span class="sxs-lookup"><span data-stu-id="da4f3-142">Only users with administrator privileges are able to receive this event.</span></span> <span data-ttu-id="da4f3-143">Die **\_ \_ eventqueueoverflowevent** -Klasse wird von [**\_ \_ eventdroppedevent**](--eventdroppedevent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="da4f3-143">The **\_\_EventQueueOverflowEvent** class is derived from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

<span data-ttu-id="da4f3-144">Weitere Informationen finden Sie in der Eigenschaft " [**MaximumQueueSize**](--eventconsumer.md) " in der [**\_ \_ eventconsumer**](--eventconsumer.md) -Klasse und in der Eigenschaft " [**highprocessoldonevents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) " in der **Win32- \_ wmisetting** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="da4f3-144">For more information, see the [**MaximumQueueSize**](--eventconsumer.md) property in the [**\_\_EventConsumer**](--eventconsumer.md) class and the [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) property in the **Win32\_WMISetting** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="da4f3-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da4f3-145">Requirements</span></span>



| <span data-ttu-id="da4f3-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da4f3-146">Requirement</span></span> | <span data-ttu-id="da4f3-147">Wert</span><span class="sxs-lookup"><span data-stu-id="da4f3-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="da4f3-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da4f3-148">Minimum supported client</span></span><br/> | <span data-ttu-id="da4f3-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da4f3-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="da4f3-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da4f3-150">Minimum supported server</span></span><br/> | <span data-ttu-id="da4f3-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da4f3-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="da4f3-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="da4f3-152">Namespace</span></span><br/>                | <span data-ttu-id="da4f3-153">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="da4f3-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="da4f3-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da4f3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da4f3-155">**\_\_Eventdroppedevent**</span><span class="sxs-lookup"><span data-stu-id="da4f3-155">**\_\_EventDroppedEvent**</span></span>](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[<span data-ttu-id="da4f3-156">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="da4f3-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

