---
description: Stellt das Objekt dar, das zum Erfassen von frei Hand Eingaben von verfügbaren Tablet Geräten verwendet wird.
ms.assetid: 189f430e-9d00-4e29-bb8c-8ac195896793
title: InkCollector-Klasse (msink AUT. h)
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
ms.openlocfilehash: 17eff388a759b9b0873929447e4c8fe008e2fba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525280"
---
# <a name="inkcollector-class"></a>InkCollector-Klasse

Stellt das Objekt dar, das zum Erfassen von frei Hand Eingaben von verfügbaren Tablet Geräten verwendet wird.

Wenn Sie das **InkCollector** -Steuerelement hinter einem transparenten Steuerelement erstellen (z. b. ein GroupBox-Element mit dem transparenten Eigenschaften Satz " **WS \_ Ex \_** "), wird die **Erfassung von** Freihand

**InkCollector** verfügt über folgende Typen von Membern:

-   [Ereignisse](#events)
-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Die **InkCollector** -Klasse enthält diese Ereignisse.



| Ereignis                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Currsorbuttondown**](inkcollector-cursorbuttondown.md) | Tritt auf, wenn der **InkCollector** eine nicht herunter gebrannte Cursor Schaltfläche erkennt.<br/>                                                                                                                                                                             |
| [**Currsorbuttonup**](inkcollector-cursorbuttonup.md)     | Tritt auf, wenn der **InkCollector** eine Cursor Schaltfläche erkennt, die aktiv ist.<br/>                                                                                                                                                                               |
| [**Cursor**](inkcollector-cursordown.md)             | Tritt auf, wenn die Cursor-QuickInfo die digitalisierende Tablet-Oberfläche kontaktiert<br/>                                                                                                                                                                                 |
| [**Cursor Bereich**](inkcollector-cursorinrange.md)       | Tritt auf, wenn ein Cursor in den physischen Erkennungsbereich (Near) des Tablet-Kontexts eintritt.<br/>                                                                                                                                                        |
| [**Cursor-Ausgabe**](inkcollector-cursoroutofrange.md) | Tritt auf, wenn der Cursor den physischen Erkennungsbereich (Nähe) des Tablet-Kontexts verlässt.<br/>                                                                                                                                                      |
| [**DoubleClick**](inkcollector-doubleclick.md)           | Tritt auf, wenn auf das **InkCollector** -Objekt Doppel geklickt wird.<br/>                                                                                                                                                                                         |
| [**Geste**](inkcollector-gesture.md)                   | Tritt auf, wenn eine anwendungsspezifische Geste erkannt wird.<br/>                                                                                                                                                                                         |
| [**MouseDown**](inkcollector-mousedown.md)               | Tritt ein, wenn sich der Mauszeiger über dem **InkCollector** -Objekt befindet und eine Maustaste gedrückt wird.<br/>                                                                                                                                                   |
| [**MouseMove**](inkcollector-mousemove.md)               | Tritt ein, wenn der Mauszeiger über das **InkCollector** -Objekt bewegt wird.<br/>                                                                                                                                                                           |
| [**MouseUp**](inkcollector-mouseup.md)                   | Tritt ein, wenn sich der Mauszeiger über dem **InkCollector** -Objekt befindet und eine Maustaste losgelassen wird.<br/>                                                                                                                                                  |
| [**Mausrad**](inkcollector-mousewheel.md)             | Tritt auf, wenn das Mausrad bewegt wird, während das **InkCollector** -Objekt den Fokus besitzt.<br/>                                                                                                                                                                     |
| [**"Netwinairpakete"**](inkcollector-newinairpackets.md)   | Tritt auf, wenn ein in-Air-Paket angezeigt wird. Dies geschieht, wenn ein Benutzer einen Stift in der Nähe des Tablets bewegt und sich der Cursor im Fenster des **InkCollector** -Objekts befindet oder wenn der Benutzer eine Maus innerhalb des zugehörigen Fensters des **InkCollector** -Objekt Objekts bewegt.<br/> |
| [**Neupakete**](inkcollector-newpackets.md)             | Tritt auf, wenn das **InkCollector** -objektpakete empfängt.<br/>                                                                                                                                                                                          |
| [**Stellung**](inkcollector-stroke.md)                     | Tritt ein, wenn der Benutzer das Zeichnen eines neuen Strichs auf einem Tablet abschließt.<br/>                                                                                                                                                                                  |
| [**System Bewegung**](inkcollector-systemgesture.md)       | Tritt auf, wenn eine System Bewegung erkannt wird.<br/>                                                                                                                                                                                                        |
| [**TabletAdded**](inkcollector-tabletadded.md)           | Tritt auf, wenn dem System ein [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) hinzugefügt wird.<br/>                                                                                                                                                                                 |
| [**Tabletreverschohe**](inkcollector-tabletremoved.md)       | Tritt auf, wenn ein [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) aus dem System entfernt wird.<br/>                                                                                                                                                                             |



 

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **InkCollector** -Klasse definiert.



| Schnittstelle         | BESCHREIBUNG                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **Iinkcollector** | Dieses Objekt implementiert die **iinkcollector** -com-Schnittstelle.<br/> |



 

### <a name="methods"></a>Methoden

Die **InkCollector** -Klasse verfügt über diese Methoden.



| Methode                                                                              | BESCHREIBUNG                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Geteventinterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Ruft den aktuellen Zustand eines bestimmten **InkCollector** -Objekt Ereignisses ab, d. h., ob das Ereignis überwacht oder verwendet wird.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Ruft ab, ob das **InkCollector** -Objekt an einer bestimmten Geste interessiert ist.<br/>                                                                |
| [**Getwindowinputrechteck**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Ruft das Fenster Rechteck in Pixel ab, in dem frei Hand Eingaben gezeichnet werden.<br/>                                                                               |
| [**Setalltabletmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Dieser Modus ermöglicht es dem **InkCollector** -Objekt, frei Hand Eingaben von jedem Tablet zu erfassen, das an den Tablet PC angeschlossen ist.<br/>                                              |
| [**"Einstellungs Element"**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Ändert einen Wert, der angibt, ob ein bestimmtes Ereignis überwacht oder verwendet werden soll.<br/>                                                            |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Ändert das Interesse des **InkCollector** -Objekts in einer bekannten Geste.<br/>                                                                            |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Dieser Modus ermöglicht es dem **InkCollector** -Objekt, frei Hand Eingaben von nur einem Tablet zu sammeln. Frei Hand Eingaben von anderen Tablets werden vom **InkCollector** -Objekt ignoriert.<br/> |
| [**Setwindowinputrechteck**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Ändert das Fenster Rechteck in Pixel, das zum Zuordnen von gezeichneter frei Hand Eingaben zum Fenster verwendet werden soll.<br/>                                                                    |



 

### <a name="properties"></a>Eigenschaften

Die **InkCollector** -Klasse verfügt über diese Eigenschaften.



| Eigenschaft                                                                             | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                             | Schreibgeschützt<br/> | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der **InkCollector** die frei Hand Eingabe neu zeichnet, wenn das Fenster ungültig wird.<br/>                                                                 |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                       | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob frei Hand Eingaben für ein **InkCollector** -Objekt gerade gezeichnet werden.<br/>                                                                                   |
| [**CollectionMode '**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                     | Schreibgeschützt<br/> | Ruft den Auflistungs Modus ab, der bestimmt, ob Freihand, Gesten oder beides beim Schreiben durch den Benutzer erkannt werden, oder legt ihn fest<br/>                                                                |
| [**Cursor**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                   | Schreibgeschützt<br/> | Ruft die [**Cursorauflistung**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) ab, die für die Verwendung im Erfassungsbereich verfügbar ist.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/> | Schreibgeschützt<br/> | Ruft das standardmäßige [**inkdrawingattributes**](inkdrawingattributes-class.md) -Objekt ab, das die Zeichnungs Attribute angibt, die beim Zeichnen und Anzeigen von Freihand verwendet werden, oder legt dieses fest.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/> | Schreibgeschützt<br/> | Ruft das Interesse an Aspekten des Pakets ab, das frei Hand Eingaben im **InkCollector** -Objekt zugeordnet ist, oder legt dieses fest.<br/>                                                                          |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                   | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob frei Hand Eingaben beim Zeichnen gerendert werden.<br/>                                                                                                       |
| [**Aktiviert**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                   | Schreibgeschützt<br/> | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob das **InkCollector** -Objekt Stift Eingaben sammelt.<br/>                                                                                       |
| [**Handle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                       | Schreibgeschützt<br/> | Ruft das Handle des Fensters ab, an das das **InkCollector** -Objekt angefügt ist, oder legt dieses fest.<br/>                                                                                           |
| [**Freihand**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)<br/>                                           | Schreibgeschützt<br/> | Ruft das [**InkDisp**](inkdisp-class.md) -Objekt ab, das dem **InkCollector** -Objekt zugeordnet ist, oder legt dieses fest.<br/>                                                                     |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                   | Schreibgeschützt<br/> | Ruft die Ränder entlang der x-Achse in Pixel ab oder legt diese fest.<br/>                                                                                                                             |
| [**MarginY**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                   | Schreibgeschützt<br/> | Ruft die Ränder entlang der y-Achse in Pixel ab oder legt diese fest.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                               | Schreibgeschützt<br/> | Ruft das aktuelle benutzerdefinierte Maus Symbol ab oder legt es fest.<br/>                                                                                                                                       |
| [**Mouum Zeiger**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                         | Schreibgeschützt<br/> | Ruft einen Wert ab oder legt einen Wert fest, der den Typ des Mauszeigers angibt, der angezeigt wird, wenn sich die Maus über einem bestimmten Teil des Objekts befindet.<br/>                                                |
| [**Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                 | Schreibgeschützt<br/> | Ruft das [**inkrenderer**](inkrenderer-class.md) -Objekt ab, das zum Zeichnen von Freihand verwendet wird, oder legt dieses fest<br/>                                                                                        |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>     | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob frei Hand Eingaben als nur eine Farbe gerendert werden, wenn sich das System im hoher Kontrast Modus befindet<br/>                                                           |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                        | Schreibgeschützt<br/> | Ruft das Tablet-Gerät ab, das das **InkCollector** -Objekt zurzeit zum Erfassen von Eingaben verwendet.<br/>                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.

Das **InkCollector** -Objekt sammelt nur frei Hand Eingaben und Gesten, die in das jeweilige Fenster eingegeben werden, mit dem es verknüpft ist. Der einzige Zweck von **InkCollector** besteht darin, frei Hand Eingaben von der Hardware (z. b. über ein [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -und [**iinktablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekt) zu erfassen und diese an eine Anwendung zu übermitteln. Im wesentlichen fungiert es als Quelle, die frei Hand Eingaben an ein oder mehrere verschiedene [**InkDisp**](inkdisp-class.md) -Objekte verteilt, die als Container fungieren, der die verteilte frei Hand Eingabe enthält.

Um einen **InkCollector** zu verwenden, erstellen Sie ihn, und informieren Sie ihn über das Fenster, in dem Sie gezeichnet werden, und aktivieren Sie es. Nachdem er aktiviert wurde, kann er so festgelegt werden, dass er nur in einem von drei Modi erfasst wird (der Modus ist in der [**inkcollectionmode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) -Enumeration angegeben):

-   InkOnly, in der ein [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt erstellt wird.
-   GestureOnly, in dem ein [**iinkgesten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) -Objekt erstellt wird.
-   Inkandgeste, bei der ein Strich, eine Geste oder potenziell beides erstellt wird, je nachdem, wie die Anwendung Ereignisse behandelt.

Dies bedeutet, dass für jede Bewegung eines Cursors, der sich innerhalb des Bereichs eines Tablets befindet, der **InkCollector** immer entweder einen Strich oder eine Geste sammelt, und manchmal beides. Gesten Unterstützung ist in mithilfe der Microsoft Gestenerkennung integriert.

Ein **InkCollector** verarbeitet alle Tablet-Eingaben. Frei Hand Eingaben können gleichzeitig von allen angefügten Tablets (einschließlich der Maus) gesammelt werden. Änderungen in den [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -und [**iinkcursorbutton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) -Objekten können bewirken, dass das **InkCollector** -Objekt ein Ereignis auslöst.

Ein **InkCollector** verwaltet auch die Liste der Cursor, die während seiner Existenz gefunden werden. Wenn **InkCollector** auf einen neuen Cursor stößt, wird das [**CursorInRange**](inkcollector-cursorinrange.md) -Ereignis ausgelöst, wobei der *NewCursor* -Parameter auf **Variant \_ true** festgelegt ist. Anwendungen verwenden den **InkCollector** , um neue Cursor zu verwalten.

Einem bestimmten Fenster Handle können mehrere **InkCollector** zugeordnet werden, selbst wenn sich Ihre Auflistungs Bereiche, die im Konstruktor oder mit der [**setwindowinputrechteck**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle) -Methode festgelegt sind, überlappen. Das einzige Verfahren für dieses Szenario ist jedoch, wenn jeder **InkCollector** [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) aufruft und einen eindeutigen Tablet verwendet. Dieses Verhalten erleichtert das Speichern von frei Hand Eingaben in einem separaten Objekt für jedes Tablet.

Ein Fehler tritt auf, wenn das Fenster Eingabe Rechteck einer aktivierten **inkcollectors** (festgelegt mit der [**aktivierten**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled) Eigenschaft) das Fenster Eingabe Rechteck eines anderen aktivierten **InkCollector** überlappt.

> [!Note]  
> Überschneidungen können ohne Fehler auftreten, solange nur eine der Eingabe Rechtecke zu einem beliebigen Zeitpunkt aktiviert ist.

 

Die Ereignisse [**mousdown**](inkcollector-mousedown.md), [**mousmove**](inkcollector-mousemove.md), [**mousup**](inkcollector-mouseup.md)und [**mouswheel**](inkcollector-mousewheel.md) geben x-und y-Koordinaten in Pixel zurück, nicht die HIMETRIC-Einheiten, die dem frei Handbereich zugeordnet sind. Dies liegt daran, dass diese Ereignisse die Mausereignisse von schreibgeschützten Anwendungen ersetzen und diese Anwendungen nur Pixel verstehen.

> [!Note]  
> Das **InkCollector** -Objekt kann nicht sicher in einem nicht-UI-Thread freigegeben werden.

 

Um die Leistung Ihrer Anwendung zu verbessern, löschen Sie das **InkCollector** -Objekt, wenn es nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Referenz zum InkEdit-Steuerelement](inkedit-control-reference.md)
</dt> <dt>

[**InkDisp-Klasse**](inkdisp-class.md)
</dt> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[InkPicture-Steuerelement Verweis](inkpicture-control-reference.md)
</dt> </dl>

 

