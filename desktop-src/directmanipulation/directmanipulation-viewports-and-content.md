---
description: Die direkte Bearbeitung verwendet Viewports, Inhalte und Kontakte, um die interaktiven Elemente der Benutzeroberfläche zu beschreiben.
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
- [Ausrichtungspunkte und Grenzen](#snap-points-and-boundaries)
- [Andockpunktoffset und RTL-Szenarien](#snap-point-offset-and-rtl-scenarios)
- [Verhalten](#behaviors)
- [Koordinatensystem](#coordinate-system)
- [Transformationen](#transforms)
- [Viewportzustand](#viewport-state)
- [Zugehörige Themen](#related-topics)

Ein *Viewport* ist ein Bereich innerhalb eines Fensters, der Eingaben von Benutzerinteraktionen empfangen und verarbeiten kann. Der Viewport stellt den Bereich des Inhalts dar, der dem Endbenutzer zu einem bestimmten Zeitpunkt angezeigt werden kann (auch als Inhaltsclip bezeichnet). Der Viewport verfügt über mehrere Funktionen:

- Sie verwaltet den Interaktionszustand (z. B. wenn der Inhalt bearbeitet werden kann, wenn Inhalt bearbeitet wird, wenn inhalt sich in Trägheitsanimation befindet) und ordnet Eingaben Ausgabetransformationen zu.
- Sie enthält Inhalt, der als Reaktion auf die Benutzerinteraktion bewegt wird. Dies kann ein HTML-Div-Element (Scrollen), eine schwenkbar-Liste (die Windows 8 Startbildschirm) oder das Popupmenü für ein Auswahlsteuerelement sein.

Ein Viewport wird durch Aufrufen von [**CreateViewport erstellt.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport) Mehrere Viewports können in einem einzelnen Fenster erstellt werden, um eine umfassende Benutzeroberfläche zu erzeugen.

*Inhalt* stellt das Element dar, das als Reaktion auf eine Interaktion transformiert wird. Anders ausgedrückt: Der Inhalt wird bewegt oder skaliert, wenn der Benutzer schwenkt oder drückt. Es gibt zwei Arten von Inhalten:

- *Primärer Inhalt* ist das einzelne systeminterne Element innerhalb eines Viewports, das auf Eingabemanipulationen und Trägheit reagiert. Primärer Inhalt wird gleichzeitig mit dem Viewport erstellt und kann nicht zu einem Viewport hinzugefügt oder daraus entfernt werden. Sie können das Verhalten des primären Inhalts mithilfe von Andockpunkten anpassen (siehe weiter oben).
- *Sekundärer Inhalt* wird relativ zur Bewegung des primären Inhalts bewegt. Sekundärer Inhalt wird getrennt vom Viewport erstellt und kann einem Viewport hinzugefügt oder daraus entfernt werden. Alle sekundären Inhaltstransformationen werden basierend auf der Transformation des primären Inhalts berechnet. Bestimmte Regeln können angewendet werden, um zu ändern, wie die Transformation basierend auf dem beabsichtigten Zweck des Elements berechnet wird, das während der Erstellung durch seine CLSID identifiziert wird.

In diesem Diagramm, das vor und nach einer Schwenkung zeigt, wurde ein einzelner Kontakt verwendet, um den primären Inhalt zu schwenken. Obwohl der Benutzer nicht direkt mit dem Schwenkindikator (sekundärer Inhalt) interagiert, wird der sekundäre Inhalt beim Schwenken des primären Inhalts bewegt. Dadurch erhalten Sie visuelle Hinweise dazu, wie weit der Benutzer geschwenken hat.

![Diagramm, das vor/nach einer Schwenkung zeigt](images/dm-art-2.png)

## <a name="configuring-a-viewport"></a>Konfigurieren eines Viewports

Nachdem Sie den Viewport erstellt haben. Konfigurieren Sie das Verhalten mithilfe einer *Interaktionskonfiguration.* Die Interaktionskonfiguration gibt an, welche Manipulationen, z. B. Schwenken, unterstützt werden.

*Das Schwenken* ändert die Position des Inhalts auf der horizontalen oder vertikalen Achse oder beidem, während ein Benutzer schwenkt. Wenn Sie die Übersetzung auf beiden Achsen konfigurieren, bewegt sich der Inhalt frei in beliebige Richtung.

Um die Bewegung des Inhalts zu beschränken, konfigurieren Sie *Schienen*, in der Regel sowohl auf der horizontalen als auch auf der vertikalen Achse. Wenn sich die Interaktion eines Benutzers hauptsächlich entlang einer einzelnen Achse befindet (dargestellt  durch die blauen Bereiche im nächsten Diagramm), wird die Schwenke geschienen, und der Inhalt bewegt sich nur entlang der geschiedenen Achse. Wenn der Benutzer schwenkt und derzeit geschienen ist und eine zweite Schwenkung ausführt, während der Inhalt träg ist, wird die neue Schwenkung weiterhin geschienen.

![Diagramm mit Inhalt in einem Viewport in einer geschiedenen Schwenke](images/dm-art-3.png)

Beispiel: Ein Viewport ist für horizontales und vertikales Schwenken konfiguriert. Im ersten Frame wird der Kontakt heruntergefahren. In der zweiten wird eine vertikale Schwenkung initiiert, und der Kontakt ist an der vertikalen Schiene gesperrt. Nachdem die Schwenkung geschienen wurde, wird nur die vertikale Komponente einer diagonalen Schwenke verwendet, um den Inhalt zu verschieben.

Wenn der Benutzer diagonal so schwenkt, dass er sich nicht in den Schienenerkennungsregionen (den weißen Regionen) befindet, wird die Schwenke nicht geschwenken, und der Inhalt wird auf beiden Achsen frei bewegt. 

![Diagramm mit Inhalt, der in einer nicht geschwenken Schwenkung bewegt wird](images/dm-art-4.png)

*Beim Zoomen* wird der Skalierungsfaktor des Inhalts geändert, wenn ein Benutzer heften oder strecken muss. Der Punkt, um den der Inhalt skaliert wird (als Zoomcenter bezeichnet), befindet sich in der Mitte der Kontakte. Wenn Sie die horizontale oder vertikale Ausrichtung festgelegt haben, ändert sich das Zoomcenter, um die Ausrichtung zu erhalten.

![Diagramm, das das Zoomen von Inhalten mit einer angegebenen Ausrichtung zeigt](images/dm-art-5.png)

Sie können dieses Verhalten überschreiben, indem Sie das Entsperren des Mittelpunkts angeben, wodurch das Zoomcenter in der Mitte der Kontakte festgelegt wird.

![Diagramm, das das Zoomen des Inhalts mit dem entsperrten Zoomcenter zeigt](images/dm-art-6.png)

*Trägheit* ist die allmähliche Verlangsamung einer Manipulation, sowohl schwenkend als auch zoomend, nachdem alle Kontakte (bei Toucheingabe) oder nach der Tastatur-/Mauseingabe (z. B. Klicken auf eine Bildlaufleiste oder Drücken der Pfeiltasten) aufgehoben wurden. Wenn ein Benutzer den Inhalt bearbeitet, wird die Bearbeitung nicht sofort nach dem Heben des Kontakts aufgehoben. Stattdessen wird der Inhalt in der aktuellen Richtung und Geschwindigkeit fortgesetzt und langsam bis zum Ende verlangsamt.

## <a name="snap-points-and-boundaries"></a>Ausrichtungspunkte und Grenzen

Eine Trägheitsanimation findet statt, nachdem die Bearbeitung beendet wurde, weil ein Finger (bei Toucheingabe) vom Bildschirm bzw. als Ergebnis einer Tastatur-/Mausaktion (z. B. Pfeiltasten, Bildlauf nach oben/unten, Scrollen mit dem Mausrad usw.) gedrückt wird.

Es gibt zwei Informationen, die die Trägheitsanimation definieren:

- Der Restpunkt der Animation – die endgültige Endposition der jeweiligen Transformationskomponente.
- Animationsdauer, Kurve, Geschwindigkeit– diese werden durch den Typ des Restpunkts bestimmt.

Die Trägheitsanimation wird von Andockpunkten und Begrenzungen beeinflusst. Grenzen geben die maximalen und minimalen Restpunkte für Inhalt an. Wenn Inhalt während der Trägheit eine Grenze erreicht, wird eine Begrenzungsanimation angewendet. Ausrichtungspunkte werden für den primären Inhalt definiert, um den Restpunkt zu ändern und die Trägheitsanimationkurve selbst zu ändern.

Sie definieren Andockpunkte mit [**SetSnapInterval,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval) wenn sich der Inhalt regelmäßig in einem Abstand befindet, oder mit [**SetSnapPoints,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints) wenn der Inhalt ungleichmäßig verteilt ist. Hier ist ein Beispiel für Andockpunkte:

![Diagramm, das zeigt, wie sich ausrichtungspunkte, die im Inhalt festgelegt sind, auf das Schwenken auswirken](images/dm-snappoint-states-3.png)

Das Diagramm enthält einen Inhalt mit einer Reihe von Unterinhaltsblöcken– Nachrichtenelemente in einer News-Reader-App oder Elemente in einer Rasteransicht. Die Absicht besteht im Ausrichten des linken Rands eines Elements am linken Rand des Viewports, nachdem die Trägheit beendet wurde.

Es gibt zwei Gruppen von Ausrichtungspunkttypen:

- *Optional im Vergleich zu Obligatorisch:* Ein optionaler Andockpunkt zeigt die Trägheitsanimation nur an, wenn sich der Trägheits-Restpunkt in der Nähe des Andockpunkts befindet. Ein obligatorischer Andockpunkt zeigt die Trägheitsanimation immer an einem angegebenen Andockpunkt an.
- *Einzelne oder mehrere:* Ein Typ mit mehreren Ausrichtungspunkten ermöglicht es dem Inhalt, sich über viele Andockpunkte hinweg zu bewegen, bevor er an einem Andockpunkt in der Nähe seines natürlichen Restpunkts zur Ruhe kommt. Ein einzelner Ausrichtungspunkttyp wählt den nächsten Andockpunkt als Restpunkt für die Trägheitsanimation aus.

Das nächste Diagramm zeigt, wie Ausrichtungspunkttypen die Restposition der Trägheitsanimation ändern.

![Diagramm, das zeigt, wie Trägheit und Andockpunkte interagieren](images/dm-snappoint-states-1.png)

In diesem Diagramm wird der Trägheitsstartpunkt als "Start" und die natürliche Endposition der Trägheit ohne Andockpunkte als "Ende" bezeichnet. Die vertikalen Linien markieren die verschiedenen Ausrichtungspunkte. In dieser Tabelle wird beschrieben, wie sich die einzelnen Ausrichtungspunkttypen auf die Endposition der Animation auswirken.

| Punkttyp         | BESCHREIBUNG                                                                                |
|--------------------|--------------------------------------------------------------------------------------------|
| Obligatorisches Single   | Der Ausrichtungspunkt P1 wird ausgewählt, da er der erste Andockpunkt in Richtung Trägheit ist.     |
| Obligatorisches Vielfaches | Der Ausrichtungspunkt P2 wird ausgewählt, da er dem Endpunkt in Richtung Trägheit am nächsten liegt. |
| Optional single    | Der Ausrichtungspunkt P1 wird ausgewählt, da er der erste Andockpunkt ist, der während der Trägheit auftritt.      |
| Optionales Vielfaches  | Der Ausrichtungspunkt P2 wird ausgewählt, da er sich in der Nähe des natürlichen Endpunkts befindet.                           |

## <a name="snap-point-offset-and-rtl-scenarios"></a>Andockpunktoffset und RTL-Szenarien

![Diagramm, das die Verwendung des Rtl-Andockpunkts zeigt](images/dm-snappoint-states-2.png)

Sie wenden den Andockpunktoffset und das Koordinatensystem mithilfe der [**SetSnapCoordinate-API**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) an, die alle Ausrichtungspunkte oder Ausrichtungsintervalle mithilfe des angegebenen Offset-/Koordinatensystems versetzt.

Das Koordinatensystem ist sehr nützlich in RTL-Szenarien, in denen Sie Ausrichtungspunkte vom linken Rand des Inhalts in umgekehrter Richtung beschreiben möchten. Im vorherigen Diagramm wird [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) mit dem **Flag DIRECTMANIPULATION \_ MOTION \_ TRANSLATEX** und **DIRECTMANIPULATION \_ COORDINATE \_ MIRRORED** verwendet, das die Ausrichtungspunkte automatisch vom linken Rand des Inhalts versetzt und in der Reihenfolge von rechts nach links liefert: S1 ist bei 0px, S2 bei 50px (und so weiter). Alle Offsets, die **setSnapCoordinate** verwenden, werden automatisch von diesem linken Rand des Inhalts versetzt, einschließlich des richtigen Skalierungsfaktors.

Sie verwenden fast immer [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) mit dem *festgelegten* Origin-Parameter, um das Festlegen von Andockpunkten außerhalb des Inhaltsbereichs zu vermeiden.

Wenn der Viewport beispielsweise 200x200 und der Inhalt 1000x200 und die Schnittstelle RTL ist, hat der Viewport den linken Rand bei x=800, wenn der Viewport zum ersten Mal angezeigt wird. Rufen [**Sie SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) mit `SetSnapCoordinate(DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_COORDINATE_MIRRORED, 1000.0)` auf, um anzugeben, dass die Ausrichtungspunkte von rechts nach links ab dem rechten Rand des Inhalts berechnet werden sollen.

## <a name="behaviors"></a>Verhalten

Ein *Verhalten* ist ein Objekt, das an einen Viewport angefügt werden kann, um zu ändern, wie [direct Manipulation](direct-manipulation-portal.md) die Ausgabetransformation des primären oder sekundären Inhalts eines Viewports behandelt. Ein Verhaltensobjekt kann einen oder mehrere Aspekte einer Bearbeitung beeinflussen, z. B. die Verarbeitung der Eingabe oder die Anwendung der Trägheitsanimation. Beispielsweise wirkt sich ein Automatisches Rollingverhalten auf die Trägheitsanimation aus, indem eine Bildlaufanimation an ein Ende des primären Inhalts ausgeführt wird. Ein schiebeübergreifendes Konfigurationsverhalten wirkt sich auf die Direkte Bearbeitungseingabeverarbeitung aus, die erkennt, wenn eine schiebeübergreifende Aktion ausgeführt wird.

Ein Verhaltensobjekt wird erstellt, indem [**CreateBehavior**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager2-createbehavior)aufgerufen wird, einem Viewport hinzugefügt wird und dann sein Verhalten asynchron konfiguriert wird. Wenn Sie das Verhalten aus dem Viewport entfernen, werden seine Auswirkungen entfernt.

## <a name="coordinate-system"></a>Koordinatensystem

Es gibt drei Hauptkoordinatensysteme, die von [direct manipulation](direct-manipulation-portal.md)verwendet werden:

- Clientkoordinatensystem: Beschreibt das Rechteck des Clientfensters. Einheiten sind in Pixel.
- Viewportkoordinatensystem: Beschreibt das Rechteck eines Bereichs innerhalb des Clients, der Eingaben verarbeiten kann. Einheiten sind anwendungsdefiniert (mit [**SetViewportRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect)).
- Inhaltskoordinatensystem: Beschreibt das Rechteck oder die Größe des primären Inhalts. Einheiten sind anwendungsdefiniert (mit [**SetContentRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect)).

Für alle drei Systeme werden Koordinaten relativ zu ihrem jeweiligen linken oberen Ursprung definiert und positiv nach rechts und unten erhöht. Diese Koordinatensysteme werden im nächsten Diagramm veranschaulicht. Nur der Abschnitt des Inhalts innerhalb des Viewportrechtecks kann vom Endbenutzer angezeigt oder bearbeitet werden.

![Diagramm, das zeigt, wie Inhalt, Client und Viewportkoordinaten interagieren](images/dm-art-7.png)

## <a name="transforms"></a>Transformationen

[Die direkte Bearbeitung](direct-manipulation-portal.md) verwaltet mehrere verschiedene Transformationen, die zur angezeigten Gesamtausgabe beitragen.

- *Inhaltstransformation:* die anfängliche Transformation, die von [der direkten Bearbeitung](direct-manipulation-portal.md) basierend auf einer Manipulation oder Trägheit berechnet wird. Sie erfasst die Auswirkungen von Andockpunkten, Railing, Standardüberlauf (Manipulation), Standardüberlauf (Trägheit) und ZoomToRect-Animationen.
- *Ausgabetransformation:* die endgültige Visual- oder Ausgabetransformation. Dies ist die Kombination aus Inhalt und Synchronisierungstransformationen.
- *Synchronisierungstransformation:* Wird berechnet, wenn Sie [**SyncContentTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-synccontenttransform)aufrufen. Sie unterstützt [die direkte Bearbeitung](direct-manipulation-portal.md) beim Anwenden einer neuen Inhaltstransformation, die von der Anwendung bereitgestellt wird, während gleichzeitig die vorhandene Ausgabetransformation beibehalten wird.
- *Anzeigetransformation:* Wird von der Anwendung im Rahmen der Nachverarbeitung angewendet. Weitere Informationen finden Sie unter [**SyncDisplayTransform.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)

Da die Ausgabetransformation eine Oberfläche visuell auf dem Bildschirm versetzen soll, führt [direct Manipulation](direct-manipulation-portal.md) die erforderliche Rundung der Ausgabetransformationskomponenten durch, sodass Text und andere Inhalte immer an einer ganzzahligen Pixelgrenze gerendert/zusammengesetzt werden. Der Rundungsmechanismus hängt von mehreren Faktoren ab, einschließlich der Geschwindigkeit der Bewegung und des Vorhandenseins von Remotedesktop. Der Rundungsmechanismus für sekundären Inhalt stimmt mit dem des primären Inhalts überein, wobei der Unterschied in der Bewegung zwischen den beiden berücksichtigt wird. Clients von [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) sollten nicht vom genauen Rundungsmechanismus der Ausgabetransformation abhängig sein, da verschiedene Faktoren dies beeinflussen.

> [!Note]
>
> Dies bedeutet, dass die Komponenten einer Inhaltstransformation möglicherweise nicht ganzzahlig sind und Subpixeloffsets enthalten können. Clients, die [die direkte Bearbeitung](direct-manipulation-portal.md) verwenden, wird empfohlen, [**getOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) zu verwenden, um die richtige visuelle Transformation zu berechnen, die bei Verwendung des manuellen Updatemodus auf den Inhalt angewendet werden soll. Bei Verwendung des automatischen Updatemodus mit dem integrierten Compositor wendet direct Manipulation diese Transformation automatisch im Auftrag des Clients an. Diese Transformation wird durch direkte Bearbeitung generiert, um beim Erstellen der visuellen Ausgabe visuell ansprechende Ergebnisse sicherzustellen.

## <a name="viewport-state"></a>Viewportzustand

Während die Eingabe verarbeitet wird, verwaltet der Viewport den Interaktionszustand und die Zuordnung der Eingabe zu Ausgabetransformationen. Überprüfen Sie den Interaktionsstatus des Viewports, indem [**Sie GetStatus**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-getstatus)aufrufen.

![Diagramm mit direktenManipulationsinteraktionszuständen](images/dm-states-diagram.png)

- Erstellen: Der Viewport wird erstellt und kann noch keine Eingaben verarbeiten. Rufen Sie [**IDirectManipulationViewport::Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable)auf, um Eingaben zu verarbeiten. Wenn **Enable** nicht aufgerufen wird, wechselt der Viewport in den Status Deaktiviert.

    > [!Note]  
    > Dies ist der Anfängliche Zustand der Interaktion.

- Aktiviert: Der Viewport kann Eingaben verarbeiten. Wenn ein Kontakt ausgeht [**(SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) wird aufgerufen), und eine Manipulation erkannt wird, geht der Viewport in Wird ausgeführt über.

- Wird ausgeführt: Der Viewport verarbeitet derzeit Eingaben und aktualisiert Inhalte. Wenn der Kontakt entfernt wird, geht der Viewport in Trägheit über, sofern konfiguriert.

- Trägheit: Der Inhalt bewegt sich in einer Trägheitsanimation. Sobald die Trägheit abgeschlossen ist, wechselt der Viewport zu Bereit. Wenn die automatische Deaktivierung für den Viewport festgelegt wurde, wechselt sie von Trägheit zu Bereit und dann zu Deaktiviert.

- Bereit: Der Viewport kann Eingaben verarbeiten. Wenn ein Kontakt ausgeht [**(SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) wird aufgerufen), und eine Manipulation erkannt wird, geht der Viewport in Wird ausgeführt über.

- Angehalten: Der Viewport wird möglicherweise angehalten, wenn seine Eingabe zu einem übergeordneten Element in der [**SetContact-Kette**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) heraufgestuft wurde. Dies wird unter [Mehrere Viewports: Treffertests und Viewporthierarchie](directmanipulation-multiple-vieports.md)ausführlicher erläutert.

- Deaktiviert: Der Viewport verarbeitet keine Eingaben und führt keine Rückrufe durch. Ein Viewport kann aus verschiedenen Zuständen deaktiviert werden, indem [**IDirectManipulationViewport::D isable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-disable)aufgerufen wird. Wenn die automatische Deaktivierung für den Viewport festgelegt wurde, wechselt sie automatisch zu Deaktiviert, nachdem eine Bearbeitung verarbeitet wurde. Um einen deaktivierten Viewport erneut zu aktivieren, rufen [**Sie IDirectManipulationViewport::Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable)auf.

## <a name="related-topics"></a>Zugehörige Themen

[Mehrere Viewports: Treffertests und Viewporthierarchie,](directmanipulation-multiple-vieports.md) [**ActivateConfiguration,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration) [**GetOutputTransform,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)
