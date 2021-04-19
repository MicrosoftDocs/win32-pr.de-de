---
description: Generiert Ereignisse in Intervallen, ähnlich einer WM-Zeit Geber \_ Meldung in der Windows-Programmierung.
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: __IntervalTimerInstruction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __IntervalTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 20dd1c9fb2d009de4d8d957b4d5980cc6d6ff45e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369802"
---
# <a name="__intervaltimerinstruction-class"></a><span data-ttu-id="c705c-103">\_\_Intervaltimerinstruction-Klasse</span><span class="sxs-lookup"><span data-stu-id="c705c-103">\_\_IntervalTimerInstruction class</span></span>

<span data-ttu-id="c705c-104">Die **\_ \_ intervaltimerinstruction** -System Klasse generiert Ereignisse in Intervallen, ähnlich einer WM-Zeit Geber \_ Meldung bei der Windows-Programmierung.</span><span class="sxs-lookup"><span data-stu-id="c705c-104">The **\_\_IntervalTimerInstruction** system class generates events at intervals, similar to a WM\_TIMER message in Windows programming.</span></span> <span data-ttu-id="c705c-105">Ein Ereignisconsumer registriert sich für das Empfangen von Intervallzeit Geber Ereignissen durch Erstellen einer Ereignis Abfrage, die auf diese Klasse verweist.</span><span class="sxs-lookup"><span data-stu-id="c705c-105">An event consumer registers to receive interval timer events by creating an event query that references this class.</span></span> <span data-ttu-id="c705c-106">Aufgrund des Betriebssystem Verhaltens gibt es keine Garantie, dass Ereignisse in genau dem angeforderten Intervall übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="c705c-106">Due to operating system behavior, there are no guarantees that events will be delivered at precisely the requested interval.</span></span>

<span data-ttu-id="c705c-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c705c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c705c-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c705c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c705c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c705c-109">Syntax</span></span>

``` syntax
class __IntervalTimerInstruction : __TimerInstruction
{
  uint32  IntervalBetweenEvents;
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a><span data-ttu-id="c705c-110">Member</span><span class="sxs-lookup"><span data-stu-id="c705c-110">Members</span></span>

<span data-ttu-id="c705c-111">Die **\_ \_ intervaltimerinstruction** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c705c-111">The **\_\_IntervalTimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="c705c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c705c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c705c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c705c-113">Properties</span></span>

<span data-ttu-id="c705c-114">Die **\_ \_ intervaltimerinstruction** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c705c-114">The **\_\_IntervalTimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c705c-115">**Intervalbetweerevents**</span><span class="sxs-lookup"><span data-stu-id="c705c-115">**IntervalBetweenEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c705c-116">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c705c-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c705c-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c705c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c705c-118">Qualifizierer: [**Einheiten**](standard-qualifiers.md) (Millisekunden)</span><span class="sxs-lookup"><span data-stu-id="c705c-118">Qualifiers: [**Units**](standard-qualifiers.md) (milliseconds)</span></span>
</dt> </dl>

<span data-ttu-id="c705c-119">Anzahl von Millisekunden zwischen Ereignis Ausgründungen.</span><span class="sxs-lookup"><span data-stu-id="c705c-119">Number of milliseconds between event firings.</span></span>

</dd> <dt>

<span data-ttu-id="c705c-120">**Skipifbestandene**</span><span class="sxs-lookup"><span data-stu-id="c705c-120">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c705c-121">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c705c-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c705c-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c705c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c705c-123">**True** gibt an, dass dieses Ereignis übersprungen werden soll, wenn das Intervall bereits verstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="c705c-123">If **TRUE**, this event is to be skipped if the interval is already passed.</span></span> <span data-ttu-id="c705c-124">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="c705c-124">The default is **FALSE**.</span></span> <span data-ttu-id="c705c-125">Diese Eigenschaft wird von [**\_ \_ timerinstruction**](--timerinstruction.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c705c-125">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<dt>

<span data-ttu-id="c705c-126">false</span><span class="sxs-lookup"><span data-stu-id="c705c-126">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="c705c-127">Wenn WMI oder der Consumer wieder verfügbar wird, wird ein Benachrichtigungs Ereignis generiert und empfangen.</span><span class="sxs-lookup"><span data-stu-id="c705c-127">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="c705c-128">TRUE</span><span class="sxs-lookup"><span data-stu-id="c705c-128">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="c705c-129">Das Timer-Ereignis tritt nicht auf, wenn WMI nicht verfügbar ist, um es im entsprechenden Zeitintervall zu generieren, oder wenn der Consumer, der den Empfang des Ereignisses anfordert, nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c705c-129">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c705c-130">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="c705c-130">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c705c-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c705c-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c705c-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c705c-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c705c-133">Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c705c-133">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c705c-134">Eindeutiger Bezeichner für dieses **\_ \_ intervaltimerinstruction** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c705c-134">Unique identifier for this **\_\_IntervalTimerInstruction** object.</span></span> <span data-ttu-id="c705c-135">Diese Eigenschaft wird von [**\_ \_ timerinstruction**](--timerinstruction.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c705c-135">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c705c-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c705c-136">Remarks</span></span>

<span data-ttu-id="c705c-137">Die **\_ \_ intervaltimerinstruction** -Klasse wird von [**\_ \_ timerinstruction**](--timerinstruction.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c705c-137">The **\_\_IntervalTimerInstruction** class is derived from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<span data-ttu-id="c705c-138">Die für ein Intervallzeit Geber Ereignis eingegebene Ereignis Abfrage basiert in der Regel auf der **timerId-** Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c705c-138">The event query entered to register for an interval timer event is usually based on the **TimerId** property.</span></span> <span data-ttu-id="c705c-139">Benachrichtigungs Ereignisse, die von einem Intervall-Timer-Ereignis generiert werden, enthalten die Eigenschaft **numfirings** , die Daten enthält, die die Anzahl der Ereignisse enthalten, die während der Zeit ausgelöst wurden, die Ereignisse nicht empfangen</span><span class="sxs-lookup"><span data-stu-id="c705c-139">Notification events generated from an interval timer event contain the property **NumFirings** which contains data reflecting how many events fired during the time the events were unable to be received.</span></span> <span data-ttu-id="c705c-140">Wenn **skipifover** auf **true** festgelegt ist, werden diese Informationen verworfen.</span><span class="sxs-lookup"><span data-stu-id="c705c-140">If **SkipIfPassed** is set to **TRUE**, that information is discarded.</span></span>

<span data-ttu-id="c705c-141">Der Wert für die **intervalbetweenevents** -Eigenschaft sollte relativ groß sein.</span><span class="sxs-lookup"><span data-stu-id="c705c-141">The value for the **IntervalBetweenEvents** property should be reasonably large.</span></span> <span data-ttu-id="c705c-142">Wenn Sie zu klein ist, kann Sie von WMI ignoriert werden, und das Ereignis kann aufgrund von Einschränkungen in einigen Betriebssystemen nicht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="c705c-142">If it is too small, WMI may ignore it and not generate the event due to limitations in some operating systems.</span></span>

<span data-ttu-id="c705c-143">WMI generiert das Intervall Timer-Ereignis, indem eine Instanz der [**\_ \_ TimerEvent**](--timerevent.md) -Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c705c-143">WMI generates the interval timer event by creating an instance of the [**\_\_TimerEvent**](--timerevent.md) class.</span></span>

<span data-ttu-id="c705c-144">Um diese Timer-Ereignisse in einem temporären Ereignisconsumer zu empfangen, führen Sie [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) mit der folgenden Ereignis Abfrage Zeichenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="c705c-144">To receive these timer events in a temporary event consumer, execute [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) with the following event query string:</span></span>


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



<span data-ttu-id="c705c-145">Um diese Timer-Ereignisse in einem permanenten Ereignisconsumer zu empfangen, müssen Sie die vorherige Abfrage in einen Ereignis Filter laden, einen logischen Consumer definieren und eine Filter-zu-Consumer-Bindung für den Filter und den Consumer erstellen.</span><span class="sxs-lookup"><span data-stu-id="c705c-145">To receive these timer events in a permanent event consumer, you must load the previous query into an event filter, define a logical consumer, and create a filter-to-consumer binding for the filter and consumer.</span></span> <span data-ttu-id="c705c-146">Weitere Informationen finden Sie [unter empfangen von Ereignissen zu allen Zeit](receiving-events-at-all-times.md)Punkten.</span><span class="sxs-lookup"><span data-stu-id="c705c-146">For more information, see [Receiving Events at All Times](receiving-events-at-all-times.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c705c-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c705c-147">Examples</span></span>

<span data-ttu-id="c705c-148">Die folgende MOF-Deklaration zeigt, wie ein Intervallzeit Geber Ereignis generiert wird, bei dem die Key-Eigenschaft alle 10 Sekunden auf "MyEvent" festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="c705c-148">The following MOF declaration shows how to generate an interval timer event with the key property set to "MyEvent" every 10 seconds:</span></span>


```mof
instance of __IntervalTimerInstruction
{
  TimerId = "MyEvent";     // inherited from __TimerInstruction
  SkipIfPassed = FALSE;    // also inherited
  IntervalBetweenEvents = 10000;
};
```



## <a name="requirements"></a><span data-ttu-id="c705c-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c705c-149">Requirements</span></span>



| <span data-ttu-id="c705c-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c705c-150">Requirement</span></span> | <span data-ttu-id="c705c-151">Wert</span><span class="sxs-lookup"><span data-stu-id="c705c-151">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c705c-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c705c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="c705c-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c705c-153">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c705c-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c705c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="c705c-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c705c-155">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c705c-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="c705c-156">Namespace</span></span><br/>                | <span data-ttu-id="c705c-157">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="c705c-157">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c705c-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c705c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c705c-159">**\_\_Timerinstruction**</span><span class="sxs-lookup"><span data-stu-id="c705c-159">**\_\_TimerInstruction**</span></span>](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[<span data-ttu-id="c705c-160">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="c705c-160">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="c705c-161">Empfangen von zeitgesteuerten oder wiederkehrenden Ereignissen</span><span class="sxs-lookup"><span data-stu-id="c705c-161">Receiving Timed or Repeating Events</span></span>](receiving-a-timed-or-repeating-event.md)
</dt> </dl>

 

