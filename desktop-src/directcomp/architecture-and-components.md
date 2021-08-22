---
title: Architektur und Komponenten
description: In diesem Thema werden die Komponenten beschrieben, aus denen Microsoft DirectComposition zusammensetzt.
ms.assetid: 7C79B330-41EA-4BA0-9103-BB5A0C3D4CE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3125a640f902bc64d55af8cdcdbf816c788e0507a48034dfb52c972fa3f068d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985460"
---
# <a name="architecture-and-components"></a>Architektur und Komponenten

> [!NOTE]
> Für Apps auf Windows 10 empfehlen wir die Verwendung von Windows.UI.Composition-APIs anstelle von DirectComposition. Weitere Informationen finden Sie unter [Modernisieren Ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema werden die Komponenten beschrieben, aus denen Microsoft DirectComposition zusammensetzt. Sie besteht aus den folgenden Abschnitten.

-   [Softwarekomponenten](#software-components)
-   [Anwendungsbibliothek](#application-library)
-   [Kompositions-Engine](#composition-engine)
-   [Zugehörige Themen](#related-topics)

## <a name="software-components"></a>Softwarekomponenten

DirectComposition besteht aus den folgenden Hauptsoftwarekomponenten.

-   Eine Anwendungsbibliothek im Benutzermodus (dcomp.dll), die die auf Component Object Model (COM) basierende öffentliche API implementiert.
-   Eine Benutzermoduskompositions-Engine (dwmcore.dll), die im dwm-Prozess (Desktopfenster-Manager) (dwm.exe) gehostet wird und die tatsächliche Desktopkomposition ausführt.
-   Eine Objektdatenbank im Kernelmodus (Teil von win32k.sys), die Befehle von der Anwendung zur Kompositions-Engine marshallt.

Eine einzelne Instanz der Kompositions-Engine verarbeitet die DirectComposition-Kompositionsstrukturen für alle Anwendungen und die DWM-Kompositionsstruktur, die den gesamten Desktop darstellt. Sowohl die Kernelmodusobjektdatenbank als auch die Benutzermoduskompositions-Engine werden einmal pro Sitzung instanziiert, sodass ein Terminalservercomputer mit mehreren Benutzern über mehrere Instanzen beider Komponenten verfügt.

Das folgende Diagramm zeigt die Hauptkomponenten von DirectComposition und deren Beziehung zueinander.

![DirectComposition-Architektur der obersten Ebene](images/directcomposition-top-level-architecture.png)

## <a name="application-library"></a>Anwendungsbibliothek

Die DirectComposition-Anwendungsbibliothek ist eine öffentliche COM-basierte API mit einem einzelnen flachen Einstiegspunkt, der aus dcomp.dll exportiert wird und einen Schnittstellenzeiger auf ein Geräteobjekt zurückgibt. Das Geräteobjekt verfügt wiederum über Methoden zum Erstellen aller anderen Objekte, die jeweils durch einen Schnittstellenzeiger dargestellt werden. Alle DirectComposition-Schnittstellen erben von der [**IUnknown-Schnittstelle**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) und implementieren sie vollständig. Alle Methoden, die DirectComposition-Schnittstellen akzeptieren, überprüfen, ob die Schnittstelle innerhalb von dcomp.dll implementiert ist oder ob sie von einer anderen Komponente implementiert wird. Da DirectComposition nicht erweiterbar ist, geben Methoden, die Schnittstellen als Parameter verwenden, E \_ INVALIDARG zurück, wenn die Schnittstellen nicht in dcomp.dll implementiert sind. Die API erfordert keine besonderen Berechtigungen. Sie kann von Prozessen aufgerufen werden, die auf der niedrigsten Zugriffsebene ausgeführt werden. Da die API jedoch nicht in Sitzung 0 ausgeführt wird, ist sie nicht für Dienste geeignet. In dieser Hinsicht ähnelt die DirectComposition-API anderen Microsoft DirectX-APIs, insbesondere Direct2D, Microsoft Direct3D und Microsoft DirectWrite.

Da die Kompositions-Engine ausschließlich für die asynchrone Ausführung konzipiert ist, sind Objekteigenschaften in der DirectComposition-API schreibgefreit. Alle Eigenschaften verfügen über Settermethoden, aber nicht über Gettermethoden. Das Lesen von Eigenschaften ist nicht nur ressourcenintensiv, sondern kann auch ungenau sein, da jeder wert, den die Kompositions-Engine zurückgibt, sofort ungültig werden kann. Dies kann beispielsweise der Fall sein, wenn eine unabhängige Animation an die zu lesende Eigenschaft gebunden ist.

Die API ist threadsicher. Eine Anwendung kann jederzeit eine beliebige Methode aus einem beliebigen Thread aufrufen. Da jedoch viele API-Methoden in einer bestimmten Sequenz aufgerufen werden müssen, kann eine Anwendung ohne Synchronisierung ein unvorhersehbares Verhalten erleben, je nachdem, wie sich die Threads verschachteln. Wenn beispielsweise zwei Threads die gleiche Eigenschaft desselben Objekts gleichzeitig in unterschiedliche Werte ändern, kann die Anwendung nicht vorhersagen, welcher der beiden Werte der endgültige Wert der Eigenschaft sein wird. Wenn zwei Threads [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) auf demselben Gerät aufrufen, erhält keiner der Threads ein echtes Transaktionsverhalten, da ein Aufruf von **Commit** für einen Thread den Batch aller Befehle sendet, die von beiden Threads ausgegeben werden, nicht nur der Thread, der **Commit** aufgerufen hat.

Das System behält den gesamten internen Zustand pro Geräteobjekt bei. Wenn eine Anwendung zwei oder mehr DirectComposition-Geräteobjekte erstellt, kann die Anwendung unabhängige Batches und einen anderen Zustand zwischen den beiden beibehalten.

Alle DirectComposition-Objekte verfügen über Affinität zwischen Geräteobjekten. -Objekte, die von einem bestimmten Geräteobjekt erstellt werden, können nur mit diesem Geräteobjekt verwendet und nur anderen Objekten zugeordnet werden, die vom gleichen Geräteobjekt erstellt wurden. Anders ausgedrückt: Jedes Geräteobjekt ist eine separate, getrennte Funktionalitätsinsel. Eine Ausnahme ist die visuelle Klasse, die das Erstellen visueller Strukturen ermöglicht, bei denen ein Visuelles zu einem anderen Geräteobjekt als das übergeordnete Objekt gehören kann. Dies ermöglicht Szenarien, in denen eine Anwendung und ein Steuerelement eine einzelne Kompositionsstruktur verwalten können, ohne dass auch ein einzelnes DirectComposition-Geräteobjekt gemeinsam verwendet werden muss.

## <a name="composition-engine"></a>Kompositions-Engine

Die DirectComposition-Kompositions-Engine wird in einem dedizierten Prozess ausgeführt, getrennt von jedem Anwendungsprozess. Ein einzelner Kompositionsprozess, dwm.exe, unterstützt jede Anwendung in einer Sitzung. Jede Anwendung kann zwei visuelle Strukturen für jedes Fenster erstellen, das sie besitzt. Alle Strukturen werden tatsächlich als Teilstrukturen einer größeren visuellen Struktur implementiert, die auch die Kompositionsstrukturen von DWM umfasst. Der DWM erstellt eine große visuelle Struktur für jeden Desktop in einer Sitzung. Dies sind die wichtigsten Vorteile dieser Architektur:

-   Die Kompositions-Engine hat Zugriff auf alle Anwendungsbitmaps und visuellen Strukturen, was prozessübergreifende Interoperabilität und Komposition von Fenstern ermöglicht.
-   Die Kompositions-Engine wird in einem vertrauenswürdigen Systemprozess ausgeführt, der von jedem Anwendungsprozess getrennt ist, sodass Anwendungen mit geringen Zugriffsrechten geschützte Inhalte sicher zusammenstellen können.
-   Die Kompositions-Engine kann erkennen, wenn ein bestimmtes Fenster vollständig verdeckt ist, und vermeidet das Verschwenden von CPU- und GPU-Ressourcen (Graphics Processing Unit), die für das Fenster zusammensetzen.
-   Die Kompositions-Engine kann direkt im Hintergrundpuffer des Bildschirms zusammenstellen, sodass keine zusätzliche Kopie erforderlich ist, die für Prozesskompositions-Engines erforderlich ist.
-   Alle Anwendungen verwenden ein einzelnes Direct3D-Gerät für die Komposition, das erhebliche Arbeitsspeichereinsparungen bietet.

Die visuelle Struktur ist eine beibehaltene Struktur. Die DirectComposition-API macht Methoden verfügbar, um die Struktur in Batches von Änderungen zu bearbeiten, die atomar verarbeitet werden. Das Stammobjekt in der DirectComposition-API ist das Geräteobjekt, das als Factory für alle anderen DirectComposition-Objekte dient und eine Methode namens [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)enthält. Die Kompositions-Engine spiegelt keine Änderungen wider, die die Anwendung an der visuellen Struktur vornimmt, bis die Anwendung **Commit** aufruft. Zu diesem Zeitpunkt werden alle Änderungen seit dem letzten **Commit** als einzelne Transaktion verarbeitet.

Die Anforderung zum Aufrufen von [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) ähnelt dem Konzept eines "Frames", mit dem Unterschied, dass die Kompositions-Engine asynchron ausgeführt wird und mehrere verschiedene Frames zwischen Aufrufen von **Commit** darstellen kann. In DirectComposition ist ein *Frame* eine einzelne Iteration der Kompositions-Engine, und das von einer Anwendung zwischen zwei **Commitaufrufen** aufgewendete Intervall wird als *Batch* bezeichnet.

DirectComposition stapelt alle Anwendungsaufrufe an die DirectComposition-API. Die Kernelobjektdatenbank, die im win32k.sys Sitzungstreiber implementiert ist, speichert alle Zustandsinformationen, die den API-Aufrufen zugeordnet sind.

Die Kompositions-Engine erzeugt einen Frame für jedes vertikale Leerzeichen in der Anzeige. Der Frame wird bei einem vertikalen Leerzeichen gestartet und ist auf das nachfolgende vertikale Leerzeichen ausgerichtet. Wenn der Frame gestartet wird, erfasst die Kompositions-Engine alle ausstehenden Batches und schließt deren Befehle in diesen Frame ein. Batches werden in einer ausstehenden Warteschlange platziert, wenn die Anwendung [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)aufruft, und die ausstehende Warteschlange wird atomar am Anfang des Frames geleert. Daher gibt es einen einzelnen Zeitpunkt, der den Anfang eines Frames markiert. Alle Batches, die vor diesem Punkt übermittelt werden, sind im Frame enthalten, während alle nach übermittelten Batches warten müssen, bis der nächste Frame verarbeitet wird. Die vollständige Kompositionsschleife sieht wie folgt aus:

1.  Schätzen Sie die Zeit des nächsten vertikalen Leerzeichens.
2.  Rufen Sie alle ausstehenden Batches ab.
3.  Verarbeiten sie die abgerufenen Batches.
4.  Aktualisieren Sie alle Animationen mithilfe der in Schritt 1 geschätzten Zeit.
5.  Bestimmen Sie die Bereiche des Bildschirms, die neu zusammengesetzt werden müssen.
6.  Erstellen Sie die geänderten Regionen neu.
7.  Stellen Sie den Rahmen dar, indem Sie die Back- und Frontpuffer für jeden Bildschirm umkehren.
8.  Wenn nichts zusammengesetzt und in den Schritten 6 und 7 dargestellt wurde, warten Sie, bis ein Commit für einen Batch ausgeführt wurde.
9.  Warten Sie auf das nächste vertikale Leerzeichen.

Wenn mehrere Monitore an eine einzelne Grafikkarte angefügt sind, verwendet die Kompositions-Engine das vertikale Leerzeichen des primären Monitors, um die Kompositionsschleife zu steuern und die Samplingzeiten der Animation festzulegen. Jeder Monitor wird durch eine separate Vollbild-Flip-Kette dargestellt. Die Kompositions-Engine wiederholt die Schritte 6 und 7 für jeden Monitor auf Roundrobin-Weise mit einem einzelnen Direct3D-Gerät. Wenn es auch mehrere Grafikkarten gibt, verwendet die Kompositions-Engine ein separates Direct3D-Gerät für jede Grafikkarte in den Schritten 6 und 7.

Kompositionsframes werden so geplant, dass sie immer mit einem vertikalen Leerzeichen beginnen, wie in der folgenden Abbildung dargestellt.

![Kompositionsrahmenplanung](images/composition-frame-scheduling.png)

Wenn die Kompositions-Engine keine Arbeit zu erledigen hat, weil sich die Kompositionsstruktur nicht geändert hat, wechselt der Kompositionsthread in den Standbymodus, während er auf einen neuen Batch wartet. Wenn ein neuer Batch übermittelt wird, wird der Kompositionsthread aktiviert, aber sofort wieder in den Standbymodus versetzt, bis der nächste vertikale Leerlauf erfolgt. Dieses Verhalten stellt vorhersagbare Start- und Endzeiten des Frames für Anwendungen und die Kompositions-Engine sicher.

Die Kompositions-Engine veröffentlicht die Framepräsentationszeiten und die aktuelle Bildfrequenz. Durch die Veröffentlichung dieser Informationen können Anwendungen die Präsentationszeit für ihre eigenen Batches schätzen, was wiederdessen die Synchronisierung von Animationen ermöglicht. Insbesondere kann eine Anwendung eine Kombination aus Framestatistiken aus der Kompositions-Engine und ein Verlaufsmodell verwenden, das annimmt, wie lange der UI-Thread benötigt, um einen Batch zu erstellen, um die Samplingzeit für seine eigenen Animationen zu bestimmen.

Beispielsweise kann die Anwendung am Anfang des in der vorherigen Abbildung gezeigten Anwendungsbatches die Kompositions-Engine abfragen, um die genaue Präsentationszeit des nächsten Frames zu bestimmen. Die Anwendung kann dann die aktuelle Zeit zusammen mit Informationen zu vorherigen Batches verwenden, die sie erstellt hat, um zu bestimmen, ob die Anwendung den aktuellen Batch vor dem nächsten vertikalen Leerlauf abschließen kann. Daher verwendet die Anwendung die Framepräsentationszeit als Samplingzeit für ihre eigenen Animationen. Wenn die Anwendung feststellt, dass ihre Arbeit wahrscheinlich nicht im aktuellen vertikalen Leerraum abgeschlossen wird, kann die Anwendung stattdessen die nachfolgende Framezeit als Samplingzeit verwenden, indem sie die von der Kompositions-Engine zurückgegebenen Bildfrequenzinformationen verwendet, um diese Zeit zu berechnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectComposition-Konzepte](directcomposition-concepts.md)
</dt> </dl>

 

 