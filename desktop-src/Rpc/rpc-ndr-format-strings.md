---
title: RPC-Zeichen folgen im Format
description: RPC-Format Zeichenfolgen (Remote Prozedur Aufruf).
ms.assetid: 9c83a039-49d3-491d-8110-29d1548730de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf0569a913d6c5a4b19b342cc288d6a8682dfc4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858439"
---
# <a name="rpc-ndr-format-strings"></a>RPC-Zeichen folgen im Format

## <a name="ndr-engine-32-bit-interpreter"></a>NDR-Engine: 32-Bit-Interpreter

In diesem Dokument werden die Format Zeichenfolgen-Deskriptoren (manchmal auch als "Mops" bezeichnet) für die 32-Bit-NDR-Engine beschrieben. In diesem Abschnitt werden die Änderungen beschrieben, die mit der Entwicklung des [**– Oi**](/windows/desktop/Midl/-oi) -interpreterers zur **– OIF** -interpreterebene verknüpft sind, sowie Ergänzungen, die sich auf Pipes und asynchrone Unterstützung beziehen.

In diesem Dokument wird die aktuelle Microsoft Interface Definition Language-Technologie (Mittel l) aus der Engine-Perspektive und die aktuelle-NDR-Engine beschrieben.

## <a name="overview"></a>Übersicht

Die NDR-Engine ist das marshallingmodul der Remote Prozedur Aufruf (RPC)-und DCOM-Komponenten. Sie behandelt alle stubbezogenen Probleme eines Remote Aufrufes. Als Prozess wird das NDR-Marshalling durch den C-Code von mit mittlerer l generierten Stub, von einem Mittelwert-JIT-typgenerator oder durch von anderen Tools generierte Stub-und manuell geschriebene Stub-Vorgänge gesteuert. Die NDR-Engine steuert wiederum die zugrunde liegende Laufzeit (DCOM oder RPC), die mit bestimmten Transporten kommuniziert.

Das ursprüngliche Ziel des Entwurfs war, ein Tool für ein effektives Marshalling für beliebige Daten bereitzustellen, basierend auf Informationen, die vom Mittelwert Compiler bereitgestellt werden. Die in diesem Dokument beschriebenen Format Zeichenfolgen – und tatsächlich alle vom Compiler generierten Informationen für die Nutzung der NDR-Engine – wurden stets als interne Schnittstelle zwischen dem Compiler und der Engine betrachtet. Ebenso sind Schnittstellen, die für die Engine zur Behandlung von Lauf Zeitproblemen verfügbar sind, größtenteils intern (einige Ausnahmen sind auf der RPC-Lauf Zeit Seite vorhanden, und einige der von der Engine verwendeten DCOM-Schnittstellen sind extern).

Zwei typische Ansätze für das Mars Hallen sind immer Inline-und datengesteuerte (interpretierte) Technologien. Die Mittel l unterstützt sowohl über die [**– OS**](/windows/desktop/Midl/-os) -und [**– Oi \***](/windows/desktop/Midl/-oi) -Switches in den von C generierten Stubs. Außerdem kann die Mittel l die TLB-Bibliotheken generieren, die vom oleautomation-Paket verwendet werden. Dementsprechend besteht eine Perspektive der internale der Engine darin, dass Sie aus zwei Teilen besteht.

Der erste besteht aus einem Satz von Routinen, die die Größe, das Marshalling usw. verarbeiten, entsprechend den typischen Datentyp Objekten, wie z. b. einer Struktur oder einem Array. Diese Routinen sind für die Leistung optimiert. so versuchen Sie z. b. in der Regel, Daten zu blockieren, soweit dies möglich ist. Dieser Teil wird häufig als Kern-NDR-Engine bezeichnet.

Der zweite Teil besteht aus einem Interpreter und den zugehörigen Teilen. Der Interpreter verwendet Routinen aus der Kern-NDR-Engine, wie aus einer internen Bibliothek, um einen Remote-Befehl auszuführen, bei dem alle zugehörigen Argumente gemarshallt und nach Bedarf gemarshallt werden.

Die Core-NDR-Engine wird auf ähnliche Weise verwendet, unabhängig davon, ob Sie von Inline-Stubdaten oder vom Interpreter verwendet wird. Alle Kern-Engine-Routinen hängen von dem Zustand ab, der von einer Stub-Nachrichtenstruktur weitergegeben wurde. Die Struktur wird vom Inline-Stub oder vom Interpreter ordnungsgemäß eingerichtet. Im Laufe der Jahre wurde die Kern-Engine in einem anderen Kontext verwendet. Derzeit ist der Interpreter tatsächlich eine Reihe von verschiedenen interpreterschleifen. Diese stehen im Zusammenhang mit den alten und neuen ([**– Oi**](/windows/desktop/Midl/-oi) / **– OIF**)-Interpretern sowie mit Schleifen im Zusammenhang mit der Datenserialisierung (Picking), der RPC-asynchronen Unterstützung und der Unterstützung für asynchrone DCOM-Unterstützung (RPC und DCOM haben unterschiedliche asynchrone Programmier Modelle)

Neben dem Hinzufügen neuer Features ist ein wichtiger Aspekt der Weiterentwicklung der NDR-Engine eine allgemeine Umstellung des Ansatzes auf Interpretern. Die Version 1.1 von NDR begann im Rahmen eines neuen Mittel-2,0-Ansatzes für das Mars Hallen, wobei die Inline-stubpunkte für Leistungsaspekte bevorzugt werden. Mit der neuesten Version von NDR ist [**– OIF**](/windows/desktop/Midl/-oi) zum häufigsten verwendeten Modus des Compilers geworden, fast zum Ausschluss von Inline-stubstuf.

Die Format Zeichenfolgen Deskriptoren der RPC-Engine für die RPC-Engine werden in den folgenden Themen ausführlicher beschrieben:

-   [Formatzeichenfolgen](format-strings.md)
-   [Prozedur Format Zeichenfolgen](procedure-format-strings.md)
-   [Prozedur Header Deskriptor](procedure-header-descriptor.md)
-   [Hand](handles.md)
-   [Der Header](the-header.md)
-   [Parameter Deskriptoren](parameter-descriptors.md)
-   [Typformatzeichenfolgen](type-format-strings.md)

 

 