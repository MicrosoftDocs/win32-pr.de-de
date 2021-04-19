---
description: Stellt ein Objekt dar, das für Anmerkung-Szenarios nützlich ist, bei denen sich Benutzer nicht mit der Erkennung von frei Hand Eingaben befassen, sondern an der Größe, Form, Farbe und Position der Handschrift interessiert sind.
ms.assetid: 61191ab3-075e-458b-9e0f-4bc255687b3c
title: InkOverlay-Klasse (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkOverlay
- InkOverlay.IInkOverlay
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: bfcc6cc4daedf0ed1bbc43e2ccc78317f9d7e17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348688"
---
# <a name="inkoverlay-class"></a>InkOverlay-Klasse

Stellt ein Objekt dar, das für Anmerkung-Szenarios nützlich ist, bei denen sich Benutzer nicht mit der Erkennung von frei Hand Eingaben befassen, sondern an der Größe, Form, Farbe und Position der Handschrift interessiert sind.

Wenn Sie das **InkOverlay** -Steuerelement hinter einem transparenten Steuerelement erstellen (z. b. ein GroupBox-Element mit dem \_ transparenten Eigenschaften Satz "WS Ex" \_ ), wird verhindert, dass **InkOverlay** frei

**InkOverlay** verfügt über diese Typen von Membern:

-   [Ereignisse](#events)
-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Die **InkOverlay** -Klasse enthält diese Ereignisse.



| Ereignis                                                     | BESCHREIBUNG                                                                                                                                                                                                                                               |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Currsorbuttondown**](inkcollector-cursorbuttondown.md) | Tritt auf, wenn **InkOverlay** eine Cursor Schaltfläche erkennt, die nicht angezeigt wird.<br/>                                                                                                                                                                           |
| [**Currsorbuttonup**](inkcollector-cursorbuttonup.md)     | Tritt auf, wenn **InkOverlay** eine Cursor Schaltfläche erkennt, die aktiv ist.<br/>                                                                                                                                                                             |
| [**Cursor**](inkcollector-cursordown.md)             | Tritt auf, wenn die Cursor-QuickInfo die digitalisierende Tablet-Oberfläche kontaktiert<br/>                                                                                                                                                                             |
| [**Cursor Bereich**](inkcollector-cursorinrange.md)       | Tritt auf, wenn ein Cursor in den physischen Erkennungsbereich (Near) des Tablet-Kontexts eintritt.<br/>                                                                                                                                                    |
| [**Cursor-Ausgabe**](inkcollector-cursoroutofrange.md) | Tritt auf, wenn der Cursor den physischen Erkennungsbereich (Nähe) des Tablet-Kontexts verlässt.<br/>                                                                                                                                                  |
| [**DoubleClick**](inkcollector-doubleclick.md)           | Tritt auf, wenn auf das **InkOverlay** -Objekt Doppel geklickt wird.<br/>                                                                                                                                                                                       |
| [**Geste**](inkcollector-gesture.md)                   | Tritt auf, wenn eine anwendungsspezifische Geste erkannt wird.<br/>                                                                                                                                                                                     |
| [**MouseDown**](inkcollector-mousedown.md)               | Tritt ein, wenn sich der Mauszeiger über dem **InkOverlay** -Objekt befindet und eine Maustaste gedrückt wird.<br/>                                                                                                                                                 |
| [**MouseMove**](inkcollector-mousemove.md)               | Tritt auf, wenn der Mauszeiger über das **InkOverlay** -Objekt bewegt wird.<br/>                                                                                                                                                                         |
| [**MouseUp**](inkcollector-mouseup.md)                   | Tritt auf, wenn sich der Mauszeiger über dem **InkOverlay** -Objekt befindet und eine Maustaste losgelassen wird.<br/>                                                                                                                                                |
| [**Mausrad**](inkcollector-mousewheel.md)             | Tritt auf, wenn das Mausrad bewegt wird, während das **InkOverlay** -Objekt den Fokus besitzt.<br/>                                                                                                                                                                   |
| [**"Netwinairpakete"**](inkcollector-newinairpackets.md)   | Tritt auf, wenn ein in-Air-Paket angezeigt wird. Dies geschieht, wenn ein Benutzer einen Stift in der Nähe des Tablets bewegt und sich der Cursor im Fenster des **InkOverlay** -Objekts befindet, oder wenn der Benutzer im zugeordneten Fenster des **InkOverlay** -Objekt Objekts eine Maus bewegt.<br/> |
| [**Neupakete**](inkcollector-newpackets.md)             | Tritt auf, wenn das **InkOverlay** -objektpakete empfängt.<br/>                                                                                                                                                                                        |
| [**Be**](inkoverlay-painted.md)                     | Tritt auf, wenn das **InkOverlay** -Objekt das erneute Zeichnen von sich selbst abgeschlossen hat.<br/>                                                                                                                                                                          |
| [**Be**](inkoverlay-painting.md)                   | Tritt ein, bevor das **InkOverlay** -Objekt sich selbst neu zeichnet.<br/>                                                                                                                                                                                        |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)   | Tritt auf, wenn sich die Auswahl von frei Hand Eingaben innerhalb des-Steuer Elements geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, Ausschneide-und Einfüge Prozeduren oder die [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) -Eigenschaft<br/>                                       |
| [**Ereignis**](inkoverlay-selectionchanging.md) | Tritt auf, wenn die Auswahl von frei Hand Eingaben innerhalb des-Steuer Elements geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und Einfüge Prozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) -Eigenschaft.<br/>                                |
| [**Selectionverschoben**](inkoverlay-selectionmoved.md)       | Tritt auf, wenn sich die Position der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und einfügeprozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) -Eigenschaft.<br/>                                         |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)     | Tritt ein, wenn die Position der aktuellen Auswahl geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) -Eigenschaft.<br/>                                  |
| [**SelectionResized**](inkoverlay-selectionresized.md)   | Tritt auf, wenn sich die Größe der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der [**Auswahl**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) Eigenschaft.<br/>                                             |
| [**Selectionresisierend**](inkoverlay-selectionresizing.md) | Tritt ein, wenn die Größe der aktuellen Auswahl geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) -Eigenschaft.<br/>                                      |
| [**Stellung**](inkcollector-stroke.md)                     | Tritt ein, wenn der Benutzer das Zeichnen eines neuen Strichs auf einem Tablet abschließt.<br/>                                                                                                                                                                              |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)       | Tritt auf, nachdem Striche aus der [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) -Eigenschaft gelöscht wurden.<br/>                                                                                                                                                      |
| [**Strokeslöschung**](inkoverlay-strokesdeleting.md)     | Tritt auf, bevor Striche aus der [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) -Eigenschaft gelöscht werden.<br/>                                                                                                                                                           |
| [**System Bewegung**](inkcollector-systemgesture.md)       | Tritt auf, wenn eine System Bewegung erkannt wird.<br/>                                                                                                                                                                                                    |
| [**TabletAdded**](inkcollector-tabletadded.md)           | Tritt auf, wenn ein [**iinktablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) zum System hinzugefügt wird.<br/>                                                                                                                                                                        |
| [**Tabletreverschohe**](inkcollector-tabletremoved.md)       | Tritt auf, wenn ein [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) aus dem System entfernt wird.<br/>                                                                                                                                                                         |



 

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **InkOverlay** -Klasse definiert.



| Schnittstelle       | BESCHREIBUNG                                                          |
|:----------------|:---------------------------------------------------------------------|
| **Iinkoverlay** | Dieses Objekt implementiert die **iinkoverlay** -com-Schnittstelle.<br/> |



 

### <a name="methods"></a>Methoden

Die **InkOverlay** -Klasse verfügt über diese Methoden.



| Methode                                                                              | BESCHREIBUNG                                                                                                                                                |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-draw)                                                     | Legt ein Rechteck fest, in dem die frei Hand Eingaben innerhalb des **InkOverlay** -Objekts neu gezeichnet werden.<br/>                                                                   |
| [**Geteventinterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Gibt den aktuellen Zustand eines bestimmten **InkOverlay** -Objekt Ereignisses zurück, d. h. ob das Ereignis überwacht oder verwendet wird.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Gibt zurück, ob das **InkOverlay** -Objekt an einer bestimmten Geste interessiert ist.<br/>                                                                |
| [**Getwindowinputrechteck**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Ruft das Fenster Rechteck in Pixel ab, in dem frei Hand Eingaben gezeichnet werden.<br/>                                                                           |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-hittestselection)                             | Bestimmt, welcher Teil der Auswahl während eines Treffer Tests getroffen wurde.<br/>                                                                             |
| [**Setalltabletmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Dieser Modus ermöglicht es dem **InkOverlay** -Objekt, frei Hand Eingaben von einem Tablet zu erfassen, das an den Tablet PC angeschlossen ist.<br/>                                            |
| [**"Einstellungs Element"**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Legt fest, ob ein bestimmtes Ereignis überwacht oder verwendet werden soll.<br/>                                                                                   |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Legt das Interesse des **InkOverlay** -Objekts in einer bekannten Geste fest.<br/>                                                                              |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Dieser Modus ermöglicht es dem **InkOverlay** -Objekt, frei Hand Eingaben von nur einem Tablet zu sammeln. Frei Hand Eingaben von anderen Tablets werden vom **InkOverlay** -Objekt ignoriert.<br/> |
| [**Setwindowinputrechteck**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Legt das Fenster Rechteck in Pixel fest, das zum Zuordnen von gezeichneter frei Hand Eingaben zum Fenster verwendet werden soll.<br/>                                                                    |



 

### <a name="properties"></a>Eigenschaften

Die **InkOverlay** -Klasse verfügt über diese Eigenschaften.



| Eigenschaft                                                                                       | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode)<br/>                                         | Lesen/Schreiben<br/> | Ruft den-Wert ab, der angibt, ob das **InkOverlay** -Objekt hinter oder vor dem bekannten Fenster angefügt wird, oder legt ihn fest.<br/>                                                       |
| [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                                       | Lesen/Schreiben<br/> | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die Eingabeaufforderung von **InkOverlay** neu gezeichnet wird, wenn das Fenster ungültig wird.<br/>                                                                   |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                                 | Schreibgeschützt<br/>  | Ruft einen Wert ab, der angibt, ob Freihand in einem **InkOverlay** -Objekt gerade gezeichnet wird.<br/>                                                                                     |
| [**CollectionMode '**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                               | Lesen/Schreiben<br/> | Ruft den Auflistungs Modus ab, der bestimmt, ob Freihand, Gesten oder beides beim Schreiben durch den Benutzer erkannt werden, oder legt ihn fest<br/>                                                                |
| [**Cursor**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                             | Schreibgeschützt<br/>  | Ruft die [**Cursorauflistung**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) ab, die für die Verwendung im Erfassungsbereich verfügbar ist.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/>           | Lesen/Schreiben<br/> | Ruft das standardmäßige [**inkdrawingattributes**](inkdrawingattributes-class.md) -Objekt ab, das die Zeichnungs Attribute angibt, die beim Zeichnen und Anzeigen von Freihand verwendet werden, oder legt dieses fest.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/>           | Lesen/Schreiben<br/> | Ruft das Interesse an Aspekten des Pakets ab, das frei Hand Eingaben im **InkOverlay** -Objekt zugeordnet ist, oder legt dieses fest.<br/>                                                                            |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                             | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob frei Hand Eingaben beim Zeichnen gerendert werden.<br/>                                                                                                       |
| [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)<br/>                                       | Lesen/Schreiben<br/> | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob **InkOverlay** sich im frei Hand Modus, Lösch Modus oder Auswahl-/Bearbeitungs Modus befindet.<br/>                                                          |
| [**Aktiviert**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                             | Lesen/Schreiben<br/> | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob das **InkOverlay** -Objekt Stift Eingaben sammelt.<br/>                                                                                         |
| [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)<br/>                                         | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob frei Hand Eingaben durch Strich oder Punkt gelöscht werden, oder legt ihn fest.<br/>                                                                                                  |
| [**EraserWidth**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_eraserwidth)<br/>                                       | Lesen/Schreiben<br/> | Ruft einen Wert ab, der die Breite des radiererstifts angibt, oder legt diesen fest.<br/>                                                                                                              |
| [**Handle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                                 | Lesen/Schreiben<br/> | Ruft das Handle des Fensters ab, an das das **InkOverlay** -Objekt angefügt ist, oder legt dieses fest.<br/>                                                                                             |
| [**Freihand**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_ink)<br/>                                                       | Lesen/Schreiben<br/> | Ruft das [**InkDisp**](inkdisp-class.md) -Objekt ab, das dem **InkOverlay** -Objekt zugeordnet ist, oder legt dieses fest.<br/>                                                                       |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                             | Lesen/Schreiben<br/> | Ruft die Ränder entlang der x-Achse in Pixel ab oder legt diese fest.<br/>                                                                                                                             |
| [**MarginY**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                             | Lesen/Schreiben<br/> | Ruft die Ränder entlang der y-Achse in Pixel ab oder legt diese fest.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                                         | Lesen/Schreiben<br/> | Ruft das aktuelle benutzerdefinierte Maus Symbol ab oder legt es fest.<br/>                                                                                                                                       |
| [**Mouum Zeiger**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                                   | Lesen/Schreiben<br/> | Ruft einen Wert ab oder legt einen Wert fest, der den Typ des Mauszeigers angibt, der angezeigt wird, wenn sich die Maus über einem bestimmten Teil des Objekts befindet.<br/>                                                |
| [**Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                           | Lesen/Schreiben<br/> | Ruft das [**inkrenderer**](inkrenderer-class.md) -Objekt ab, das zum Zeichnen von Freihand verwendet wird, oder legt dieses fest<br/>                                                                                        |
| [**Auswahl**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                           | Lesen/Schreiben<br/> | Ruft die [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ab, die derzeit im **InkOverlay** -Steuerelement ausgewählt ist, oder legt Sie fest.<br/>                                                 |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>               | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob frei Hand Eingaben als nur eine Farbe gerendert werden, wenn sich das System im hoher Kontrast Modus befindet<br/>                                                           |
| [**SupportHighContrastSelectionUI**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_supporthighcontrastselectionui)<br/> | Lesen/Schreiben<br/> | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die gesamte Auswahl Benutzeroberfläche im hohen Kontrast gezeichnet wird, wenn sich das System im hoher Kontrast Modus befindet<br/>                                                  |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                                  | Schreibgeschützt<br/>  | Ruft das Tablet-Gerät ab, das das **InkOverlay** -Objekt zurzeit zum Erfassen von Eingaben verwendet.<br/>                                                                                        |



 

## <a name="mfc-implementation-notes"></a>Hinweise zur MFC-Implementierung

Wenn Sie das InkOverlay-Objekt an ein CView-Objekt angefügt haben, geben Sie das InkOverlay-Objekt als Antwort auf die WM-Lösch Nachricht frei, \_ wie im folgenden Beispiel gezeigt:


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="remarks"></a>Bemerkungen

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.

Das **InkOverlay** -Objekt eignet sich gut für die Aufnahme und das einfache schreiben. Der primäre Verwendungszweck dieses Objekts besteht darin, frei Hand Eingaben als frei Hand Eingaben anzuzeigen.

Im Allgemeinen ist die Lauf Zeit Benutzeroberfläche für dieses Objekt ein transparentes Fenster mit undurchsichtigem frei Hand Eingaben.

Die Ereignisse [**mousdown**](inkcollector-mousedown.md), [**mousmove**](inkcollector-mousemove.md), [**mousup**](inkcollector-mouseup.md)und [**mouswheel**](inkcollector-mousewheel.md) geben x-Koordinaten und y-Koordinaten in Pixel zurück, nicht die dem Leerraum zugeordneten HIMETRIC-Einheiten. Dies liegt daran, dass diese Ereignisse die Mausereignisse von schreibgeschützten Anwendungen ersetzen und diese Anwendungen nur Pixel verstehen.

> [!Caution]  
> Wenn Sie die [**AttachMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode) -Eigenschaft des **InkOverlay** -Objekts auf Infront festlegen, erstellen Sie das **InkOverlay** -Objekt in dem Thread, in dem das Formular ausgeführt wird. Die Anwendung reagiert möglicherweise nicht mehr, wenn das **InkOverlay** -Objekt in einem anderen Thread erstellt wird und seine **AttachMode** -Eigenschaft auf Infront festgelegt ist.

 

> [!Note]  
> Das **InkOverlay** -Objekt kann nicht sicher in einem nicht-UI-Thread freigegeben werden.

 

Um die Leistung Ihrer Anwendung zu verbessern, löschen Sie Ihr **InkOverlay** -Objekt, wenn es nicht mehr benötigt wird.

Wenn Sie das InkOverlay-Objekt an ein CView-Objekt angefügt haben, geben Sie das InkOverlay-Objekt als Antwort auf die WM-Lösch Nachricht frei, \_ wie im folgenden Beispiel gezeigt:


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkCollector-Klasse**](inkcollector-class.md)
</dt> <dt>

[InkPicture-Steuerelement Verweis](inkpicture-control-reference.md)
</dt> <dt>

[Referenz zum InkEdit-Steuerelement](inkedit-control-reference.md)
</dt> </dl>

 

