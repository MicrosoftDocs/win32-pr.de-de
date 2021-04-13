---
description: Nachdem die frei Hand Eingaben erfasst wurden, können Anwendungen diese Daten auf andere Medien verwalten, bearbeiten und/oder übertragen.
ms.assetid: 5a8c370e-79cb-47f0-a7b3-a631874ad757
title: Frei Hand Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de73291269398ae42a47ee26897c8da9bac8abe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525964"
---
# <a name="ink-data"></a>Frei Hand Daten

Nachdem die frei Hand Eingaben erfasst wurden, können Anwendungen diese Daten auf andere Medien verwalten, bearbeiten und/oder übertragen. Die Aktionen der Auswahl, dem Kopieren, verschieben, speichern, anzeigen und Ändern der frei Hand Eingaben erfolgen für das frei [**Hand Objekt und die darin**](inkdisp-class.md) enthaltenen Elemente, wie z. b. die [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung und die [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte.

> [!Note]  
> Mithilfe Real-Time Tablettstifts können Anwendungen Daten in einem eigenen Format (z. b. beim Speichern von Strichen) verwalten.

 

## <a name="ink-strokes-and-packets"></a>Frei Hand Eingaben, Striche und Pakete

Ein [**Ink**](inkdisp-class.md) -Objekt ist der grundlegende Datentyp, von dem die vom [**InkCollector**](inkcollector-class.md) -Objekt gesammelten Eingaben verwaltet, manipuliert und gespeichert werden. Ein **Ink** -Objekt enthält ein oder mehrere [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte und allgemeine Methoden und Eigenschaften, mit denen diese Striche verwaltet und bearbeitet werden können. Ein Strich wird als Satz von Daten definiert, die in einer einzelnen Stift-nach-unten-, Stift-und Stift Bewegung aufgezeichnet werden. Die Strich Daten enthalten eine Sammlung von Paketen. Ein Paket ist der Satz von Daten, den das Tablet-Gerät an jedem Beispiel Punkt sendet. Diese Daten enthalten Informationen wie z. b. Koordinaten, Stift Druck, Stift Winkel und alles andere, was die Hardware übertragen kann. Die [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) -Eigenschaft des **Stroke** -Objekts beschreibt die Pakete, die von einem [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) generiert werden.

## <a name="strokes"></a>Striche

Sie können eine Momentaufnahme der Striche in einem frei Hand Objekt mithilfe der [**Striche**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) -Eigenschaft des **Ink** [**-Objekts abrufen**](inkdisp-class.md) . Die **Strokes** -Eigenschaft ist eine Auflistung von Verweisen auf die Striche im **Ink** -Objekt zum Zeitpunkt, zu dem die **Strokes** -Eigenschaft gelesen wird. Wenn später Striche dem **Ink** -Objekt hinzugefügt oder daraus gelöscht werden, wird eine zuvor abgerufene [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung nicht aktualisiert. Außerdem ist die **Strokes** -Eigenschaft ein Wert, der wie ein beliebiger Wert den Gültigkeitsbereich verlässt, es sei denn, er wird einer Variablen zugewiesen.

Damit eine [**Striche**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) -Eigenschaft mit einem frei [**Hand Objekt synchronisiert**](inkdisp-class.md) wird, müssen Sie Sie in einem Ereignishandler für die Ereignisse " [**StrokesAdded**](inkstrokes-strokesadded.md) " und " [**StrokesRemoved**](inkstrokes-strokesremoved.md) " der [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung einschließen. Der Handler sollte eine neue Kopie der **Striche** -Eigenschaft abrufen, wenn beide Ereignisse ausgelöst werden. Achten Sie darauf, den Ereignishandler nicht zu einer **Striche** -Auflistung hinzuzufügen, die sich außerhalb des gültigen Bereichs befindet, bevor das Ereignis ausgelöst wird.

Beachten Sie, dass in diesem Beispiel `theAddedStrokesIDs` mit einer neuen Kopie der Striche-Eigenschaft im- `StrokesAdded_Event` Handler aktualisiert wird.


```C++
public void StrokesAdded_Event(object sender, StrokesEventArgs e)
{
    int [] theAddedStrokesIDs = e.StrokeIds;
    theListBox.Items.Clear();
    foreach (int i in theAddedStrokesIDs)
    {
        theListBox.Items.Add("Added Stroke ID: " + i.ToString());
    }
}
```



## <a name="packetdescription-property"></a>PacketDescription (Eigenschaft)

Die [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) -Eigenschaft des [**Ink**](inkdisp-class.md) -Objekts definiert den Satz der Informationen in jedem Paket, das die Anwendung von einem Tablet PC-Gerät erhält. Die Informationen enthalten in der Regel Koordinaten, aber Sie können viel ausführlichere Informationen enthalten (abhängig von den Funktionen des Tablet PC-Digitalisierungsprogramms), z. b. Stift Druck oder Stift Winkel. Durch Festlegen von Paketbeschreibungen für das [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt, bevor frei Hand Eingaben gesammelt werden (mithilfe der DesiredPacketDescription-Eigenschaft), haben Sie die vollständige Kontrolle über die Eigenschaften der Tablet PC-Geräte, die Sie erhalten möchten.

## <a name="extended-properties"></a>Erweiterte Eigenschaften

Erweiterte Eigenschaften bieten einen Mechanismus zum Anfügen von Anwendungs definierten Daten [**an frei**](inkdisp-class.md) Hand Eingaben und andere Objekte. Weitere Informationen zu erweiterten Eigenschaften finden Sie in der [**ExtendedProperties**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties) -Auflistung.

## <a name="ink-rendering"></a>Frei Hand Rendering

Das [**Rendererobjekt**](inkrenderer-class.md) ist für das [**Rendern**](inkdisp-class.md)von Freihand zuständig. Bei einem passenden Tablet-Kontext kann  das Rendererobjekt den Leerraum-Koordinaten Pixel zuordnen, Ansichts Transformationen anwenden und Freihand auf Bildschirmen und Druckern anzeigen. Die [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw) -und [**drawstroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke) -Methoden sind die primären Methoden zum Rendern von frei Hand Eingaben. Weitere Informationen zum Anzeigen von frei Hand Eingaben in einem Fenster finden Sie unter dem **Renderer** -Objekt.

## <a name="cusps"></a>Cusps

Ein Strich beginnt normalerweise, wenn der Stift auf die Zeichen Oberfläche herabgesetzt wird, und endet, wenn der Stift ausgelöst wird. Innerhalb eines Strichs werden die Spitzen, Winkel und radikalen Änderungen der Richtung als "cusps" bezeichnet. Die Endpunkte eines Strichs werden auch als "cusps" betrachtet. Der Großbuchstabe "L" hat beispielsweise drei cusps, eine in der Mitte und eine an jedem Ende.

Wenn ein Strich eingegeben wird, wird er normalerweise durch eine Bezier-Kurve (oder Polylinienkurve) gerglädert und gerendert. Bezier-Kurven können die cusps in kleine Schleifen umwandeln. Beispielsweise könnte die Spitze des kursiven Buchstabens "i" so geglättet werden, dass Sie dem geschweifsiven "e" ähnelt. Um dies zu verhindern, haben Microsoft-Renderer eine "Pre-Bezier"-Phase, in der die cusps anders behandelt werden.

Cusps können auch verwendet werden, um [**Strich**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) Objekte in Lösch Bare Einheiten zu unterteilen. Wenn Sie z. b. die vertikale Seite eines Großbuchstaben "L" auswählen, können Sie nur auf diese Seite löschen. Der Teil des Strichs, der gelöscht werden soll, ist der Teil zwischen zwei cusps.

 

 
