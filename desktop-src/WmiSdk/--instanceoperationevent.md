---
description: Dient als Basisklasse für alle systeminternen Ereignisse, die mit einer-Instanz in Beziehung stehen.
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: __InstanceOperationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d3111b74c876cc7ffedb959eca7f46812ed92e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352696"
---
# <a name="__instanceoperationevent-class"></a><span data-ttu-id="a3ac5-103">\_\_Instanceoperationevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="a3ac5-103">\_\_InstanceOperationEvent class</span></span>

<span data-ttu-id="a3ac5-104">Die **\_ \_ instanceoperationevent** -System Klasse fungiert als Basisklasse für alle systeminternen Ereignisse, die sich auf eine Instanz beziehen.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-104">The **\_\_InstanceOperationEvent** system class serves as a base class for all intrinsic events that relate to an instance.</span></span>

<span data-ttu-id="a3ac5-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a3ac5-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3ac5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3ac5-107">Syntax</span></span>

``` syntax
class __InstanceOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="a3ac5-108">Member</span><span class="sxs-lookup"><span data-stu-id="a3ac5-108">Members</span></span>

<span data-ttu-id="a3ac5-109">Die **\_ \_ instanceoperationevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a3ac5-109">The **\_\_InstanceOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="a3ac5-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a3ac5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a3ac5-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a3ac5-111">Properties</span></span>

<span data-ttu-id="a3ac5-112">Die **\_ \_ instanceoperationevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-112">The **\_\_InstanceOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a3ac5-113">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a3ac5-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3ac5-114">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="a3ac5-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a3ac5-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a3ac5-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3ac5-116">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="a3ac5-117">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3ac5-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="a3ac5-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3ac5-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="a3ac5-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a3ac5-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a3ac5-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3ac5-121">Die Instanz, auf die sich das Ereignis auswirkt.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-121">Instance affected by the event.</span></span> <span data-ttu-id="a3ac5-122">Bei Erstellungs Ereignissen handelt es sich hierbei um die neu erstellte Instanz.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-122">For creation events, this is the newly created instance.</span></span> <span data-ttu-id="a3ac5-123">Bei Änderungs Ereignissen handelt es sich hierbei um die neue Version der geänderten Instanz.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-123">For modification events, this is the new version of the changed instance.</span></span> <span data-ttu-id="a3ac5-124">Bei Lösch Ereignissen handelt es sich hierbei um die gelöschte Instanz.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-124">For deletion events, this is the deleted instance.</span></span>

</dd> <dt>

<span data-ttu-id="a3ac5-125">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="a3ac5-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3ac5-126">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a3ac5-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a3ac5-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a3ac5-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3ac5-128">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="a3ac5-129">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="a3ac5-130">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="a3ac5-131">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="a3ac5-132">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a3ac5-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3ac5-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3ac5-133">Remarks</span></span>

<span data-ttu-id="a3ac5-134">Die **\_ \_ instanceoperationevent** -Klasse wird von [**\_ \_ Event**](--event.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-134">The **\_\_InstanceOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="a3ac5-135">Instanzen von **\_ \_ instanceoperationevent** werden nicht erstellt; es werden nur Instanzen der Unterklassen erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-135">Instances of **\_\_InstanceOperationEvent** are not created; only instances of its subclasses are created.</span></span> <span data-ttu-id="a3ac5-136">Die folgenden Klassen werden von **\_ \_ instanceoperationevent** abgeleitet:</span><span class="sxs-lookup"><span data-stu-id="a3ac5-136">The following classes derive from **\_\_InstanceOperationEvent**:</span></span>

[<span data-ttu-id="a3ac5-137">**\_\_Instancecreationevent**</span><span class="sxs-lookup"><span data-stu-id="a3ac5-137">**\_\_InstanceCreationEvent**</span></span>](--instancecreationevent.md)

[<span data-ttu-id="a3ac5-138">**\_\_Instancemodificationevent**</span><span class="sxs-lookup"><span data-stu-id="a3ac5-138">**\_\_InstanceModificationEvent**</span></span>](--instancemodificationevent.md)

[<span data-ttu-id="a3ac5-139">**\_\_Instancedeletionevent**</span><span class="sxs-lookup"><span data-stu-id="a3ac5-139">**\_\_InstanceDeletionEvent**</span></span>](--instancedeletionevent.md)

<span data-ttu-id="a3ac5-140">**Übersicht**</span><span class="sxs-lookup"><span data-stu-id="a3ac5-140">**Overview**</span></span>

<span data-ttu-id="a3ac5-141">Ebenso wie eine WMI-Klasse, die jeden Typ von System Ressource darstellt, die mithilfe von WMI verwaltet werden kann, gibt es eine WMI-Klasse, die die einzelnen Arten von WMI-Ereignissen darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-141">Just as there is a WMI class that represents each type of system resource that can be managed using WMI, there is a WMI class that represents each type of WMI event.</span></span> <span data-ttu-id="a3ac5-142">Wenn ein Ereignis auftritt, das von WMI überwacht werden kann, wird eine Instanz der entsprechenden WMI-Ereignisklasse erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-142">When an event that can be monitored by WMI occurs, an instance of the corresponding WMI event class is created.</span></span> <span data-ttu-id="a3ac5-143">Ein WMI-Ereignis tritt auf, wenn diese Instanz erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-143">A WMI event occurs when that instance is created.</span></span>

<span data-ttu-id="a3ac5-144">Es gibt drei Haupttypen von WMI-Ereignis Klassen, die alle von der WMI- [**\_ \_ Ereignis**](--event.md) Klasse abgeleitet sind: systeminterne Ereignisse, Extrinsic-Ereignisse und Timer-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-144">There are three major types of WMI event classes, all of which are derived from the [**\_\_Event**](--event.md) WMI class: Intrinsic Events, Extrinsic Events, and Timer Events.</span></span> <span data-ttu-id="a3ac5-145">Systeminterne Ereignisse werden wiederum durch drei verschiedene Klassen dargestellt, die von der **\_ \_ Ereignis** Klasse abgeleitet werden: [**\_ \_ namespaceoperationevent**](--namespaceoperationevent.md), **\_ \_ instanceoperationevent** und [**\_ \_ classoperationevent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="a3ac5-145">Intrinsic Events, in turn, are represented by three distinct classes derived from the **\_\_Event** class: [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md), **\_\_InstanceOperationEvent**, and [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

<span data-ttu-id="a3ac5-146">Systeminterne Ereignisse</span><span class="sxs-lookup"><span data-stu-id="a3ac5-146">Intrinsic Events</span></span>

<span data-ttu-id="a3ac5-147">Systeminterne Ereignisse werden verwendet, um eine Ressource zu überwachen, die von einer Klasse im CIM-Repository repräsentiert wird.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-147">Intrinsic events are used to monitor a resource represented by a class in the CIM repository.</span></span> <span data-ttu-id="a3ac5-148">Jede Ressource wird durch eine Instanz einer-Klasse dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-148">Each resource is represented by an instance of a class.</span></span> <span data-ttu-id="a3ac5-149">Dies bedeutet, dass die Überwachung einer Ressource mithilfe von WMI tatsächlich das Überwachen der Instanzen beinhaltet, die der Ressource entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-149">This means that monitoring a resource using WMI actually involves monitoring the instances that correspond to the resource.</span></span>

<span data-ttu-id="a3ac5-150">Systeminterne Ereignisse können auch verwendet werden, um Änderungen an einem Namespace oder einer Klasse im Repository zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-150">Intrinsic events can also be used to monitor changes to a namespace or class in the repository.</span></span> <span data-ttu-id="a3ac5-151">Allerdings ist das Überwachen von Änderungen an Namespaces oder Klassen für Systemadministratoren beschränkt.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-151">However, monitoring changes to namespaces or classes is of limited value to system administrators.</span></span>

<span data-ttu-id="a3ac5-152">Ein System internes Ereignis wird durch eine Instanz einer Klasse dargestellt, die von \_ \_ instanceoperationevent, \_ \_ namespaceoperationevent oder \_ \_ classoperationevent abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-152">An intrinsic event is represented by an instance of a class derived from \_\_InstanceOperationEvent, \_\_NamespaceOperationEvent, or \_\_ClassOperationEvent.</span></span> <span data-ttu-id="a3ac5-153">Alle Änderungen an Instanzen in WMI werden durch die \_ \_ instanceoperationevent-Klasse und die daraus abgeleiteten Klassen dargestellt: \_ \_ instancecreationevent, \_ \_ instancemodificationevent und \_ \_ instancedeletionevent.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-153">Any changes to instances in WMI are represented by the \_\_InstanceOperationEvent class and the classes derived from it: \_\_InstanceCreationEvent, \_\_InstanceModificationEvent, and \_\_InstanceDeletionEvent.</span></span>

<span data-ttu-id="a3ac5-154">Das Überwachen von Ressourcen mithilfe von WMI umfasst das Überwachen von Instanzen, und alle Änderungen an den Instanzen werden durch \_ \_ instanceoperationevent und die daraus abgeleiteten Klassen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-154">Monitoring resources using WMI involves monitoring instances and all changes to instances are represented by \_\_InstanceOperationEvent and the classes derived from it.</span></span> <span data-ttu-id="a3ac5-155">Dies bedeutet, dass Überwachungsressourcen letztendlich das Überwachen von Instanzen von \_ \_ instanceoperationevent-abgeleiteten Klassen beinhalten.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-155">This means that monitoring resources ultimately involves monitoring instances of \_\_InstanceOperationEvent-derived classes.</span></span>

<span data-ttu-id="a3ac5-156">Sie registrieren Interesse an Instanzen einer dieser Klassen, indem Sie eine in WQL ausgedrückte Benachrichtigungs Abfrage ausgeben.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-156">You register interest in instances of one of these classes by issuing a notification query expressed in WQL.</span></span> <span data-ttu-id="a3ac5-157">Die Abfrage verwendet eine Syntax, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="a3ac5-157">The query uses syntax similar to the following:</span></span>

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

<span data-ttu-id="a3ac5-158">Eine ausführlichere Erläuterung der Verwendung von WMI-Instanzereignissen zum Überwachen von Computeraktivitäten finden Sie unter [wie kann ich unterschiedliche Arten von Ereignissen mit nur einem Skript überwachen?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3ac5-158">For a longer discussion of using the WMI instance events to monitor computer activity, see [How Can I Monitor for Different Types of Events With Just One Script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)</span></span>

## <a name="examples"></a><span data-ttu-id="a3ac5-159">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3ac5-159">Examples</span></span>

<span data-ttu-id="a3ac5-160">Das Codebeispiel für den [Monitor Process Event](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript in der TechNet Gallery verwendet **\_ \_ instanceoperationevent** , um das erste WMI-Instanzereignis für den [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process)zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-160">The [Monitor process event](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript code sample on TechNet Gallery uses **\_\_InstanceOperationEvent** to monitors the first WMI instance event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3ac5-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3ac5-161">Requirements</span></span>



| <span data-ttu-id="a3ac5-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3ac5-162">Requirement</span></span> | <span data-ttu-id="a3ac5-163">Wert</span><span class="sxs-lookup"><span data-stu-id="a3ac5-163">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a3ac5-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3ac5-164">Minimum supported client</span></span><br/> | <span data-ttu-id="a3ac5-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3ac5-165">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a3ac5-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3ac5-166">Minimum supported server</span></span><br/> | <span data-ttu-id="a3ac5-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3ac5-167">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="a3ac5-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="a3ac5-168">Namespace</span></span><br/>                | <span data-ttu-id="a3ac5-169">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="a3ac5-169">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="a3ac5-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3ac5-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3ac5-171">**\_\_Ereignis**</span><span class="sxs-lookup"><span data-stu-id="a3ac5-171">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="a3ac5-172">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="a3ac5-172">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a3ac5-173">Bestimmen des zu empfangenden Ereignis Typs</span><span class="sxs-lookup"><span data-stu-id="a3ac5-173">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="a3ac5-174">Schreiben in eine Protokolldatei auf Grundlage eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="a3ac5-174">Writing to a Log File Based on an Event</span></span>](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 

