---
description: Die folgenden Überlegungen zum Tablet PC-Threading gelten speziell für die verwaltete Bibliothek.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Überlegungen zum Threading verwalteter Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8677375b8bbdb5f171329927d01e6178b5cb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362347"
---
# <a name="managed-library-threading-considerations"></a><span data-ttu-id="4e37b-103">Überlegungen zum Threading verwalteter Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="4e37b-103">Managed Library Threading Considerations</span></span>

<span data-ttu-id="4e37b-104">Die folgenden Überlegungen zum Tablet PC-Threading gelten speziell für die verwaltete Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="4e37b-104">The following Tablet PC threading considerations are specific to the Managed Library.</span></span>

-   [<span data-ttu-id="4e37b-105">Thread Sicherheit</span><span class="sxs-lookup"><span data-stu-id="4e37b-105">Thread-Safety</span></span>](#thread-safety)
-   [<span data-ttu-id="4e37b-106">STA-und MTA-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="4e37b-106">STA and MTA Applications</span></span>](#sta-and-mta-applications)
-   [<span data-ttu-id="4e37b-107">Überlegungen zum Windows Forms Threading</span><span class="sxs-lookup"><span data-stu-id="4e37b-107">Windows Forms Threading Considerations</span></span>](#windows-forms-threading-considerations)
-   [<span data-ttu-id="4e37b-108">Überlegungen Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="4e37b-108">Clipboard Considerations</span></span>](#clipboard-considerations)
-   [<span data-ttu-id="4e37b-109">Ausnahmen innerhalb von Ereignis Handlern</span><span class="sxs-lookup"><span data-stu-id="4e37b-109">Exceptions within Event Handlers</span></span>](#exceptions-within-event-handlers)
-   [<span data-ttu-id="4e37b-110">Verwerfen von Objekten und Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="4e37b-110">Disposing Objects and Controls</span></span>](#disposing-objects-and-controls)
-   [<span data-ttu-id="4e37b-111">StylusInput-APIs</span><span class="sxs-lookup"><span data-stu-id="4e37b-111">StylusInput APIs</span></span>](#stylusinput-apis)

## <a name="thread-safety"></a><span data-ttu-id="4e37b-112">Thread-Safety</span><span class="sxs-lookup"><span data-stu-id="4e37b-112">Thread-Safety</span></span>

<span data-ttu-id="4e37b-113">Die verwalteten Bibliotheks Klassen der Tablet PC-Plattform sind im Allgemeinen nicht Thread sicher.</span><span class="sxs-lookup"><span data-stu-id="4e37b-113">The Tablet PC Platform's Managed Library classes are not generally thread-safe.</span></span> <span data-ttu-id="4e37b-114">Die folgenden Auflistungen sind auf Element Ebene Thread sicher. Diese Auflistungen garantieren jedoch nicht, dass ein Enumerator geschützt ist, wenn ein anderer Thread gleichzeitig mit der Auflistung arbeitet:</span><span class="sxs-lookup"><span data-stu-id="4e37b-114">The following collections are thread-safe at the member level; however, these collections do not guarantee that an enumerator is protected if another thread operates on the collection simultaneously:</span></span>

-   <span data-ttu-id="4e37b-115">[Cursor Buttons](/previous-versions/ms839506(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="4e37b-115">[CursorButtons](/previous-versions/ms839506(v=msdn.10))</span></span>
-   <span data-ttu-id="4e37b-116">[Cursor](/previous-versions/ms839493(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="4e37b-116">[Cursors](/previous-versions/ms839493(v=msdn.10))</span></span>
-   <span data-ttu-id="4e37b-117">[DivisionUnits](/previous-versions/ms837954(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="4e37b-117">[DivisionUnits](/previous-versions/ms837954(v=msdn.10))</span></span>
-   <span data-ttu-id="4e37b-118">[Erkennungs Alternativen](/previous-versions/ms830115(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="4e37b-118">[RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))</span></span>
-   <span data-ttu-id="4e37b-119">[Erkennungen](/previous-versions/ms828520(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="4e37b-119">[Recognizers](/previous-versions/ms828520(v=msdn.10))</span></span>
-   <span data-ttu-id="4e37b-120">[Tablets](/previous-versions/ms827599(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="4e37b-120">[Tablets](/previous-versions/ms827599(v=msdn.10))</span></span>

## <a name="sta-and-mta-applications"></a><span data-ttu-id="4e37b-121">STA-und MTA-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="4e37b-121">STA and MTA Applications</span></span>

<span data-ttu-id="4e37b-122">Verwaltete Anwendungen, die mithilfe der in Microsoft Visual Studio .net enthaltenen Assistenten erstellt werden, sind standardmäßig Single Thread-Apartment (STA).</span><span class="sxs-lookup"><span data-stu-id="4e37b-122">Managed applications created by using the wizards contained in Microsoft Visual Studio .NET are single-threaded apartment (STA) by default.</span></span> <span data-ttu-id="4e37b-123">Sie können das Apartment für Ihre Anwendung ändern, indem Sie das STA-Thread-oder Multithread-Apartment-Thread Attribut (MTA) auf dem Einstiegspunkt der Anwendung festlegen.</span><span class="sxs-lookup"><span data-stu-id="4e37b-123">You can change the apartment for your application by setting the STA thread or multithreaded apartment (MTA) thread attribute on the entry point of your application.</span></span>

<span data-ttu-id="4e37b-124">Wenn Ihre Anwendung in einem MTA ausgeführt wird, müssen Sie Thread sicheren Code schreiben. auf diese Weise können Sie jedoch bestimmte Leistungsprobleme bei der Ereignis Behandlung verbessern.</span><span class="sxs-lookup"><span data-stu-id="4e37b-124">If your application runs in an MTA, you must write thread-safe code; however, by doing so you can improve certain event handling performance issues.</span></span>

<span data-ttu-id="4e37b-125">Weitere Informationen zu den STA-und MTA-Thread Attributen finden Sie unter " [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) Class" und " [mtathlesattribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) Class".</span><span class="sxs-lookup"><span data-stu-id="4e37b-125">For more information about the STA thread and MTA thread attributes, see [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) class and [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) Class.</span></span>

## <a name="windows-forms-threading-considerations"></a><span data-ttu-id="4e37b-126">Überlegungen zum Windows Forms Threading</span><span class="sxs-lookup"><span data-stu-id="4e37b-126">Windows Forms Threading Considerations</span></span>

<span data-ttu-id="4e37b-127">Die Steuerelemente [InkPicture](/previous-versions/aa514604(v=msdn.10)) und [InkEdit](/previous-versions/ms552265(v=vs.100)) erweitern Windows Forms-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="4e37b-127">The [InkPicture](/previous-versions/aa514604(v=msdn.10)) and [InkEdit](/previous-versions/ms552265(v=vs.100)) controls extend Windows Forms controls.</span></span> <span data-ttu-id="4e37b-128">Windows Forms Steuerelemente verwenden das STA-Modell (Single Thread-Apartment), da Windows Forms auf systemeigenen Win32-Fenstern basieren, die von Natur aus Single Thread sind.</span><span class="sxs-lookup"><span data-stu-id="4e37b-128">Windows Forms controls use the single-threaded apartment (STA) model because Windows Forms are based on native Win32 windows that are inherently single threaded.</span></span> <span data-ttu-id="4e37b-129">In verwaltetem Code sollten frei Hand Steuerelemente im gleichen Thread wie der Haupt Thread für das Formular erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4e37b-129">In managed code, ink controls should be created in the same thread as the main thread for the form.</span></span>

<span data-ttu-id="4e37b-130">In einer STA-Anwendung treten bestimmte Ereignisse in einem anderen Thread als dem Benutzeroberflächen Thread der Anwendung auf.</span><span class="sxs-lookup"><span data-stu-id="4e37b-130">In an STA application, certain events happen on a thread other than the application's user interface (UI) thread.</span></span> <span data-ttu-id="4e37b-131">Wenn Sie ein Windows Forms Objekt oder Steuerelement aufrufen, einschließlich der [InkPicture](/previous-versions/aa514604(v=msdn.10)) -und [InkEdit](/previous-versions/ms552265(v=vs.100)) -Steuerelemente, verwenden Sie in einem Tablet PC-Ereignishandler die geerbte [Control.](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) Call-Methode des-Objekts oder des-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="4e37b-131">When calling any Windows Forms object or control, including the [InkPicture](/previous-versions/aa514604(v=msdn.10)) and [InkEdit](/previous-versions/ms552265(v=vs.100)) controls, from within a Tablet PC event handler, use the object or control's inherited [Control.Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) method.</span></span> <span data-ttu-id="4e37b-132">Die [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) -Eigenschaft, die von der Control-Klasse geerbt wurde, kann verwendet werden, um zu bestimmen, ob dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4e37b-132">The [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) property, inherited from the Control class, can be used to determine if this is necessary.</span></span>

<span data-ttu-id="4e37b-133">Beispielsweise wird im folgenden Ereignishandler für das [Erkennungs](/previous-versions/ms829424(v=msdn.10)) Ereignis die [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) -Eigenschaft getestet, und wenn **true**, wird der Ereignishandler aus dem Benutzeroberflächen Thread erneut aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4e37b-133">For example, in the following event handler for the [Recognition](/previous-versions/ms829424(v=msdn.10)) event, the [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) property is tested and if **TRUE**, the event handler is re-invoked from the user interface thread.</span></span>


```C++
void recoContext_Recognition(object sender, 
        RecognizerContextRecognitionEventArgs e)
{
    if (InvokeRequired)
    {
        Invoke( new RecognizerContextRecognitionEventHandler(  
                     recoContext_Recognition ),
                    new object[] { sender, e } );
        return;
    }
     // Use the recognition result here.
}
```



<span data-ttu-id="4e37b-134">Wenn Sie ein [UserControl-Steuer](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) Element in einem Browser (siehe [websteuer Elemente](web-controls.md)) in awebpagein platzieren, wird es als STA-Anwendung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e37b-134">If you put a [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) onto awebpagein a browser (see [Web Controls](web-controls.md)), then it runs as an STA application.</span></span> <span data-ttu-id="4e37b-135">Für intelligente Client Anwendungen (siehe [keine Berührungs Bereitstellung](no-touch-deployment.md)) hat der Entwickler vollständige Kontrolle über den [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="4e37b-135">For smart client applications (see [No Touch Deployment](no-touch-deployment.md)), the developer has full control over the [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1).</span></span> <span data-ttu-id="4e37b-136">(Der Standardwert ist in der Regel STA, kann jedoch MTA sein, je nach Version der CLR.) Informationen zu Threading Problemen im Zusammenhang mit [**RealTimeStylus**](realtimestylus-class.md)finden Sie unter [Threading Überlegungen für die StylusInput-APIs](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="4e37b-136">(The default is generally STA, but may be MTA, depending on your version of CLR.) For threading issues involving the [**RealTimeStylus**](realtimestylus-class.md), see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

<span data-ttu-id="4e37b-137">Weitere Informationen zum Aufrufen von Windows Forms aus einer MTA-Anwendung finden Sie unter [Beispiel für Multithreaded Windows Forms Control](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).</span><span class="sxs-lookup"><span data-stu-id="4e37b-137">For more information about calling Windows Forms from an MTA application, see [Multithreaded Windows Forms Control Sample](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).</span></span>

## <a name="clipboard-considerations"></a><span data-ttu-id="4e37b-138">Überlegungen Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="4e37b-138">Clipboard Considerations</span></span>

<span data-ttu-id="4e37b-139">Das [Zwischenablage](../dataxchg/clipboard.md) Objekt funktioniert nur in einem STA-Thread.</span><span class="sxs-lookup"><span data-stu-id="4e37b-139">The [Clipboard](../dataxchg/clipboard.md) object works only from an STA thread.</span></span> <span data-ttu-id="4e37b-140">Wenn Sie versuchen, in einen Thread, der nicht STA ist, in die Zwischenablage zu kopieren oder aus der Zwischenablage einzufügen, erhalten Sie eine [ThreadStateException](/previous-versions/windows/).</span><span class="sxs-lookup"><span data-stu-id="4e37b-140">When trying to copy to or paste from the Clipboard from a thread that is not STA, you get a [ThreadStateException](/previous-versions/windows/).</span></span> <span data-ttu-id="4e37b-141">Wenn es sich bei der Anwendung um einen MTA handelt, erstellen Sie einen STA-Thread, um die Methodenaufrufe der Zwischenablage und einige andere Aspekte der Benutzeroberfläche Ihrer Anwendung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4e37b-141">If your application is MTA, create an STA thread to handle the Clipboard's method calls and some of the other UI aspects of your application.</span></span>

## <a name="exceptions-within-event-handlers"></a><span data-ttu-id="4e37b-142">Ausnahmen innerhalb von Ereignis Handlern</span><span class="sxs-lookup"><span data-stu-id="4e37b-142">Exceptions within Event Handlers</span></span>

<span data-ttu-id="4e37b-143">Ausnahmen können nicht innerhalb von Tablet PC-Ereignis Handlern ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4e37b-143">Exceptions cannot be thrown from within Tablet PC event handlers.</span></span> <span data-ttu-id="4e37b-144">Wenn z. b. ein Ereignishandlerdelegat für ein Tablet PC-Objekt oder eine Sammlung über drei registrierte Handler verfügt und der erste eine Ausnahme auslöst, wird die folgende Sequenz ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="4e37b-144">For example, if an event handler delegate for a Tablet PC object or collection has three registered handlers and the first one throws an exception, then the following sequence occurs:</span></span>

1.  <span data-ttu-id="4e37b-145">Der erste Handler wird beendet.</span><span class="sxs-lookup"><span data-stu-id="4e37b-145">The first handler exits.</span></span>
2.  <span data-ttu-id="4e37b-146">Die Ausnahme ist verloren gegangen.</span><span class="sxs-lookup"><span data-stu-id="4e37b-146">The exception is lost.</span></span>
3.  <span data-ttu-id="4e37b-147">Die verbleibenden Handler werden nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4e37b-147">The remaining handlers are not invoked.</span></span>

## <a name="disposing-objects-and-controls"></a><span data-ttu-id="4e37b-148">Verwerfen von Objekten und Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="4e37b-148">Disposing Objects and Controls</span></span>

<span data-ttu-id="4e37b-149">Um einen Speicher Verluste zu vermeiden, müssen Sie explizit [die verwerfen](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) -Methode für ein Tablet PC-Objekt oder-Steuerelement, an das ein Ereignishandler angefügt wurde, abrufen, bevor das Objekt oder das Steuerelement den Gültigkeitsbereich verlässt.</span><span class="sxs-lookup"><span data-stu-id="4e37b-149">To avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC object or control to which an event handler has been attached before the object or control goes out of scope.</span></span>

<span data-ttu-id="4e37b-150">Um die Leistung in Ihrer Anwendung zu verbessern, löschen Sie alle Tablet PC-Objekte oder Steuerelemente, die die verwerfen [-Methode implementieren](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) , manuell, wenn das Objekt oder Steuerelement nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="4e37b-150">To improve performance in your application, manually dispose of any Tablet PC object or control that implements the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method when the object or control is no longer needed.</span></span>

## <a name="stylusinput-apis"></a><span data-ttu-id="4e37b-151">StylusInput-APIs</span><span class="sxs-lookup"><span data-stu-id="4e37b-151">StylusInput APIs</span></span>

<span data-ttu-id="4e37b-152">Informationen zu Threading Überlegungen für das [**RealTimeStylus**](realtimestylus-class.md) -Objekt und die StylusInput-Anwendungs Programmierschnittstellen (APIs) finden Sie unter [Überlegungen zum Threading für die StylusInput-APIs](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="4e37b-152">For information about threading considerations for the [**RealTimeStylus**](realtimestylus-class.md) object and the StylusInput application programming interfaces (APIs) see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

 

 
