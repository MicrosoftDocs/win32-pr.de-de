---
description: Bewirkt, dass ein Ereignis zu einem bestimmten Zeitpunkt zu einem bestimmten Zeitpunkt generiert wird.
ms.assetid: bcb64c81-3b40-4665-a880-a100629656e0
ms.tgt_platform: multiple
title: __AbsoluteTimerInstruction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AbsoluteTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f4f55e635e42ec34e9b3558a0784d319e4d91ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350988"
---
# <a name="__absolutetimerinstruction-class"></a><span data-ttu-id="61f61-103">\_\_Absolutetimerinstruction-Klasse</span><span class="sxs-lookup"><span data-stu-id="61f61-103">\_\_AbsoluteTimerInstruction class</span></span>

<span data-ttu-id="61f61-104">Die **\_ \_ absolutetimerinstruction** -System Klasse bewirkt, dass ein Ereignis zu einem bestimmten Zeitpunkt zu einem bestimmten Zeitpunkt generiert wird.</span><span class="sxs-lookup"><span data-stu-id="61f61-104">The **\_\_AbsoluteTimerInstruction** system class causes an event to be generated on a specific date at a specific time.</span></span> <span data-ttu-id="61f61-105">Ein Ereignisconsumer registriert sich, um ein absolutes Timer-Ereignis zu erhalten, indem eine Instanz dieser Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="61f61-105">An event consumer registers to receive an absolute timer event by creating an instance of this class.</span></span> <span data-ttu-id="61f61-106">Das Ereignis wird einmal generiert.</span><span class="sxs-lookup"><span data-stu-id="61f61-106">The event is generated one time.</span></span>

<span data-ttu-id="61f61-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="61f61-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="61f61-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="61f61-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="61f61-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="61f61-109">Syntax</span></span>

``` syntax
class __AbsoluteTimerInstruction : __TimerInstruction
{
  datetime EventDateTime;
  boolean  SkipIfPassed = FALSE;
  string   TimerId;
};
```

## <a name="members"></a><span data-ttu-id="61f61-110">Member</span><span class="sxs-lookup"><span data-stu-id="61f61-110">Members</span></span>

<span data-ttu-id="61f61-111">Die **\_ \_ absolutetimerinstruction** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="61f61-111">The **\_\_AbsoluteTimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="61f61-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="61f61-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61f61-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="61f61-113">Properties</span></span>

<span data-ttu-id="61f61-114">Die **\_ \_ absolutetimerinstruction** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="61f61-114">The **\_\_AbsoluteTimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61f61-115">**EventDateTime**</span><span class="sxs-lookup"><span data-stu-id="61f61-115">**EventDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61f61-116">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="61f61-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="61f61-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="61f61-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="61f61-118">Zeichenfolge mit fester Länge im [DMTF-Format](date-and-time-format.md) , das angibt, wann der Timer ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="61f61-118">Fixed-length string in [DMTF format](date-and-time-format.md) that specifies when the timer fires.</span></span>

</dd> <dt>

<span data-ttu-id="61f61-119">**Skipifbestandene**</span><span class="sxs-lookup"><span data-stu-id="61f61-119">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61f61-120">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="61f61-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61f61-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61f61-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61f61-122">**True** gibt an, dass das Timer-Ereignis auftritt, wenn WMI es nicht im richtigen Zeitintervall generieren kann oder der Consumer, der den Empfang des Ereignisses anfordert, nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="61f61-122">If **TRUE**, the timer event occurs if WMI cannot generate it at the correct time interval, or the consumer requesting to receive the event is unavailable.</span></span> <span data-ttu-id="61f61-123">**True** gibt an, dass das Ereignis nicht auftritt.</span><span class="sxs-lookup"><span data-stu-id="61f61-123">If **TRUE**, the event will not occur.</span></span> <span data-ttu-id="61f61-124">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="61f61-124">The default is **FALSE**.</span></span> <span data-ttu-id="61f61-125">Wenn WMI oder der Consumer verfügbar wird, wird ein Benachrichtigungs Ereignis generiert und empfangen.</span><span class="sxs-lookup"><span data-stu-id="61f61-125">When WMI or the consumer becomes available, a notification event is generated and received.</span></span> <span data-ttu-id="61f61-126">Diese Eigenschaft wird von [**\_ \_ timerinstruction**](--timerinstruction.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="61f61-126">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<dt>

<span data-ttu-id="61f61-127">false</span><span class="sxs-lookup"><span data-stu-id="61f61-127">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="61f61-128">Wenn WMI oder der Consumer wieder verfügbar wird, wird ein Benachrichtigungs Ereignis generiert und empfangen.</span><span class="sxs-lookup"><span data-stu-id="61f61-128">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="61f61-129">TRUE</span><span class="sxs-lookup"><span data-stu-id="61f61-129">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="61f61-130">Das Timer-Ereignis tritt nicht auf, wenn WMI nicht verfügbar ist, um es im entsprechenden Zeitintervall zu generieren, oder wenn der Consumer, der den Empfang des Ereignisses anfordert, nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="61f61-130">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="61f61-131">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="61f61-131">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61f61-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="61f61-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61f61-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61f61-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61f61-134">Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="61f61-134">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="61f61-135">Eindeutige vom Benutzer zugewiesene Zeichenfolge, die ein bestimmtes Timer-Ereignis bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="61f61-135">Unique user-assigned string that identifies a specific timer event.</span></span> <span data-ttu-id="61f61-136">Um Namenskonflikte mit anderen Zeit Geber Bezeichners zu vermeiden, kann die Zeichen folgen Form einer Umgebungs Stil-GUID für verteilte Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61f61-136">To avoid naming conflicts with other timer identifiers, the string form of a distributed computer environment style GUID can be used.</span></span> <span data-ttu-id="61f61-137">Diese Eigenschaft wird von [**\_ \_ timerinstruction**](--timerinstruction.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="61f61-137">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61f61-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61f61-138">Remarks</span></span>

<span data-ttu-id="61f61-139">Die **\_ \_ absolutetimerinstruction** -Klasse wird von [**\_ \_ timerinstruction**](--timerinstruction.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="61f61-139">The **\_\_AbsoluteTimerInstruction** class is derived from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<span data-ttu-id="61f61-140">WMI generiert das absolute Timer-Ereignis, indem eine Instanz der [**\_ \_ TimerEvent**](--timerevent.md) -Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="61f61-140">WMI generates the absolute timer event by creating an instance of the [**\_\_TimerEvent**](--timerevent.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="61f61-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61f61-141">Requirements</span></span>



| <span data-ttu-id="61f61-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61f61-142">Requirement</span></span> | <span data-ttu-id="61f61-143">Wert</span><span class="sxs-lookup"><span data-stu-id="61f61-143">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="61f61-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61f61-144">Minimum supported client</span></span><br/> | <span data-ttu-id="61f61-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61f61-145">Windows Vista</span></span><br/>       |
| <span data-ttu-id="61f61-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61f61-146">Minimum supported server</span></span><br/> | <span data-ttu-id="61f61-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61f61-147">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="61f61-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="61f61-148">Namespace</span></span><br/>                | <span data-ttu-id="61f61-149">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="61f61-149">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="61f61-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61f61-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61f61-151">**\_\_Timerinstruction**</span><span class="sxs-lookup"><span data-stu-id="61f61-151">**\_\_TimerInstruction**</span></span>](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[<span data-ttu-id="61f61-152">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="61f61-152">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="61f61-153">Empfangen von zeitgesteuerten oder wiederkehrenden Ereignissen</span><span class="sxs-lookup"><span data-stu-id="61f61-153">Receiving Timed or Repeating Events</span></span>](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[<span data-ttu-id="61f61-154">Empfangen von Ereignissen zu allen Zeitpunkten</span><span class="sxs-lookup"><span data-stu-id="61f61-154">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="61f61-155">Empfangen von Ereignissen für die Dauer der Anwendung</span><span class="sxs-lookup"><span data-stu-id="61f61-155">Receiving Events for the Duration of Your Application</span></span>](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

