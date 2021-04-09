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
# <a name="tracelogging-cc-quick-start"></a>Tracelogging C/C++-Schnellstart

Im folgenden Abschnitt werden die grundlegenden Schritte beschrieben, die zum Hinzufügen von tracelogging zu nativem Code im Benutzermodus erforderlich sind.

## <a name="prerequisites"></a>Voraussetzungen

-   Windows 10
-   Microsoft Visual Studio 2013
-   Das Windows 10 Software Development Kit (SDK) ist erforderlich, um einen benutzermodusanbieter zu schreiben.
-   Das Windows-Treiberkit (WDK) für Windows 10 ist erforderlich, um einen kernelmodusanbieter zu schreiben.

> [!IMPORTANT]
> Verknüpfen Sie advapi32. lib, um diese Beispiele zu kompilieren.

### <a name="simpletraceloggingexampleh"></a>SimpleTraceLoggingExample. h

Dieser Beispiel Header enthält die tracelogging-APIs, und der Forward deklariert das Anbieter handle, das zum Protokollieren von Ereignissen verwendet wird. Alle Klassen, die tracelogging verwenden möchten, enthalten diesen Header und können dann die Protokollierung starten.

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

Die Header Datei enthält die Datei "traceloggingprovider. h", die die native tracelogging-API definiert. Sie müssen zuerst Windows. h einschließen, da es Konstanten definiert, die von "traceloggingprovider. h" verwendet werden.

Die Header Datei "Forward" deklariert das Anbieter Handle `g_hMyComponentProvider` , das Sie an die tracelogging-APIs übergeben, um Ereignisse zu protokollieren. Dieser Handle muss für jeden Code zugänglich sein, der tracelogging verwenden möchte.

[**Tracelogging \_ DECLARE \_ Provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) ist ein Makro, das ein `extern const TraceLoggingHProvider` Handle mit dem von Ihnen bereitgestellten Namen erstellt, das im obigen Beispiel lautet `g_hMyComponentProvider` . Die tatsächliche Anbieter handle-Variable wird in einer Codedatei zuzuordnen.

### <a name="simpletraceloggingexamplecpp"></a>SimpleTraceLoggingExample. cpp

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

Im obigen Beispiel ist SimpleTraceLoggingExample. h enthalten, das die globale Anbieter Variable enthält, die der Code zum Protokollieren von Ereignissen verwendet.

Das [**tracelogging \_ define \_ Provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) -Makro ordnet Speicher zu und definiert die Anbieter handle-Variable. Der Variablenname, den Sie für dieses Makro bereitstellen, muss mit dem Namen identisch sein, den Sie in der Header Datei im " [**tracelogging \_ Declare \_ Provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) "-Makro verwendet haben. Dieses Handle bleibt gültig, solange es sich im Gültigkeitsbereich befindet.

### <a name="register-the-provider-handle"></a>Registrieren des Anbieter Handles

Bevor Sie das Anbieter Handle zum Protokollieren von Ereignissen verwenden können, müssen Sie [**traceloggingregister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) aufzurufen, um das Anbieter Handle zu registrieren. Dies erfolgt in der Regel in "Main ()" oder "DllMain ()", kann jedoch jederzeit ausgeführt werden, solange der Versuch besteht, ein Ereignis zu protokollieren. Wenn Sie ein Ereignis protokollieren, bevor Sie das Anbieter handle registrieren, tritt kein Fehler auf, aber das Ereignis wird nicht protokolliert. Der folgende Code aus dem obigen Beispiel registriert das Anbieter handle.

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

### <a name="log-a-tracelogging-event"></a>Protokollieren eines tracelogging-Ereignisses

Nachdem der Anbieter registriert wurde, protokolliert der folgende Code ein einfaches Ereignis.

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

Das [**traceloggingwrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) -Makro nimmt bis zu 99 Argumente an und wird als mehrere-Anweisungen ausgeführt. Dies bedeutet, dass die protokollierten Werte keine temporären C++-Objekte sein sollten. Der Ereignis Name wird im UTF-8-Format gespeichert. Sie dürfen keine eingebetteten `null` Zeichen im Ereignis oder anderen Feldnamen verwenden. Es gibt keine weiteren Beschränkungen für zulässige Zeichen.

Jedes Argument, das auf den Ereignis Namen folgt, muss in einem [tracelogging-Wrapper Makro](tracelogging-wrapper-macros.md)umschlossen werden. Wenn Sie C++ verwenden, können Sie das `TraceLoggingValue` Wrapper Makro verwenden, um den Typ des Arguments automatisch abzuleiten. Wenn Sie den Treiber in C schreiben, müssen Sie typspezifische Feld Makros wie `TraceLoggingInt32` , `TraceLoggingUnicodeString` , `TraceLoggingString` usw. verwenden. Die tracelogging-Wrapper Makros werden in "traceloggingprovider. h" definiert.

Zusätzlich zur Protokollierung einzelner Ereignisse können Sie Ereignisse auch nach Aktivität gruppieren, indem Sie die in traceloggingactivity. h gefundenen traceloggingwrite- [**Activity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) -bzw. traceloggingwrite [**Testart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart)- / [](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) Makros verwenden. Aktivitäten korrelieren Ereignisse und sind nützlich für Szenarien mit einem Anfang und einem Ende. Beispielsweise können Sie eine Aktivität zum Messen eines Szenarios verwenden, das mit dem Starten einer Anwendung beginnt, einschließlich der Zeit, die für den Begrüßungsbildschirm benötigt wird, und endet, wenn der Startbildschirm der Anwendung sichtbar wird.

Aktivitäten erfassen einzelne Ereignisse und Schachteln andere Aktivitäten, die zwischen dem Anfang und dem Ende dieser Aktivität auftreten. Aktivitäten verfügen über einen prozessbezogenen Bereich und müssen vom Thread an den Thread übermittelt werden, um multithreadereignisse ordnungsgemäß zu schachteln.

Der Gültigkeitsbereich eines Anbieter Handles ist strikt auf das Modul (dll, exe oder sys-Datei) beschränkt, in dem es definiert ist – das Handle sollte nicht an andere DLLs übermittelt werden. Wenn ein [**traceloggingwrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) -Makro in A.DLL mithilfe eines in B.DLL definierten Anbieter Handles aufgerufen wird, kann dies zu Problemen führen. Die sicherste und effizienteste Methode, um diese Anforderung zu erfüllen, besteht darin, einfach direkt auf das Handle des globalen Anbieters zu verweisen und das Anbieter handle nie als Parameter zu übergeben.

### <a name="unregister-the-provider"></a>Aufheben der Registrierung des Anbieters

Wenn Sie mit dem Protokollieren von Ereignissen fertig sind, müssen Sie die Registrierung des tracelogging-Anbieters aufheben. Der folgende Code hebt die Registrierung des Anbieters auf.

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a>Kompatibilität

Abhängig von der Konfiguration kann traceloggingprovider. h abwärts kompatibel sein (kompatibel mit Windows Vista oder höher) oder für spätere Betriebssystemversionen optimiert werden. Traceloggingprovider. h verwendet winver (Benutzermodus) und NTDDI_VERSION (Kernel Modus), um zu bestimmen, ob es mit früheren Betriebssystemversionen kompatibel sein oder für neuere Betriebssystemversionen optimiert werden soll.

Wenn Sie für den Benutzermodus <Windows. h-> vor der Festlegung von WINVER einschließen, legt <Windows. h> winver auf die Standardversion des SDK-Betriebssystems fest. Wenn winver auf 0x602 oder höher festgelegt ist, optimiert traceloggingprovider. h das Verhalten für Windows 8 (Ihre APP wird unter früheren Versionen von Windows nicht ausgeführt). Wenn Sie Ihr Programm auf Vista oder Windows 7 ausführen müssen, stellen Sie sicher, dass winver auf den entsprechenden Wert festgelegt ist, bevor Sie <Windows. h-> einschließen.

Wenn Sie <WDM. h-> vor dem Festlegen von NTDDI_VERSION einschließen, wird von <WDM. h> auf einen Standardwert festgelegt. Wenn NTDDI_VERSION auf 0x06040000 oder höher festgelegt ist, optimiert traceloggingprovider. h das Verhalten für Windows 10 (der Treiber funktioniert nicht in früheren Versionen von Windows).

## <a name="summary-and-next-steps"></a>Zusammenfassung und nächste Schritte

Informationen zum Erfassen und Anzeigen von tracelogging-Daten mit den neuesten internen Versionen der Windows Performance Tools (WPT) finden Sie unter [aufzeichnen und Anzeigen von tracelogging-Ereignissen](tracelogging-record-and-display-tracelogging-events.md).

Weitere C++ tracelogging-Beispiele finden Sie unter [C/C++ tracelogging-Beispiele](tracelogging-c-cpp-tracelogging-examples.md) .

 

 




