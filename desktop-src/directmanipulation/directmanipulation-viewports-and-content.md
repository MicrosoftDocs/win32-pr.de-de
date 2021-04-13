---
description: Die direkte Bearbeitung verwendet Viewports, Inhalte und Kontakte, um die interaktiven Elemente der Benutzeroberfläche zu beschreiben.
ms.assetid: 1564F6F2-844F-4392-9EB5-AA46059D514C
title: Viewports und Inhalt
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9cda367067ea860ce6a42a16e81d38393937276a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568554"
---
# <a name="viewports-and-content"></a>Viewports und Inhalt

Die [direkte Bearbeitung](direct-manipulation-portal.md) verwendet *Viewports*, *Inhalte* und *Kontakte* , um die interaktiven Elemente der Benutzeroberfläche zu beschreiben.

- [Konfigurieren eines Viewports](#configuring-a-viewport)
- [Andockpunkte und-Begrenzungen](#snap-points-and-boundaries)
- [Snap-in-Offset und RTL-Szenarios](#snap-point-offset-and-rtl-scenarios)
- [Verhalten](#behaviors)
- [Koordinatensystem](#coordinate-system)
- [Transformationen](#transforms)
- [Status des Viewports](#viewport-state)
- [Zugehörige Themen](#related-topics)

Bei einem *Viewport* handelt es sich um eine Region innerhalb eines Fensters, die Eingaben von Benutzerinteraktionen empfangen und verarbeiten kann. Der Viewport stellt den Bereich des Inhalts dar, der für den Endbenutzer zu einem bestimmten Zeitpunkt (auch als inhaltsclip bezeichnet) angezeigt werden kann. Der Viewport verfügt über mehrere Funktionen:

- Er verwaltet den Interaktions Zustand (z. b., wenn der Inhalt für die Bearbeitung bereit ist, wenn der Inhalt bearbeitet wird, wenn sich der Inhalt in der Trägheit-Animation befindet) und Eingaben in Ausgabe Transformationen zuordnet.
- Sie enthält Inhalte, die als Reaktion auf die Benutzerinteraktion verschoben werden. Dabei kann es sich um ein HTML-div-Element (Scrollen), eine Aufzähl Bare Liste (der Start Bildschirm von Windows 8) oder das Popup Menü für ein Select-Steuerelement handeln.

Ein Viewport wird durch Aufrufen von [**createviewport**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport)erstellt. Es können mehrere Viewports in einem einzelnen Fenster erstellt werden, um eine umfangreiche Benutzeroberfläche zu erstellen.

Der *Inhalt* stellt das Element dar, das als Reaktion auf eine Interaktion transformiert wird. Mit anderen Worten: der Inhalt ist das, was bewegt oder skaliert wird, wenn der Benutzer sich anrichtet oder pingt. Es gibt zwei Arten von Inhalten:

- *Primärer Inhalt* ist das einzelne, systeminterne Element innerhalb eines Viewports, das auf Eingabe Manipulationen und Trägheit antwortet. Primärer Inhalt wird zur gleichen Zeit wie der Viewport erstellt und kann nicht zu einem Viewport hinzugefügt oder daraus entfernt werden. Sie können das Verhalten von primärem Inhalt mithilfe von Andock Punkten (später erläutert) anpassen.
- Der *sekundäre Inhalt* wird relativ zur Bewegung des primären Inhalts verschoben. Sekundär Inhalte werden getrennt vom Viewport erstellt und können einem Viewport hinzugefügt oder daraus entfernt werden. Alle sekundären Inhalts Transformationen werden basierend auf der Transformation des primären Inhalts berechnet. Bestimmte Regeln können angewendet werden, um zu ändern, wie die Transformation basierend auf dem beabsichtigten Zweck des Elements berechnet wird, das durch die CLSID während der Erstellung identifiziert wird.

In diesem Diagramm, das vor und nach einer schwenken angezeigt wird, wurde ein einzelner Kontakt zum Schwenken des primär Inhalts verwendet. Obwohl der Benutzer nicht direkt mit dem Schwenk Indikator (sekundärer Inhalt) interagiert, wird der sekundäre Inhalt verschoben, wenn der primäre Inhalt in den primär Inhalt wechselt. Auf diese Weise werden visuelle Hinweise dazu bereitstellen, wie weit sich der Benutzer befindet.

![Diagramm, das vor/nach einer schwenken angezeigt wird](images/dm-art-2.png)

## <a name="configuring-a-viewport"></a>Konfigurieren eines Viewports

Nachdem Sie den Viewport erstellt haben. Konfigurieren Sie das Verhalten mithilfe einer *Interaktions Konfiguration*. Die Interaktions Konfiguration gibt an, welche Manipulationen, wie z. b. Schwenken, unterstützt werden.

Durch *Schwenken* wird die Position des Inhalts auf der horizontalen oder vertikalen Achse oder beides als Benutzer-Pans geändert. Wenn Sie die Übersetzung auf beiden Achsen konfigurieren, wechselt der Inhalt in beliebiger Richtung frei.

Um die Inhalts Bewegung einzuschränken, konfigurieren Sie *Rails*, in der Regel auf der horizontalen und vertikalen Achse. Wenn sich die Interaktion eines Benutzers hauptsächlich entlang einer einzelnen Achse (dargestellt durch die blauen Bereiche im nächsten Diagramm) befindet, wird die *Pan-Achse* entfernt, und der Inhalt wird nur entlang der Raster Achse verschoben. Wenn der Benutzer einen Flatter hat und aktuell eine zweite schwenken ausführt, während sich der Inhalt in Trägheit befindet, wird die neue Pan-Komponente weiter entfernt.

![Diagramm, das Inhalte in einem Viewport in einer Raten schwenken anzeigt](images/dm-art-3.png)

Beispiel: ein Viewport ist für horizontales und vertikales schwenken konfiguriert. Im ersten Frame kommt der Kontakt ins Spiel. In der zweiten wird eine vertikale schwenken initiiert, und der Kontakt wird an die vertikale Schiene gebunden. Schließlich wird nach dem Schwenken der Pan nur die vertikale Komponente einer Diagonalen schwenken zum Verschieben des Inhalts verwendet.

Wenn der Benutzer diagonal in eine Weise umzieht, dass Sie sich nicht in den Rails-Erkennungs Bereichen befinden (die weißen Bereiche), wird die schwenken *entrachtet* , und der Inhalt wird auf beiden Achsen frei verschoben.

![Diagramm mit Inhalten, die sich in eine ungerentete schwenken bewegen](images/dm-art-4.png)

Beim *Zoomen* wird der Skalierungsfaktor des Inhalts geändert, wenn ein Benutzer pingt oder gestreckt wird. Der Punkt, um den der Inhalt skaliert wird (Zoom Center genannt), befindet sich in der Mitte der Kontakte. Wenn Sie die horizontale oder vertikale Ausrichtung festgelegt haben, ändert sich das Zoom Center, um die Ausrichtung beizubehalten.

![Diagramm, das das Zoomen von Inhalten mit angegebener Ausrichtung anzeigt](images/dm-art-5.png)

Sie können dieses Verhalten überschreiben, indem Sie Unlock Center angeben, das das Zoom Center in der Mitte der Kontakte festlegt.

![Diagramm, das das Zoomen von Inhalten mit entsperrtem Zoom Center anzeigt](images/dm-art-6.png)

*Trägheit* ist die schrittweise Verlangsamung der Bearbeitung, sowohl schwenken als auch zoomen, nachdem alle Kontakte (im Fall von Finger Eingaben) oder nach der Tastatur-/MoU-Eingabe (z. b. durch Klicken auf eine Schiebe Leiste oder durch Drücken der Pfeiltasten) angehoben wurden. Wenn ein Benutzer den Inhalt manipuliert, wird die Manipulation nicht sofort beendet, nachdem der Kontakt aufgehoben wurde. Stattdessen wird der Inhalt in der aktuellen Richtung und Geschwindigkeit fortgesetzt und langsam zu einem Ende verlangsamt.

## <a name="snap-points-and-boundaries"></a>Andockpunkte und-Begrenzungen

Eine Trägheits Animation findet statt, nachdem die Bearbeitung beendet wurde, weil ein Finger vom Bildschirm entfernt wurde (im Fall von Touch), oder als Ergebnis einer Tastatur-und Maus Aktion (z. b. Pfeiltasten, Bild-auf-ab, Mausrad Scrollen usw.).

Es gibt zwei Informationen, die die Trägheit-Animation definieren:

- Der Rest-Punkt der Animation – die endgültige Endposition der jeweiligen Transformations Komponente.
- Die Dauer der Animation, die Kurve, die Geschwindigkeit – diese werden durch den Typ des Rest-Punkts bestimmt.

Die Trägheit-Animation wirkt sich auf die-Snap-Ins und-Grenzen aus. Grenzen geben den maximalen und den minimalen Rest für den Inhalt an. Wenn der Inhalt während der Trägheit eine Grenze erreicht, wird eine Begrenzungs Animation angewendet. Andockpunkte werden auf dem primären Inhalt definiert, um den Rest-Punkt zu ändern und die Animations Animations Kurve selbst zu ändern.

Sie definieren Andockpunkte mit " [**sintsnapinterval**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval) ", wenn der Inhalt regelmäßig entfernt wird, [**oder mit "**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints) ", wenn der Inhalt nicht gleichmäßig verteilt ist. Im folgenden finden Sie ein Beispiel für Andockpunkte:

![Diagramm, das zeigt, wie die in den Inhalten festgelegten Ausrichtungs Punkte sich](images/dm-snappoint-states-3.png)

Im Diagramm finden Sie einen Inhalt mit einer Reihe von unter Inhalts Blöcken – News Items in einer Newsreader-APP oder Elemente in einer Rasteransicht. Die Absicht besteht darin, den linken Rand eines Elements nach dem Ende der Trägheit an den linken Rand des Viewports zu andocken.

Es gibt zwei Gruppen von andockpunkt Typen:

- *Optional oder obligatorisch*: ein optionaler andockpunkt dostet die Trägheit-Animation nur dann, wenn sich der Trägheit-Rest-Punkt in der Nähe des Andock Punkts befindet Ein obligatorischer andockpunkt dostet die Trägheit-Animation immer an einen angegebenen andockpunkt.
- *Single vs. Multiple*: ein Multiple-Snap-pointtyp ermöglicht dem Inhalt das Verschieben von über vielen Andock Punkten vor dem Erreichen eines Rests an einem andockpunkt in der Nähe des natürlichen Rest Punkts. Mit einem einzelnen Andock Punkttyp wird der nächste nächste Punkt als Rest Punkt für die Trägheit-Animation ausgewählt.

Im nächsten Diagramm wird veranschaulicht, wie andockpunkt Typen die Rest Position der Trägheit-Animation ändern.

![Diagramm, das zeigt, wie Trägheit und Andockpunkte interagieren](images/dm-snappoint-states-1.png)

In diesem Diagramm ist der Startpunkt der Trägheit als "Start" gekennzeichnet und die Endposition der natürlichen Trägheit, wenn keine Andockpunkte als "End" vorhanden sind. Die vertikalen Linien markieren die verschiedenen Andockpunkte. In dieser Tabelle wird beschrieben, wie sich die einzelnen Arten von Andock Punkten auf die Endposition der Animation auswirken.

| Punkttyp         | BESCHREIBUNG                                                                                |
|--------------------|--------------------------------------------------------------------------------------------|
| Obligatorischer einzelner   | Der Endpunkt P1 wird ausgewählt, da er der erste andockpunkt in der Richtung der Trägheit ist.     |
| Obligatorisch (mehrmals) | Der andockpunkt P2 wird ausgewählt, da er am nächsten am Endpunkt in der Richtung der Trägheit liegt. |
| Optionales einzelnes    | Der Snap-in P1 wird ausgewählt, weil es sich um den ersten während der Trägheit gefundenen Punkt handelt.      |
| Optional mehrfach  | Der andockpunkt P2 wird ausgewählt, da er sich in der Nähe des natürlichen Endpunkts befindet                           |

## <a name="snap-point-offset-and-rtl-scenarios"></a>Snap-in-Offset und RTL-Szenarios

![Diagramm mit der Verwendung des RTL-Snap-Ins](images/dm-snappoint-states-2.png)

Sie wenden den Endpunkt Offset und das Koordinatensystem mithilfe der [**setsnapkoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) -API an – die alle Andockpunkte oder Snap-Ins mithilfe des angegebenen Offset-/Koordinaten Systems Offsets.

Das Koordinatensystem ist in RTL-Szenarien sehr nützlich, in denen Sie Snap-Points vom linken Rand des Inhalts in umgekehrter Richtung beschreiben möchten. Im vorherigen Diagramm wird [**setsnapkoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) mit dem Flag **directmanipulation \_ Motion \_ TranslateX** und **directmanipulation \_ Koordinaten \_ gespiegelt** verwendet, das automatisch die Punkt Punkte vom linken Rand des Inhalts ablegt und Sie in der Reihenfolge von rechts nach links angibt: S1 liegt bei 0px, S2 bei 50 px (usw.). Jeder Offset, der mit **setsnapkoordinate** festgelegt wird, wird von dieser linken Kante des Inhalts automatisch versetzt, einschließlich des richtigen Skalierungsfaktors.

Sie verwenden fast immer [**setsnapkoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) mit dem *Origin* -Parametersatz, um zu vermeiden, dass Snap-Points außerhalb des Inhalts Bereichs festgelegt werden.

Wenn der Viewport beispielsweise 200 x 200 beträgt und der Inhalt 1000 x 200 beträgt und die Schnittstelle RTL ist, erhält der Viewport den linken Rand bei x = 800, wenn der Viewport zum ersten Mal angezeigt wird. Geben Sie "" in " [**" mit der**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) `SetSnapCoordinate(DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_COORDINATE_MIRRORED, 1000.0)` rechten Kante des Inhalts an, um anzugeben, dass die Andockpunkte von rechts nach links berechnet werden sollen.

## <a name="behaviors"></a>Verhalten

Ein *Verhalten* ist ein Objekt, das an einen Viewport angefügt werden kann, um zu ändern, wie die [direkte Bearbeitung](direct-manipulation-portal.md) die Ausgabe Transformation des primären oder sekundären Inhalts eines Viewports behandelt. Ein Verhaltens Objekt wirkt sich möglicherweise auf einen oder mehrere Aspekte einer Manipulation aus, z. b. wie Eingaben verarbeitet werden oder wie die Trägheit-Animation angewendet wird. Beispielsweise wirkt sich ein Auto Scroll-Verhalten auf die Trägheit-Animation aus, indem eine Bildlauf-Animation an einem Ende des primären Inhalts durchgeführt wird. Ein Kreuz Folie-Konfigurations Verhalten wirkt sich auf die Eingabe Verarbeitung direkter Manipulationen aus, die erkennt, wenn eine Kreuz Folie ausgeführt wird.

Ein Verhaltens Objekt wird durch Aufrufen von [**CreateBehavior**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager2-createbehavior)erstellt, zu einem Viewport hinzugefügt, und das zugehörige Verhalten wird asynchron konfiguriert. Wenn Sie das Verhalten aus dem Viewport entfernen, werden seine Auswirkungen entfernt.

## <a name="coordinate-system"></a>Koordinatensystem

Es gibt drei Haupt Koordinatensysteme, die bei [direkter Bearbeitung](direct-manipulation-portal.md)eingesetzt werden:

- Client Koordinatensystem: Beschreibt das Rechteck des Client Fensters. Die Einheiten sind in Pixel.
- Viewport-Koordinatensystem: Beschreibt das Rechteck eines Bereichs innerhalb des Clients, der Eingaben verarbeiten kann. Einheiten sind Anwendungs definiert (mithilfe von [**setviewportrect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect)).
- Inhalts Koordinatensystem: Beschreibt das Rechteck oder die Größe von primärem Inhalt. Einheiten sind Anwendungs definiert (mithilfe von [**setcontentrect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect)).

Für alle drei Systeme werden die Koordinaten relativ zum jeweiligen oberen linken Ursprung definiert und sind positiv rechts und nach unten. Diese Koordinatensysteme werden im nächsten Diagramm veranschaulicht. Nur der Abschnitt des Inhalts innerhalb des Viewportrechtecks kann vom Endbenutzer angezeigt oder bearbeitet werden.

![Diagramm, das zeigt, wie Inhalts-, Client-und viewportkoordinaten interagieren](images/dm-art-7.png)

## <a name="transforms"></a>Transformationen

[Direkte Manipulation](direct-manipulation-portal.md) verwaltet mehrere verschiedene Transformationen, die zur Gesamtzahl der angezeigten Ausgaben beitragen.

- *Inhalts Transformation* – die anfängliche Transformation, die durch [direkte Bearbeitung](direct-manipulation-portal.md) basierend auf einer Manipulation oder Trägheit berechnet wird. Es erfasst die Auswirkungen von Andock Punkten, das Geländer, das Standard Überschreitungen (Manipulation), den Standard overbounce (Trägheit) und zoomtoriect-Animationen.
- *Output Transform* : die endgültige Visualisierung oder Ausgabe Transformation. Dabei handelt es sich um die Kombination aus dem Inhalt und den Synchronisierungs Transformationen.
- *Synchronisierungs Transformation* – wird berechnet, wenn [**synccontenttransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-synccontenttransform)aufgerufen wird. Sie hilft bei der [direkten Bearbeitung](direct-manipulation-portal.md) einer neuen Inhalts Transformation, die von der Anwendung bereitgestellt wird, während gleichzeitig die vorhandene Ausgabe Transformation beibehalten wird.
- *Anzeige Transformation* – wird von der Anwendung im Rahmen der Nachbearbeitung angewendet. Weitere Informationen finden Sie unter [**syncdisplaytransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform) .

Da die Ausgabe Transformation dazu gedacht ist, eine Oberfläche visuell auf dem Bildschirm zu versetzen, führt die [direkte Manipulation](direct-manipulation-portal.md) die erforderliche Rundung der Ausgabe Transformations Komponenten durch, sodass Text und andere Inhalte immer an einer ganzzahligen Pixel Grenze gerendert/zusammengesetzt werden. Der Rundungs Mechanismus hängt von mehreren Faktoren ab, einschließlich der Geschwindigkeit der Bewegung und der Anwesenheit Remotedesktop. Der Rundungs Mechanismus für Sekundär Inhalt stimmt mit dem des primären Inhalts überein, während der Unterschied zwischen den beiden Bewegungen berücksichtigt wird. Clients von [**getoutputtransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) sollten nicht von der exakten Rundungs Methode der Ausgabe Transformation abhängig sein, da Sie durch verschiedene Faktoren beeinflusst wird.

> [!Note]
>
> Dies bedeutet, dass die Komponenten einer Inhalts Transformation nicht ganzzahlig sein können und auch unter Pixel Offsets enthalten können. Clients, die [direkte Manipulation](direct-manipulation-portal.md) verwenden, wird empfohlen, [**getoutputtransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) zu verwenden, um die richtige visuelle Transformation zu berechnen, die auf den Inhalt angewendet werden soll, wenn der manuelle Update Modus verwendet wird. Wenn Sie den automatischen Aktualisierungs Modus mit dem integrierten Compositor verwenden, wendet die direkte Bearbeitung diese Transformation automatisch auf den Namen des Clients an. Diese Transformation wird durch direkte Bearbeitung generiert, um bei der Komposition der visuellen Ausgabe visuell ansprechende Ergebnisse sicherzustellen.

## <a name="viewport-state"></a>Status des Viewports

Während der Eingabe verarbeitet der Viewport den Interaktions Status und die Zuordnung von Eingaben zu Ausgabe Transformationen. Überprüfen Sie den Interaktions Zustand des Viewports durch Aufrufen von [**GetStatus**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-getstatus).

![Diagramm mit directmanipulation-Interaktions Zuständen](images/dm-states-diagram.png)

- Erstellung – der Viewport wird erstellt und kann die Eingabe noch nicht verarbeiten. Um die Eingabe zu verarbeiten, nennen Sie [**idirectmanipulationviewport:: enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable). Wenn **enable** nicht aufgerufen wird, wechselt der Viewport in den deaktivierten Zustand.

    > [!Note]  
    > Dies ist der anfängliche Zustand der Interaktion.

- Aktiviert – der Viewport ist bereit für die Verarbeitung von Eingaben. Wenn ein Kontakt angezeigt wird ([**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) wird aufgerufen) und eine Manipulation erkannt wird, wechselt der Viewport in "wird ausgeführt".

- Wird ausgeführt – der Viewport verarbeitet momentan Eingaben und aktualisiert Inhalt. Wenn der Kontakt angehoben wird, wechselt der Viewport zu Trägheit, wenn er konfiguriert ist.

- Trägheit – der Inhalt bewegt sich in einer Trägheit-Animation. Sobald die Trägheit abgeschlossen ist, wird der Viewport in bereit angezeigt. Wenn die automatische Deaktivierung für den Viewport festgelegt wurde, wird der Wechsel von Trägheit in bereit und dann zu deaktiviert.

- Bereit – der Viewport ist bereit für die Verarbeitung von Eingaben. Wenn ein Kontakt angezeigt wird ([**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) wird aufgerufen) und eine Manipulation erkannt wird, wechselt der Viewport in "wird ausgeführt".

- Angehalten – der Viewport wird möglicherweise angehalten, wenn seine Eingabe zu einem übergeordneten Element in der [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) -Kette herauf gestuft wurde. Dies wird in [mehreren Viewports ausführlicher erläutert: Treffer Tests und viewporthierarchie](directmanipulation-multiple-vieports.md).

- Deaktiviert – der Viewport verarbeitet keine Eingaben und führt keine Rückrufe aus. Ein Viewport kann durch Aufrufen von [**idirectmanipulationviewport::D isable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-disable)aus verschiedenen Zuständen deaktiviert werden. Wenn die automatische Deaktivierung für den Viewport festgelegt wurde, wird der Übergang nach der Verarbeitung einer Bearbeitung automatisch in deaktiviert. Um einen deaktivierten Viewport erneut zu aktivieren, nennen Sie [**idirectmanipulationviewport:: enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable).

## <a name="related-topics"></a>Zugehörige Themen

[Mehrere Viewports: Treffer Tests und viewporthierarchie](directmanipulation-multiple-vieports.md), [**activateconfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration), [**getoutputtransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform), [**syncdisplaytransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)
