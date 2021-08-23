---
title: TraceLogging C/C++-Schnellstart
description: Im folgenden Abschnitt werden die grundlegenden Schritte beschrieben, die zum Hinzufügen von TraceLogging zu nativem Benutzermoduscode erforderlich sind.
ms.assetid: 444DA34B-7949-457D-A3EC-2F0CFBEDD1E2
ms.topic: article
ms.date: 02/20/2020
ms.openlocfilehash: cb3734e3f314270e3d8082f5c9d25d38ce065829b94c659023950e5e2709047b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966499"
---
# <a name="tracelogging-cc-quick-start"></a>TraceLogging C/C++-Schnellstart

Im folgenden Abschnitt werden die grundlegenden Schritte beschrieben, die zum Hinzufügen von TraceLogging zu nativem Benutzermoduscode erforderlich sind.

## <a name="prerequisites"></a>Voraussetzungen

-   Windows 10
-   Microsoft Visual Studio 2013
-   Windows 10 Das Software Development Kit (SDK) ist erforderlich, um einen Benutzermodusanbieter zu schreiben.
-   Windows Driver Kit (WDK) für Windows 10 ist erforderlich, um einen Kernelmodusanbieter zu schreiben.

> [!IMPORTANT]
> Verknüpfen Sie advapi32.lib, um diese Beispiele zu kompilieren.

### <a name="simpletraceloggingexampleh"></a>SimpleTraceLoggingExample.h

Dieser Beispielheader enthält die TraceLogging-APIs und deklariert das Anbieterhandle, das zum Protokollieren von Ereignissen verwendet wird. Jede Klasse, die TraceLogging verwenden möchte, enthält diesen Header und kann dann mit der Protokollierung beginnen.

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

Die Headerdatei enthält TraceLoggingProvider.h, die die native TraceLogging-API definiert. Sie müssen zuerst Windows.h einschließen, da sie konstanten definiert, die von TraceLoggingProvider.h verwendet werden.

Die Headerdatei-Weiterleitung deklariert das Anbieterhandle, `g_hMyComponentProvider` das Sie an die TraceLogging-APIs übergeben, um Ereignisse zu protokollieren. Auf dieses Handle muss für jeden Code zugegriffen werden können, der TraceLogging verwenden möchte.

[**TRACELOGGING \_ DECLARE \_ PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) ist ein Makro, das ein `extern const TraceLoggingHProvider` Handle mit dem von Ihnen angegebenen Namen erstellt, der im obigen Beispiel `g_hMyComponentProvider` lautet. Sie ordnen die tatsächliche Anbieterhandlevariable in einer Codedatei zu.

### <a name="simpletraceloggingexamplecpp"></a>SimpleTraceLoggingExample.cpp

Im folgenden Beispiel wird der Anbieter registriert, ein Ereignis protokolliert und die Registrierung des Anbieters aufgehoben.

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

Das obige Beispiel enthält SimpleTraceLoggingExample.h, das die globale Anbietervariable enthält, die Ihr Code zum Protokollieren von Ereignissen verwendet.

Das [**TRACELOGGING \_ DEFINE \_ PROVIDER-Makro**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) ordnet Speicher zu und definiert die Anbieterhandlevariable. Der Variablenname, den Sie für dieses Makro angeben, muss mit dem Namen übereinstimmen, den Sie im [**TRACELOGGING \_ DECLARE \_ PROVIDER-Makro**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) in Ihrer Headerdatei verwendet haben. Dieses Handle bleibt gültig, solange es sich im Gültigkeitsbereich befindet.

### <a name="register-the-provider-handle"></a>Registrieren des Anbieterhandle

Bevor Sie das Anbieterhandle zum Protokollieren von Ereignissen verwenden können, müssen Sie [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) aufrufen, um Ihr Anbieterhandle zu registrieren. Dies erfolgt in der Regel in Main() oder DLLMain(), kann aber jederzeit erfolgen, solange es jedem Versuch vorausgeht, ein Ereignis zu protokollieren. Wenn Sie ein Ereignis protokollieren, bevor Sie das Anbieterhandle registrieren, tritt kein Fehler auf, aber das Ereignis wird nicht protokolliert. Der folgende Code aus dem obigen Beispiel registriert das Anbieterhandle.

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

### <a name="log-a-tracelogging-event"></a>Protokollieren eines Tracelogging-Ereignisses

Nachdem der Anbieter registriert wurde, protokolliert der folgende Code ein einfaches Ereignis.

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

Das [**TraceLoggingWrite-Makro**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) nimmt bis zu 99 Argumente entgegen und wird als mehrere Anweisungen ausgeführt. Dies bedeutet, dass es sich bei den protokollierten Werten nicht um temporäre C++-Objekte handelt. Der Ereignisname wird im UTF-8-Format gespeichert. Sie dürfen keine eingebetteten `null` Zeichen im Ereignis oder in anderen Feldnamen verwenden. Es gibt keine anderen Grenzwerte für zulässige Zeichen.

Jedes Argument, das auf den Ereignisnamen folgt, muss innerhalb eines [TraceLogging Wrapper-Makros](tracelogging-wrapper-macros.md)umschlossen werden. Wenn Sie C++ verwenden, können Sie das `TraceLoggingValue` Wrappermakro verwenden, um den Typ des Arguments automatisch abzuleitung. Wenn Sie Ihren Treiber in C schreiben, müssen Sie typspezifische Feldmakros wie `TraceLoggingInt32` , `TraceLoggingUnicodeString` , `TraceLoggingString` usw. verwenden. Die TraceLogging-Wrappermakros sind in TraceLoggingProvider.h definiert.

Zusätzlich zur Protokollierung einzelner Ereignisse können Sie Ereignisse auch nach Aktivität gruppieren, indem Sie die Makros [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) oder [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart) / [**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) in TraceLoggingActivity.h verwenden. Aktivitäten korrelieren Ereignisse und sind nützlich für Szenarien, die einen Anfang und ein Ende haben. Beispielsweise können Sie eine Aktivität verwenden, um ein Szenario zu messen, das mit dem Start einer Anwendung beginnt, die Zeit einschließt, die für die Bereitstellung des Begrüßungsbildschirms benötigt wird, und endet, wenn der Anfangsbildschirm der Anwendung sichtbar wird.

Aktivitäten erfassen einzelne Ereignisse und schachteln andere Aktivitäten, die zwischen dem Start und dem Ende dieser Aktivität auftreten. Aktivitäten haben einen Prozessbereich und müssen von Thread zu Thread übergeben werden, um Multithreadereignisse ordnungsgemäß zu schachteln.

Der Bereich eines Anbieterhandle ist streng auf das Modul (DLL, EXE oder SYS-Datei) beschränkt, in dem es definiert ist. Das Handle sollte nicht an andere DLLs übergeben werden. Wenn ein [**TraceLoggingWrite-Makro**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) in A.DLL mithilfe eines in B.DLL definierten Anbieterhandle aufgerufen wird, kann dies zu Problemen führen. Die sicherste und effizienteste Möglichkeit, diese Anforderung zu erfüllen, besteht darin, immer direkt auf das globale Anbieterhandle zu verweisen und das Anbieterhandle niemals als Parameter zu übergeben.

### <a name="unregister-the-provider"></a>Aufheben der Registrierung des Anbieters

Wenn Sie die Protokollierung von Ereignissen abgeschlossen haben, müssen Sie die Registrierung des TraceLogging-Anbieters aufheben. Mit dem folgenden Code wird die Registrierung des Anbieters aufgehoben.

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a>Kompatibilität

Abhängig von der Konfiguration kann TraceLoggingProvider.h abwärtskompatibel (kompatibel mit Windows Vista oder höher) oder für höhere Betriebssystemversionen optimiert werden. TraceLoggingProvider.h verwendet WINVER (Benutzermodus) und NTDDI_VERSION (Kernelmodus), um zu bestimmen, ob es mit früheren Betriebssystemversionen kompatibel oder für neuere Betriebssystemversionen optimiert werden soll.

Wenn Sie für den Benutzermodus <windows.h-> einschließen, bevor Sie WINVER festlegen, legt <windows.h> WINVER auf die Standardversion des ZIELbetriebssystem des SDK fest. Wenn WINVER auf 0x602 oder höher festgelegt ist, optimiert TraceLoggingProvider.h das Verhalten für Windows 8 (Ihre App wird nicht in früheren Versionen von Windows ausgeführt). Wenn Ihr Programm unter Vista oder Windows 7 ausgeführt werden soll, müssen Sie WINVER auf den entsprechenden Wert festlegen, bevor Sie <windows.h-> einschließen.

Wenn Sie <wdm.h-> einschließen, bevor Sie NTDDI_VERSION festlegen, legt <wdm.h> NTDDI_VERSION auf einen Standardwert fest. Wenn NTDDI_VERSION auf 0x06040000 oder höher festgelegt ist, optimiert TraceLoggingProvider.h das Verhalten für Windows 10 (Ihr Treiber funktioniert nicht mit früheren Versionen von Windows).

## <a name="summary-and-next-steps"></a>Zusammenfassung und nächste Schritte

Informationen zum Erfassen und Anzeigen von TraceLogging-Daten mithilfe der neuesten internen Versionen der Windows Performance Tools (WPT) finden Sie unter Aufzeichnen und Anzeigen von [TraceLogging-Ereignissen.](tracelogging-record-and-display-tracelogging-events.md)

Weitere [C++-TraceLogging-Beispiele](tracelogging-c-cpp-tracelogging-examples.md) finden Sie unter C/C++-Ablaufverfolgungsbeispiele.

 

 




