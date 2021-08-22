---
description: Stellt ein Objekt dar, das für Anmerkungsszenarien nützlich ist, in denen Es benutzern nicht darum geht, Freihanderkennung durchzuführen, sondern stattdessen an Größe, Form, Farbe und Position der Freihandfarbe interessiert ist.
ms.assetid: 61191ab3-075e-458b-9e0f-4bc255687b3c
title: InkOverlay-Klasse (Msinkaut.h)
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
ms.openlocfilehash: d1a818c1fef9006abad2dd31da5a41f43aeb3df9a9b75d348d8987938abfcea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967119"
---
# <a name="inkoverlay-class"></a>InkOverlay-Klasse

Stellt ein Objekt dar, das für Anmerkungsszenarien nützlich ist, in denen Es benutzern nicht darum geht, Freihanderkennung durchzuführen, sondern stattdessen an Größe, Form, Farbe und Position der Freihandfarbe interessiert ist.

Durch das Erstellen des **InkOverlay-Steuerelements** hinter einem transparenten Steuerelement (z. B. eine GroupBox mit festgelegter WS \_ EX \_ TRANSPARENT-Eigenschaft) wird verhindert, dass **InkOverlay InkOverlay** inkk erfasst.

**InkOverlay** verfügt über diese Typen von Membern:

-   [Ereignisse](#events)
-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Die **InkOverlay-Klasse** verfügt über diese Ereignisse.



| Ereignis                                                     | BESCHREIBUNG                                                                                                                                                                                                                                               |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | Tritt ein, wenn **inkOverlay** eine Cursorschaltfläche erkennt, die nicht angezeigt wird.<br/>                                                                                                                                                                           |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | Tritt ein, wenn **inkOverlay** eine cursor-Schaltfläche erkennt, die aktiv ist.<br/>                                                                                                                                                                             |
| [**Cursordown**](inkcollector-cursordown.md)             | Tritt ein, wenn die Cursorspitze mit der digitalisierenden Tablettoberfläche in Kontakt tritt.<br/>                                                                                                                                                                             |
| [**Cursorinrange**](inkcollector-cursorinrange.md)       | Tritt ein, wenn ein Cursor in den physischen Erkennungsbereich (Näherung) des Tabletkontexts eintritt.<br/>                                                                                                                                                    |
| [**Cursoroutofrange**](inkcollector-cursoroutofrange.md) | Tritt ein, wenn der Cursor den physischen Erkennungsbereich (Nähe) des Tabletkontexts verlässt.<br/>                                                                                                                                                  |
| [**Doubleclick**](inkcollector-doubleclick.md)           | Tritt ein, wenn auf das **InkOverlay-Objekt** doppelklickt wird.<br/>                                                                                                                                                                                       |
| [**Geste**](inkcollector-gesture.md)                   | Tritt ein, wenn eine anwendungsspezifische Geste erkannt wird.<br/>                                                                                                                                                                                     |
| [**Mousedown**](inkcollector-mousedown.md)               | Tritt ein, wenn sich der Mauszeiger über dem **InkOverlay-Objekt** befindet und eine Maustaste gedrückt wird.<br/>                                                                                                                                                 |
| [**Mousemove**](inkcollector-mousemove.md)               | Tritt ein, wenn der Mauszeiger über das **InkOverlay-Objekt** bewegt wird.<br/>                                                                                                                                                                         |
| [**Mouseup**](inkcollector-mouseup.md)                   | Tritt ein, wenn sich der Mauszeiger über dem **InkOverlay-Objekt** befindet und eine Maustaste losgelassen wird.<br/>                                                                                                                                                |
| [**Mousewheel**](inkcollector-mousewheel.md)             | Tritt ein, wenn das Mausrad bewegt wird, während das **InkOverlay-Objekt** den Fokus besitzt.<br/>                                                                                                                                                                   |
| [**Newinairpackets**](inkcollector-newinairpackets.md)   | Tritt ein, wenn ein In-Air-Paket angezeigt wird. Dies geschieht, wenn ein Benutzer einen Stift in der Nähe des Tabletts verschiebt und sich der Cursor im Fenster des **InkOverlay-Objekts** befindet oder der Benutzer eine Maus innerhalb des zugeordneten Fensters des **InkOverlay-Objektobjekts** bewegt.<br/> |
| [**Newpackets**](inkcollector-newpackets.md)             | Tritt ein, wenn das **InkOverlay-Objekt** Pakete empfängt.<br/>                                                                                                                                                                                        |
| [**Gemalt**](inkoverlay-painted.md)                     | Tritt ein, wenn das **InkOverlay-Objekt** die Neuzeichnung abgeschlossen hat.<br/>                                                                                                                                                                          |
| [**Malerei**](inkoverlay-painting.md)                   | Tritt ein, bevor sich das **InkOverlay-Objekt** neu gezeichnet hat.<br/>                                                                                                                                                                                        |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)   | Tritt ein, wenn sich die Auswahl von Freihand innerhalb des Steuerelements geändert hat, z. [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) B. durch Änderungen an der Benutzeroberfläche, Ausschneide- und Einfügeverfahren oder die Selection-Eigenschaft.<br/>                                       |
| [**Selectionchanging**](inkoverlay-selectionchanging.md) | Tritt ein, wenn sich die Auswahl von Freihand im Steuerelement ändert, z. B. durch Änderungen [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) an der Benutzeroberfläche, Ausschneide- und Einfügeprozessen oder die Selection-Eigenschaft.<br/>                                |
| [**Selectionmoved**](inkoverlay-selectionmoved.md)       | Tritt ein, wenn sich die Position der aktuellen Auswahl geändert hat, z. B. [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) durch Änderungen an der Benutzeroberfläche, Prozeduren zum Ausschneiden und Einfügen oder die Selection-Eigenschaft.<br/>                                         |
| [**Selectionmoving**](inkoverlay-selectionmoving.md)     | Tritt ein, wenn sich die Position der aktuellen Auswahl ändert, z. B. durch Änderungen [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) an der Benutzeroberfläche, Prozeduren zum Ausschneiden und Einfügen oder die Selection-Eigenschaft.<br/>                                  |
| [**Selectionresized**](inkoverlay-selectionresized.md)   | Tritt ein, wenn sich die Größe der aktuellen Auswahl geändert hat, z. B. [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) durch Änderungen an der Benutzeroberfläche, Prozeduren zum Ausschneiden und Einfügen oder die Selection-Eigenschaft.<br/>                                             |
| [**Selectionresizing**](inkoverlay-selectionresizing.md) | Tritt ein, wenn sich die Größe der aktuellen Auswahl ändert, z. B. durch Änderungen [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) an der Benutzeroberfläche, Prozeduren zum Ausschneiden und Einfügen oder die Selection-Eigenschaft.<br/>                                      |
| [**Takt**](inkcollector-stroke.md)                     | Tritt ein, wenn der Benutzer mit dem Zeichnen eines neuen Strichs auf einem Tablet fertig ist.<br/>                                                                                                                                                                              |
| [**Striche gelöscht**](inkoverlay-strokesdeleted.md)       | Tritt ein, nachdem Striche aus der [**Ink-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) gelöscht wurden.<br/>                                                                                                                                                      |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)     | Tritt ein, bevor Striche aus der [**Ink-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) gelöscht werden.<br/>                                                                                                                                                           |
| [**Systemgesture**](inkcollector-systemgesture.md)       | Tritt ein, wenn eine Systemgeste erkannt wird.<br/>                                                                                                                                                                                                    |
| [**Tabletadded**](inkcollector-tabletadded.md)           | Tritt ein, wenn dem System eine [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) hinzugefügt wird.<br/>                                                                                                                                                                        |
| [**Tabletremoved**](inkcollector-tabletremoved.md)       | Tritt ein, wenn ein [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) aus dem System entfernt wird.<br/>                                                                                                                                                                         |



 

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **InkOverlay-Klasse** definiert.



| Schnittstelle       | BESCHREIBUNG                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkOverlay** | Dieses Objekt implementiert die **IInkOverlay-COM-Schnittstelle.**<br/> |



 

### <a name="methods"></a>Methoden

Die **InkOverlay-Klasse** verfügt über diese Methoden.



| Methode                                                                              | BESCHREIBUNG                                                                                                                                                |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-draw)                                                     | Legt ein Rechteck fest, in dem die Farbe innerhalb des **InkOverlay-Objekts** neu gezeichnet werden soll.<br/>                                                                   |
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Gibt den aktuellen Zustand eines bestimmten **InkOverlay-Objektereignisses** zurück, d. h., ob das Ereignis überwacht oder verwendet wird.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Gibt zurück, ob das **InkOverlay-Objekt** an einer bestimmten Geste interessiert ist.<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Ruft das Fensterrechteck in Pixel ab, in dem Ink gezeichnet wird.<br/>                                                                           |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-hittestselection)                             | Bestimmt, welcher Teil der Auswahl während eines Treffertests erreicht wurde.<br/>                                                                             |
| [**Setalltabletsmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | In diesem Modus kann das **InkOverlay-Objekt InkOverlay** von jedem Tablet sammeln, das an den Tablet PC angefügt ist.<br/>                                            |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Legt fest, ob ein bestimmtes Ereignis überwacht oder verwendet werden soll.<br/>                                                                                   |
| [**Setgesturestatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Legt das Interesse des **InkOverlay-Objekts** in einer bekannten Geste fest.<br/>                                                                              |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | In diesem Modus kann das **InkOverlay-Objekt Nur InkOverlay** von nur einem Tablet erfassen. Inkoverlay von anderen Tablets wird vom **InkOverlay-Objekt** ignoriert.<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Legt das Fensterrechteck in Pixel fest, das zum Zuordnen von gezeichneter Ink zum Fenster verwendet werden soll.<br/>                                                                    |



 

### <a name="properties"></a>Eigenschaften

Die **InkOverlay-Klasse** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                       | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode)<br/>                                         | Lesen/Schreiben<br/> | Ruft den Wert ab, der angibt, ob das **InkOverlay-Objekt** hinter oder vor dem bekannten Fenster angefügt wird, oder legt diesen fest.<br/>                                                       |
| [**Autoredraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                                       | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob **das InkOverlay die InkOverlay-Eigenschaft** neu zeichnet, wenn das Fenster ungültig wird, oder legt diesen fest.<br/>                                                                   |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                                 | Schreibgeschützt<br/>  | Ruft einen Wert ab, der angibt, ob InkOverlay derzeit für ein **InkOverlay-Objekt gezeichnet** wird.<br/>                                                                                     |
| [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                               | Lesen/Schreiben<br/> | Ruft den Auflistungsmodus ab, der bestimmt, ob Ink-, Gesten- oder beides beim Schreiben durch den Benutzer erkannt wird, oder legt diesen fest.<br/>                                                                |
| [**Cursor**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                             | Schreibgeschützt<br/>  | Ruft die [**Cursors-Auflistung**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) ab, die für die Verwendung im Freiraumbereich verfügbar ist.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/>           | Lesen/Schreiben<br/> | Ruft das Standardobjekt [**InkDrawingAttributes**](inkdrawingattributes-class.md) ab, das die Zeichnungsattribute angibt, die beim Zeichnen und Anzeigen von Ink verwendet werden, oder legt dieses fest.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/>           | Lesen/Schreiben<br/> | Ruft das Interesse an Aspekten des Pakets ab, das dem im InkOverlay-Objekt gezeichneten **InkOverlay-Objekt zugeordnet** ist, oder legt dieses fest.<br/>                                                                            |
| [**Dynamicrendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                             | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob ink beim Gezeichneten gerendert wird, oder legt diesen fest.<br/>                                                                                                       |
| [**Editingmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)<br/>                                       | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob **sich InkOverlay im InkOverlay-Modus,** im Löschmodus oder im Auswahl-/Bearbeitungsmodus befindet, oder legt diesen fest.<br/>                                                          |
| [**Aktiviert**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                             | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob das **InkOverlay-Objekt** Stifteingaben sammelt, oder legt diesen fest.<br/>                                                                                         |
| [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)<br/>                                         | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob die Ink-Datei per Strich oder Punkt gelöscht wird, oder legt diesen fest.<br/>                                                                                                  |
| [**EraserWidth**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_eraserwidth)<br/>                                       | Lesen/Schreiben<br/> | Ruft einen Wert ab, der die Breite der Radiererstiftspitze angibt, oder legt diesen fest.<br/>                                                                                                              |
| [**Behandeln**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                                 | Lesen/Schreiben<br/> | Ruft das Handle des Fensters ab, an das das **InkOverlay-Objekt** angefügt ist, oder legt dieses fest.<br/>                                                                                             |
| [**Freihand**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_ink)<br/>                                                       | Lesen/Schreiben<br/> | Ruft das [**InkDisp-Objekt ab,**](inkdisp-class.md) das dem **InkOverlay-Objekt** zugeordnet ist, oder legt dieses fest.<br/>                                                                       |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                             | Lesen/Schreiben<br/> | Ruft die Ränder entlang der X-Achse in Pixel ab oder legt sie fest.<br/>                                                                                                                             |
| [**MarginY**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                             | Lesen/Schreiben<br/> | Ruft die Ränder entlang der y-Achse in Pixel ab oder legt sie fest.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                                         | Lesen/Schreiben<br/> | Ruft das aktuelle benutzerdefinierte Maussymbol ab oder legt es fest.<br/>                                                                                                                                       |
| [**Mousepointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                                   | Lesen/Schreiben<br/> | Ruft einen Wert ab, der den Typ des Mauszeigers angibt, der angezeigt wird, wenn sich die Maus über einem bestimmten Teil des Objekts befindet, oder legt diesen fest.<br/>                                                |
| [**Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                           | Lesen/Schreiben<br/> | Ruft das [**InkRenderer-Objekt ab,**](inkrenderer-class.md) das zum Zeichnen von Ink verwendet wird, oder legt dieses fest.<br/>                                                                                        |
| [**Auswahl**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                           | Lesen/Schreiben<br/> | Ruft die [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ab, die derzeit im **InkOverlay-Steuerelement** ausgewählt ist, oder legt sie fest.<br/>                                                 |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>               | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob Ink als nur eine Farbe gerendert wird, wenn sich das System im hoher Kontrast befindet, oder legt diesen fest.<br/>                                                           |
| [**SupportHighContrastSelectionUI**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_supporthighcontrastselectionui)<br/> | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob die auswahlbenutzeroberfläche mit hohem Kontrast gezeichnet wird, wenn sich das System im hoher Kontrast befindet, oder legt ihn fest.<br/>                                                  |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                                  | Schreibgeschützt<br/>  | Ruft das Tablettgerät ab, das das **InkOverlay-Objekt** derzeit zum Erfassen von Eingaben verwendet.<br/>                                                                                        |



 

## <a name="mfc-implementation-notes"></a>Hinweise zur MFC-Implementierung

Wenn Sie das InkOverlay-Objekt an ein CView-Objekt angefügt haben, geben Sie das InkOverlay-Objekt als Antwort auf die WM DESTROY-Nachricht frei, wie \_ im folgenden Beispiel gezeigt:


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="remarks"></a>Hinweise

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance-Methode**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ instanziiert werden.

Das **InkOverlay-Objekt** eignet sich gut für die Notiznahme und einfaches Beschriften. Die primäre beabsichtigte Verwendung dieses Objekts ist die Anzeige von Ink als Ink.

Im Allgemeinen ist die Laufzeitbenutzeroberfläche für dieses Objekt ein transparentes Fenster mit nicht transparenter Ink-Oberfläche.

Die [**Ereignisse MouseDown,**](inkcollector-mousedown.md) [**MouseMove,**](inkcollector-mousemove.md) [**MouseUp**](inkcollector-mouseup.md)und [**MouseWheel**](inkcollector-mousewheel.md) geben x-Koordinaten und y-Koordinaten in Pixel und nicht die HIMETRIC-Einheiten zurück, die dem Freiraum zugeordnet sind. Dies liegt daran, dass diese Ereignisse die Mausereignisse von Nicht-Stiftanwendungen ersetzen und diese Anwendungen nur Pixel verstehen.

> [!Caution]  
> Wenn Sie die [**AttachMode-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode) des **InkOverlay-Objekts** auf InFront festlegen, erstellen Sie das **InkOverlay-Objekt** in dem Thread, in dem das Formular ausgeführt wird. Ihre Anwendung reagiert möglicherweise nicht mehr, wenn das **InkOverlay-Objekt** in einem anderen Thread erstellt und die **AttachMode-Eigenschaft** auf InFront festgelegt ist.

 

> [!Note]  
> Das **InkOverlay-Objekt** kann nicht sicher in einem Nicht-UI-Thread freigegeben werden.

 

Um die Leistung Ihrer Anwendung zu verbessern, veräußern Sie das **InkOverlay-Objekt,** wenn es nicht mehr benötigt wird.

Wenn Sie das InkOverlay-Objekt an ein CView-Objekt angefügt haben, geben Sie das InkOverlay-Objekt als Antwort auf die WM DESTROY-Nachricht frei, wie \_ im folgenden Beispiel gezeigt:


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkCollector-Klasse**](inkcollector-class.md)
</dt> <dt>

[Referenz zum InkPicture-Steuerelement](inkpicture-control-reference.md)
</dt> <dt>

[Referenz zum InkEdit-Steuerelement](inkedit-control-reference.md)
</dt> </dl>

 

