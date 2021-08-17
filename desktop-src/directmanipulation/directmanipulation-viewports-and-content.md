---
description: Direkte Bearbeitung verwendet Viewports, Inhalte und Kontakte, um die interaktiven Elemente der Benutzeroberfläche zu beschreiben.
ms.assetid: 1564F6F2-844F-4392-9EB5-AA46059D514C
title: Viewports und Inhalt
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a103df916e5880380064250d05806169ff4187e6a8be0b22d2dd72d92343f38f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787074"
---
# <a name="viewports-and-content"></a>Viewports und Inhalt

[Die direkte Bearbeitung](direct-manipulation-portal.md) verwendet *Viewports,* *Inhalte* und *Kontakte,* um die interaktiven Elemente der Benutzeroberfläche zu beschreiben.

- [Konfigurieren eines Viewports](#configuring-a-viewport)
- [Ausrichtungspunkte und Begrenzungen](#snap-points-and-boundaries)
- [Snap point offset and RTL scenarios (Snappunktoffset und RTL-Szenarien)](#snap-point-offset-and-rtl-scenarios)
- [Verhalten](#behaviors)
- [Koordinatensystem](#coordinate-system)
- [Transformationen](#transforms)
- [Viewportzustand](#viewport-state)
- [Zugehörige Themen](#related-topics)

Ein *Viewport* ist eine Region innerhalb eines Fensters, die Eingaben von Benutzerinteraktionen empfangen und verarbeiten kann. Der Viewport stellt den Bereich des Inhalts dar, der dem Endbenutzer zu einem bestimmten Zeitpunkt angezeigt werden kann (auch als Inhaltsclip bezeichnet). Der Viewport verfügt über mehrere Funktionen:

- Sie verwaltet den Interaktionszustand (z. B. wenn der Inhalt bearbeitet werden kann, wenn Inhalt bearbeitet wird, wenn inhalt in Trägheitsanimation ist) und ordnet Eingaben Ausgabetransformationen zu.
- Sie enthält Inhalte, die als Reaktion auf die Benutzerinteraktion verschoben werden. Dies kann ein HTML-Div-Element (Scrollen), eine Schwenkliste (die Windows 8 Startbildschirm) oder das Popupmenü für ein Auswahlsteuerelement sein.

Ein Viewport wird durch Aufrufen von [**CreateViewport**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport)erstellt. Mehrere Viewports können in einem einzigen Fenster erstellt werden, um eine umfassende Benutzeroberfläche zu erzielen.

*Content* stellt das Element dar, das als Reaktion auf eine Interaktion transformiert wird. Anders ausgedrückt: Der Inhalt wird verschoben oder skaliert, wenn der Benutzer schwenkt oder kneift. Es gibt zwei Arten von Inhalten:

- *Primärer Inhalt* ist das einzelne systeminterne Element innerhalb eines Viewports, das auf Eingabemanipulationen und Trägheit reagiert. Primärer Inhalt wird zur gleichen Zeit wie der Viewport erstellt und kann nicht hinzugefügt oder aus einem Viewport entfernt werden. Sie können das Verhalten primärer Inhalte mithilfe von Andockpunkten anpassen (weiter unten erläutert).
- *Sekundärer Inhalt* wird relativ zur Bewegung des primären Inhalts verschoben. Sekundäre Inhalte werden getrennt vom Viewport erstellt und können einem Viewport hinzugefügt oder daraus entfernt werden. Alle sekundären Inhaltstransformationen werden basierend auf der Transformation des primären Inhalts berechnet. Bestimmte Regeln können angewendet werden, um zu ändern, wie die Transformation basierend auf dem beabsichtigten Zweck des Elements berechnet wird, das während der Erstellung durch seine CLSID identifiziert wird.

In diesem Diagramm, das vor und nach einem Schwenken zeigt, wurde ein einzelner Kontakt zum Schwenken primärer Inhalte verwendet. Obwohl der Benutzer nicht direkt mit dem Schwenkindikator (sekundärer Inhalt) interagiert, wird der sekundäre Inhalt verschoben, während der primäre Inhalt schwenkt. Dies bietet visuelle Hinweise dazu, wie weit der Benutzer schwenkt hat.

![Diagramm, das vor/nach einer Schwenkung zeigt](images/dm-art-2.png)

## <a name="configuring-a-viewport"></a>Konfigurieren eines Viewports

Nachdem Sie den Viewport erstellt haben. konfigurieren Sie sein Verhalten mithilfe einer *Interaktionskonfiguration.* Die Interaktionskonfiguration gibt an, welche Bearbeitungen wie Schwenken unterstützt werden.

*Das Schwenken* ändert die Position des Inhalts entlang der horizontalen oder vertikalen Achse oder beides, wenn ein Benutzer schwenkt. Wenn Sie die Übersetzung auf beiden Achsen konfigurieren, bewegt sich der Inhalt frei in jede Richtung.

Um die Bewegung des Inhalts einzuschränken, konfigurieren Sie Schienen , in der Regel sowohl auf der *horizontalen* als auch auf der vertikalen Achse. Wenn die Interaktion eines Benutzers in erster Linie entlang einer einzelnen Achse erfolgt (dargestellt durch die blauen Bereiche im nächsten Diagramm), wird der Schwenk *geschienen,* und der Inhalt bewegt sich nur auf der Schienenachse. Wenn der Benutzer schwenkt und derzeit geschienen wird und eine zweite Schwenkung ausführt, während sich der Inhalt in Trägheit befindet, wird die neue Schwenk weiter geschienen.

![Diagramm mit Inhalt innerhalb eines Viewports in einer Schienenschnee](images/dm-art-3.png)

Beispiel: Ein Viewport ist für horizontales und vertikales Schwenken konfiguriert. Im ersten Frame kommt der Kontakt herunter. In der zweiten wird eine vertikale Schwenkung initiiert, und der Kontakt wird an der vertikalen Schiene gesperrt. Sobald der Schwenk geschienen ist, wird nur die vertikale Komponente eines diagonalen Schwenkens verwendet, um den Inhalt zu verschieben.

Wenn der Benutzer diagonal in einer Weise schwenkt, dass er sich nicht in den Schienenerkennungsbereichen (den weißen Bereichen) befindet, ist der Schwenk *nicht geergt,* und der Inhalt bewegt sich frei in beiden Achsen.

![Diagramm zum Verschieben von Inhalten in einer geerbten Schwenkbewegung](images/dm-art-4.png)

*Durch das Zoomen* wird der Skalierungsfaktor des Inhalts geändert, wenn ein Benutzer eindrückt oder gestreckt wird. Der Punkt, um den der Inhalt skaliert wird (als Zoommittelpunkt bezeichnet), befindet sich in der Mitte der Kontakte. Wenn Sie die horizontale oder vertikale Ausrichtung festgelegt haben, ändert sich der Zoommittelpunkt, um die Ausrichtung beizubehalten.

![Diagramm, das das Zoomen von Inhalten mit einer angegebenen Ausrichtung zeigt](images/dm-art-5.png)

Sie können dieses Verhalten überschreiben, indem Sie entsperren center angeben, wodurch der Zoommittelpunkt in der Mitte der Kontakte festgelegt wird.

![Diagramm, das das Zoomen von Inhalten mit entsperrter Zoommitte zeigt](images/dm-art-6.png)

*Trägheit* ist die allmähliche Verlangsamung einer Manipulation, sowohl schwenkend als auch zoomend, nachdem alle Kontakte (bei Berührung) oder nach der Tastatur-/Mauseingabe (z. B. Klicken auf eine Bildlaufleiste oder Drücken der Pfeiltasten) entfernt wurden. Wenn ein Benutzer den Inhalt bearbeitet, wird die Bearbeitung nicht sofort beendet, nachdem der Kontakt aufgehoben wurde. Stattdessen wird der Inhalt in der aktuellen Richtung und Geschwindigkeit fortgesetzt und verlangsamt sich allmählich bis zum Ende.

## <a name="snap-points-and-boundaries"></a>Ausrichtungspunkte und Begrenzungen

Eine Trägheitsanimation findet statt, nachdem die Bearbeitung beendet wurde, wenn ein Finger vom Bildschirm (bei Toucheingabe) oder aufgrund einer Tastatur-/Mausaktion (z. B. Pfeiltasten, Nach oben/Unten, Mausrad scrollen usw.) entfernt wird.

Es gibt zwei Informationen, die die Trägheitsanimation definieren:

- Der Restpunkt der Animation– die endende Position der jeweiligen Transformationskomponente.
- Dauer, Kurve und Geschwindigkeit der Animation– diese werden durch den Typ des Restpunkts bestimmt.

Die Trägheitsanimation wird von Ausrichtungspunkten und Begrenzungen beeinflusst. Begrenzungen geben die maximalen und minimalen Restpunkte für Den Inhalt an. Wenn Inhalt während der Trägheit eine Grenze erreicht, wird eine Begrenzungsanimation angewendet. Ausrichtungspunkte werden für den primären Inhalt definiert, um den Restpunkt und die Trägheitsanimationskurve selbst zu ändern.

Sie definieren Ausrichtungspunkte mit [**SetSnapInterval,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval) wenn der Inhalt regelmäßig leer ist, oder mit [**SetSnapPoints,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints) wenn der Inhalt ungleichmäßig verteilt ist. Hier sehen Sie ein Beispiel für Ausrichtungspunkte:

![Diagramm, das zeigt, wie sich im Inhalt festgelegte Ausrichtungspunkte auf das Schwenken auswirken](images/dm-snappoint-states-3.png)

Im Diagramm gibt es einen Inhalt mit einer Reihe von Unterinhaltsblöcken– Nachrichtenelemente in einer App vom Typ "News-Reader" oder Elemente in einer Rasteransicht. Die Absicht besteht darin, den linken Rand eines Elements am linken Rand des Viewports zu ausrichten, nachdem die Trägheit beendet wurde.

Es gibt zwei Gruppen von Ausrichtungspunkttypen:

- *Optional im Vergleich zu Obligatorisch:* Ein optionaler Andockpunkt richtet die Trägheitsanimation nur an, wenn sich der Trägheits-Restpunkt in der Nähe des Ausrichtungspunkts befindet. Bei einem obligatorischen Andockpunkt wird die Trägheitsanimation immer an einem angegebenen Andockpunkt ausgerichtet.
- *Single vs. Multiple*: Ein Typ mit mehreren Andockpunkten ermöglicht es dem Inhalt, sich über viele Andockpunkte zu bewegen, bevor er an einem Andockpunkt in der Nähe seines natürlichen Ruhepunkts in den Ruhezustand wechselt. Ein einzelner Ausrichtungspunkttyp wählt den nächsten Ausrichtungspunkt als Restpunkt für die Trägheitsanimation aus.

Das nächste Diagramm zeigt, wie Ausrichtungspunkttypen die Restposition der Trägheitsanimation ändern.

![Diagramm, das zeigt, wie Trägheit und Ausrichtungspunkte interagieren](images/dm-snappoint-states-1.png)

In diesem Diagramm wird der Trägheitsstartpunkt als "Start" und die natürliche Trägheitsendeposition ohne Ausrichtungspunkte als "Ende" bezeichnet. Die vertikalen Linien markieren die verschiedenen Ausrichtungspunkte. In dieser Tabelle wird beschrieben, wie sich jeder Ausrichtungspunkttyp auf die Endposition der Animation auswirkt.

| Punkttyp         | BESCHREIBUNG                                                                                |
|--------------------|--------------------------------------------------------------------------------------------|
| Obligatorischer Einzelner   | Der Ausrichtungspunkt P1 wird ausgewählt, da er der erste Ausrichtungspunkt in Richtung Trägheit ist.     |
| Obligatorisches Vielfaches | Der Ausrichtungspunkt P2 wird ausgewählt, da er dem Endpunkt in Richtung Trägheit am nächsten liegt. |
| Optional single    | Der Ausrichtungspunkt P1 wird ausgewählt, da es sich um den ersten Ausrichtungspunkt handelt, der während der Trägheit gefunden wurde.      |
| Optionales Vielfaches  | Der Ausrichtungspunkt P2 wird ausgewählt, da er sich in der Nähe des natürlichen Endpunkts befindet.                           |

## <a name="snap-point-offset-and-rtl-scenarios"></a>Snap point offset and RTL scenarios (Snappunktoffset und RTL-Szenarien)

![Diagramm zur Verwendung des RTL-Andockpunkts](images/dm-snappoint-states-2.png)

Sie wenden den Ausrichtungspunktoffset und das Koordinatensystem mithilfe der [**SetSnapCoordinate-API**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) an, die alle Ausrichtungspunkte oder Ausrichtungsintervalle mithilfe des angegebenen Offset-/Koordinatensystems versetzt.

Das Koordinatensystem ist sehr nützlich in RTL-Szenarien, in denen Sie Ausrichtungspunkte vom linken Rand des Inhalts in umgekehrter Richtung beschreiben möchten. Im vorherigen Diagramm wird [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) mit dem **DIRECTMANIPULATION \_ MOTION \_ TRANSLATEX-** und **DIRECTMANIPULATION \_ COORDINATE \_ MIRRORED-Flag** verwendet, das automatisch die Ausrichtungspunkte vom linken Rand des Inhalts versetzt und in der Reihenfolge von rechts nach links angibt: S1 ist bei 0px, S2 ist bei 50px (und so weiter). Alle Offsets, die **SetSnapCoordinate** verwenden, werden automatisch von diesem linken Rand des Inhalts abgesetzt, einschließlich des richtigen Skalierungsfaktors.

Sie verwenden fast immer [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) mit dem festgelegten *Origin-Parameter,* um das Festlegen von Ausrichtungspunkten außerhalb des Inhaltsbereichs zu vermeiden.

Wenn der Viewport beispielsweise 200x200 ist und der Inhalt 1000x200 ist und die Schnittstelle RTL ist, hat der Viewport den linken Rand bei x=800, wenn der Viewport zum ersten Mal angezeigt wird. Rufen [**Sie SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) mit auf, um anzugeben, dass die Ausrichtungspunkte beginnend am rechten Rand des Inhalts von rechts nach links `SetSnapCoordinate(DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_COORDINATE_MIRRORED, 1000.0)` berechnet werden sollen.

## <a name="behaviors"></a>Verhalten

Ein *Verhalten* ist ein Objekt, das an einen Viewport angefügt werden kann, um zu ändern, wie die direkte [Manipulation](direct-manipulation-portal.md) die Ausgabetransformation des primären oder sekundären Inhalts eines Viewports behandelt. Ein Verhaltensobjekt kann sich auf einen oder mehrere Aspekte einer Manipulation auswirken, z. B. die Verarbeitung der Eingabe oder die Anwendung der Trägheitsanimation. Ein Automatisches Bildlaufverhalten wirkt sich beispielsweise auf die Trägheitsanimation aus, indem eine Bildlaufanimation in Richtung eines Endes des primären Inhalts erstellt wird. Ein übergreifendes Konfigurationsverhalten wirkt sich auf die Direkte Bearbeitungseingabeverarbeitung aus, die erkennt, wenn eine übergreifende Schiebeaktion ausgeführt wird.

Ein Verhaltensobjekt wird durch Aufrufen von [**CreateBehavior**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager2-createbehavior)erstellt, einem Viewport hinzugefügt und dann asynchron konfiguriert. Durch das Entfernen des Verhaltens aus dem Viewport werden seine Auswirkungen entfernt.

## <a name="coordinate-system"></a>Koordinatensystem

Es gibt drei Hauptkoordinatensysteme, die von der direkten [Manipulation verwendet werden:](direct-manipulation-portal.md)

- Clientkoordinatensystem: Beschreibt das Rechteck des Clientfensters. Einheiten werden in Pixeln angegeben.
- Viewportkoordinatensystem: Beschreibt das Rechteck eines Bereich innerhalb des Clients, der Eingaben verarbeiten kann. Einheiten sind anwendungsdefiniert (mit [**SetViewportRect).**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect)
- Inhaltskoordinatensystem: Beschreibt das Rechteck oder die Größe des primären Inhalts. Einheiten sind anwendungsdefiniert (mit [**SetContentRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect)).

Für alle drei Systeme werden Koordinaten relativ zum jeweiligen Ursprung links oben definiert und sind nach rechts und unten positiv. Diese Koordinatensysteme werden im nächsten Diagramm dargestellt. Nur der Abschnitt des Inhalts innerhalb des Viewportrechtecks kann vom Endbenutzer angezeigt oder bearbeitet werden.

![Diagramm, das zeigt, wie Die Koordinaten von Inhalt, Client und Viewport interagieren](images/dm-art-7.png)

## <a name="transforms"></a>Transformationen

[Die direkte Manipulation](direct-manipulation-portal.md) verwaltet mehrere verschiedene Transformationen, die zur insgesamt angezeigten Ausgabe beitragen.

- *Inhaltstransformation:* Die ursprüngliche Transformation, die von der direkten [Manipulation basierend](direct-manipulation-portal.md) auf einer Manipulation oder Trägheit berechnet wird. Er erfasst die Auswirkungen von Ausrichtungspunkten, Railing, Standardübersprung (Manipulation), Standardübersprung (Trägheit) und ZoomToRect-Animationen.
- *Ausgabetransformation:* die endgültige Visual- oder Ausgabetransformation. Dabei handelt es sich um die Kombination aus dem Inhalt und den Synchronisierungstransformationen.
- *Synchronisierungstransformation:* wird berechnet, wenn [**Sie SyncContentTransform aufrufen.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-synccontenttransform) Sie hilft [der direkten Bearbeitung](direct-manipulation-portal.md) dabei, eine neue Inhaltstransformation anzuwenden, die von der Anwendung bereitgestellt wird, während gleichzeitig die vorhandene Ausgabetransformation beibehalten wird.
- *Anzeigetransformation:* Wird von der Anwendung im Rahmen der Nachverarbeitung angewendet. Weitere [**Informationen finden Sie unter SyncDisplayTransform.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)

Da die Ausgabetransformation dazu dient, eine Oberfläche visuell auf dem Bildschirm zu veroffen, führt die direkte [Bearbeitung](direct-manipulation-portal.md) die erforderliche Rundung der Ausgabetransformationskomponenten durch, sodass Text und anderer Inhalt immer an einer integralen Pixelgrenze gerendert/zusammengesetzt werden. Der Rundungsmechanismus hängt von mehreren Faktoren ab, einschließlich der Geschwindigkeit der Bewegung und dem Vorhandensein Remotedesktop. Der Rundungsmechanismus für sekundären Inhalt entspricht dem des primären Inhalts, wobei der Unterschied bei der Bewegung zwischen den beiden berücksichtigt wird. Clients von [**GetOutputTransform sollten**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) nicht vom genauen Rundungsmechanismus der Ausgabetransformation abhängen, da sich verschiedene Faktoren darauf auswirken.

> [!Note]
>
> Dies bedeutet, dass die Komponenten einer Inhaltstransformation möglicherweise nicht ganzzahlig sind und Unterpixeloffsets enthalten können. Clients, [die die direkte Bearbeitung](direct-manipulation-portal.md) verwenden, wird empfohlen, [**getOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) zu verwenden, um die richtige visuelle Transformation zu berechnen, die auf den Inhalt angewendet werden soll, wenn der manuelle Aktualisierungsmodus verwendet wird. Bei Verwendung des automatischen Updatemodus mit dem integrierten Compositor wendet die direkte Manipulation diese Transformation automatisch im Auftrag des Clients an. Diese Transformation wird durch die direkte Bearbeitung generiert, um sicherzustellen, dass beim Verfassen der visuellen Ausgabe visuell ansprechende Ergebnisse erzielt werden.

## <a name="viewport-state"></a>Viewportzustand

Während die Eingabe verarbeitet wird, verwaltet der Viewport den Interaktionszustand und die Zuordnung der Eingabe zu Ausgabetransformationen. Überprüfen Sie den Interaktionsstatus des Viewports, indem Sie [**GetStatus aufrufen.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-getstatus)

![Diagramm, das den Interaktionszuständen der direkten Manipulation zeigt](images/dm-states-diagram.png)

- Erstellen: Der Viewport wird erstellt und kann die Eingabe noch nicht verarbeiten. Rufen Sie zum Verarbeiten der Eingabe [**IDirectManipulationViewport::Enable auf.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable) Wenn **Enable** nicht aufgerufen wird, wird der Viewport in den Status Deaktiviert versetzt.

    > [!Note]  
    > Dies ist der anfängliche Zustand der Interaktion.

- Aktiviert: Der Viewport kann Eingaben verarbeiten. Wenn ein Kontakt auskommt [**(SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) wird aufgerufen) und eine Manipulation erkannt wird, geht der Viewport in Wird ausgeführt über.

- Wird ausgeführt: Der Viewport verarbeitet derzeit Eingaben und aktualisiert Inhalte. Wenn der Kontakt aufgehoben wird, geht der Viewport in Trägheit über, sofern konfiguriert.

- Trägheit: Der Inhalt wird in einer Trägheitsanimation bewegt. Sobald die Trägheit abgeschlossen ist, wird der Viewport in Ready (Bereit) übergewechselt. Wenn die automatische Deaktivierung für den Viewport festgelegt wurde, wird sie von Trägheit zu Bereit und dann zu Deaktiviert.

- Bereit: Der Viewport kann Eingaben verarbeiten. Wenn ein Kontakt auskommt [**(SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) wird aufgerufen) und eine Manipulation erkannt wird, geht der Viewport in Wird ausgeführt über.

- Angehalten: Der Viewport kann angehalten werden, wenn seine Eingabe zu einem übergeordneten Element in der [**SetContact-Kette promotet**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) wurde. Dies wird unter Mehrere [Viewports: Treffertests und Viewporthierarchie](directmanipulation-multiple-vieports.md)ausführlicher erläutert.

- Deaktiviert: Der Viewport verarbeiten keine Eingaben oder Rückrufe. Ein Viewport kann durch Aufrufen von [**IDirectManipulationViewport::D deaktiviert werden.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-disable) Wenn die automatische Deaktivierung für den Viewport festgelegt wurde, wird sie automatisch auf Deaktiviert umgeschaltet, nachdem eine Bearbeitung verarbeitet wurde. Um einen deaktivierten Viewport erneut zu aktivieren, rufen Sie [**IDirectManipulationViewport::Enable auf.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable)

## <a name="related-topics"></a>Zugehörige Themen

[Mehrere Viewports: Treffertests und Viewporthierarchie,](directmanipulation-multiple-vieports.md) [**ActivateConfiguration,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration) [**GetOutputTransform,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)
