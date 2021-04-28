---
description: 'InkDisp-Klasse: Stellt die gesammelten Freihandstriche innerhalb eines Freihandraums dar.'
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: InkDisp-Klasse (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDisp
- InkDisp.IInkDisp
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: e4214d6b03e5823bd5012017e418066763c8132c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109988"
---
# <a name="inkdisp-class"></a>InkDisp-Klasse

Stellt die gesammelten Freihandstriche innerhalb eines Freihandraums dar.

**InkDisp** verfügt über folgende Typen von Membern:

-   [Ereignisse](#events)
-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Die **InkDisp-Klasse** verfügt über diese Ereignisse.



| Ereignis                                    | BESCHREIBUNG                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [**InkAdded**](inkdisp-inkadded.md)     | Tritt ein, wenn dem **InkDisp-Objekt** ein Strich hinzugefügt wird.<br/>     |
| [**InkDeleted**](inkdisp-inkdeleted.md) | Tritt ein, wenn ein Strich aus dem **InkDisp-Objekt** gelöscht wird.<br/> |



 

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **InkDisp-Klasse** definiert.



| Schnittstelle    | BESCHREIBUNG                                                       |
|:-------------|:------------------------------------------------------------------|
| **IInkDisp** | Dieses Objekt implementiert die **IInkDisp-COM-Schnittstelle.**<br/> |



 

### <a name="methods"></a>Methoden

Die **InkDisp-Klasse** verfügt über diese Methoden.



| Methode                                                                   | BESCHREIBUNG                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStrokesAtRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | Fügt eine Strichauflistung am angegebenen Rechteck in das **InkDisp-Objekt** ein.<br/>                                                                                                       |
| [**Canpaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | Gibt an, ob das [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) in ein **InkDisp-Objekt** konvertiert werden kann.<br/>                                                                                       |
| [**Clip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | Entfernt Teile eines Strichs oder eine Auflistung von Strichen, die sich außerhalb eines Rechtecks befinden.<br/>                                                                                                       |
| [**Clipboardcopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | Kopiert die [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) in die Zwischenablage.<br/>                                                                                                           |
| [**ClipboardCopyWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | Kopiert die [**IInkStrokeDisp-Objekte,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) die im bekannten Rechteck enthalten sind, in die Zwischenablage.<br/>                                                               |
| [**ZwischenablagePaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | Kopiert das [**IDataObject aus**](/windows/desktop/api/objidl/nn-objidl-idataobject) der Zwischenablage in das **InkDisp-Objekt.**<br/>                                                                                               |
| [**Klon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | Erstellt ein doppeltes **InkDisp-Objekt.**<br/>                                                                                                                                                   |
| [**Ink.createstroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | Erstellt einen Strich aus Punkten oder Paketdaten.<br/>                                                                                                                                              |
| [**CreateStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | Erstellt eine [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) für dieses **InkDisp-Objekt.**<br/>                                                                                                |
| [**DeleteStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | Löscht einen Strich aus dem **InkDisp-Objekt.**<br/>                                                                                                                                             |
| [**DeleteStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | Löscht Striche aus dem **InkDisp-Objekt.**<br/>                                                                                                                                              |
| [**ExtractStrokes-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | Extrahiert Striche aus dem **InkDisp-Objekt** und gibt ein neues **InkDisp-Objekt** zurück, das die extrahierten Striche enthält.<br/>                                                                       |
| [**ExtractWithRectangle-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | Striche aus einem vorhandenen **InkDisp-Klassenobjekt** werden schneidet oder kopiert und in ein neues Objekt der **InkDisp-Klasse** kopiert, indem das bekannte Rechteck verwendet wird, um zu bestimmen, welche Striche extrahiert werden sollen.<br/> |
| [**Getboundingbox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | Ruft das umgebende Feld aller Striche im **InkDisp-Objekt** ab.<br/>                                                                                                               |
| [**HitTestCircle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | Ruft die [**InkStrokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ab, die sich entweder vollständig innerhalb eines bekannten Kreises befindet oder von diesem schneidet.<br/>                                                  |
| [**HitTestWithLasso**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | Ruft die Striche innerhalb eines Polylinienauswahlbereichs ab.<br/>                                                                                                                                   |
| [**HitTestWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | Ruft die Striche ab, die in einem angegebenen Rechteck enthalten sind.<br/>                                                                                                                    |
| [**Laden**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | Füllt ein neues **InkDisp-Objekt** mit bekannten Binärdaten auf.<br/>                                                                                                                                |
| [**Ink.nearestpoint**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | Ruft das [**IInkStrokeDisp-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) innerhalb des **InkDisp-Objekts** ab, das einem bekannten Punkt am nächsten ist, und stellt optional zusätzliche Informationen bereit.<br/>                       |
| [**Speichern**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | Konvertiert die Ink in ein angegebenes Format und gibt die Binärdaten zurück.<br/>                                                                                                                       |



 

### <a name="properties"></a>Eigenschaften

Die **InkDisp-Klasse** verfügt über diese Eigenschaften.



| Eigenschaft                                                                           | Zugriffstyp           | BESCHREIBUNG                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Customstrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | Schreibgeschützt<br/>  | Ruft die [**IInkCustomStrokes-Auflistung**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) ab, die mit der Freihandeingabe beibehalten werden soll.<br/>                             |
| [**Schmutzig**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | Lesen/Schreiben<br/> | Ruft den Wert ab, der angibt, ob ein **InkDisp-Objekt** seit dem letzten Speichern der Ink geändert wurde, oder legt diesen fest.<br/> |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Schreibgeschützt<br/>  | Ruft die Auflistung anwendungsdefinierter Daten ab.<br/>                                                                             |
| [**Striche**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | Schreibgeschützt<br/>  | Ruft die [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ab, die im **InkDisp-Objekt** enthalten ist.<br/>                             |



 

## <a name="remarks"></a>Bemerkungen

Dieses Objekt kann instanziiert werden, indem die [**CoCreateInstance-Methode**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ aufgerufen wird.

> [!Note]  
> Die erste Instanziierung dieses Objekts bewirkt, dass auch GDI+ instanziiert wird. Ein Nebeneffekt ist, dass GDI+ immer wieder instanziiert wird, wenn Sie ein einzelnes Ink-Objekt in einer Schleife verwenden und es innerhalb der Schleife erstellen und zerstören. Dies kann zu einer Leistungsbeeinträchtigung in Ihrer Anwendung führen. Um dies zu verhindern, behalten Sie jederzeit eine einzelne Instanz eines Ink-Objekts bei, während Ihre Anwendung Ink verwendet.

 

Ein **InkDisp-Objekt** ist ein Container mit Strichdaten (Punktdaten). Die Strichdaten oder die vom Stift gesammelten Punkte werden in ein **InkDisp-Objekt** gespeichert. Die [**Strokes-Eigenschaft**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) enthält die Daten für alle Striche innerhalb des **InkDisp-Objekts.**

Das [**InkCollector-Objekt,**](inkcollector-class.md) [**das InkOverlay-Objekt**](inkoverlay-class.md) und das [InkPicture-Steuerelement](inkpicture-control-reference.md) sammeln Punkte vom Eingabegerät und speichern sie in einem **InkDisp-Objekt.** Diese Objekte fungieren im Wesentlichen als Quelle, die Ink an ein oder viele verschiedene **InkDisp-Objekte** verteilt, die als Container fungieren, die die verteilte Ink-Datei enthalten.

Der Freiraum ist ein virtueller Koordinatenraum, dem die Koordinaten des Tablet-Kontexts zugeordnet werden. Dieses Leerzeichen ist auf ein HIMETRIC-Koordinatensystem festgelegt. In Freiraumkoordinaten entspricht eine Bewegung von 0 zu 1 1 HIMETRIC-Einheit. Diese Zuordnung erleichtert das Zuordnen mehrerer **InkDisp-Objekte.**

Das [**InkRenderer-Objekt**](inkrenderer-class.md) verwaltet die Zuordnungen zwischen Ink und dem Anzeigefenster.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[InkStrokes-Sammlung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**IInkTablet-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

