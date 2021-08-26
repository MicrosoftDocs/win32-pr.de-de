---
description: Nachdem die Ink gesammelt wurde, können Anwendungen diese Daten verwalten, bearbeiten und/oder auf andere Medien übertragen.
ms.assetid: 5a8c370e-79cb-47f0-a7b3-a631874ad757
title: Ink-Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f62f566e48859ba2aea7013783b3ccc8c825b8559fdec34e24438d68b6ee65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939410"
---
# <a name="ink-data"></a>Ink-Daten

Nachdem die Ink gesammelt wurde, können Anwendungen diese Daten verwalten, bearbeiten und/oder auf andere Medien übertragen. Die Aktionen zum Auswählen, Kopieren, Verschieben, Speichern, Anzeigen und Ändern der [**Ink**](inkdisp-class.md) erfolgen für das Ink-Objekt und seine enthaltenen Member, z. B. die [**Strokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) und [**die Stroke-Objekte.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

> [!Note]  
> Mit Real-Time Stift können Anwendungen Daten in einem eigenen Format verwalten (z. B. Striche speichern).

 

## <a name="ink-strokes-and-packets"></a>Ink, Strokes und Packets

Ein [**Ink-Objekt**](inkdisp-class.md) ist der grundlegende Datentyp, der die vom [**InkCollector-Objekt gesammelten**](inkcollector-class.md) Eingaben verwaltet, bearbeitet und speichert. Ein **Ink-Objekt** enthält mindestens ein [**Stroke-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) sowie allgemeine Methoden und Eigenschaften zum Verwalten und Bearbeiten dieser Striche. Ein Strich wird als Satz von Daten definiert, die in einer einzelnen Stift-Nach-Unten-, Stift- und Stift-Nach-Oben-Sequenz erfasst werden. Die Strichdaten enthalten eine Auflistung von Paketen. Ein Paket ist der Satz von Daten, die das Tabletgerät an jedem Beispielpunkt sendet. Diese Daten enthalten Informationen wie Koordinaten, Stiftdruck, Stiftwinkel und alles andere, was die Hardware übertragen kann. Die [**PacketDescription-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) des **Stroke-Objekts** beschreibt die Pakete, die ein [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) generiert.

## <a name="strokes"></a>Striche

Sie können eine Momentaufnahme der Striche in einem [**Ink-Objekt**](inkdisp-class.md) abrufen, indem Sie die [**Strokes-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) des **Ink-Objekts** verwenden. Die **Strokes-Eigenschaft** ist eine Auflistung von Verweisen auf die Striche im **Ink-Objekt** zum Zeitpunkt des Lesens der **Strokes-Eigenschaft.** Wenn Striche anschließend dem **Ink-Objekt** hinzugefügt oder daraus gelöscht werden, wird eine zuvor [**abgerufene Strokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) nicht aktualisiert. Darüber hinaus ist die **Strokes-Eigenschaft** ein -Wert und geht wie jeder wert aus dem Gültigkeitsbereich, es sei denn, sie wird einer Variablen zugewiesen.

Um eine [**Strokes-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) mit einem [**Ink-Objekt**](inkdisp-class.md) synchronisiert zu halten, umschließen Sie sie in einem Ereignishandler für die [**StrokesAdded-**](inkstrokes-strokesadded.md) und [**StrokesRemoved-Ereignisse**](inkstrokes-strokesremoved.md) in der [**Strokes-Auflistung.**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) Der Handler sollte eine neue Kopie der **Strokes-Eigenschaft** abrufen, wenn eines der Ereignisse ausgelöst wird. Achten Sie darauf, den Ereignishandler nicht einer **Strokes-Auflistung** hinzuzufügen, die sich außerhalb des Gültigkeitsbereichs befindet, bevor das Ereignis ausgelöst wird.

Beachten Sie, dass in diesem Beispiel `theAddedStrokesIDs` mit einer neuen Kopie der Strokes-Eigenschaft im Handler aktualisiert `StrokesAdded_Event` wird.


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



## <a name="packetdescription-property"></a>PacketDescription-Eigenschaft

Die [**PacketDescription-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) des [**Ink-Objekts**](inkdisp-class.md) definiert den Satz von Informationen in jedem Paket, das die Anwendung von einem Tablet PC-Gerät erhält. Die Informationen enthalten in der Regel Koordinaten, können aber viel ausführlichere Informationen enthalten (je nachdem, welche Funktionen der Tablet PC-Digitizer bietet), z. B. Stiftdruck oder Stiftwinkel. Durch Festlegen von Paketbeschreibungen für das [**InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) vor dem Sammeln von Inks (mithilfe der DesiredPacketDescription-Eigenschaft) haben Sie die vollständige Kontrolle darüber, welche Der Tablet PC-Geräteeigenschaften Sie empfangen möchten.

## <a name="extended-properties"></a>Erweiterte Eigenschaften

Erweiterte Eigenschaften stellen einen Mechanismus zum Anfügen von anwendungsdefinierte Daten an [**Ink**](inkdisp-class.md) und andere Objekte bereit. Weitere Informationen zu erweiterten Eigenschaften finden Sie in der [**ExtendedProperties-Auflistung.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties)

## <a name="ink-rendering"></a>Ink Rendering

Das [**Rendererobjekt**](inkrenderer-class.md) ist für das Rendern von [**Ink**](inkdisp-class.md)zuständig. Bei einem geeigneten Tablet-Kontext kann das **Rendererobjekt** Freihandraumkoordinaten Pixeln zuordnen, Ansichtstransformationen anwenden und Freihand auf Bildschirmen und Druckern anzeigen. Die [**Draw-**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw) und [**DrawStroke-Methoden**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke) sind die primären Methoden zum Rendern von Ink. Weitere Informationen zum Anzeigen von Ink in einem Fenster finden Sie im **Rendererobjekt.**

## <a name="cusps"></a>Spitzen

Ein Strich beginnt normalerweise, wenn der Stift auf die Zeichenoberfläche herabgesetzt wird, und endet, wenn der Stift ausgelöst wird. Innerhalb eines Strichs werden die Spitzen, Winkel und inneren Richtungsänderungen als Cusps bezeichnet. Die Endpunkte eines Strichs werden auch als Cusps betrachtet. Beispielsweise hat der Großbuchstabe "L" drei Cusps, einen in der Mitte und einen an jedem Ende.

Wenn ein Strich eingegeben wird, wird er normalerweise geglättet und mithilfe einer Bézierkurve (oder Polylinienkurve) gerendert. Bézierkurven können Cusps in kleine Schleifen umwandeln. Beispielsweise kann die Spitze des geschweiften Buchstabens "i" geglättet werden, um dem geschweiften "e" zu ähneln. Um dies zu verhindern, verfügen Microsoft-Renderer über eine "Pre-Bezier"-Phase, die die Cusps unterschiedlich behandelt.

Cusps können auch verwendet werden, um [**Strichobjekte**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) in löschbare Einheiten zu unterteilen. Wenn Sie z. B. die vertikale Seite eines Großbuchstabens "L" auswählen, kann dies darauf hindeuten, dass nur diese Seite entfernt wird. Der Teil des Strichs, der gelöscht werden soll, ist der Teil zwischen zwei Cusps.

 

 
