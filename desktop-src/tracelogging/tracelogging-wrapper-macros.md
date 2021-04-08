---
title: Tracelogging-Wrapper Makros
description: Listet die Wrapper Makros für tracelogging-Anbieter auf.
ms.assetid: 806F43F3-D376-4DBD-A4C5-B5F01E5D009D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc28b3a35074089b1f5c613b041534b8b282423
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714153"
---
# <a name="tracelogging-wrapper-macros"></a>Tracelogging-Wrapper Makros

Listet die Wrapper Makros für tracelogging-Anbieter auf.

Um Ereignisse mit tracelogging-Anbietern aufzuzeichnen, müssen Sie die tracelogging-Schreib Makros [**traceloggingwrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) oder [**traceloggingschreiteactivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity)verwenden. Beide Makros erfordern, dass Sie alle Ereignisdaten in einem Wrapper Makro umschließen. Es gibt mehrere unterschiedliche Wrapper Makros für verschiedene Datentypen. Eine komplette Liste der tracelogging-Makros finden Sie unter [tracelogging-Makros](trace-logging-macros.md).

Zusätzlich zu den obigen Wrapper Makros sind mehrere Makros für einzelne Datentypen verfügbar. Alle diese Makros haben das gleiche Format wie das [traceloggingvalue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) -Makro. Sie können das traceloggingvalue-Makro verwenden, um automatisch das entsprechende zu verwendende Wrapper Makro zu erkennen, oder Sie können das spezifische Makro direkt verwenden.

-   [**Traceloggingbinary**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingbinary)
-   [**Traceloggingchannel**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingchannel)
-   [**Traceloggingcustomattribute**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingcustomattribute)
-   [**Traceloggingdescription**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingdescription)
-   [**Traceloggingeventtag**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingeventtag)
-   [**Traceloggingschlüsselwort**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingkeyword)
-   [**Tracelogginglevel**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogginglevel)
-   [**Traceloggingopcode**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingopcode)
-   [**Traceloggingsocketaddress**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingsocketaddress)
-   [**Traceloggingstruct**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingstruct)
-   [**Traceloggingvalue**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue)

> [!Note]
>
> **Traceloggingoptiongroup** ist speziell für die Verwendung innerhalb des tracelogging- \_ \_ Anbieters definiert.
>
> -   [**Traceloggingoptiongroup**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup)

 

Im folgenden finden Sie die einzelnen Wrapper Makros.

-   TraceLoggingInt8

-   TraceLoggingUInt8

-   TraceLoggingInt16

-   TraceLoggingUInt16

-   TraceLoggingInt32

-   TraceLoggingUInt32

-   TraceLoggingInt64

-   TraceLoggingUInt64

-   TraceLoggingFloat32

-   TraceLoggingFloat64

-   Traceloggingbool

-   Traceloggingfiletime

-   Traceloggingguid

-   Traceloggingpointer

-   Traceloggingsystemtime

-   TraceLoggingHexInt8

-   TraceLoggingHexUInt8

-   TraceLoggingHexInt32

-   TraceLoggingHexUInt32

-   TraceLoggingHexInt64

-   TraceLoggingHexUInt64

-   Traceloggingwchar

-   Traceloggingchar

-   Traceloggingintptr

-   Tracelogginguintptr

-   Traceloggingboolean

-   TraceLoggingHexInt16

-   TraceLoggingHexUInt16

-   Traceloggingpid

-   Traceloggingtid

-   Traceloggingport

-   Traceloggingwinerror

-   Traceloggingntstatus

-   Tracelogginghresult

-   Traceloggingsocketaddress

-   Traceloggingsid

-   Traceloggingstring

-   Traceloggingwidestring

-   Traceloggingzähltedstring

-   Traceloggingzähltedwientstring

-   Traceloggingansistring

-   Traceloggingunicodestring

-   Traceloggingbinary (void- \* Daten, Größe der Daten in Bytes, \[ Optionaler \] Name) die Parameter für dieses Makro unterscheiden sich von den oben genannten. Wenn der *Name* -Parameter angegeben wird, muss es sich um ein Zeichenfolgenliteral (keine Variable) handeln, und es darf keine eingebetteten NULL-Zeichen enthalten. Wenn der *Name* -Parameter nicht angegeben wird, wird automatisch ein Name generiert.

Die tracelogging-API stellt auch mehrere Makros für Arrays zur Verfügung. Diese Arrays können abhängig vom Wrapper Makro, das Sie verwenden möchten, entweder eine Fixed-Länge aufweisen oder eine Variable Länge aufweisen. Alle diese Wrapper Makros folgen diesem Format.

`TraceLoggingBooleanArray(pVals, cVals, name, desc, tags)`

Der Parameter *pvals* verweist auf das Daten *Array und gibt* die Anzahl der Elemente im Array an. *cvals* müssen eine Konstante sein und dürfen keine Variable sein. Wie bei den Einzelwert-Wrapper Makros sind *Name*, **DESC** und *Tags* optionale Parameter und müssen dieselben Einschränkungen einhalten wie das **traceloggingvalue** -Makro.

-   TraceLoggingInt8FixedArray

-   TraceLoggingUInt8FixedArray

-   TraceLoggingInt16FixedArray

-   TraceLoggingUInt16FixedArray

-   TraceLoggingInt32FixedArray

-   TraceLoggingUInt32FixedArray

-   TraceLoggingInt64FixedArray

-   TraceLoggingUInt64FixedArray

-   TraceLoggingFloat32FixedArray

-   TraceLoggingFloat64FixedArray

-   Traceloggingboolfixedarray

-   Traceloggingguidfixedarray

-   Traceloggingpointerfixedarray

-   Traceloggingfiletimefixedarray

-   Traceloggingsystemtimefixedarray

-   TraceLoggingHexInt8FixedArray

-   TraceLoggingHexUInt8FixedArray

-   TraceLoggingHexInt32FixedArray

-   TraceLoggingHexUInt32FixedArray

-   TraceLoggingHexInt64FixedArray

-   TraceLoggingHexUInt64FixedArray

-   Traceloggingwcharfixedarray

-   Traceloggingcharfixedarray

-   Traceloggingintptrfixedarray

-   Tracelogginguintptrfixedarray

-   Traceloggingbooleanfixedarray

-   TraceLoggingHexInt16FixedArray

-   TraceLoggingHexUInt16FixedArray

-   TraceLoggingInt8Array

-   TraceLoggingUInt8Array

-   TraceLoggingInt16Array

-   TraceLoggingUInt16Array

-   TraceLoggingInt32Array

-   TraceLoggingUInt32Array

-   TraceLoggingInt64Array

-   TraceLoggingUInt64Array

-   TraceLoggingFloat32Array

-   TraceLoggingFloat64Array

-   Traceloggingboolarray

-   Traceloggingguidarray

-   Traceloggingpointerarray

-   Traceloggingfiletimearray

-   Traceloggingsystemtimearray

-   TraceLoggingHexInt8Array

-   TraceLoggingHexUInt8Array

-   TraceLoggingHexInt32Array

-   TraceLoggingHexUInt32Array

-   TraceLoggingHexInt64Array

-   TraceLoggingHexUInt64Array

-   Traceloggingwchararray

-   Traceloggingchararray

-   Traceloggingintptrarray

-   Tracelogginguintptrarray

-   Traceloggingbooleanarray

-   TraceLoggingHexInt16Array

-   TraceLoggingHexUInt16Array

 

 




