---
description: Stellt das -Objekt dar, das zum Erfassen von Freiform von verfügbaren Tablettgeräten verwendet wird.
ms.assetid: 189f430e-9d00-4e29-bb8c-8ac195896793
title: InkCollector-Klasse (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkCollector
- InkCollector.IInkCollector
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 02ecf89a1ce8db89105ac9fa0243552efaf5218da98f6d3b0fdfbd58f874d449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718176"
---
# <a name="inkcollector-class"></a>InkCollector-Klasse

Stellt das -Objekt dar, das zum Erfassen von Freiform von verfügbaren Tablettgeräten verwendet wird.

Durch das **Erstellen des InkCollector-Steuerelements** hinter einem transparenten Steuerelement (z. B. einer GroupBox mit dem **WS EX \_ TRANSPARENT-Eigenschaftensatz) \_** wird verhindert, dass **InkCollector InkCollector-Daten** sammelt.

**InkCollector verfügt** über diese Membertypen:

-   [Ereignisse](#events)
-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Die **InkCollector-Klasse** verfügt über diese Ereignisse.



| Ereignis                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | Tritt ein, wenn **der InkCollector** eine Cursorschaltfläche erkennt, die nicht mehr angezeigt wird.<br/>                                                                                                                                                                             |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | Tritt ein, wenn **der InkCollector** eine Cursorschaltfläche erkennt, die geöffnet ist.<br/>                                                                                                                                                                               |
| [**Cursordown**](inkcollector-cursordown.md)             | Tritt ein, wenn die Cursorspitze die digitalisierende Tablet-Oberfläche kontaktiert.<br/>                                                                                                                                                                                 |
| [**Cursorinrange**](inkcollector-cursorinrange.md)       | Tritt ein, wenn ein Cursor in den physischen Erkennungsbereich (Näherung) des Tablet-Kontexts eintritt.<br/>                                                                                                                                                        |
| [**Cursoroutofrange**](inkcollector-cursoroutofrange.md) | Tritt ein, wenn der Cursor den physischen Erkennungsbereich (Näherung) des Tablet-Kontexts verlässt.<br/>                                                                                                                                                      |
| [**Doubleclick**](inkcollector-doubleclick.md)           | Tritt ein, wenn **auf das InkCollector-Objekt** doppelklickt.<br/>                                                                                                                                                                                         |
| [**Geste**](inkcollector-gesture.md)                   | Tritt auf, wenn eine anwendungsspezifische Geste erkannt wird.<br/>                                                                                                                                                                                         |
| [**Mousedown**](inkcollector-mousedown.md)               | Tritt ein, wenn sich der Mauszeiger über dem **InkCollector-Objekt** befindet und eine Maustaste gedrückt wird.<br/>                                                                                                                                                   |
| [**Mousemove**](inkcollector-mousemove.md)               | Tritt ein, wenn der Mauszeiger über das **InkCollector-Objekt bewegt** wird.<br/>                                                                                                                                                                           |
| [**Mouseup**](inkcollector-mouseup.md)                   | Tritt ein, wenn sich der Mauszeiger über dem **InkCollector-Objekt** befindet und eine Maustaste losgelassen wird.<br/>                                                                                                                                                  |
| [**Mousewheel**](inkcollector-mousewheel.md)             | Tritt ein, wenn sich das Mausrad bewegt, während das **InkCollector-Objekt** den Fokus besitzt.<br/>                                                                                                                                                                     |
| [**Newinairpackets**](inkcollector-newinairpackets.md)   | Tritt auf, wenn ein Paket in der Luft angezeigt wird. Dies geschieht, wenn ein Benutzer einen Stift in die Nähe des Tablets bewegt und sich der Cursor im Fenster des **InkCollector-Objekts** befindet oder der Benutzer eine Maus im zugeordneten Fenster des **InkCollector-Objektobjekts** bewegt.<br/> |
| [**Newpackets**](inkcollector-newpackets.md)             | Tritt ein, wenn das **InkCollector-Objekt** Pakete empfängt.<br/>                                                                                                                                                                                          |
| [**Takt**](inkcollector-stroke.md)                     | Tritt ein, wenn der Benutzer mit dem Zeichnen eines neuen Strichs auf einem Tablet fertig ist.<br/>                                                                                                                                                                                  |
| [**Systemgesture**](inkcollector-systemgesture.md)       | Tritt ein, wenn eine Systemgeste erkannt wird.<br/>                                                                                                                                                                                                        |
| [**Tabletadded**](inkcollector-tabletadded.md)           | Tritt ein, wenn [**dem System**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) ein Tablet hinzugefügt wird.<br/>                                                                                                                                                                                 |
| [**Tabletremoved**](inkcollector-tabletremoved.md)       | Tritt ein, wenn [**ein Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) aus dem System entfernt wird.<br/>                                                                                                                                                                             |



 

### <a name="interfaces"></a>Schnittstellen

Die **InkCollector-Klasse** definiert diese Schnittstellen.



| Schnittstelle         | BESCHREIBUNG                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **IInkCollector** | Dieses Objekt implementiert die **IInkCollector-COM-Schnittstelle.**<br/> |



 

### <a name="methods"></a>Methoden

Die **InkCollector-Klasse** verfügt über diese Methoden.



| Methode                                                                              | BESCHREIBUNG                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Retrieves the current state of a particular **InkCollector** object event, that is, whether the event is being listened for or used.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Ruft ab, ob **das InkCollector-Objekt** an einer bestimmten Geste interessiert ist.<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Ruft das Fensterrechteck in Pixel ab, in dem Ink gezeichnet wird.<br/>                                                                               |
| [**Setalltabletsmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Dieser Modus ermöglicht dem **InkCollector-Objekt** das Sammeln von Ink-Daten von jedem Tablet, das an den Tablet-PC angeschlossen ist.<br/>                                              |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Ändert einen Wert, der angibt, ob ein bestimmtes Ereignis lauschen oder verwendet werden soll.<br/>                                                            |
| [**Setgesturestatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Ändert das Interesse des **InkCollector-Objekts** in einer bekannten Geste.<br/>                                                                            |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Dieser Modus ermöglicht es dem **InkCollector-Objekt,** Ink von nur einem Tablet zu erfassen. Ink von anderen Tablets wird vom **InkCollector-Objekt** ignoriert.<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Ändert das Fensterrechteck in Pixel, das zum Zuordnen gezeichneter Ink-Daten zum Fenster verwendet werden soll.<br/>                                                                    |



 

### <a name="properties"></a>Eigenschaften

Die **InkCollector-Klasse** verfügt über diese Eigenschaften.



| Eigenschaft                                                                             | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autoredraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                             | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob der **InkCollector die InkCollector-Eigenschaft** neu zeichnet, wenn das Fenster ungültig wird, oder legt diesen fest.<br/>                                                                 |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                       | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob in einem **InkCollector-Objekt derzeit eine InkCollector-Eigenschaft gezeichnet** wird.<br/>                                                                                   |
| [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                     | Schreibgeschützt<br/> | Ruft den Auflistungsmodus ab, der bestimmt, ob Ink-, Gesten- oder beides beim Schreiben durch den Benutzer erkannt wird, oder legt diesen fest.<br/>                                                                |
| [**Cursor**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                   | Schreibgeschützt<br/> | Ruft die [**Cursors-Auflistung**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) ab, die für die Verwendung im Freiraumbereich verfügbar ist.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/> | Schreibgeschützt<br/> | Ruft das Standardobjekt [**InkDrawingAttributes**](inkdrawingattributes-class.md) ab, das die Zeichnungsattribute angibt, die beim Zeichnen und Anzeigen von Ink verwendet werden, oder legt dieses fest.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/> | Schreibgeschützt<br/> | Ruft das Interesse an Aspekten des Pakets ab, das dem im **InkCollector-Objekt gezeichneten InkCollector zugeordnet** ist, oder legt dieses fest.<br/>                                                                          |
| [**Dynamicrendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                   | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob ink beim Gezeichneten gerendert wird, oder legt diesen fest.<br/>                                                                                                       |
| [**Aktiviert**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                   | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob das **InkCollector-Objekt** Stifteingaben sammelt, oder legt diesen fest.<br/>                                                                                       |
| [**Behandeln**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                       | Schreibgeschützt<br/> | Ruft das Handle des Fensters ab, an das das **InkCollector-Objekt** angefügt ist, oder legt dieses fest.<br/>                                                                                           |
| [**Freihand**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)<br/>                                           | Schreibgeschützt<br/> | Ruft das [**InkDisp-Objekt ab,**](inkdisp-class.md) das dem **InkCollector-Objekt** zugeordnet ist, oder legt dieses fest.<br/>                                                                     |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                   | Schreibgeschützt<br/> | Ruft die Ränder entlang der X-Achse in Pixel ab oder legt sie fest.<br/>                                                                                                                             |
| [**MarginY**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                   | Schreibgeschützt<br/> | Ruft die Ränder entlang der y-Achse in Pixel ab oder legt sie fest.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                               | Schreibgeschützt<br/> | Ruft das aktuelle benutzerdefinierte Maussymbol ab oder legt es fest.<br/>                                                                                                                                       |
| [**Mousepointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                         | Schreibgeschützt<br/> | Ruft einen Wert ab, der den Typ des Mauszeigers angibt, der angezeigt wird, wenn sich die Maus über einem bestimmten Teil des Objekts befindet, oder legt diesen fest.<br/>                                                |
| [**Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                 | Schreibgeschützt<br/> | Ruft das [**InkRenderer-Objekt ab,**](inkrenderer-class.md) das zum Zeichnen von Ink verwendet wird, oder legt dieses fest.<br/>                                                                                        |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>     | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob Ink als nur eine Farbe gerendert wird, wenn sich das System im hoher Kontrast befindet, oder legt diesen fest.<br/>                                                           |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                        | Schreibgeschützt<br/> | Ruft das Tablettgerät ab, das das **InkCollector-Objekt** derzeit zum Erfassen von Eingaben verwendet.<br/>                                                                                      |



 

## <a name="remarks"></a>Hinweise

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance-Methode**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ instanziiert werden.

Das **InkCollector-Objekt** erfasst nur Ink- und Gesten, die in das spezifische Fenster eingegeben werden, dem es zugeordnet ist. Der einzige Zweck von **InkCollector** besteht in der Erfassung von Ink-Daten von der Hardware (z. B. über ein [**IInkCursor-**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) und [**IInkTablet-Objekt)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) und deren Bereitstellung an eine Anwendung. Sie fungiert im Wesentlichen als Quelle, die Dieb in ein oder viele verschiedene [**InkDisp-Objekte**](inkdisp-class.md) verteilt, die als Container fungieren, der die verteilte Ink-Datei enthält.

Um einen **InkCollector** zu verwenden, erstellen Sie ihn, teilen ihm mit, in welchem Fenster gezeichnete Ink-Daten gesammelt und aktiviert werden. Nachdem sie aktiviert wurde, kann sie so festgelegt werden, dass sie nur in einem von drei Modi erfasst wird (der Modus wird in der [**InkCollectionMode-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) angegeben):

-   InkOnly, in dem ein [**IInkStrokeDisp-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) erstellt wird.
-   GestureOnly, in dem ein [**IInkGesture-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) erstellt wird.
-   InkAndGesture, bei dem ein Strich, eine Geste oder möglicherweise beides erstellt wird, je nachdem, wie die Anwendung Ereignisse behandelt.

Dies bedeutet, dass der **InkCollector** für jede Bewegung eines Cursors innerhalb des Bereichs eines Tablets immer entweder einen Strich oder eine Geste erfasst und manchmal beides. Die Gestenunterstützung ist mithilfe der Gestenerkennung von Microsoft integriert.

Ein **InkCollector verarbeitet** alle Tableteingaben. Ink kann von allen angefügten Tablets (einschließlich der Maus) gleichzeitig gesammelt werden. Änderungen an [**den IInkCursor-**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) und [**IInkCursorButton-Objekten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) können dazu führen, dass **das InkCollector-Objekt** ein Ereignis ausspricht.

Ein **InkCollector verwaltet** auch die Liste der Cursor, die während seiner Existenz auftreten. Wenn der **InkCollector** einen neuen Cursor findet, wird das [**CursorInRange-Ereignis**](inkcollector-cursorinrange.md) mit dem *parameter newCursor* auf **VARIANT TRUE \_ festgelegt.** Anwendungen verwenden **den InkCollector,** um neue Cursor zu verwalten.

Mehr als ein **InkCollector** kann einem bestimmten Fensterhandle zugeordnet werden, auch wenn sich deren Sammlungsbereiche im Konstruktor oder mit der [**SetWindowInputRectangle-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle) überlappen. Dieses Szenario funktioniert jedoch nur, wenn jeder **InkCollector** [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) aufruft und ein eindeutiges Tablet verwendet. Dieses Verhalten erleichtert das Speichern von Ink in einem separaten Objekt für jedes Tablet.

Ein Fehler tritt auf, wenn das Fenstereingaberechteck eines aktivierten **InkCollectors** (festgelegt mit der [**Enabled-Eigenschaft)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled) das Fenstereingaberechteck eines anderen aktivierten **InkCollector überlappt.**

> [!Note]  
> Überlappungen können ohne Fehler auftreten, solange nur eines der Eingaberechtecke zu einem bekannten Zeitpunkt aktiviert ist.

 

Die [**Ereignisse MouseDown,**](inkcollector-mousedown.md) [**MouseMove,**](inkcollector-mousemove.md) [**MouseUp**](inkcollector-mouseup.md)und [**MouseWheel**](inkcollector-mousewheel.md) geben x- und y-Koordinaten in Pixel und nicht die HIMETRIC-Einheiten zurück, die dem Freiraum zugeordnet sind. Dies liegt daran, dass diese Ereignisse die Mausereignisse von Nicht-Stiftanwendungen ersetzen und diese Anwendungen nur Pixel verstehen.

> [!Note]  
> Das **InkCollector-Objekt** kann nicht sicher in einem Nicht-UI-Thread freigegeben werden.

 

Um die Leistung Ihrer Anwendung zu verbessern, veralten Sie Das **InkCollector-Objekt,** wenn es nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[InkEdit-Steuerelementreferenz](inkedit-control-reference.md)
</dt> <dt>

[**InkDisp-Klasse**](inkdisp-class.md)
</dt> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[InkPicture-Steuerelementreferenz](inkpicture-control-reference.md)
</dt> </dl>

 

