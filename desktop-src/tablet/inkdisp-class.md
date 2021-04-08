---
description: Stellt die gesammelten Hand Striche innerhalb eines frei Hand Raums dar.
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: InkDisp-Klasse (msink AUT. h)
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
ms.openlocfilehash: 429cbf85bdc92753cda1e58a0e89086b4b5b8b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750209"
---
# <a name="inkdisp-class"></a>InkDisp-Klasse

Stellt die gesammelten Hand Striche innerhalb eines frei Hand Raums dar.

**InkDisp** verfügt über folgende Typen von Membern:

-   [Ereignisse](#events)
-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Die **InkDisp** -Klasse enthält diese Ereignisse.



| Ereignis                                    | BESCHREIBUNG                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [**InkAdded**](inkdisp-inkadded.md)     | Tritt auf, wenn dem **InkDisp** -Objekt ein Strich hinzugefügt wird.<br/>     |
| [**InkDeleted**](inkdisp-inkdeleted.md) | Tritt auf, wenn ein Strich aus dem **InkDisp** -Objekt gelöscht wird.<br/> |



 

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **InkDisp** -Klasse definiert.



| Schnittstelle    | BESCHREIBUNG                                                       |
|:-------------|:------------------------------------------------------------------|
| **IInkDisp** | Dieses Objekt implementiert die **IInkDisp** -com-Schnittstelle.<br/> |



 

### <a name="methods"></a>Methoden

Die **InkDisp** -Klasse verfügt über diese Methoden.



| Methode                                                                   | BESCHREIBUNG                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addstrokesatrechteck**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | Fügt eine Strich Auflistung im angegebenen Rechteck in das **InkDisp** -Objekt ein.<br/>                                                                                                       |
| [**CanPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | Gibt an, ob das [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) -Objekt in ein **InkDisp** -Objekt konvertiert werden kann.<br/>                                                                                       |
| [**Techno**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | Entfernt Teile eines Strichs oder eine Auflistung von Strichen außerhalb eines Rechtecks.<br/>                                                                                                       |
| [**ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | Kopiert die [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung in die Zwischenablage.<br/>                                                                                                           |
| [**Clipboardcopywithrechteck**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | Kopiert die [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte, die im bekannten Rechteck enthalten sind, in die Zwischenablage.<br/>                                                               |
| [**ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | Kopiert das [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) aus der Zwischenablage in das **InkDisp** -Objekt.<br/>                                                                                               |
| [**Klon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | Erstellt ein doppeltes **InkDisp** -Objekt.<br/>                                                                                                                                                   |
| [**"Kreatestroke"**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | Erstellt einen Strich aus Punkten oder Paketdaten.<br/>                                                                                                                                              |
| [**"Kreatestrokes"**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | Erstellt eine [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung für dieses **InkDisp** -Objekt.<br/>                                                                                                |
| [**DeleteStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | Löscht einen Strich aus dem **InkDisp** -Objekt.<br/>                                                                                                                                             |
| [**DeleteStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | Löscht Striche aus dem **InkDisp** -Objekt.<br/>                                                                                                                                              |
| [**ExtractStrokes-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | Extrahiert Striche aus dem **InkDisp** -Objekt und gibt ein neues **InkDisp** -Objekt zurück, das die extrahierten Striche enthält.<br/>                                                                       |
| [**Extractwithrechteck-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | Schneidet Striche von einem vorhandenen InkDisp- **Klassen** Objekt ab oder kopiert sie in ein neues **InkDisp-Klassen** Objekt, indem das bekannte Rechteck verwendet wird, um zu bestimmen, welche Striche extrahiert werden sollen.<br/> |
| [**GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | Ruft das umgebende Feld aller Striche im **InkDisp** -Objekt ab.<br/>                                                                                                               |
| [**Hittestcircle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | Ruft die [**inkstrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ab, die sich entweder vollständig innerhalb oder durch einen Bekanntenkreis überschneiden.<br/>                                                  |
| [**Hittestwithlasso**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | Ruft die Striche innerhalb eines polylinienauswahlbereichs ab.<br/>                                                                                                                                   |
| [**Hittestwithrechteck**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | Ruft die Striche ab, die innerhalb eines angegebenen Rechtecks enthalten sind.<br/>                                                                                                                    |
| [**Laden**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | Füllt ein neues **InkDisp** -Objekt mit bekannten Binärdaten auf.<br/>                                                                                                                                |
| [**NearestPoint**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | Ruft das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt im **InkDisp** -Objekt ab, das sich am nächsten an einem bekannten Punkt befindet, wobei optional zusätzliche Informationen bereitgestellt werden.<br/>                       |
| [**Speichern**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | Konvertiert die frei Hand Eingabe in ein angegebenes Format und gibt die Binärdaten zurück.<br/>                                                                                                                       |



 

### <a name="properties"></a>Eigenschaften

Die **InkDisp** -Klasse verfügt über diese Eigenschaften.



| Eigenschaft                                                                           | Zugriffstyp           | BESCHREIBUNG                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | Schreibgeschützt<br/>  | Ruft die [**iinkcustomstrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) -Auflistung ab, die mit der frei Hand Eingabe beibehalten werden soll.<br/>                             |
| [**TZI**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | Lesen/Schreiben<br/> | Ruft den Wert ab, der angibt, ob ein **InkDisp** -Objekt seit dem letzten Speichern der frei Hand Eingabe geändert wurde, oder legt ihn fest.<br/> |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Schreibgeschützt<br/>  | Ruft die Auflistung von Anwendungs definierten Daten ab.<br/>                                                                             |
| [**Striche**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | Schreibgeschützt<br/>  | Ruft die [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ab, die im **InkDisp** -Objekt enthalten ist.<br/>                             |



 

## <a name="remarks"></a>Bemerkungen

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.

> [!Note]  
> Die erste Instanziierung dieses Objekts bewirkt, dass GDI+ ebenfalls instanziiert wird. Ein Nebeneffekt ist, dass bei Verwendung eines einzelnen frei Hand Objekts in einer Schleife, das in der Schleife erstellt und zerstört wird, GDI+ immer wieder instanziiert wird. Dies kann zu Leistungseinbußen in Ihrer Anwendung führen. Um dies zu verhindern, behalten Sie immer eine einzelne Instanz eines Ink-Objekts bei, während Ihre Anwendung frei Hand Eingaben verwendet.

 

Ein **InkDisp** -Objekt ist ein Container von Stroke-Daten (Point). Die Strich Daten oder die vom Stift erfassten Punkte werden in ein **InkDisp** -Objekt eingefügt. Die [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) -Eigenschaft enthält die Daten für alle Striche innerhalb des **InkDisp** -Objekts.

Das [**InkCollector**](inkcollector-class.md) -Objekt, das [**InkOverlay**](inkoverlay-class.md) -Objekt und das [InkPicture](inkpicture-control-reference.md) -Steuerelement sammelt Punkte vom Eingabegerät und setzt Sie in ein **InkDisp** -Objekt. Diese Objekte fungieren im Wesentlichen als Quelle, die frei Hand Eingaben an ein oder mehrere verschiedene **InkDisp** -Objekte verteilt, die als Container fungieren, die den verteilten frei Hand Eingaben enthalten.

Der frei Hand Raum ist ein virtueller Koordinaten Bereich, dem die Koordinaten des Tablet-Kontexts zugeordnet werden. Dieser Raum ist auf ein HIMETRIC-Koordinatensystem korrigiert. In frei Hand Raumkoordinaten ist ein Wechsel zwischen 0 und 1 ein Wert von 1 himetrik. Mit dieser Zuordnung können mehrere **InkDisp** -Objekte problemlos miteinander verknüpft werden.

Das [**inkrenderer**](inkrenderer-class.md) -Objekt verwaltet die Zuordnungen zwischen frei Hand Eingaben und dem Anzeige Fenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Inkstrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Iinktablet-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

