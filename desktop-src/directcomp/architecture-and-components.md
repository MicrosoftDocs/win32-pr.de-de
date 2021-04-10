---
title: Architektur und Komponenten
description: In diesem Thema werden die Komponenten beschrieben, die Microsoft directcomposition bilden.
ms.assetid: 7C79B330-41EA-4BA0-9103-BB5A0C3D4CE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2de495aa170560b1e7082cacf1893a8c94905a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039424"
---
# <a name="architecture-and-components"></a>Architektur und Komponenten

> [!NOTE]
> Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen. Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema werden die Komponenten beschrieben, die Microsoft directcomposition bilden. Sie besteht aus den folgenden Abschnitten.

-   [Softwarekomponenten](#software-components)
-   [Anwendungsbibliothek](#application-library)
-   [Kompositions Modul](#composition-engine)
-   [Zugehörige Themen](#related-topics)

## <a name="software-components"></a>Softwarekomponenten

Directcomposition besteht aus den folgenden Hauptsoftware Komponenten.

-   Eine Benutzermodus-Anwendungsbibliothek (dcomp.dll), die die Component Object Model (com)-basierte öffentliche API implementiert.
-   Eine im DWM-dwm.exe Prozess (Desktopfenster-Manager (DWM) gehostete Benutzermodus-Kompositions-Engine (dwmcore.dll), die die tatsächliche Desktop Komposition ausführt.
-   Eine Kernel Modus-Objektdatenbank (Teil win32k.sys), die Befehle von der Anwendung an die Kompositions-Engine marshunkt.

Eine einzelne Instanz der Kompositions-Engine verarbeitet die directcomposition-Kompositions Strukturen für alle Anwendungen und die DWM-Kompositionsstruktur, die den gesamten Desktop darstellt. Sowohl die kernelmodusobjektdatenbank als auch die Benutzermodus-Kompositions-Engine werden einmal pro Sitzung instanziiert, sodass ein Terminal Server Computer mit mehreren Benutzern mehrere Instanzen dieser Komponenten aufweist.

Das folgende Diagramm zeigt die Hauptkomponenten von directcomposition und deren Beziehung zueinander.

![Architektur der obersten Ebene von directcomposition](images/directcomposition-top-level-architecture.png)

## <a name="application-library"></a>Anwendungsbibliothek

Die directcomposition-Anwendungsbibliothek ist eine öffentliche com-basierte API mit einem einzelnen flachen Einstiegspunkt, der aus dcomp.dll exportiert wird und einen Schnittstellen Zeiger auf ein Geräte Objekt zurückgibt. Das Geräte Objekt wiederum verfügt über Methoden zum Erstellen aller anderen Objekte, die jeweils durch einen Schnittstellen Zeiger dargestellt werden. Alle directcomposition-Schnittstellen erben von und implementieren die [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle vollständig. Alle Methoden, die directcomposition-Schnittstellen akzeptieren, überprüfen, ob die Schnittstelle innerhalb von dcomp.dll implementiert wird oder ob Sie von einer anderen Komponente implementiert wird. Da directcomposition nicht erweiterbar ist, geben Methoden, die Schnittstellen als Parameter annehmen, E \_ invalidArg zurück, wenn die Schnittstellen nicht in dcomp.dll implementiert werden. Die API erfordert keine besonderen Berechtigungen. Sie kann von Prozessen aufgerufen werden, die auf der niedrigsten Zugriffsebene ausgeführt werden. Da die API jedoch nicht in Sitzung 0 funktioniert, eignet sie sich nicht für Dienste. In dieser Hinsicht ähnelt die directcomposition-API anderen Microsoft DirectX-APIs, insbesondere Direct2D, Microsoft Direct3D und Microsoft DirectWrite.

Da die Kompositions-Engine ausschließlich für die asynchrone Ausführung konzipiert ist, sind Objekteigenschaften in der directcomposition-API schreibgeschützt. Alle Eigenschaften haben Setter-Methoden, aber keine Getter-Methoden. Das Lesen von Eigenschaften ist nicht nur ressourcenintensiv, sondern kann auch ungenau sein, da jeder von der Kompositions-Engine zurückgegebene Wert sofort ungültig werden kann. Dies kann vorkommen, wenn z. b. eine unabhängige Animation an die gelesene Eigenschaft gebunden ist.

Die API ist Thread sicher. Eine Anwendung kann jederzeit jede Methode von einem beliebigen Thread aus abrufen. Da jedoch viele API-Methoden in einer bestimmten Sequenz aufgerufen werden müssen, kann eine Anwendung ohne Synchronisierung ein unvorhersehbares Verhalten aufweisen, je nachdem, wie die Threads interverlassen. Wenn beispielsweise zwei Threads dieselbe Eigenschaft desselben Objekts gleichzeitig in andere Werte ändern, kann die Anwendung nicht vorhersagen, welcher der beiden Werte der endgültige Wert der Eigenschaft ist. Wenn zwei Threads einen [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) auf demselben Gerät aufrufen, erhält kein Thread ein wirklich Transaktionales Verhalten, da ein Aufruf von **Commit** in einem Thread den Batch aller Befehle übermittelt, die von beiden Threads ausgegeben werden, nicht nur die, die **Commit** aufgerufen haben.

Das System verwaltet den gesamten internen Status pro Geräte Objekt. Wenn eine Anwendung zwei oder mehr directcomposition-Geräte Objekte erstellt, kann die Anwendung unabhängige Batches und einen anderen Zustand zwischen beiden verwalten.

Alle directcomposition-Objekte verfügen über eine Affinität zwischen Geräte Objekten; Objekte, die von einem bestimmten Geräte Objekt erstellt werden, können nur mit diesem Geräte Objekt verwendet werden und können nur anderen Objekten zugeordnet werden, die vom gleichen Geräte Objekt erstellt werden. Das heißt, jedes Geräte Objekt ist eine separate, Zusammenhang lose Insel der Funktionalität. Die einzige Ausnahme ist die Klasse "Visual", die das bilden von visuellen Strukturen ermöglicht, in denen ein visuelles Element zu einem anderen Geräte Objekt als das übergeordnete Element gehören kann. Dies ermöglicht Szenarien, in denen eine Anwendung und ein Steuerelement eine einzelne Kompositionsstruktur verwalten können, ohne auch ein einzelnes directcomposition-Geräte Objekt freigeben zu müssen.

## <a name="composition-engine"></a>Kompositions Modul

Die directcomposition-Kompositions-Engine wird bei einem dedizierten Prozess unabhängig von einem beliebigen Anwendungsprozess ausgeführt. Bei einem einzelnen Kompositionsprozess (dwm.exe) werden alle Anwendungen in einer Sitzung unterstützt. Jede Anwendung kann zwei visuelle Strukturen für jedes Fenster erstellen, das Sie besitzt. Alle Strukturen werden tatsächlich als Teil Strukturen eines größeren visuellen Baums implementiert, der auch die Kompositions Strukturen von DWM umfasst. Der DWM-Konstruktor erstellt eine große visuelle Struktur für jeden Desktop in einer Sitzung. Dies sind die wichtigsten Vorteile dieser Architektur:

-   Die Kompositions-Engine verfügt über Zugriff auf alle Anwendungs Bitmaps und visuelle Strukturen, die prozessübergreifende Fenster Interoperabilität und-Komposition ermöglicht.
-   Die Kompositions-Engine wird in einem vertrauenswürdigen System Prozess ausgeführt, der von keinem beliebigen Anwendungsprozess getrennt ist, sodass Anwendungen mit niedrigen Zugriffsrechten geschützte Inhalte sicher verfassen können.
-   Die Kompositions-Engine kann erkennen, wenn ein bestimmtes Fenster vollständig geledert wird, und vermeiden, dass CPU-und GPU-Ressourcen (Graphics Processing Unit) für das Fenster verschwendet werden.
-   Die Kompositions-Engine kann direkt auf den Bildschirm Puffer zurückgesetzt werden, sodass keine zusätzliche Kopie erforderlich ist, die für prozessspezifische Kompositions-Engines erforderlich ist.
-   Alle Anwendungen verwenden ein einzelnes Direct3D-Gerät für die Komposition, das beträchtliche Speicher Einsparungen bietet.

Die visuelle Struktur ist eine beibehaltene Struktur. Die directcomposition-API macht Methoden zum Bearbeiten der Struktur in den Änderungen, die atomarisch verarbeitet werden, verfügbar. Das Stamm Objekt in der directcomposition-API ist das Device-Objekt, das als Factory für alle anderen directcomposition-Objekte fungiert und eine Methode namens [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)enthält. Die Kompositions-Engine reflektiert keine Änderungen, die die Anwendung an der visuellen Struktur vornimmt, bis die Anwendung **Commit** aufruft. an diesem Punkt werden alle Änderungen seit dem letzten **Commit** als einzelne Transaktion verarbeitet.

Die Anforderung zum Aufrufen von [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) ähnelt dem Konzept eines "Frames", mit der Ausnahme, dass die Kompositions-Engine asynchron ausgeführt wird, dass Sie mehrere verschiedene Frames zwischen den Aufrufen von **Commit** darstellen kann. In directcomposition ist ein *Frame* eine einzelne Iteration der Kompositions-Engine, und das Intervall, das von einer Anwendung zwischen zwei Aufrufen von **Commit** aufgewendet wird, wird als *Batch* bezeichnet.

Directcomposition fasst alle Anwendungs Aufrufe an die directcomposition-API um. Die im win32k.sys-Sitzungs Treiber implementierte Kernel Objektdatenbank speichert alle Zustandsinformationen, die mit den API-aufrufen verknüpft sind.

Die Kompositions-Engine erzeugt einen Frame für jede vertikale leere in der Anzeige. Der Frame wird bei einem vertikalen Leerraum gestartet und zielt auf den nachfolgenden vertikalen Leerraum ab. Wenn der Frame gestartet wird, übernimmt die Kompositions-Engine alle ausstehenden Batches und schließt Ihre Befehle in diesen Frame ein. Batches werden in eine ausstehende Warteschlange eingefügt, wenn die Anwendung [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)aufruft, und die ausstehende Warteschlange wird atomarisch am Anfang des Frames geleert. Daher gibt es einen einzelnen Zeitpunkt, der den Anfang eines Frames markiert. Alle Batches, die vor diesem Punkt übermittelt werden, werden in den Frame eingeschlossen, während alle nach übermittelten Batches warten müssen, bis der nächste Frame verarbeitet wird. Die vollständige Kompositions Schleife lautet wie folgt:

1.  Schätzen Sie die Zeit des nächsten vertikalen leeren.
2.  Ruft alle ausstehenden Batches ab.
3.  Verarbeiten Sie die abgerufenen Batches.
4.  Aktualisieren Sie alle Animationen mit der in Schritt 1 geschätzten Zeit.
5.  Bestimmen Sie die Bereiche des Bildschirms, die neu zusammengesetzt werden müssen.
6.  Erstellen Sie die geänderten Bereiche neu.
7.  Zeigen Sie den Rahmen an, indem Sie die Back-und Front-Puffer für die einzelnen Bildschirme kippen.
8.  Wenn in den Schritten 6 und 7 nichts zusammengesetzt und angezeigt wurde, warten Sie, bis ein Commit für einen Batch ausgeführt wurde.
9.  Warten Sie auf den nächsten vertikalen Leerraum.

Wenn mehrere Monitore an eine einzelne Grafikkarte angefügt sind, verwendet die Kompositions-Engine den vertikalen Leerraum des primären Monitors, um die Zusammenfassungs Schleife zu steuern und die Zeit für die Animations Stichprobe festzulegen. Jeder Monitor wird durch eine separate voll Bild-Flip-Kette dargestellt. die Kompositions-Engine wiederholt die Schritte 6 und 7 für jeden Monitor im Roundrobin-Verfahren mithilfe eines einzelnen Direct3D-Geräts. Wenn auch mehrere Videoadapter vorhanden sind, verwendet die Kompositions-Engine in den Schritten 6 und 7 ein separates Direct3D-Gerät für jede Grafikkarte.

Kompositions Rahmen werden so geplant, dass Sie immer mit einem vertikalen Leerraum beginnen, wie in der folgenden Abbildung dargestellt.

![Kompositions Rahmenplanung](images/composition-frame-scheduling.png)

Wenn die Kompositions-Engine keine Arbeit hat, da die Kompositionsstruktur nicht geändert wurde, wird der Kompositions Thread beim Warten auf einen neuen Batch nicht angezeigt. Wenn ein neuer Batch übermittelt wird, wird der Kompositions Thread reaktiviert, aber sofort wieder in den Standbymodus versetzt, bis der nächste vertikale Leerraum liegt. Durch dieses Verhalten wird die vorhersagbare Frame Start-und Endzeit für Anwendungen und die Kompositions-Engine sichergestellt.

Die Kompositions-Engine veröffentlicht die Frame Präsentations Zeiten und die aktuelle Framerate. Durch das Veröffentlichen dieser Informationen können Anwendungen die Präsentationszeit für Ihre eigenen Batches einschätzen, die wiederum das Synchronisieren von Animationen ermöglicht. Insbesondere kann eine Anwendung eine Kombination aus Frame Statistiken aus der Kompositions-Engine verwenden, und ein Verlaufs Modell, wie lange der UI-Thread benötigt, um einen Batch zu erstellen, um die Zeit für die Stichprobenentnahme für seine eigenen Animationen zu ermitteln.

Beispielsweise kann die Anwendung am Anfang des Anwendungs Batches, der in der obigen Abbildung gezeigt wurde, das Kompositions Modul Abfragen, um die genaue Präsentationszeit des nächsten Frames zu bestimmen. Die Anwendung kann dann die aktuelle Zeit zusammen mit Informationen zu vorherigen Batches verwenden, die Sie erstellt hat, um zu bestimmen, ob die Anwendung den aktuellen Batch vor dem nächsten vertikalen leeren vervollständigen kann. Daher verwendet die Anwendung die Frame Präsentationszeit als Stichproben Zeit für Ihre eigenen Animationen. Wenn die Anwendung feststellt, dass es unwahrscheinlich ist, dass die Arbeit im aktuellen vertikalen Leerraum beendet wird, kann die Anwendung stattdessen die nachfolgende Frame Zeit als samplingzeit verwenden, wobei die von der Kompositions-Engine zurückgegebenen Frameraten Informationen verwendet werden, um diese Zeit zu berechnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directcomposition-Konzepte](directcomposition-concepts.md)
</dt> </dl>

 

 