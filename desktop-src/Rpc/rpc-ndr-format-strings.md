---
title: RPC-NDR-Formatzeichenfolgen
description: RPC-Formatzeichenfolgen (Remote Procedure Call, Remoteprozeduraufruf).
ms.assetid: 9c83a039-49d3-491d-8110-29d1548730de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a481e2c992f3fd4dda2d5552fbbabb7e9b01e6eb639a092e25ba9a26bd59a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926304"
---
# <a name="rpc-ndr-format-strings"></a>RPC-NDR-Formatzeichenfolgen

## <a name="ndr-engine-32-bit-interpreter"></a>NDR-Engine: 32-Bit-Interpreter

In diesem Dokument werden die Formatzeichenfolgendeskriptoren für die 32-Bit-NDR-Engine beschrieben, die manchmal auch als MOPs bezeichnet werden. In diesem Abschnitt werden Änderungen im Zusammenhang mit der Entwicklung vom [**–Oi-Interpreter**](/windows/desktop/Midl/-oi) zur **–Oif-Interpreterebene** sowie Ergänzungen im Zusammenhang mit Pipes und asynchroner Unterstützung beschrieben.

In diesem Dokument werden die Microsoft Interface Definition Language (MIDL)-Technologie aus Der Engine-Perspektive und die aktuelle NDR-Engine beschrieben.

## <a name="overview"></a>Übersicht

Die NDR-Engine ist die Marshalling-Engine der RPC- (Remote Procedure Call) und DCOM-Komponenten. Er behandelt alle Stub-bezogenen Probleme eines Remoteaufrufs. Als Prozess wird das NDR-Marshalling durch den C-Code aus MIDL-generierten Stubs, einem MIDL JIT-Typgenerator oder durch Stubs gesteuert, die von anderen Tools generiert oder manuell geschrieben wurden. Die NDR-Engine steuert wiederum die zugrunde liegende Laufzeit (DCOM oder RPC), die mit bestimmten Transporten kommuniziert.

Das ursprüngliche Ziel des Entwurfs war es, ein Tool für effektives Marshalling für beliebige Daten basierend auf den vom MIDL-Compiler bereitgestellten Informationen zu bieten. Die in diesem Dokument beschriebenen Formatzeichenfolgen – und tatsächlich alle vom Compiler für die NDR-Engine-Verbrauch generierten Informationen – wurden immer als interne Schnittstelle zwischen dem Compiler und der Engine betrachtet. Ebenso sind schnittstellen, die der Engine zur Behandlung von Laufzeitproblemen zur Verfügung stehen, größtenteils intern (einige Ausnahmen sind auf der RPC-Laufzeitseite vorhanden, und einige von der Engine verwendete DCOM-Schnittstellen sind extern).

Zwei typische Ansätze für das Marshalling waren immer Inline- und datengesteuerte (interpretierte) Technologien. MIDL unterstützt sowohl über die [**Schalter "-Os"**](/windows/desktop/Midl/-os) als auch [**"-Oi" \***](/windows/desktop/Midl/-oi) in den von C generierten Stubs. Darüber hinaus kann MIDL die vom oleautomation-Paket verwendeten TLB-Bibliotheken generieren. Entsprechend besteht eine Perspektive der Internen der Engine darin, dass sie aus zwei Teilen besteht.

Die erste ist eine Reihe von Routinen, die Größen- und Marshallingaufgaben verarbeiten, die typischen Datentypobjekten wie einer Struktur oder einem Array entspricht. Diese Routinen sind für die Leistung optimiert. Beispielsweise versuchen sie in der Regel, das Kopieren von Daten nach Möglichkeit zu blockieren. Dieser Teil wird häufig als NDR-Kern-Engine bezeichnet.

Der zweite Teil besteht aus einem Interpreter und den zugehörigen Teilen. Der Interpreter verwendet Routinen aus der NDR-Kern-Engine wie aus einer internen Bibliothek, um einen Remoteaufruf auszuführen, bei dem alle Argumente gemarshallt und nicht gemarshallt werden.

Die NDR-Kern-Engine wird auf ähnliche Weise verwendet, unabhängig davon, ob sie von Inlinestubs oder vom Interpreter verwendet wird. Alle Kern-Engine-Routinen hängen vom Zustand ab, der von einer Stubnachrichtenstruktur übergeben wird. Die -Struktur wird entsprechend durch den Inlinestub oder den Interpreter eingerichtet. Im Laufe der Jahre wurde die Kern-Engine in einem anderen Kontext verwendet. Derzeit besteht der Interpreter tatsächlich aus mehreren unterschiedlichen Interpreterschleifen. Diese stehen im Zusammenhang mit den alten und neuen Interpretern [**(–Oi**](/windows/desktop/Midl/-oi) im Vergleich zu **–Oif)** sowie mit Schleifen im Zusammenhang mit datenserialisierung (Pickling), rpc-asynchroner Unterstützung und Asynchroner DCOM-Unterstützung (RPC und DCOM verfügen über unterschiedliche asynchrone Programmiermodelle).

Abgesehen von neuen Features ist ein wichtiger Aspekt der Entwicklung der NDR-Engine eine allgemeine Verschiebung des Interpreteransatzes. NDR Version 1.1 begann im Rahmen eines neuen MIDL 2.0-Ansatzes für das Marshalling, bei dem die Inlinestubs aus Leistungsaspekten bevorzugt wurden. Mit der neuesten Version von NDR ist [**–Oif**](/windows/desktop/Midl/-oi) zum am häufigsten verwendeten Modus des Compilers geworden, fast bis zum Ausschluss von Inlinestubs.

Formatzeichenfolgendeskriptoren der RPC-NDR-Engine werden in den folgenden Themen ausführlicher beschrieben:

-   [Formatzeichenfolgen](format-strings.md)
-   [Prozedurformatzeichenfolgen](procedure-format-strings.md)
-   [Prozedurheaderdeskriptor](procedure-header-descriptor.md)
-   [Ziehpunkte](handles.md)
-   [Der Header](the-header.md)
-   [Parameterdeskriptoren](parameter-descriptors.md)
-   [Typformatzeichenfolgen](type-format-strings.md)

 

 