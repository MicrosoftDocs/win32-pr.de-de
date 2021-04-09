---
title: Tracelogging C/C++-Schnellstart
description: Im folgenden Abschnitt werden die grundlegenden Schritte beschrieben, die zum Hinzufügen von tracelogging zu nativem Code im Benutzermodus erforderlich sind.
ms.assetid: 444DA34B-7949-457D-A3EC-2F0CFBEDD1E2
ms.topic: article
ms.date: 02/20/2020
ms.openlocfilehash: 7be18feb7f372922b7e3b811cd0c9941240e18e3
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2020
ms.locfileid: "103948483"
---
# <a name="tracelogging-cc-quick-start"></a><span data-ttu-id="60721-103">Tracelogging C/C++-Schnellstart</span><span class="sxs-lookup"><span data-stu-id="60721-103">TraceLogging C/C++ Quick Start</span></span>

<span data-ttu-id="60721-104">Im folgenden Abschnitt werden die grundlegenden Schritte beschrieben, die zum Hinzufügen von tracelogging zu nativem Code im Benutzermodus erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="60721-104">The following section describes the basic steps required to add TraceLogging to native user-mode code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="60721-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="60721-105">Prerequisites</span></span>

-   <span data-ttu-id="60721-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="60721-106">Windows 10</span></span>
-   <span data-ttu-id="60721-107">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="60721-107">Microsoft Visual Studio 2013</span></span>
-   <span data-ttu-id="60721-108">Das Windows 10 Software Development Kit (SDK) ist erforderlich, um einen benutzermodusanbieter zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="60721-108">Windows 10 Software Development Kit (SDK) is required to write a user-mode provider</span></span>
-   <span data-ttu-id="60721-109">Das Windows-Treiberkit (WDK) für Windows 10 ist erforderlich, um einen kernelmodusanbieter zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="60721-109">Windows Driver Kit (WDK) for Windows 10 is required to write a kernel-mode provider</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60721-110">Verknüpfen Sie advapi32. lib, um diese Beispiele zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="60721-110">Link advapi32.lib in order to compile these examples.</span></span>

### <a name="simpletraceloggingexampleh"></a><span data-ttu-id="60721-111">SimpleTraceLoggingExample. h</span><span class="sxs-lookup"><span data-stu-id="60721-111">SimpleTraceLoggingExample.h</span></span>

<span data-ttu-id="60721-112">Dieser Beispiel Header enthält die tracelogging-APIs, und der Forward deklariert das Anbieter handle, das zum Protokollieren von Ereignissen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60721-112">This example header includes the TraceLogging APIs and forward declares the provider handle that will be used to log events.</span></span> <span data-ttu-id="60721-113">Alle Klassen, die tracelogging verwenden möchten, enthalten diesen Header und können dann die Protokollierung starten.</span><span class="sxs-lookup"><span data-stu-id="60721-113">Any class that wishes to use TraceLogging will include this header and can then start logging.</span></span>

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

<span data-ttu-id="60721-114">Die Header Datei enthält die Datei "traceloggingprovider. h", die die native tracelogging-API definiert.</span><span class="sxs-lookup"><span data-stu-id="60721-114">The header file includes TraceLoggingProvider.h which defines the native TraceLogging API.</span></span> <span data-ttu-id="60721-115">Sie müssen zuerst Windows. h einschließen, da es Konstanten definiert, die von "traceloggingprovider. h" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60721-115">You must include Windows.h first because it defines constants used by TraceLoggingProvider.h.</span></span>

<span data-ttu-id="60721-116">Die Header Datei "Forward" deklariert das Anbieter Handle `g_hMyComponentProvider` , das Sie an die tracelogging-APIs übergeben, um Ereignisse zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="60721-116">The header file forward declares the provider handle `g_hMyComponentProvider` that you will pass to the TraceLogging APIs to log events.</span></span> <span data-ttu-id="60721-117">Dieser Handle muss für jeden Code zugänglich sein, der tracelogging verwenden möchte.</span><span class="sxs-lookup"><span data-stu-id="60721-117">This handle needs to be accessible to any code that wishes to use TraceLogging.</span></span>

<span data-ttu-id="60721-118">[**Tracelogging \_ DECLARE \_ Provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) ist ein Makro, das ein `extern const TraceLoggingHProvider` Handle mit dem von Ihnen bereitgestellten Namen erstellt, das im obigen Beispiel lautet `g_hMyComponentProvider` .</span><span class="sxs-lookup"><span data-stu-id="60721-118">[**TRACELOGGING\_DECLARE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) is a macro that creates an `extern const TraceLoggingHProvider` handle using the name that you provide, which in the example above is `g_hMyComponentProvider`.</span></span> <span data-ttu-id="60721-119">Die tatsächliche Anbieter handle-Variable wird in einer Codedatei zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="60721-119">You will allocate the actual provider handle variable in a code file.</span></span>

### <a name="simpletraceloggingexamplecpp"></a><span data-ttu-id="60721-120">SimpleTraceLoggingExample. cpp</span><span class="sxs-lookup"><span data-stu-id="60721-120">SimpleTraceLoggingExample.cpp</span></span>

<span data-ttu-id="60721-121">Im folgenden Beispiel wird der Anbieter registriert, ein Ereignis protokolliert und die Registrierung des Anbieters aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="60721-121">The following example registers the provider, logs an event, and unregisters the provider.</span></span>

```C++
#include "SimpleTraceLoggingExample.h"

    // Define the GUID to use in TraceLoggingProviderRegister 
    // {3970F9cf-2c0c-4f11-b1cc-e3a1e9958833}
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyComponentProvider,
    "SimpleTraceLoggingProvider",
    (0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33));


void main()
{

    char sampleValue[] = "Sample value";

    // Register the provider
    TraceLoggingRegister(g_hMyComponentProvider);
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
}
```

<span data-ttu-id="60721-122">Im obigen Beispiel ist SimpleTraceLoggingExample. h enthalten, das die globale Anbieter Variable enthält, die der Code zum Protokollieren von Ereignissen verwendet.</span><span class="sxs-lookup"><span data-stu-id="60721-122">The example above includes SimpleTraceLoggingExample.h which contains the global provider variable that your code will use to log events.</span></span>

<span data-ttu-id="60721-123">Das [**tracelogging \_ define \_ Provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) -Makro ordnet Speicher zu und definiert die Anbieter handle-Variable.</span><span class="sxs-lookup"><span data-stu-id="60721-123">The [**TRACELOGGING\_DEFINE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) macro allocates storage and defines the provider handle variable.</span></span> <span data-ttu-id="60721-124">Der Variablenname, den Sie für dieses Makro bereitstellen, muss mit dem Namen identisch sein, den Sie in der Header Datei im " [**tracelogging \_ Declare \_ Provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) "-Makro verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="60721-124">The variable name that you provide to this macro must match the name you used in the [**TRACELOGGING\_DECLARE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) macro in your header file.</span></span> <span data-ttu-id="60721-125">Dieses Handle bleibt gültig, solange es sich im Gültigkeitsbereich befindet.</span><span class="sxs-lookup"><span data-stu-id="60721-125">This handle will remain valid as long as it is in scope.</span></span>

### <a name="register-the-provider-handle"></a><span data-ttu-id="60721-126">Registrieren des Anbieter Handles</span><span class="sxs-lookup"><span data-stu-id="60721-126">Register the provider handle</span></span>

<span data-ttu-id="60721-127">Bevor Sie das Anbieter Handle zum Protokollieren von Ereignissen verwenden können, müssen Sie [**traceloggingregister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) aufzurufen, um das Anbieter Handle zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="60721-127">Before you can use the provider handle to log events you must call [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) to register your provider handle.</span></span> <span data-ttu-id="60721-128">Dies erfolgt in der Regel in "Main ()" oder "DllMain ()", kann jedoch jederzeit ausgeführt werden, solange der Versuch besteht, ein Ereignis zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="60721-128">This is typically done in Main() or DLLMain() but can be done at any time as long as it precedes any attempt to log an event.</span></span> <span data-ttu-id="60721-129">Wenn Sie ein Ereignis protokollieren, bevor Sie das Anbieter handle registrieren, tritt kein Fehler auf, aber das Ereignis wird nicht protokolliert.</span><span class="sxs-lookup"><span data-stu-id="60721-129">If you log an event before registering the provider handle, no error will occur but the event will not be logged.</span></span> <span data-ttu-id="60721-130">Der folgende Code aus dem obigen Beispiel registriert das Anbieter handle.</span><span class="sxs-lookup"><span data-stu-id="60721-130">The following code from the example above registers the provider handle.</span></span>

```C++
    // Define the GUID to use in TraceLoggingProviderRegister 
    // {3970F9cf-2c0c-4f11-b1cc-e3a1e9958833}
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyComponentProvider,
    "SimpleTraceLoggingProvider",
    (0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33));


void main()
{

    char sampleValue[] = "Sample value";

    // Register the provider
    TraceLoggingRegister(g_hMyComponentProvider);
```

### <a name="log-a-tracelogging-event"></a><span data-ttu-id="60721-131">Protokollieren eines tracelogging-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="60721-131">Log a Tracelogging event</span></span>

<span data-ttu-id="60721-132">Nachdem der Anbieter registriert wurde, protokolliert der folgende Code ein einfaches Ereignis.</span><span class="sxs-lookup"><span data-stu-id="60721-132">After the provider is registered, the following code logs a simple event.</span></span>

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

<span data-ttu-id="60721-133">Das [**traceloggingwrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) -Makro nimmt bis zu 99 Argumente an und wird als mehrere-Anweisungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60721-133">The [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) macro takes up to ninety-nine arguments and executes as several statements.</span></span> <span data-ttu-id="60721-134">Dies bedeutet, dass die protokollierten Werte keine temporären C++-Objekte sein sollten.</span><span class="sxs-lookup"><span data-stu-id="60721-134">This means that the values being logged should not be C++ temporary objects.</span></span> <span data-ttu-id="60721-135">Der Ereignis Name wird im UTF-8-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="60721-135">The event name is stored in UTF-8 format.</span></span> <span data-ttu-id="60721-136">Sie dürfen keine eingebetteten `null` Zeichen im Ereignis oder anderen Feldnamen verwenden.</span><span class="sxs-lookup"><span data-stu-id="60721-136">You must not use embedded `null` characters in the event or other field names.</span></span> <span data-ttu-id="60721-137">Es gibt keine weiteren Beschränkungen für zulässige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="60721-137">There are no other limits on permitted characters.</span></span>

<span data-ttu-id="60721-138">Jedes Argument, das auf den Ereignis Namen folgt, muss in einem [tracelogging-Wrapper Makro](tracelogging-wrapper-macros.md)umschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="60721-138">Each argument following the event name must be wrapped inside of a [TraceLogging Wrapper Macro](tracelogging-wrapper-macros.md).</span></span> <span data-ttu-id="60721-139">Wenn Sie C++ verwenden, können Sie das `TraceLoggingValue` Wrapper Makro verwenden, um den Typ des Arguments automatisch abzuleiten.</span><span class="sxs-lookup"><span data-stu-id="60721-139">If you are using C++, you can use the `TraceLoggingValue` wrapper macro to automatically infer the type of the argument.</span></span> <span data-ttu-id="60721-140">Wenn Sie den Treiber in C schreiben, müssen Sie typspezifische Feld Makros wie `TraceLoggingInt32` , `TraceLoggingUnicodeString` , `TraceLoggingString` usw. verwenden. Die tracelogging-Wrapper Makros werden in "traceloggingprovider. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="60721-140">If you are writing your driver in C, you must use type-specific field macros such as `TraceLoggingInt32`, `TraceLoggingUnicodeString`, `TraceLoggingString`, etc. The TraceLogging wrapper macros are defined in TraceLoggingProvider.h</span></span>

<span data-ttu-id="60721-141">Zusätzlich zur Protokollierung einzelner Ereignisse können Sie Ereignisse auch nach Aktivität gruppieren, indem Sie die in traceloggingactivity. h gefundenen traceloggingwrite- [**Activity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) -bzw. traceloggingwrite [**Testart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart)- / [](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) Makros verwenden.</span><span class="sxs-lookup"><span data-stu-id="60721-141">In addition to logging single events you can also group events by activity by using the [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) or [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart)/[**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) macros found in TraceLoggingActivity.h.</span></span> <span data-ttu-id="60721-142">Aktivitäten korrelieren Ereignisse und sind nützlich für Szenarien mit einem Anfang und einem Ende.</span><span class="sxs-lookup"><span data-stu-id="60721-142">Activities correlate events and are useful for scenarios that have a beginning and an end.</span></span> <span data-ttu-id="60721-143">Beispielsweise können Sie eine Aktivität zum Messen eines Szenarios verwenden, das mit dem Starten einer Anwendung beginnt, einschließlich der Zeit, die für den Begrüßungsbildschirm benötigt wird, und endet, wenn der Startbildschirm der Anwendung sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="60721-143">For example, you might use an activity to measure a scenario that starts with the launch of an application, includes the time it takes for the splash screen becomes available, and ends when the initial screen of the application becomes visible.</span></span>

<span data-ttu-id="60721-144">Aktivitäten erfassen einzelne Ereignisse und Schachteln andere Aktivitäten, die zwischen dem Anfang und dem Ende dieser Aktivität auftreten.</span><span class="sxs-lookup"><span data-stu-id="60721-144">Activities capture single events and nest other activities that occur between the start and end of that activity.</span></span> <span data-ttu-id="60721-145">Aktivitäten verfügen über einen prozessbezogenen Bereich und müssen vom Thread an den Thread übermittelt werden, um multithreadereignisse ordnungsgemäß zu schachteln.</span><span class="sxs-lookup"><span data-stu-id="60721-145">Activities have per-process scope and must be passed from thread to thread to properly nest multi-threaded events.</span></span>

<span data-ttu-id="60721-146">Der Gültigkeitsbereich eines Anbieter Handles ist strikt auf das Modul (dll, exe oder sys-Datei) beschränkt, in dem es definiert ist – das Handle sollte nicht an andere DLLs übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="60721-146">The scope of a provider handle is strictly limited to the module (DLL, EXE, or SYS file) in which it is defined – the handle should not be passed to other DLLs.</span></span> <span data-ttu-id="60721-147">Wenn ein [**traceloggingwrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) -Makro in A.DLL mithilfe eines in B.DLL definierten Anbieter Handles aufgerufen wird, kann dies zu Problemen führen.</span><span class="sxs-lookup"><span data-stu-id="60721-147">If a [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) macro is invoked in A.DLL using a provider handle defined in B.DLL, it may cause problems.</span></span> <span data-ttu-id="60721-148">Die sicherste und effizienteste Methode, um diese Anforderung zu erfüllen, besteht darin, einfach direkt auf das Handle des globalen Anbieters zu verweisen und das Anbieter handle nie als Parameter zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="60721-148">The safest and most efficient way to meet this requirement is to just always directly reference the global provider handle and never pass the provider handle as a parameter.</span></span>

### <a name="unregister-the-provider"></a><span data-ttu-id="60721-149">Aufheben der Registrierung des Anbieters</span><span class="sxs-lookup"><span data-stu-id="60721-149">Unregister the provider</span></span>

<span data-ttu-id="60721-150">Wenn Sie mit dem Protokollieren von Ereignissen fertig sind, müssen Sie die Registrierung des tracelogging-Anbieters aufheben.</span><span class="sxs-lookup"><span data-stu-id="60721-150">When you are finished logging events you must unregister the TraceLogging provider.</span></span> <span data-ttu-id="60721-151">Der folgende Code hebt die Registrierung des Anbieters auf.</span><span class="sxs-lookup"><span data-stu-id="60721-151">The following code unregisters the provider.</span></span>

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a><span data-ttu-id="60721-152">Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="60721-152">Compatibility</span></span>

<span data-ttu-id="60721-153">Abhängig von der Konfiguration kann traceloggingprovider. h abwärts kompatibel sein (kompatibel mit Windows Vista oder höher) oder für spätere Betriebssystemversionen optimiert werden.</span><span class="sxs-lookup"><span data-stu-id="60721-153">Depending on its configuration, TraceLoggingProvider.h can be backwards-compatible (compatible with Windows Vista or later), or can be optimized for later OS versions.</span></span> <span data-ttu-id="60721-154">Traceloggingprovider. h verwendet winver (Benutzermodus) und NTDDI_VERSION (Kernel Modus), um zu bestimmen, ob es mit früheren Betriebssystemversionen kompatibel sein oder für neuere Betriebssystemversionen optimiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="60721-154">TraceLoggingProvider.h uses WINVER (user mode) and NTDDI_VERSION (kernel mode) to determine whether it should be compatible with earlier OS versions or be optimized for newer OS versions.</span></span>

<span data-ttu-id="60721-155">Wenn Sie für den Benutzermodus <Windows. h-> vor der Festlegung von WINVER einschließen, legt <Windows. h> winver auf die Standardversion des SDK-Betriebssystems fest.</span><span class="sxs-lookup"><span data-stu-id="60721-155">For user-mode, if you include <windows.h> before setting WINVER, <windows.h> sets WINVER to the SDK's default target OS version.</span></span> <span data-ttu-id="60721-156">Wenn winver auf 0x602 oder höher festgelegt ist, optimiert traceloggingprovider. h das Verhalten für Windows 8 (Ihre APP wird unter früheren Versionen von Windows nicht ausgeführt).</span><span class="sxs-lookup"><span data-stu-id="60721-156">If WINVER is set to 0x602 or higher, TraceLoggingProvider.h optimizes its behavior for Windows 8 (your app will not run on earlier versions of Windows).</span></span> <span data-ttu-id="60721-157">Wenn Sie Ihr Programm auf Vista oder Windows 7 ausführen müssen, stellen Sie sicher, dass winver auf den entsprechenden Wert festgelegt ist, bevor Sie <Windows. h-> einschließen.</span><span class="sxs-lookup"><span data-stu-id="60721-157">If you need your program to run on Vista or Windows 7, be sure to set WINVER to the appropriate value before including <windows.h>.</span></span>

<span data-ttu-id="60721-158">Wenn Sie <WDM. h-> vor dem Festlegen von NTDDI_VERSION einschließen, wird von <WDM. h> auf einen Standardwert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60721-158">Similarly, if you include <wdm.h> before setting NTDDI_VERSION, <wdm.h> sets NTDDI_VERSION to a default value.</span></span> <span data-ttu-id="60721-159">Wenn NTDDI_VERSION auf 0x06040000 oder höher festgelegt ist, optimiert traceloggingprovider. h das Verhalten für Windows 10 (der Treiber funktioniert nicht in früheren Versionen von Windows).</span><span class="sxs-lookup"><span data-stu-id="60721-159">If NTDDI_VERSION is set to 0x06040000 or higher, TraceLoggingProvider.h optimizes its behavior for Windows 10 (your driver will not work on earlier versions of Windows).</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="60721-160">Zusammenfassung und nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="60721-160">Summary and next steps</span></span>

<span data-ttu-id="60721-161">Informationen zum Erfassen und Anzeigen von tracelogging-Daten mit den neuesten internen Versionen der Windows Performance Tools (WPT) finden Sie unter [aufzeichnen und Anzeigen von tracelogging-Ereignissen](tracelogging-record-and-display-tracelogging-events.md).</span><span class="sxs-lookup"><span data-stu-id="60721-161">To see how to capture and view TraceLogging data using the latest internal versions of the Windows Performance Tools (WPT), see [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md).</span></span>

<span data-ttu-id="60721-162">Weitere C++ tracelogging-Beispiele finden Sie unter [C/C++ tracelogging-Beispiele](tracelogging-c-cpp-tracelogging-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="60721-162">See [C/C++ Tracelogging Examples](tracelogging-c-cpp-tracelogging-examples.md) for more C++ TraceLogging examples.</span></span>

 

 




