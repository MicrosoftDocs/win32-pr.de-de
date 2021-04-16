---
description: Viele der in diesem Thema beschriebenen Debuggingfunktionen sind in der DirectShow-Basisklassen Bibliothek implementiert. Weitere Informationen finden Sie unter DirectShow-Basisklassen.
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: Debugging von DirectShow-Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1198e17f438d57775ea0f74d5920f63dc4761743
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522555"
---
# <a name="debugging-directshow-filters"></a><span data-ttu-id="4c00b-104">Debugging von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="4c00b-104">Debugging DirectShow Filters</span></span>

<span data-ttu-id="4c00b-105">Viele der in diesem Thema beschriebenen Debuggingfunktionen sind in der DirectShow-Basisklassen Bibliothek implementiert.</span><span class="sxs-lookup"><span data-stu-id="4c00b-105">Many of the debugging facilities described in this topic are implemented in the DirectShow base class library.</span></span> <span data-ttu-id="4c00b-106">Weitere Informationen finden Sie unter [DirectShow-Basisklassen](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="4c00b-106">For more information, see [DirectShow Base Classes](directshow-base-classes.md).</span></span>

## <a name="assertion-checking"></a><span data-ttu-id="4c00b-107">Assertionüberprüfung</span><span class="sxs-lookup"><span data-stu-id="4c00b-107">Assertion Checking</span></span>

<span data-ttu-id="4c00b-108">Verwenden Sie die Assert-Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="4c00b-108">Use assertion checking liberally.</span></span> <span data-ttu-id="4c00b-109">Assertionen können Annahmen, die Sie in Ihrem Code vornehmen, über Vorbedingungen und nach Bedingungen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4c00b-109">Assertions can verify assumptions that you make in your code about preconditions and postconditions.</span></span> <span data-ttu-id="4c00b-110">DirectShow bietet mehrere Assert-Makros.</span><span class="sxs-lookup"><span data-stu-id="4c00b-110">DirectShow provides several assertion macros.</span></span> <span data-ttu-id="4c00b-111">Weitere Informationen finden Sie unter [Assert-und breakpointmakros](assert-and-breakpoint-macros.md).</span><span class="sxs-lookup"><span data-stu-id="4c00b-111">For more information, see [Assert and Breakpoint Macros](assert-and-breakpoint-macros.md).</span></span>

## <a name="object-names"></a><span data-ttu-id="4c00b-112">Objektnamen</span><span class="sxs-lookup"><span data-stu-id="4c00b-112">Object Names</span></span>

<span data-ttu-id="4c00b-113">In Debugbuilds gibt es eine globale Liste von Objekten, die von der [**cbaseobject**](cbaseobject.md) -Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="4c00b-113">In debug builds, there is a global list of objects that derive from the [**CBaseObject**](cbaseobject.md) class.</span></span> <span data-ttu-id="4c00b-114">Wenn Objekte erstellt werden, werden Sie der Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4c00b-114">As objects are created, they are added to the list.</span></span> <span data-ttu-id="4c00b-115">Wenn Sie zerstört werden, werden Sie aus der Liste entfernt.</span><span class="sxs-lookup"><span data-stu-id="4c00b-115">When they are destroyed, they are removed from the list.</span></span> <span data-ttu-id="4c00b-116">Um eine Liste dieser Objekte anzuzeigen, müssen Sie die [**dbgdumpobjectregiester**](dbgdumpobjectregister.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4c00b-116">To display a list of those objects, call the [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) function.</span></span>

<span data-ttu-id="4c00b-117">Die Konstruktormethode für die [**cbaseobject**](cbaseobject.md) -Basisklasse – und die meisten davon abgeleiteten Klassen – enthalten einen Parameter für den Namen des Objekts.</span><span class="sxs-lookup"><span data-stu-id="4c00b-117">The constructor method for the [**CBaseObject**](cbaseobject.md) base class—and most classes derived from it—includes a parameter for the name of the object.</span></span> <span data-ttu-id="4c00b-118">Geben Sie Ihren Objekten eindeutige Namen, um Sie zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4c00b-118">Give your objects unique names to identify them.</span></span> <span data-ttu-id="4c00b-119">Verwenden Sie das [**Name**](name.md) -Makro, wenn Sie den Namen deklarieren, sodass der Name nur in Debugbuilds zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="4c00b-119">Use the [**NAME**](name.md) macro when you declare the name, so that the name is allocated only in debug builds.</span></span> <span data-ttu-id="4c00b-120">In Einzelhandels Builds wird der Name **null**.</span><span class="sxs-lookup"><span data-stu-id="4c00b-120">In retail builds, the name becomes **NULL**.</span></span>

## <a name="debug-logging"></a><span data-ttu-id="4c00b-121">Debugprotokollierung</span><span class="sxs-lookup"><span data-stu-id="4c00b-121">Debug Logging</span></span>

<span data-ttu-id="4c00b-122">Die [**dbglog**](dbglog.md) -Funktion zeigt Debugmeldungen an, während das Programm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c00b-122">The [**DbgLog**](dbglog.md) function displays debugging messages as your program executes.</span></span> <span data-ttu-id="4c00b-123">Verwenden Sie diese Funktion, um die Ausführung der Anwendung oder des Filters nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="4c00b-123">Use this function to trace the execution of your application or filter.</span></span> <span data-ttu-id="4c00b-124">Sie können Rückgabecodes, die Werte von Variablen und alle anderen relevanten Informationen protokollieren.</span><span class="sxs-lookup"><span data-stu-id="4c00b-124">You can log return codes, the values of variables, and any other relevant information.</span></span>

<span data-ttu-id="4c00b-125">Jede Debugmeldung weist einen Typ auf, z \_ . b. Protokoll Ablauf Verfolgung oder Protokoll \_ Fehler, und eine Debugebene, die die Wichtigkeit der Nachricht angibt.</span><span class="sxs-lookup"><span data-stu-id="4c00b-125">Every debug message has a type, such as LOG\_TRACE or LOG\_ERROR, and a debug level, which indicates the importance of the message.</span></span> <span data-ttu-id="4c00b-126">Nachrichten mit niedrigeren debugebenen sind wichtiger als solche mit höheren Ebenen.</span><span class="sxs-lookup"><span data-stu-id="4c00b-126">Messages with lower debug levels are more important than those with higher levels.</span></span>

<span data-ttu-id="4c00b-127">Im folgenden Beispiel trennt ein hypothetischer Filter die Verbindung einer PIN von einem Array von Pins.</span><span class="sxs-lookup"><span data-stu-id="4c00b-127">In the following example, a hypothetical filter disconnects a pin from an array of pins.</span></span> <span data-ttu-id="4c00b-128">Wenn der Verbindungsversuch erfolgreich ist, zeigt der Filter eine Protokoll Ablauf \_ Verfolgungs Meldung an.</span><span class="sxs-lookup"><span data-stu-id="4c00b-128">If the disconnect attempt succeeds, the filter displays a LOG\_TRACE message.</span></span> <span data-ttu-id="4c00b-129">Wenn der Versuch fehlschlägt, wird eine Protokoll \_ Fehlermeldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="4c00b-129">If the attempt fails, it displays a LOG\_ERROR message:</span></span>


```C++
hr = m_PinArray[iPin]->Disconnect();
if (FAILED(hr))
{
    DbgLog((
        LOG_ERROR, 
        1, 
        TEXT("Could not disconnect pin %d. HRESULT = %#x", 
        iPin, 
        hr
        ));
 
   // Error handling code (not shown).
}
DbgLog((LOG_TRACE, 3, TEXT("Disconnected pin %d"), iPin));
```



<span data-ttu-id="4c00b-130">Beim Debuggen können Sie die Debugebene für jeden Nachrichtentyp festlegen.</span><span class="sxs-lookup"><span data-stu-id="4c00b-130">When you are debugging, you can set the debug level for each message type.</span></span> <span data-ttu-id="4c00b-131">Außerdem verwaltet jedes Modul (dll oder ausführbare Datei) seine eigenen debugebenen.</span><span class="sxs-lookup"><span data-stu-id="4c00b-131">Also, each module (DLL or executable) maintains its own debugging levels.</span></span> <span data-ttu-id="4c00b-132">Wenn Sie einen Filter testen, erhöhen Sie die debugebenen für die dll, die den Filter enthält.</span><span class="sxs-lookup"><span data-stu-id="4c00b-132">If you are testing a filter, raise the debug levels for the DLL that contains the filter.</span></span>

<span data-ttu-id="4c00b-133">Weitere Informationen finden Sie unter [Debug Output Functions](debug-output-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4c00b-133">For more information, see [Debug Output Functions](debug-output-functions.md).</span></span>

## <a name="critical-sections"></a><span data-ttu-id="4c00b-134">Kritische Abschnitte</span><span class="sxs-lookup"><span data-stu-id="4c00b-134">Critical Sections</span></span>

<span data-ttu-id="4c00b-135">Um Deadlocks leichter nachvollziehen zu können, schließen Sie Assertionen ein, die bestimmen, ob der aufrufende Code einen bestimmten kritischen Abschnitt besitzt.</span><span class="sxs-lookup"><span data-stu-id="4c00b-135">To make deadlocks easier to track, include assertions that determine whether the calling code owns a given critical section.</span></span> <span data-ttu-id="4c00b-136">Die [**critcheckin**](critcheckin.md) -und [**critcheckout**](critcheckout.md) -Funktionen geben an, ob der aufrufende Thread einen kritischen Abschnitt besitzt.</span><span class="sxs-lookup"><span data-stu-id="4c00b-136">The [**CritCheckIn**](critcheckin.md) and [**CritCheckOut**](critcheckout.md) functions indicate whether the calling thread owns a critical section.</span></span> <span data-ttu-id="4c00b-137">In der Regel würden Sie diese Funktionen innerhalb eines Assert-Makros aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4c00b-137">Typically, you would call these functions from inside an assert macro.</span></span>

<span data-ttu-id="4c00b-138">Sie können auch die [**dbglocktrace**](dbglocktrace.md) -Funktion verwenden, um zu verfolgen, wann kritische Abschnitte gespeichert oder freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4c00b-138">You can also use the [**DbgLockTrace**](dbglocktrace.md) function to trace when critical sections are held or released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c00b-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4c00b-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c00b-140">Debuggen in DirectShow</span><span class="sxs-lookup"><span data-stu-id="4c00b-140">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



