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
ms.openlocfilehash: 928bda8af246b41bab2c285a5292155917ba8903c6dd71c20177dbf906c64924
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939160"
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
| [**ZwischenablagePaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | Kopiert das [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) aus der Zwischenablage in das **InkDisp-Objekt.**<br/>                                                                                               |
| [**Klon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | Erstellt ein doppeltes **InkDisp-Objekt.**<br/>                                                                                                                                                   |
| [**Ink.createstroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | Erstellt einen Strich aus Punkten oder Paketdaten.<br/>                                                                                                                                              |
| [**CreateStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | Erstellt eine [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) für dieses **InkDisp-Objekt.**<br/>                                                                                                |
| [**DeleteStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | Löscht einen Strich aus dem **InkDisp-Objekt.**<br/>                                                                                                                                             |
| [**DeleteStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | Löscht Striche aus dem **InkDisp-Objekt.**<br/>                                                                                                                                              |
| [**ExtractStrokes-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | Extrahiert Striche aus dem **InkDisp-Objekt** und gibt ein neues **InkDisp-Objekt** zurück, das die extrahierten Striche enthält.<br/>                                                                       |
| [**ExtractWithRectangle-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | Schneidet oder kopiert Striche aus einem vorhandenen **InkDisp-Klassenobjekt** und setzt sie in ein neues **InkDisp-Klassenobjekt** ein, indem das bekannte Rechteck verwendet wird, um zu bestimmen, welche Striche extrahiert werden sollen.<br/> |
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
| [**Extendedproperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Schreibgeschützt<br/>  | Ruft die Auflistung anwendungsdefinierter Daten ab.<br/>                                                                             |
| [**Striche**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | Schreibgeschützt<br/>  | Ruft die [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ab, die im **InkDisp-Objekt** enthalten ist.<br/>                             |



 

## <a name="remarks"></a>Hinweise

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance-Methode**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ instanziiert werden.

> [!Note]  
> Die erste Instanziierung dieses Objekts bewirkt auch, dass GDI+ instanziiert wird. Ein Nebeneffekt ist: Wenn Sie ein einzelnes Ink-Objekt in einer Schleife verwenden und es innerhalb der Schleife erstellen und zerstören, führen Sie dazu, dass GDI+ immer wieder instanziiert werden. Dies kann zu einer Leistungsbeeinträchtigung in Ihrer Anwendung führen. Um dies zu verhindern, behalten Sie eine einzelne Instanz eines Ink-Objekts jederzeit bei, während Ihre Anwendung Ink verwendet.

 

Ein **InkDisp-Objekt** ist ein Container mit Strichdaten (Punktdaten). Die Strichdaten oder die vom Stift gesammelten Punkte werden in ein **InkDisp-Objekt** gesetzt. Die [**Strokes-Eigenschaft**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) enthält die Daten für alle Striche im **InkDisp-Objekt.**

Das [**InkCollector-Objekt,**](inkcollector-class.md) [**das InkOverlay-Objekt**](inkoverlay-class.md) und das [InkPicture-Steuerelement](inkpicture-control-reference.md) sammeln Punkte vom Eingabegerät und legen sie in ein **InkDisp-Objekt** ab. Diese Objekte fungieren im Wesentlichen als Quelle, die Ink in ein oder mehrere verschiedene **InkDisp-Objekte** verteilt, die als Container fungieren, die die verteilte Ink enthalten.

Der Freihandraum ist ein virtueller Koordinatenbereich, dem die Koordinaten des Tabletkontexts zugeordnet werden. Dieser Raum ist auf ein HIMETRIC-Koordinatensystem festgelegt. In Freihandraumkoordinaten entspricht eine Verschiebung von 0 zu 1 einer HIMETRIC-Einheit. Diese Zuordnung erleichtert das Verknüpfen mehrerer **InkDisp-Objekte.**

Das [**InkRenderer-Objekt**](inkrenderer-class.md) verwaltet die Zuordnungen zwischen Ink und dem Anzeigefenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[InkStrokes-Sammlung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**IInkTablet-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

