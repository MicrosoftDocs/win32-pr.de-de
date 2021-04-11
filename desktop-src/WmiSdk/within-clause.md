---
description: Verwenden Sie die within-Klausel in Ereignis Abfragen zum Angeben eines Abruf Intervalls oder Gruppierungs Intervalls.
ms.assetid: e2fc7627-fb3d-4966-b38b-441333868ae3
ms.tgt_platform: multiple
title: WITHIN-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d863e2e71d52fe60aeed7697feeb1231164c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131152"
---
# <a name="within-clause"></a><span data-ttu-id="8e6f0-103">WITHIN-Klausel</span><span class="sxs-lookup"><span data-stu-id="8e6f0-103">WITHIN Clause</span></span>

<span data-ttu-id="8e6f0-104">Ereignisconsumer verwenden die within-Klausel in Ereignis Abfragen zum Angeben eines Abruf *Intervalls* oder *Gruppierungs Intervalls*.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-104">Event consumers use the WITHIN clause in event queries to specify a *polling interval* or a *grouping interval*.</span></span>

<span data-ttu-id="8e6f0-105">Ein Abruf Intervall ist das Intervall, das Windows-Verwaltungsinstrumentation (WMI) verwendet, um den für die-Klasse Verantwortlichen Datenanbieter für systeminterne [Ereignisse](determining-the-type-of-event-to-receive.md)abzurufen, von denen das abgefragte Ereignis ein Member ist.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-105">A polling interval is the interval that Windows Management Instrumentation (WMI) uses to poll the data provider responsible for the class for [intrinsic events](determining-the-type-of-event-to-receive.md), of which the event queried is a member.</span></span> <span data-ttu-id="8e6f0-106">Das Intervall ist der höchstzulässige Zeitraum, der vor dem Übermitteln einer Ereignisbenachrichtigung verstreichen darf.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-106">This interval is the maximum amount of time that can pass before notification of an event must be delivered.</span></span> <span data-ttu-id="8e6f0-107">Ein Consumer verwendet ein Abruf Intervall in einer within-Klausel, wenn der Consumer eine Benachrichtigung über Änderungen an einer Klasse benötigt und ein Ereignis Anbieter nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-107">A consumer uses a polling interval in a WITHIN clause when the consumer requires notification of changes to a class, and an event provider is unavailable.</span></span> <span data-ttu-id="8e6f0-108">Der Consumer registriert sich für ein System internes Ereignis und schließt das Abruf Intervall ein.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-108">The consumer registers for an intrinsic event and includes the polling interval.</span></span>

<span data-ttu-id="8e6f0-109">Zum Angeben eines Abruf Intervalls platzieren Sie die within-Klausel direkt vor der WHERE-Klausel, wie im folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="8e6f0-109">To specify a polling interval, place the WITHIN clause immediately before the WHERE clause, as shown following:</span></span>


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



<span data-ttu-id="8e6f0-110">Intrinsiceventclass ist die intrinsische Ereignisklasse, von der das Ereignis ein Member ist, das Intervall das Abruf Intervall und Value der Wert für die Eigenschaft, für die der Consumer eine Benachrichtigung verlangt.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-110">IntrinsicEventClass is the intrinsic event class of which the event is a member, interval is the polling interval, and value is the value for the property on which the consumer requires notification.</span></span>

<span data-ttu-id="8e6f0-111">Beim Abruf Intervall handelt es sich um eine Gleit Komma Zahl, und es kann eine Bruch Zahl sein, um Werte zu akzeptieren, die kleiner als 1 Sekunde sind.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-111">The polling interval is a floating-point number, and can be fractional to accept values smaller than 1 second.</span></span> <span data-ttu-id="8e6f0-112">Allerdings sollte das Intervall eine Anzahl von Sekunden anstelle eines extrem kleinen Werts wie z. b. 0,001 darstellen, da die Angabe eines zu kleinen Werts bewirken kann, dass WMI die Anweisung aufgrund der ressourcenintensiven Abruf Vorgänge als ungültige – ablehnt.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-112">However, the interval should represent a number of seconds rather than an extremely small value such as 0.001, because specifying a value that is too small can cause WMI to reject the statement as not valid—due to the resource-intensive nature of polling.</span></span> <span data-ttu-id="8e6f0-113">Da die meisten Ereignisconsumer keine sofortige Benachrichtigung benötigen, empfiehlt es sich, ein Intervall zu verwenden, das größer als 5 Minuten ist.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-113">Because most event consumers do not require immediate notification, it is recommended that they use an interval that is greater than 5 minutes.</span></span>

<span data-ttu-id="8e6f0-114">Im folgenden Beispiel für eine Abfrage wird von WMI alle 10 Sekunden eine Überprüfung auf Änderungen vorgenommen, die an Instanzen der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-114">The following query example requests that WMI check every 10 seconds for changes that occur to instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span> <span data-ttu-id="8e6f0-115">Wenn eine Instanz der-Klasse innerhalb des angegebenen Abruf Intervalls geändert wird, wird für jede Änderung ein Benachrichtigungs Ereignis gesendet.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-115">If an instance of the class is modified within the specified polling interval, a notification event is sent for each modification.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="8e6f0-116">Abhängig von der Abfrage können ein Ereignis Anbieter und WMI die Aufgabe der Bereitstellung von Ereignissen freigeben.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-116">Depending on the query, an event provider and WMI can share the task of providing events.</span></span> <span data-ttu-id="8e6f0-117">Beispielsweise ein Ereignis Anbieter, der Ereignisse der System Klassen [**\_ \_ instancecreationevent**](--instancecreationevent.md) und [**\_ \_ instancemodificationevent**](--instancemodificationevent.md) und keine Ereignisse der [**\_ \_ instancedeletionevent**](--instancedeletionevent.md) -System Klasse unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-117">For example, an event provider that supports events of the [**\_\_InstanceCreationEvent**](--instancecreationevent.md) and [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) system classes, and not events of the [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md) system class.</span></span> <span data-ttu-id="8e6f0-118">Mit der folgenden Abfrage kann der Ereignis Anbieter die Erstellungs-und Änderungs Ereignisse generieren, während Sie auftreten, und diese bei der Erstellung übermittelt haben.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-118">The following query enables the event provider to generate the creation and modification events as they occur and have them delivered when they are created.</span></span> <span data-ttu-id="8e6f0-119">Die Abfrage ermöglicht außerdem WMI, mithilfe des Abruf Mechanismus alle 10 Sekunden **\_ \_ instancedeletionevent** -Ereignisse zu generieren.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-119">The query also allows WMI to generate **\_\_InstanceDeletionEvent** events every 10 (ten) seconds using the polling mechanism.</span></span>


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



<span data-ttu-id="8e6f0-120">Sie können auch die within-Klausel verwenden, um ein Gruppierungs Intervall anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-120">You can also use the WITHIN clause to specify a grouping interval.</span></span> <span data-ttu-id="8e6f0-121">Ein Gruppierungs Intervall ist eine Ganzzahl ohne Vorzeichen 32 ohne Vorzeichen, die den Zeitraum angibt, nach dem ein erstes Ereignis empfangen wird, in dem WMI ähnliche Ereignisse erfassen sollte.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-121">A grouping interval is an unsigned 32-bit integer that specifies the time period, after receiving an initial event, during which WMI should collect similar events.</span></span> <span data-ttu-id="8e6f0-122">Wenn dieser Zeitraum abläuft, übermittelt WMI das Aggregat Ereignis, das aus allen ähnlichen Ereignissen besteht.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-122">When this time period expires, WMI delivers the aggregate event, made up of all the similar events.</span></span> <span data-ttu-id="8e6f0-123">Weitere Informationen finden Sie unter [Group-Klausel](group-clause.md).</span><span class="sxs-lookup"><span data-stu-id="8e6f0-123">For more information, see [GROUP Clause](group-clause.md).</span></span>

<span data-ttu-id="8e6f0-124">Ereignisconsumer, die sich für häufig auftretende Ereignisse registrieren, verwenden ein Gruppierungs Intervall mit der within-Klausel.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-124">Event consumers that register for frequently occurring events use a grouping interval with the WITHIN clause.</span></span> <span data-ttu-id="8e6f0-125">Das Hinzufügen einer Gruppe in der WHERE-Klausel in einer Ereignis Abfrage führt dazu, dass WMI ein Aggregat Ereignis anstelle von vielen Ereignissen sendet.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-125">Adding GROUP WITHIN to the WHERE clause in an event query results in WMI sending one aggregate event rather than many events.</span></span> <span data-ttu-id="8e6f0-126">Das Aggregat Ereignis wird durch die [**\_ \_ aggregateevent**](--aggregateevent.md) -System Klasse dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-126">The aggregate event is represented by the [**\_\_AggregateEvent**](--aggregateevent.md) system class.</span></span>

<span data-ttu-id="8e6f0-127">Zum Angeben eines Gruppierungs Intervalls platzieren Sie die within-Klausel direkt nach der Group-Klausel.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-127">To specify a grouping interval, place the WITHIN clause immediately after the GROUP clause.</span></span>


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



<span data-ttu-id="8e6f0-128">EventClass ist die Ereignisklasse, deren Member das Ereignis ist. der Wert ist der Wert für die Eigenschaft, für die der Consumer eine Benachrichtigung erfordert, und das Intervall ist das Gruppierungs Intervall.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-128">EventClass is the event class of which the event is a member, value is the value for the property on which the consumer requires notification, and Interval is the grouping interval.</span></span>

<span data-ttu-id="8e6f0-129">Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="8e6f0-129">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="8e6f0-130">Permanente Ereignisconsumer können nur mit Abruf Abfragen erstellt werden, wenn Sie über Administratorrechte verfügen.</span><span class="sxs-lookup"><span data-stu-id="8e6f0-130">Permanent event consumers can be created with polling queries only if you have administrator privileges.</span></span>

 

 
