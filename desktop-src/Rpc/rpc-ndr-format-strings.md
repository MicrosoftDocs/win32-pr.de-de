---
title: RPC-NDR-Formatzeichenfolgen
description: RPC-Formatzeichenfolgen (Remote Procedure Call).
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

Dieses Dokument beschreibt die Formatzeichenfolgendeskriptoren, die manchmal als MOPs bezeichnet werden, für die 32-Bit-NDR-Engine. In diesem Abschnitt werden Änderungen im Zusammenhang mit der Weiterentwicklung des [**–Oi-Interpreters**](/windows/desktop/Midl/-oi) zur **–Oif-Interpreterebene** sowie Ergänzungen im Zusammenhang mit Pipes und asynchroner Unterstützung beschrieben.

In diesem Dokument werden die aktuelle midl-Technologie (Microsoft Interface Definition Language) aus Engine-Sicht und die aktuelle NDR-Engine beschrieben.

## <a name="overview"></a>Übersicht

Die NDR-Engine ist die Marshalling-Engine der RPC- (Remote Procedure Call) und DCOM-Komponenten. Er behandelt alle stubbezogenen Probleme eines Remoteaufrufs. Als Prozess wird das NDR-Marshalling durch den C-Code von MIDL-generierten Stubs, einem MIDL-JIT-Generator oder von Stubs gesteuert, die von anderen Tools generiert oder manuell geschrieben wurden. Die NDR-Engine steuert wiederum die zugrunde liegende Laufzeit (DCOM oder RPC), die mit bestimmten Transporten kommuniziert.

Das ursprüngliche Ziel des Entwurfs war es, ein Tool für effektives Marshalling für beliebige Daten bereitzustellen, basierend auf den vom MIDL-Compiler bereitgestellten Informationen. Die in diesem Dokument beschriebenen Formatzeichenfolgen – und tatsächlich alle vom Compiler für den NDR-Engine-Verbrauch generierten Informationen – wurden immer als interne Schnittstelle zwischen dem Compiler und der Engine betrachtet. Ebenso sind Schnittstellen, die der Engine zur Behandlung von Laufzeitproblemen zur Verfügung stehen, größtenteils intern (einige Ausnahmen sind auf der RPC-Laufzeitseite vorhanden, und einige von der Engine verwendete DCOM-Schnittstellen sind extern).

Zwei typische Ansätze für das Marshalling waren schon immer Inline- und datengesteuerte (interpretierte) Technologien. MIDL unterstützt beide über die Schalter [**"-Os"**](/windows/desktop/Midl/-os) und [**"-Oi" \***](/windows/desktop/Midl/-oi) in den C-generierten Stubs. Darüber hinaus kann MIDL die TLB-Bibliotheken generieren, die vom oleautomation-Paket verwendet werden. Entsprechend besteht eine Perspektive der Internen der Engine darin, dass sie aus zwei Teilen besteht.

Die erste ist eine Reihe von Routinen, die Größenangaben, Marshalling usw. verarbeiten, die typischen Datentypobjekten wie einer Struktur oder einem Array entsprechen. Diese Routinen sind für die Leistung optimiert. Beispielsweise versuchen sie in der Regel, Daten nach Möglichkeit zu blockieren. Dieser Teil wird häufig als NDR-Kern-Engine bezeichnet.

Der zweite Teil besteht aus einem Interpreter und den zugehörigen Teilen. Der Interpreter verwendet Routinen aus der NDR-Kern-Engine wie aus einer internen Bibliothek, um einen Remoteaufruf mit allen zugehörigen gemarshallten und unmarshaled-Argumenten auszuführen.

Die NDR-Kern-Engine wird auf ähnliche Weise verwendet, unabhängig davon, ob sie von Inlinestubs oder vom Interpreter verwendet wird. Alle Kern-Engine-Routinen hängen vom Zustand ab, der von einer Stubnachrichtenstruktur übergeben wird. Die -Struktur wird durch den Inlinestub oder den Interpreter entsprechend eingerichtet. Im Laufe der Jahre wurde die Kern-Engine in einem anderen Kontext verwendet. derzeit ist der Interpreter tatsächlich ein Satz von mehreren unterschiedlichen Interpreterschleifen. Diese beziehen sich auf die alten und neuen Interpreter ([**–Oi**](/windows/desktop/Midl/-oi) im Vergleich zu **–Oif**) sowie auf Schleifen im Zusammenhang mit der Datenserialisierung (Pickling), der asynchronen RPC-Unterstützung und der Asynchronen DCOM-Unterstützung (RPC und DCOM haben unterschiedliche asynchrone Programmiermodelle).

Neben dem Hinzufügen neuer Features ist ein wichtiger Aspekt der Weiterentwicklung der NDR-Engine eine allgemeine Verschiebung des Ansatzes zu Interpretern. Version 1.1 von NDR begann im Rahmen eines neuen MIDL 2.0-Marshallingansatzes, wobei die Inlinestubs aus Leistungsgründen bevorzugt wurden. Mit der neuesten Version von NDR ist [**–Oif**](/windows/desktop/Midl/-oi) zum am häufigsten verwendeten Modus des Compilers geworden, fast bis auf den Ausschluss von Inlinestubs.

Deskriptoren für Formatzeichenfolgen der RPC-NDR-Engine werden in den folgenden Themen ausführlicher beschrieben:

-   [Formatzeichenfolgen](format-strings.md)
-   [Prozedurformatzeichenfolgen](procedure-format-strings.md)
-   [Prozedurheaderdeskriptor](procedure-header-descriptor.md)
-   [Ziehpunkte](handles.md)
-   [Der Header](the-header.md)
-   [Parameterdeskriptoren](parameter-descriptors.md)
-   [Typformatzeichenfolgen](type-format-strings.md)

 

 