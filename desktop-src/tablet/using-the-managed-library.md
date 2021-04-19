---
description: Übersicht über die verwaltete Bibliothek und Hinweise zur Verwendung der von Tablet PC Platform verwalteten Bibliothek.
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: Verwenden der verwalteten Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1a1050705a6d74e6b183d04ec1c8f82d3954f0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106349754"
---
# <a name="using-the-managed-library"></a><span data-ttu-id="db220-103">Verwenden der verwalteten Bibliothek</span><span class="sxs-lookup"><span data-stu-id="db220-103">Using the Managed Library</span></span>

<span data-ttu-id="db220-104">Der Common Language Runtime ist die Grundlage des Microsoft .NET-Frameworks.</span><span class="sxs-lookup"><span data-stu-id="db220-104">The common language runtime is the foundation of the Microsoft .NET Framework.</span></span> <span data-ttu-id="db220-105">Sie können sich den Common Language Runtime als einen Agent vorstellen, der Code zur Ausführungszeit verwaltet, Kerndienste wie Speicherverwaltung, Thread Verwaltung und Remoting bereitstellt und gleichzeitig eine strikte Code Sicherheit erzwingt.</span><span class="sxs-lookup"><span data-stu-id="db220-105">You can think of the common language runtime as an agent that manages code at execution time, providing core services such as memory management, thread management, and remoting, while also enforcing strict code safety.</span></span> <span data-ttu-id="db220-106">Tatsächlich ist das Konzept der Code Verwaltung ein grundlegendes Prinzip der Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="db220-106">In fact, the concept of code management is a fundamental principle of the common language runtime.</span></span> <span data-ttu-id="db220-107">Code, der auf den Common Language Runtime abzielt, wird als verwalteter Code bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="db220-107">Code that targets the common language runtime is known as managed code.</span></span> <span data-ttu-id="db220-108">Code, der nicht auf den Common Language Runtime ausgerichtet ist, wird als nativer Code bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="db220-108">Code that does not target the common language runtime is known as native code.</span></span>

<span data-ttu-id="db220-109">Die Framework-Klassenbibliothek ist eine umfassende, objektorientierte Auflistung wiederverwendbarer Klassen, die Sie verwenden können, um Anwendungen zu entwickeln, die von herkömmlichen Befehlszeilen-oder grafischen Benutzeroberflächen Anwendungen (GUI) bis hin zu Anwendungen abhängig sind, die auf den neuesten Innovationen von ASP.net und Webdiensten basieren.</span><span class="sxs-lookup"><span data-stu-id="db220-109">The Framework class library is a comprehensive, object-oriented collection of reusable classes that you can use to develop applications ranging from traditional command-line or graphical user interface (GUI) applications to applications based on the latest innovations provided by ASP.NET and Web Services.</span></span>

<span data-ttu-id="db220-110">Die verwaltete Tablet PC-Bibliothek enthält eine Reihe verwalteter Objekte, die das Framework erweitern, um die Eingabe und Ausgabe der Handschrift auf Tablet PC sowie den Datenaustausch mit anderen Computern zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="db220-110">The Tablet PC Managed Library contains a set of managed objects that extends the Framework to provide support for input and output of handwriting on Tablet PC as well as data interchange with other computers.</span></span>

## <a name="exceptions"></a><span data-ttu-id="db220-111">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="db220-111">Exceptions</span></span>

<span data-ttu-id="db220-112">Die verwalteten Bibliotheksobjekte in der Tablet PC-API umschließen die Implementierungen der com-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="db220-112">The managed library objects in the Tablet PC API wrap the COM library implementations.</span></span> <span data-ttu-id="db220-113">Wenn das zugrunde liegende Objekt oder Steuerelement der com-Bibliothek einen Fehler zurückgibt, löst die verwaltete API eine Marshal. ThrowExceptionForHR-Ausnahme aus, die die Details der inneren com-Ausnahme bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="db220-113">When the underlying COM library object or control returns an error, the managed API's will throw a Marshal.ThrowExceptionForHR exception that provides the details on the inner COM exception.</span></span> <span data-ttu-id="db220-114">Weitere Informationen zu den möglichen Fehlern, die zurückgegeben werden können, finden Sie in der Referenz zu den HRESULT-Werten in der COM-Bibliotheks Referenz.</span><span class="sxs-lookup"><span data-stu-id="db220-114">You can refer to the HRESULT values in the COM Library Reference for details on the possible errors that may be returned.</span></span>

## <a name="object-comparison"></a><span data-ttu-id="db220-115">Objektvergleich</span><span class="sxs-lookup"><span data-stu-id="db220-115">Object Comparison</span></span>

<span data-ttu-id="db220-116">Für alle Objekte in der von Tablet PC Platform verwalteten Bibliothek wird gleich nicht außer Kraft gesetzt, um zwei gleich [**wertige**](/previous-versions/windows/) Objekte ordnungsgemäß zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="db220-116">For all objects in the Tablet PC Platform Managed library, [**Equals**](/previous-versions/windows/) is not overridden to correctly compare two objects that are the same.</span></span> <span data-ttu-id="db220-117">Die verwaltete Anwendungsprogrammierschnittstelle (API) unterstützt nicht den Vergleich von Objekten auf Gleichheit, entweder über die **Gleichheits** Funktion oder über den Gleichheits Operator (= =).</span><span class="sxs-lookup"><span data-stu-id="db220-117">The managed application programming interface (API) does not support the comparison of objects for equality, either through the **Equals** function or through the equals (==) operator.</span></span>

## <a name="binding-to-the-latest-microsoftinkdll"></a><span data-ttu-id="db220-118">Binden an den neuesten Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="db220-118">Binding to the Latest Microsoft.Ink.dll</span></span>

<span data-ttu-id="db220-119">Die neueste Microsoft.Ink.dll Assembly ist ein kompatibles Ersatz für Microsoft.Ink.dll Version 1,0 und Microsoft.Ink.15.dll.</span><span class="sxs-lookup"><span data-stu-id="db220-119">The latest Microsoft.Ink.dll assembly is a compatible replacement for Microsoft.Ink.dll version 1.0 and Microsoft.Ink.15.dll.</span></span> <span data-ttu-id="db220-120">In den meisten Fällen müssen Sie keine Änderungen an Ihren Anwendungen vornehmen, die mit den älteren Assemblys verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="db220-120">In most cases, you do not need to make any changes to your applications that are distributed with the older assemblies.</span></span> <span data-ttu-id="db220-121">In einigen Fällen müssen Sie jedoch das Common Language Runtime Lade Modul anweisen, die neuere Dynamic Link Library (dll) zu verwenden, wo immer auf die älteren DLLs verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="db220-121">However, in some cases you need to instruct the common language runtime loader to use the newer dynamic-link library (DLL) wherever the older DLLs have been referenced.</span></span>

<span data-ttu-id="db220-122">Das einzige Mal, dass Sie mithilfe der folgenden Vorgehensweise explizit an die neue Assembly binden müssen, ist, wenn Ihre Anwendung eine Komponente verwendet, die auf die Assembly der Version 1,0 oder 1,5 in Verbindung mit einer Komponente verweist, die auf eine neuere versionsassembly (z. b. 1,7) verweist, und wenn diese Komponenten Daten austauschen können.</span><span class="sxs-lookup"><span data-stu-id="db220-122">The only time you need to explicitly bind to the new assembly by using the following technique is if your application uses a component that references the version 1.0 or 1.5 assembly in combination with a component that references a more recent version assembly,such as 1.7, and if those components may exchange data.</span></span>

<span data-ttu-id="db220-123">Die beste Möglichkeit, den Common Language Runtime Loader anzuweisen, die neuere DLL zu verwenden, besteht darin, die Assemblyversionen auf Anwendungsebene umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="db220-123">The best way to instruct the common language runtime loader to use the newer DLL is to redirect assembly versions at the application level.</span></span> <span data-ttu-id="db220-124">Sie können angeben, dass Ihre Anwendung die neuere Version der Assembly verwendet, indem Sie Assemblybindungsinformationen in die Konfigurationsdatei der Anwendung einfügen.</span><span class="sxs-lookup"><span data-stu-id="db220-124">You can specify that your application use the newer version of the assembly by putting assembly binding information in your application's configuration file.</span></span> <span data-ttu-id="db220-125">Weitere Informationen zum Umleiten von Assemblyversionen auf Anwendungsebene finden Sie unter [umleiten](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue)von Assemblyversionen, insbesondere im Abschnitt "angeben der Assemblybindung in Konfigurationsdateien".</span><span class="sxs-lookup"><span data-stu-id="db220-125">For more information about redirecting assembly versions at the application level, see [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), specifically the section "Specifying Assembly Binding in Configuration Files."</span></span>

<span data-ttu-id="db220-126">Sie müssen eine Konfigurationsdatei im gleichen Verzeichnis wie die ausführbare Datei erstellen.</span><span class="sxs-lookup"><span data-stu-id="db220-126">You will need to create a configuration file in the same directory as your executable file.</span></span> <span data-ttu-id="db220-127">Die Konfigurationsdatei muss denselben Namen wie die ausführbare Datei aufweisen, gefolgt von der Dateierweiterung ". config".</span><span class="sxs-lookup"><span data-stu-id="db220-127">The configuration file must have the same name as your executable, followed by the .config file extension.</span></span> <span data-ttu-id="db220-128">Beispielsweise muss für eine Anwendung MyApp.exe die Konfigurationsdatei die MyApp.exe.config Datei sein.</span><span class="sxs-lookup"><span data-stu-id="db220-128">For example, for an application, MyApp.exe, the configuration file must be the MyApp.exe.config file.</span></span> <span data-ttu-id="db220-129">Die Konfigurationsdatei verwendet ein [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) -Element, um zu erzwingen, dass alle früheren Versionen der aktuellen Version zugeordnet werden, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="db220-129">The configuration file uses a [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) element to force all prior versions to be mapped to the latest version, as shown in the following example:</span></span>

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

<span data-ttu-id="db220-130">Weitere Informationen zu Konfigurationsdateien, einschließlich Beispielen zum Erstellen der Extensible Markup Language (XML) für die Konfigurationsdatei, finden Sie unter [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) und [umleiten](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue)von Assemblyversionen.</span><span class="sxs-lookup"><span data-stu-id="db220-130">For more information about configuration files, including examples of how to construct the Extensible Markup Language (XML) for the configuration file, see both [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) and [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).</span></span>

<span data-ttu-id="db220-131">Anwendungen, die mit Microsoft Windows XP Tablet PC Edition Development Kit 1,7 und höheren Versionen erstellt wurden, werden automatisch an die neue Version der Microsoft. Ink-Assembly gebunden.</span><span class="sxs-lookup"><span data-stu-id="db220-131">Applications created with Microsoft Windows XP Tablet PC Edition Development Kit 1.7 and later versions are automatically bound to the new version of the Microsoft.Ink assembly.</span></span> <span data-ttu-id="db220-132">Weitere Informationen zur Assemblybindung finden Sie [unter so](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp)sucht Common Language Runtime nach Assemblys.</span><span class="sxs-lookup"><span data-stu-id="db220-132">For more information about assembly binding see [How the Runtime Locates Assemblies](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).</span></span>

> [!Note]  
> <span data-ttu-id="db220-133">Die Verwendung der Anwendungs Richtlinie für die Bindung an die aktualisierte Assembly funktioniert nicht für Anwendungen, die die [Divider](/previous-versions/ms583616(v=vs.100)) - [Klasse oder die Klasse](/previous-versions/aa514041(v=msdn.10)) "-Klasse" verwenden.</span><span class="sxs-lookup"><span data-stu-id="db220-133">Using application policy to bind to the updated assembly does not work for applications that use the [Divider](/previous-versions/ms583616(v=vs.100)) class or the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) class.</span></span> <span data-ttu-id="db220-134">Anwendungen, die eine dieser Klassen verwenden, müssen entweder weiterhin Microsoft.Ink.15.dll verwenden oder nach Verweis auf die aktualisierte Assembly neu kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="db220-134">Applications that use either of those classes must either continue to use Microsoft.Ink.15.dll or be recompiled after referencing the updated assembly.</span></span>

 

## <a name="working-with-events"></a><span data-ttu-id="db220-135">Arbeiten mit Ereignissen</span><span class="sxs-lookup"><span data-stu-id="db220-135">Working with Events</span></span>

<span data-ttu-id="db220-136">Wenn der Code in einem Ereignishandler für eines der verwalteten Objekte eine Ausnahme auslöst, wird die Ausnahme nicht an den Benutzer übermittelt.</span><span class="sxs-lookup"><span data-stu-id="db220-136">If the code within an event handler for any of the managed objects throws an exception, the exception is not delivered to the user.</span></span> <span data-ttu-id="db220-137">Um sicherzustellen, dass Ausnahmen übermittelt werden, verwenden Sie try-catch-Blöcke in ihren Ereignis Handlern für verwaltete Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="db220-137">To ensure that exceptions are delivered, use try-catch blocks in your event handlers for managed events.</span></span>

## <a name="managing-forms"></a><span data-ttu-id="db220-138">Verwalten von Formularen</span><span class="sxs-lookup"><span data-stu-id="db220-138">Managing Forms</span></span>

<span data-ttu-id="db220-139">Die [Formular](/dotnet/api/system.windows.forms.form?view=netcore-3.1) Klasse und ihre Basisklassen definieren keinen Finalizer.</span><span class="sxs-lookup"><span data-stu-id="db220-139">The [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class and its base classes do not define a finalizer.</span></span> <span data-ttu-id="db220-140">Zum Bereinigen der Ressourcen in einem Formular schreiben Sie eine Unterklasse, die einen Finalizer (z. b. den C- \# debugtor mit ~) [bereitstellt,](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1)der "verwerfen" aufruft.</span><span class="sxs-lookup"><span data-stu-id="db220-140">To clean up your resources on a form, write a subclass that provides a finalizer (for example, the C\# destructor using the ~) that calls [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1).</span></span> <span data-ttu-id="db220-141">Um die Bereinigung durchzuführen, überschreibt der Finalizer den Löschvorgang und ruft dann die-Basisklasse ab.</span><span class="sxs-lookup"><span data-stu-id="db220-141">To do the cleanup the finalizer overrides Dispose and then calls the base class Dispose.</span></span> <span data-ttu-id="db220-142">Verweisen Sie nicht auf andere Objekte, die die [Finalize](/previous-versions/windows/) -Methode in der verwerfen-Methode benötigen, wenn der boolesche Parameter **false** ist, da diese Objekte möglicherweise bereits fertiggestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="db220-142">Do not refer to other objects that require the [Finalize](/previous-versions/windows/) method in the Dispose method when the Boolean parameter is **FALSE**, because those objects may already have been finalized.</span></span> <span data-ttu-id="db220-143">Weitere Informationen zum Freigeben von Ressourcen finden Sie unter [Finalize-Methoden und-debugktoren](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).</span><span class="sxs-lookup"><span data-stu-id="db220-143">For more information about releasing resources see [Finalize Methods and Destructors](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).</span></span>

## <a name="forms-and-the-recognizercontext"></a><span data-ttu-id="db220-144">Formulare und Erkennungs Kontext</span><span class="sxs-lookup"><span data-stu-id="db220-144">Forms and the RecognizerContext</span></span>

<span data-ttu-id="db220-145">[Erkenzercontext](/previous-versions/ms552546(v=vs.100)) -Ereignisse werden in einem anderen Thread als dem Thread ausgeführt, in dem sich das Formular befindet.</span><span class="sxs-lookup"><span data-stu-id="db220-145">[RecognizerContext](/previous-versions/ms552546(v=vs.100)) events run in a different thread than the thread that the form is on.</span></span> <span data-ttu-id="db220-146">Steuerelemente in Windows Forms sind an einen bestimmten Thread gebunden und sind nicht Thread sicher.</span><span class="sxs-lookup"><span data-stu-id="db220-146">Controls in Windows Forms are bound to a specific thread and are not thread safe.</span></span> <span data-ttu-id="db220-147">Daher müssen Sie eine der Methoden zum Aufrufen des Steuer Elements verwenden, um den Aufruf an den richtigen Thread zu Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="db220-147">Therefore, you must use one of the control's invoke methods to marshal the call to the proper thread.</span></span> <span data-ttu-id="db220-148">Vier Methoden in einem Steuerelement sind Thread sicher: die Methoden " [Aufruf](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1)", " [begincallback](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1)", " [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)" und " [forategraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) ".</span><span class="sxs-lookup"><span data-stu-id="db220-148">Four methods on a control are thread safe: the [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1), and [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) methods.</span></span> <span data-ttu-id="db220-149">Verwenden Sie für alle anderen Methodenaufrufe eine dieser Aufruf Methoden, wenn Sie von einem anderen Thread aufrufen.</span><span class="sxs-lookup"><span data-stu-id="db220-149">For all other method calls, use one of these invoke methods when calling from a different thread.</span></span> <span data-ttu-id="db220-150">Weitere Informationen zur Verwendung dieser Methoden finden Sie unter Bearbeiten [von Steuerelementen aus Threads](/previous-versions/757y83z4(v=vs.140)).</span><span class="sxs-lookup"><span data-stu-id="db220-150">For more information on using these methods, see [Manipulating Controls from Threads](/previous-versions/757y83z4(v=vs.140)).</span></span>

## <a name="waiting-for-events"></a><span data-ttu-id="db220-151">Warten auf Ereignisse</span><span class="sxs-lookup"><span data-stu-id="db220-151">Waiting for Events</span></span>

<span data-ttu-id="db220-152">Die Tablet PC-Umgebung ist multithreaded.</span><span class="sxs-lookup"><span data-stu-id="db220-152">The Tablet PC environment is multithreaded.</span></span> <span data-ttu-id="db220-153">Verwenden Sie die [**cowaitformultiplehandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) -Funktion anstelle von anderen Wait-Methoden, um die Eingabe von com-aufrufen (Re-Entrant Component Object Model) in Ihr Multithread-Apartment (MTA) zuzulassen, während die Anwendung auf ein Ereignis wartet.</span><span class="sxs-lookup"><span data-stu-id="db220-153">Use the [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) function instead of other wait methods to allow re-entrant Component Object Model (COM) calls to enter your multithreaded apartment (MTA) while your application is waiting on an event.</span></span>

## <a name="using-ink-strokes-collections"></a><span data-ttu-id="db220-154">Verwenden von Ink-Auflistungen</span><span class="sxs-lookup"><span data-stu-id="db220-154">Using Ink Strokes Collections</span></span>

<span data-ttu-id="db220-155">Instanzen von [Striche](/previous-versions/ms552701(v=vs.100)) -Auflistungen, die von einem [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekt abgerufen werden, werden nicht in die Garbage Collection</span><span class="sxs-lookup"><span data-stu-id="db220-155">Instances of [Strokes](/previous-versions/ms552701(v=vs.100)) collections which are obtained from an [Ink](/previous-versions/aa515768(v=msdn.10)) object are not garbage collected.</span></span> <span data-ttu-id="db220-156">Um einen Speicher Verluste zu vermeiden, verwenden Sie jedes Mal, wenn Sie mit einer dieser Auflistungen arbeiten, die using-Anweisung, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="db220-156">In order to avoid a memory leak, any time that you are working with one of these collections, make use of the "using" statement as shown below.</span></span>


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a><span data-ttu-id="db220-157">Verwerfen von verwalteten Objekten und Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="db220-157">Disposing Managed Objects and Controls</span></span>

<span data-ttu-id="db220-158">Um einen Speicher Verluste zu vermeiden, müssen Sie explizit [die verwerfen](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) -Methode für ein Tablet PC-Objekt oder-Steuerelement, an das ein Ereignishandler angefügt wurde, abrufen, bevor das Objekt oder das Steuerelement den Gültigkeitsbereich verlässt.</span><span class="sxs-lookup"><span data-stu-id="db220-158">To avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC object or control to which an event handler has been attached before the object or control goes out of scope.</span></span>

<span data-ttu-id="db220-159">Um die Leistung Ihrer Anwendung zu verbessern, müssen Sie die folgenden Objekte, Steuerelemente und Sammlungen manuell löschen, wenn Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="db220-159">To improve the performance of your application, manually dispose of the following objects, controls, and collection when they are no longer needed.</span></span>

-   <span data-ttu-id="db220-160">[Unter Teiler](/previous-versions/ms583616(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="db220-160">[Divider](/previous-versions/ms583616(v=vs.100))</span></span>
-   <span data-ttu-id="db220-161">[Freihand](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="db220-161">[Ink](/previous-versions/aa515768(v=msdn.10))</span></span>
-   <span data-ttu-id="db220-162">[InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="db220-162">[InkCollector](/previous-versions/ms583683(v=vs.100))</span></span>
-   <span data-ttu-id="db220-163">[InkEdit](/previous-versions/ms552265(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="db220-163">[InkEdit](/previous-versions/ms552265(v=vs.100))</span></span>
-   <span data-ttu-id="db220-164">[InkOverlay](/previous-versions/ms552322(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="db220-164">[InkOverlay](/previous-versions/ms552322(v=vs.100))</span></span>
-   <span data-ttu-id="db220-165">[InkPicture](/previous-versions/aa514604(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="db220-165">[InkPicture](/previous-versions/aa514604(v=msdn.10))</span></span>
-   <span data-ttu-id="db220-166">["Pendel Panel"](/previous-versions/aa514041(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="db220-166">[PenInputPanel](/previous-versions/aa514041(v=msdn.10))</span></span>
-   <span data-ttu-id="db220-167">[Erkennungs Kontext](/previous-versions/ms552546(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="db220-167">[RecognizerContext](/previous-versions/ms552546(v=vs.100))</span></span>
-   <span data-ttu-id="db220-168">[Striche](/previous-versions/ms552701(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="db220-168">[Strokes](/previous-versions/ms552701(v=vs.100))</span></span>

<span data-ttu-id="db220-169">Das folgende C- \# Beispiel veranschaulicht einige Szenarien, in [](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) denen die verwerfen-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db220-169">The following C\# example demonstrates some scenarios in which the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method is used.</span></span>


```C++
// A field for a Divider object
private Microsoft.Ink.Divider theDivider;

// A method that creates a Divider object
public void CreateDivider()
{
    // Make sure any previous Divider object was disposed of.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
    // Create the Divider object.
    theDivider = new Microsoft.Ink.Divider();

    // The remainder of the method
}

// A method that disposes of the Divider object
public void DisposeDivider()
{
    // The remainder of the method

    // Dispose of the Divider object.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
}

// A method that uses a local PenInputPanel object.
public void UsePenInputPanel()
{
    // Create the PenInputPanel object.
    Microsoft.Ink.PenInputPanel thePenInputPanel =
        new Microsoft.Ink.PenInputPanel();

    // The remainder of the method

    // Dispose of the PenInputPanel object before exiting.
    thePenInputPanel.Dispose();
    thePenInputPanel = null;
}
```



 

 