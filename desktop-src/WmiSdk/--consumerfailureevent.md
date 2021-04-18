---
description: Stellt das Vorkommen eines anderen Ereignisses dar, das aufgrund eines Fehlers eines Ereignisconsumer gelöscht wird.
ms.assetid: bb6a1ce9-72a2-4528-8bc8-71ac053b6b1d
ms.tgt_platform: multiple
title: __ConsumerFailureEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ConsumerFailureEvent
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 571785245c05d18678c10a65b192a25022fff8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350967"
---
# <a name="__consumerfailureevent-class"></a><span data-ttu-id="e71c9-103">\_\_Consumerfailureevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="e71c9-103">\_\_ConsumerFailureEvent class</span></span>

<span data-ttu-id="e71c9-104">Die **\_ \_ consumerfailureevent** -System Klasse stellt das Vorkommen eines anderen Ereignisses dar, das aufgrund eines Fehlers eines Ereignisconsumers gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="e71c9-104">The **\_\_ConsumerFailureEvent** system class represents the occurrence of some other event that is being dropped because of the failure of an event consumer.</span></span>

<span data-ttu-id="e71c9-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e71c9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e71c9-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e71c9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e71c9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e71c9-107">Syntax</span></span>

``` syntax
class __ConsumerFailureEvent : __EventDroppedEvent
{
  uint32              ErrorCode;
  string              ErrorDescription;
  object              ErrorObject;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="e71c9-108">Member</span><span class="sxs-lookup"><span data-stu-id="e71c9-108">Members</span></span>

<span data-ttu-id="e71c9-109">Die **\_ \_ consumerfailureevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e71c9-109">The **\_\_ConsumerFailureEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="e71c9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e71c9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e71c9-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e71c9-111">Properties</span></span>

<span data-ttu-id="e71c9-112">Die **\_ \_ consumerfailureevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e71c9-112">The **\_\_ConsumerFailureEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e71c9-113">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e71c9-113">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71c9-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e71c9-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e71c9-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e71c9-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e71c9-116">Der vom Consumer zurückgegebene Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e71c9-116">Error code returned by the consumer.</span></span>

</dd> <dt>

<span data-ttu-id="e71c9-117">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e71c9-117">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71c9-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e71c9-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e71c9-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e71c9-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e71c9-120">Erweiterte Fehlercode Beschreibung, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e71c9-120">Extended error code description, if available.</span></span>

</dd> <dt>

<span data-ttu-id="e71c9-121">**Customerrorobject**</span><span class="sxs-lookup"><span data-stu-id="e71c9-121">**ErrorObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71c9-122">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="e71c9-122">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e71c9-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e71c9-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e71c9-124">Das Objekt ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="e71c9-124">Object in error.</span></span>

</dd> <dt>

<span data-ttu-id="e71c9-125">**Event**</span><span class="sxs-lookup"><span data-stu-id="e71c9-125">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71c9-126">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="e71c9-126">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e71c9-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e71c9-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e71c9-128">Das Ereignis ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="e71c9-128">Event in error.</span></span> <span data-ttu-id="e71c9-129">Diese Eigenschaft wird von [**\_ \_ eventdroppedevent**](--eventdroppedevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e71c9-129">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e71c9-130">**Intendidconsumer**</span><span class="sxs-lookup"><span data-stu-id="e71c9-130">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71c9-131">Datentyp: **\_ \_ eventconsumer**</span><span class="sxs-lookup"><span data-stu-id="e71c9-131">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="e71c9-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e71c9-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e71c9-133">Verweis auf den gewünschten Consumer.</span><span class="sxs-lookup"><span data-stu-id="e71c9-133">Reference to the intended consumer.</span></span> <span data-ttu-id="e71c9-134">Diese Eigenschaft wird von [**\_ \_ eventdroppedevent**](--eventdroppedevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e71c9-134">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e71c9-135">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e71c9-135">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71c9-136">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="e71c9-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e71c9-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e71c9-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e71c9-138">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="e71c9-138">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="e71c9-139">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e71c9-139">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="e71c9-140">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="e71c9-140">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e71c9-141">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e71c9-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e71c9-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e71c9-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e71c9-143">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e71c9-143">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="e71c9-144">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="e71c9-144">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="e71c9-145">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="e71c9-145">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="e71c9-146">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e71c9-146">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="e71c9-147">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e71c9-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e71c9-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e71c9-148">Remarks</span></span>

<span data-ttu-id="e71c9-149">Die **\_ \_ consumerfailureevent** -Klasse wird von [**\_ \_ eventdroppedevent**](--eventdroppedevent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e71c9-149">The **\_\_ConsumerFailureEvent** class is derived from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e71c9-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e71c9-150">Requirements</span></span>



| <span data-ttu-id="e71c9-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e71c9-151">Requirement</span></span> | <span data-ttu-id="e71c9-152">Wert</span><span class="sxs-lookup"><span data-stu-id="e71c9-152">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e71c9-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e71c9-153">Minimum supported client</span></span><br/> | <span data-ttu-id="e71c9-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e71c9-154">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e71c9-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e71c9-155">Minimum supported server</span></span><br/> | <span data-ttu-id="e71c9-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e71c9-156">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e71c9-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="e71c9-157">Namespace</span></span><br/>                | <span data-ttu-id="e71c9-158">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="e71c9-158">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e71c9-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e71c9-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e71c9-160">**\_\_Eventdroppedevent**</span><span class="sxs-lookup"><span data-stu-id="e71c9-160">**\_\_EventDroppedEvent**</span></span>](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[<span data-ttu-id="e71c9-161">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="e71c9-161">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

