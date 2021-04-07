---
description: In diesem Thema wird beschrieben, wie ein benutzerdefinierter Videorenderer für DirectShow geschrieben wird.
ms.assetid: abba5113-125f-4dac-b566-99c0d9b5978c
title: Alternative Videorenderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070e55375d9d1d5a32c306853aafcb431a76c368
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747280"
---
# <a name="alternative-video-renderers"></a>Alternative Videorenderer

In diesem Thema wird beschrieben, wie ein benutzerdefinierter Videorenderer für DirectShow geschrieben wird.

> [!Note]  
> Anstatt einen benutzerdefinierten Videorenderer zu schreiben, empfiehlt es sich, ein Plug-in-zuordnerpresenter für den Video Mischungs-Renderer (VMR) oder den [**erweiterten Videorenderer**](enhanced-video-renderer-filter.md) (EVR) zu schreiben. Mit diesem Ansatz erhalten Sie alle Vorteile der VMR/EVR, einschließlich der Unterstützung für die DirectX-Video Beschleunigung (DXVA), der Deinterlacing von Hardware und der Frame-Step-Methode, und Sie sind wahrscheinlich stabiler als ein benutzerdefinierter Videorenderer. Weitere Informationen finden Sie unter den folgenden Themen:
>
> -   [VMR-renderlosen Wiedergabemodus (benutzerdefinierter Zuweiser)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
> -   [Schreiben von EVR Presenter](/windows/desktop/medfound/how-to-write-an-evr-presenter)

 

## <a name="writing-an-alternative-renderer"></a>Schreiben eines alternativen Renderers

Microsoft DirectShow stellt einen Fenster basierten Videorenderer bereit. Außerdem wird in der Lauf Zeit Installation ein Vollbild-Renderer bereitstellt. Sie können die DirectShow-Basisklassen zum Schreiben alternativer Videorenderer verwenden. Damit Alternative Renderer ordnungsgemäß mit DirectShow-basierten Anwendungen interagieren können, müssen die Renderer den in diesem Artikel beschriebenen Richtlinien entsprechen. Sie können die [**cbaserenderer**](cbaserenderer.md) -Klasse und die [**cbasevideorenderer**](cbasevideorenderer.md) -Klasse verwenden, um diese Richtlinien bei der Implementierung eines alternativen Videorenderers zu befolgen. Aufgrund der kontinuierlichen Entwicklung von DirectShow sollten Sie die Implementierung regelmäßig überprüfen, um sicherzustellen, dass die Renderer mit der neuesten Version von DirectShow kompatibel sind.

In diesem Thema werden viele Benachrichtigungen erläutert, die ein Renderer für die Behandlung verantwortlich ist. Eine kurze Übersicht über DirectShow-Benachrichtigungen kann beim Festlegen der Stufe helfen. Es gibt im Wesentlichen drei Arten von Benachrichtigungen, die in DirectShow auftreten:

-   *Streambenachrichtigungen*, bei denen es sich um Ereignisse handelt, die im Mediendaten Strom auftreten und von einem Filter an den nächsten weitergeleitet werden. Dabei kann es sich um das beginnen-leeren, das Beenden oder das Senden von Datenströmen handeln, die durch Aufrufen der entsprechenden Methode für die Eingabe-PIN des downstreamfilters (z. b. [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)) gesendet werden.
-   *Filtern Sie Diagramm Benachrichtigungen*, bei denen es sich um Ereignisse handelt, die von einem Filter an [**den \_**](ec-complete.md)Filter Graph-Manager gesendet werden Dies wird erreicht, indem die [**imediaeventsink:: notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) -Methode für den Filter Graph-Manager aufgerufen wird.
-   *Anwendungs Benachrichtigungen*, die von der steuernden Anwendung vom Filter Graph-Manager abgerufen werden. Eine Anwendung ruft die [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) -Methode im Filter Graph-Manager auf, um diese Ereignisse abzurufen. Häufig übergibt der Filter Graph-Manager die empfangenen Ereignisse an die Anwendung.

In diesem Thema wird die Verantwortung des rendererfilters bei der Behandlung von empfangenen Datenstrom Benachrichtigungen und beim Senden entsprechender Filter Diagramm Benachrichtigungen erläutert.

## <a name="handling-end-of-stream-and-flushing-notifications"></a>Verarbeiten von Streamende und leeren von Benachrichtigungen

Eine End-of-Stream-Benachrichtigung beginnt mit einem upstreamfilter (z. b. dem Quell Filter), wenn dieser Filter erkennt, dass er keine weiteren Daten senden kann. Sie wird durch jeden Filter im Diagramm geleitet und endet schließlich mit dem Renderer, der für das anschließende Senden einer EC- [**\_ vollständigen**](ec-complete.md) Benachrichtigung an den Filter Graph-Manager zuständig ist. Renderer haben besondere Verantwortlichkeiten, wenn diese Benachrichtigungen behandelt werden.

Ein Renderer empfängt eine Benachrichtigung über das Ende des Datenstroms, wenn die [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode der Eingabe-PIN vom upstreamfilter aufgerufen wird. Ein Renderer sollte diese Benachrichtigung notieren und weiterhin alle Daten Renderingdaten, die Sie bereits empfangen haben. Nachdem alle verbleibenden Daten empfangen wurden, sollte der Renderer eine " [**EC \_ Complete**](ec-complete.md) "-Benachrichtigung an den Filter Graph-Manager senden. Die " **EC \_ Complete** "-Benachrichtigung sollte nur einmal von einem Renderer gesendet werden, wenn das Ende eines Streams erreicht wird. Außerdem dürfen keine **EC- \_ Complete** -Benachrichtigungen gesendet werden, außer wenn das Filter Diagramm ausgeführt wird. Wenn das Filter Diagramm angehalten wird, wenn ein Quell Filter eine End-of-Stream-Benachrichtigung sendet, sollte das **EC \_ Complete** nicht gesendet werden, bis das Filter Diagramm schließlich ausgeführt wird.

Alle Aufrufe der [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode oder der [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) -Methode nach einer Datenstrom Benachrichtigung sollten abgelehnt werden. **E \_ "Unerwartet** " ist die geeignetste Fehlermeldung, die in diesem Fall zurückgegeben wird.

Beim Beenden eines Filter Diagramms sollten alle zwischengespeicherten Datenstrom Benachrichtigungen gelöscht und beim nächsten Start nicht erneut gesendet werden. Dies liegt daran, dass der Filter Graph-Manager immer alle Filter vor dem Ausführen hält, sodass das ordnungsgemäße leeren erfolgt. Wenn z. b. das Filter Diagramm angehalten wird und eine Datenstrom-Benachrichtigung empfangen wird, und dann das Filter Diagramm angehalten wird, sollte der Renderer beim anschließenden Ausführen keine [**EC \_ Complete**](ec-complete.md) -Benachrichtigung senden. Wenn keine Suchvorgänge stattgefunden haben, sendet der Quell Filter automatisch eine andere datenstreambenachrichtigung während des anhaltezustands, der einem Testlauf vorangestellt wird. Wenn andererseits eine Suche stattgefunden hat, während das Filter Diagramm angehalten wurde, kann es vorkommen, dass der Quell Filterdaten enthält, die gesendet werden, sodass keine Datenstrom-Benachrichtigung gesendet wird.

Videorenderer sind häufig von streamingbenachrichtigungen für mehr als das Senden von [**EC \_ Complete**](ec-complete.md) -Benachrichtigungen abhängig. Wenn z. b. die Wiedergabe eines Datenstroms abgeschlossen ist (d. h., es wird eine Datenstrom Benachrichtigung gesendet) und ein anderes Fenster über ein Video-rendererfenster gezogen wird, wird eine Reihe von WM-Zeichnungs Fenstern generiert. [**\_**](/windows/desktop/gdi/wm-paint) Die übliche Vorgehensweise zum Ausführen von videorendererversuchen besteht darin, den aktuellen Frame beim Empfang von **WM \_** -Zeichnungs Nachrichten nicht neu zu zeichnen (basierend auf der Annahme, dass ein anderer Frame gezeichnet werden soll). Wenn jedoch das Ende der Stream-Benachrichtigung gesendet wurde, befindet sich der Renderer in einem Wartezustand. Es wird noch ausgeführt, aber es wird darauf hingewiesen, dass keine zusätzlichen Daten empfangen werden. Unter diesen Umständen zeichnet der Renderer den Wiedergabe Bereich in der Regel schwarz.

Das Behandeln von Leerung ist eine zusätzliche Komplikation für Renderer. Das leeren erfolgt durch ein paar von [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Methoden namens [**beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) und [**endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush). Das leeren ist im Grunde ein zusätzlicher Zustand, den der Renderer verarbeiten muss. Es ist unzulässig, dass ein Quell Filter **beginflush** aufruft, ohne **endflush** aufzurufen, sodass der Status kurz und diskret ist. der Renderer muss jedoch Daten oder Benachrichtigungen, die er während des Leerungs Übergangs empfängt, ordnungsgemäß verarbeiten.

Alle Daten, die nach dem Aufrufen von [**beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) empfangen werden, sollten sofort abgelehnt werden, indem Sie **\_ false** zurückgeben Außerdem sollten alle zwischengespeicherten Datenstrom Benachrichtigungen auch gelöscht werden, wenn ein Renderer geleert wird. Ein Renderer wird in der Regel als Reaktion auf eine Suche geleert. Durch das leeren wird sichergestellt, dass alte Daten aus dem Filter Diagramm gelöscht werden, bevor neue Beispiele gesendet werden. (In der Regel wird die Wiedergabe von zwei Abschnitten eines Streams, einer nach anderen, am besten durch verzögerte Befehle behandelt, anstatt darauf zu warten, dass ein Abschnitt abgeschlossen wird, und dann einen Seek-Befehl auszugeben.)

## <a name="handling-state-changes-and-pause-completion"></a>Behandeln von Zustandsänderungen und Beenden der Beendigung

Ein rendererfilter verhält sich wie jeder andere Filter im Filter Diagramm, wenn der Zustand geändert wird, mit der folgenden Ausnahme. Nachdem der Renderer angehalten wurde, werden einige Daten in der Warteschlange eingereiht und können nach der anschließenden Ausführung gerendert werden. Wenn der Videorenderer beendet wird, behält er diese Daten in der Warteschlange. Dies ist eine Ausnahme von der DirectShow-Regel, dass keine Ressourcen von Filtern gehalten werden sollen, während das Filter Diagramm angehalten wird.

Der Grund für diese Ausnahme ist, dass der Renderer beim Speichern von Ressourcen immer ein Bild hat, mit dem das Fenster neu gezeichnet werden kann, wenn [**eine \_ WM**](/windows/desktop/gdi/wm-paint) -Zeichnungs Nachricht empfangen wird. Außerdem verfügt sie über ein Bild, das Methoden, wie z. b. [**cbasecontrolvideo:: getstaticimage**](cbasecontrolvideo-getstaticimage.md), zu erfüllen, die eine Kopie des aktuellen Bilds anfordern. Ein weiterer Effekt bei der Aufrechterhaltung von Ressourcen besteht darin, dass die Zuweisung von an das Image die Zuweisung der Zuweisung verhindert, dass die Zuweisung der nächsten Zustandsänderung erheblich beschleunigt wird, da die Abbild Puffer bereits zugeordnet sind.

Ein Videorenderer sollte nur bei der Ausführung von ein-und ausgehen. Während der Ausführung wird der Filter möglicherweise gerengt (z. b. beim Zeichnen eines statischen Poster-Bilds in einem Fenster), sollte aber nicht freigegeben werden. Audiorenderer führen während der angehaltenen Ausführung kein Rendering durch (Sie können z. b. auch andere Aktivitäten ausführen, z. b. das Wave-Gerät). Die Zeit, zu der die Beispiele gerendert werden sollen, wird durch Kombinieren der streamzeit im Beispiel mit der als Parameter an die [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) -Methode übergebenen Verweis Zeit erreicht. Renderer sollten Beispiele mit Startzeiten, die kleiner oder gleich den Endzeiten sind, ablehnen.

Wenn eine Anwendung ein Filter Diagramm anhält, wird das Filter Diagramm nicht von der [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) -Methode zurückgegeben, bis die Daten in der Warteschlange vorhanden sind. Um dies sicherzustellen, sollte beim Anhalten eines Renderers S false zurückgegeben werden, \_ Wenn keine Daten vorhanden sind, die darauf warten, gerendert zu werden. Wenn sich Daten in der Warteschlange befinden, können Sie **S \_ OK** zurückgeben.

Der Filter Graph-Manager überprüft alle Rückgabewerte beim Anhalten eines Filter Diagramms, um sicherzustellen, dass die Renderer Daten in die Warteschlange eingereiht haben. Wenn mindestens ein Filter nicht bereit ist, ruft der Filter Diagramm-Manager die Filter im Diagramm durch Aufrufen von [**imediafilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)ab. Die **GetState** -Methode nimmt einen Timeout Parameter an. Ein Filter (in der Regel ein Renderer), der noch darauf wartet, dass Daten vor dem Abschluss der Zustandsänderung eintreffen, gibt den **VFW \_ S \_ State \_ Intermediate** zurück, wenn die **GetState** -Methode abläuft. Sobald die Daten beim Renderer eintreffen, sollte **GetState** sofort mit **S \_ OK** zurückgegeben werden.

Sowohl im zwischen-als auch im abgeschlossenen Zustand ist der gemeldete Filter Zustand " \_ angehalten". Nur der Rückgabewert gibt an, ob der Filter wirklich bereit ist. Wenn ein Renderer auf das Eintreffen der Daten wartet, sendet der Quell Filter eine Streamende Benachrichtigung, und die Statusänderung muss ebenfalls abgeschlossen werden.

Wenn alle Filter tatsächlich über Daten verfügen, die darauf warten, gerendert zu werden, vervollständigt das Filter Diagramm die Änderung des anhaltezustands.

## <a name="handling-termination"></a>Behandeln der Beendigung

Videorenderer müssen Beendigungs Ereignisse des Benutzers ordnungsgemäß behandeln. Dies impliziert das ordnungsgemäße Ausblenden des Fensters und das wissen, was zu tun ist, wenn ein Fenster danach gezwungen wird, angezeigt zu werden. Außerdem müssen Videorenderer den Filter Graph-Manager benachrichtigen, wenn das Fenster zerstört wird (oder genauer, wenn der Renderer aus dem Filter Diagramm entfernt wird), um Ressourcen freizugeben.

Wenn der Benutzer das Videofenster schließt (z. b. durch Drücken von Alt + F4), besteht die Konvention darin, das Fenster sofort auszublenden und eine [**EC \_ userabort**](ec-userabort.md) -Benachrichtigung an den Filter Graph-Manager zu senden. Diese Benachrichtigung wird an die Anwendung übermittelt, wodurch das Abspielen des Diagramms beendet wird. Nach dem Senden von " **EC \_ userabort**" sollte ein Videorenderer alle zusätzlichen, übermittelten Beispiele ablehnen.

Das vom Graph beendete Flag sollte vom Renderer beibehalten werden, bis er anschließend beendet wird. an diesem Punkt sollte er zurückgesetzt werden, damit eine Anwendung die Benutzeraktion außer Kraft setzen und die Darstellung des Diagramms fortsetzen kann, wenn es sich wünscht. Wenn ALT + F4 gedrückt wird, während das Video ausgeführt wird, wird das Fenster ausgeblendet, und alle weiteren übermittelten Beispiele werden abgelehnt. Wenn das Fenster anschließend angezeigt wird (z. b. über [**IVideoWindow::p UT \_ sichtbar**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible)), sollten keine [**EC- \_ Repaint**](ec-repaint.md) -Benachrichtigungen generiert werden.

Der Videorenderer sollte außerdem das [**EC- \_ Fenster \_**](ec-window-destroyed.md) , das beim Beenden des Videorenderers gelöscht wird, an das Filter Diagramm senden. Es empfiehlt sich, dies zu behandeln, wenn die [**ibasefilter:: joinfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) -Methode des Renderers mit einem NULL-Parameter aufgerufen wird (was anzeigt, dass der Renderer aus dem Filter Diagramm entfernt werden soll), anstatt zu warten, bis das eigentliche Videofenster zerstört wird. Wenn diese Benachrichtigung gesendet wird, kann der Plug-in-Verteiler im Filter Graph-Manager Ressourcen übergeben, die vom Fenster Fokus auf andere Filter, z. b. Audiogeräte, abhängen.

## <a name="handling-dynamic-format-changes"></a>Behandeln dynamischer Format Änderungen

In einigen Fällen kann der upstreamfilter des Renderers versuchen, das Videoformat zu ändern, während das Video wiedergegeben wird. In den meisten Fällen ist dies das Video Dekompressor, das eine dynamische Formatänderung auslöst.

Ein upstreamfilter, der versucht, Formate dynamisch zu ändern, sollte immer die [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) -Methode für die Renderer-Eingabe-PIN aufgerufen werden. Ein Videorenderer hat einige Möglichkeiten, welche Arten von dynamischen Formatänderungen er unterstützen sollte. Der upstreamfilter sollte mindestens das Ändern von Paletten ermöglichen. Wenn ein upstreamfilter die Medientypen ändert, wird der Medientyp dem ersten im neuen Format übermittelten Beispiel angefügt. Wenn der Renderer Beispiele in einer Warteschlange zum Rendern enthält, sollte das Format erst geändert werden, wenn das Beispiel mit der Typänderung gerendert wird.

Ein Videorenderer kann auch eine Formatänderung vom Decoder anfordern. Beispielsweise könnte der Decoder den Decoder bitten, ein DirectDraw-kompatibles Format mit einer negativen **biheight** bereitzustellen. Wenn der Renderer angehalten wurde, sollte er [**queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) in der upstreampin aufgerufen werden, um zu sehen, welche Formate der Decoder bereitstellen kann. Der Decoder listet jedoch möglicherweise nicht alle Typen auf, die akzeptiert werden können, sodass der Renderer einige Typen anbieten sollte, auch wenn der Decoder Sie nicht ankündigt.

Wenn der Decoder zum angeforderten Format wechseln kann, wird er von [**queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept)in " **\_ OK** " zurückgegeben. Der Renderer fügt dann den neuen Medientyp an das nächste Medien Beispiel auf der upstreamzuweisung an. Damit dies funktioniert, muss der Renderer eine benutzerdefinierte Zuweisung bereitstellen, die eine private Methode zum Anfügen des Medientyps an das nächste Beispiel implementiert. (Geben Sie in dieser privaten Methode [**imediasample:: setmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) ein, um den Typ festzulegen.)

Die Eingabe-PIN des Renderers sollte die benutzerdefinierte Zuweisung des Renderers in der [**IMemInputPin:: getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) -Methode zurückgeben. Überschreiben Sie [**IMemInputPin:: notifyzuweisung**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) , sodass es fehlschlägt, wenn der upstreamfilter die Zuweisung des Renderers nicht verwendet.

Bei einigen Decodern bewirkt das Festlegen von **biheight** auf eine positive Zahl für YUV-Typen, dass der Decoder das Bild nach oben zeichnet. (Dies ist falsch und sollte im Decoder als Fehler angesehen werden.)

Immer dann, wenn eine Formatänderung durch den Videorenderer erkannt wird, sollte eine Benachrichtigung über die Änderung der [**EC- \_ Anzeige \_**](ec-display-changed.md) gesendet werden. Die meisten Videorenderer wählen während der Verbindung ein Format aus, sodass das Format effizient über GDI gezeichnet werden kann. Wenn der Benutzer den aktuellen Anzeigemodus ändert, ohne den Computer neu zu starten, findet ein Renderer möglicherweise eine ungültige Abbild Format Verbindung und sollte diese Benachrichtigung senden. Der erste Parameter sollte die PIN sein, die erneut eine Verbindung herstellen muss. Der Filter Diagramm-Manager ordnet an, dass das Filter Diagramm angehalten und die PIN erneut verbunden wird. Während der nachfolgenden erneuten Verbindung kann der Renderer ein geeignetere Format akzeptieren.

Wenn ein Videorenderer eine palettenänderung im Stream erkennt, sollte die [**\_ \_ geänderte**](ec-palette-changed.md) Benachrichtigung der EC-Palette an den Filter Graph-Manager gesendet werden. Die DirectShow-Videorenderer erkennen, ob eine Palette im dynamischen Format tatsächlich geändert wurde. Die Videorenderer führen dies nicht nur aus, um die Anzahl der gesendeten Änderungen an der **EC- \_ Palette \_** zu filtern, sondern auch die Menge an Palettenerstellung, Installation und Löschvorgang zu verringern.

Schließlich erkennt der Videorenderer möglicherweise auch, dass sich die Größe des Videos geändert hat. in diesem Fall sollte die Benachrichtigung über [**eine \_ geänderte EC-Video \_ Größe \_**](ec-video-size-changed.md) gesendet werden. Eine Anwendung kann diese Benachrichtigung verwenden, um Speicherplatz in einem Verbund Dokument auszuhandeln. Die tatsächlichen Video Dimensionen sind über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Steuerelement Schnittstelle verfügbar. Die DirectShow-Renderer erkennen, ob die Größe des Videos tatsächlich geändert wurde oder nicht, bevor diese Ereignisse gesendet werden.

## <a name="handling-persistent-properties"></a>Behandeln von permanenten Eigenschaften

Alle Eigenschaften, die über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -und die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle festgelegt werden, sind für die Verbindungs Dauer permanent. Daher sollten beim Trennen und erneuten Verbinden eines Renderers keine Auswirkungen auf die Fenstergröße,-Position oder-Stile angezeigt werden. Wenn sich die Video Dimensionen jedoch zwischen den Verbindungen ändern, sollte der Renderer die Quell-und Ziel Rechtecke auf ihre Standardwerte zurücksetzen. Die Quell-und Zielpositionen werden über die **ibasicvideo** -Schnittstelle festgelegt.

Sowohl [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) als auch [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) bieten ausreichenden Zugriff auf Eigenschaften, damit eine Anwendung alle Daten in der Schnittstelle in einem persistenten Format speichern und wiederherstellen kann. Dies ist nützlich für Anwendungen, die die genaue Konfiguration und die Eigenschaften von Filter Diagrammen während einer Bearbeitungs Sitzung speichern und später wiederherstellen müssen.

## <a name="handling-ec_repaint-notifications"></a>Behandeln von EC- \_ Repaint-Benachrichtigungen

Die [**EC \_ Repaint**](ec-repaint.md) -Benachrichtigung wird nur gesendet, wenn der Renderer entweder angehalten oder beendet wurde. Diese Benachrichtigung signalisiert dem Filter Graph-Manager, dass der Renderer Daten benötigt. Wenn das Filter Diagramm angehalten wird, wenn es eine dieser Benachrichtigungen empfängt, wird das Filter Diagramm angehalten. warten Sie, bis alle Filterdaten empfangen haben (durch Aufrufen von [**GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)), und beenden Sie es dann erneut. Wenn er angehalten wurde, sollte ein Videorenderer an dem Bild halten, damit nachfolgende WM-Zeichnungs Meldungen verarbeitet werden können. [**\_**](/windows/desktop/gdi/wm-paint)

Wenn ein Videorenderer eine WM-Zeichnungs [**Nachricht \_**](/windows/desktop/gdi/wm-paint) erhält, wenn er angehalten oder angehalten wird, und er nichts hat, mit dem das Fenster gezeichnet werden soll, sollte der [**EC \_ Repaint**](ec-repaint.md) an den Filter Graph-Manager gesendet werden. Wenn eine **EC \_ Repaint** -Benachrichtigung empfangen wird, während Sie angehalten wurde, ruft der Filter Graph-Manager [**imediaposition::p UT \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) mit der aktuellen Position auf (d. h., sucht nach der aktuellen Position). Dies bewirkt, dass die Quell Filter das Filter Diagramm leeren und bewirkt, dass neue Daten über das Filter Diagramm gesendet werden.

Ein Renderer darf jeweils nur eine dieser Benachrichtigungen senden. Nachdem der Renderer eine Benachrichtigung gesendet hat, sollte daher sichergestellt werden, dass nicht mehr gesendet werden, bis einige Beispiele übermittelt wurden. Die herkömmliche Vorgehensweise besteht darin, ein Flag zu verwenden, das kennzeichnet, dass ein Repaint gesendet werden kann, das ausgeschaltet wird, nachdem eine [**EC \_ Repaint**](ec-repaint.md) -Benachrichtigung gesendet wurde. Dieses Flag sollte zurückgesetzt werden, wenn Daten übermittelt werden, oder wenn die Eingabe-PIN geleert wird, aber nicht, wenn das Ende des Streams in der eingabepin signalisiert wird.

Wenn der Renderer seine [**EC- \_ Repaint**](ec-repaint.md) -Benachrichtigungen nicht überwacht, wird der Filter Graph-Manager mit **EC \_ Repaint** -Anforderungen überflutet (was relativ aufwendig ist). Wenn ein Renderer z. b. kein Bild hat, das gezeichnet werden soll, und ein anderes Fenster in einem vollständigen Drag-Vorgang auf das Fenster des Renderers gezogen wird, empfängt der Renderer mehrere [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldungen. Nur der erste muss eine **EC \_ Repaint** -Ereignis Benachrichtigung vom Renderer an den Filter Graph-Manager generieren.

Ein Renderer sollte seine Eingabe-PIN als ersten Parameter an die [**EC \_ Repaint**](ec-repaint.md) -Benachrichtigung senden. Auf diese Weise wird die angefügte Ausgabepin für [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)abgefragt, und wenn diese unterstützt wird, wird zuerst die **EC \_ Repaint** -Benachrichtigung gesendet. Dadurch können Ausgabe Pins Repaint verarbeiten, bevor das Filter Diagramm berührt werden muss. Dies wird nicht durchgeführt, wenn das Filter Diagramm angehalten wird, da keine Puffer von der Zuweiser Renderer-Zuweisung bereitgestellt werden können.

Wenn die Ausgabe-PIN die Anforderung nicht verarbeiten kann und das Filter Diagramm ausgeführt wird, wird die [**EC \_ Repaint**](ec-repaint.md) -Benachrichtigung ignoriert. Eine Ausgabe-PIN muss **S \_ OK** aus [**imediaeventsink:: notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) zurückgeben, um zu signalisieren, dass die Repaint-Anforderung erfolgreich verarbeitet wurde. Die Ausgabepin wird für den Arbeits Thread des Filter-Graph-Managers aufgerufen, wodurch vermieden wird, dass der Renderer die Ausgabepin direkt aufruft und somit alle Deadlockprobleme nach sich zieht. Wenn das Filter Diagramm beendet oder angehalten wurde und die Ausgabe die Anforderung nicht verarbeitet, wird die Standard Verarbeitung durchgeführt.

## <a name="handling-notifications-in-full-screen-mode"></a>Behandeln von Benachrichtigungen im Full-Screen Modus

Der [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Plug-in-Verteiler (PID) im Filter Diagramm verwaltet die Vollbildwiedergabe. Ein Videorenderer wird für einen spezialisierten Vollbild-Renderer ausgetauscht, ein Fenster eines Renderers auf den voll Bildschirm gestreckt, oder der Renderer muss die Vollbildwiedergabe direkt implementieren. Um mit voll Bild Protokollen zu interagieren, sollte ein Videorenderer eine [**EC- \_ Aktivierungs**](ec-activate.md) Benachrichtigung senden, wenn das Fenster aktiviert oder deaktiviert ist. Anders ausgedrückt: für jede WM activateapp-Nachricht, die ein Renderer empfängt, sollte eine **EC- \_ Aktivierungs** Benachrichtigung gesendet werden \_ .

Wenn ein Renderer im Vollbildmodus verwendet wird, verwalten diese Benachrichtigungen den Wechsel in den und aus diesem Vollbildmodus. Die Fenster Deaktivierung tritt normalerweise auf, wenn ein Benutzer Alt + Tab drückt, um zu einem anderen Fenster zu wechseln, das der DirectShow-Vollbild-Renderer als Hinweis verwendet, um zum typischen Renderingmodus zurückzukehren.

Wenn die [**EC- \_ Aktivierungs**](ec-activate.md) Benachrichtigung an den Filter Graph-Manager gesendet wird, wenn der Vollbildmodus gewechselt wird, sendet der Filter Graph-Manager eine [**EC- \_ Vollbild \_**](ec-fullscreen-lost.md) -Benachrichtigung an die steuernde Anwendung. Die Anwendung kann diese Benachrichtigung verwenden, um z. b. den Status einer voll Bild Schaltfläche wiederherzustellen. Die **EC- \_ Aktivierungs** Benachrichtigungen werden intern von DirectShow verwendet, um den Vollbild-Wechsel für Hinweise von den Videorenderer zu verwalten.

## <a name="summary-of-notifications"></a>Zusammenfassung der Benachrichtigungen

In diesem Abschnitt werden die Filter Diagramm Benachrichtigungen aufgelistet, die von einem Renderer gesendet werden können.



| Ereignisbenachrichtigung                                        | BESCHREIBUNG                                                                                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktivieren von EC \_**](ec-activate.md)                       | Wird von Videorenderer im Vollbild-Renderingmodus für jede \_ empfangene WM activateapp-Nachricht gesendet.                                                                                                  |
| [**EC \_ Complete**](ec-complete.md)                       | Wird von renderatoren gesendet, nachdem alle Daten gerendert wurden.                                                                                                                                               |
| [**EC- \_ Anzeige \_ geändert**](ec-display-changed.md)        | Wird von Videorenderer gesendet, wenn sich ein Anzeige Format ändert.                                                                                                                                            |
| [**EC- \_ Palette \_ geändert**](ec-palette-changed.md)        | Wird gesendet, wenn ein Videorenderer eine palettenänderung im Stream erkennt.                                                                                                                            |
| [**EC- \_ Repaint**](ec-repaint.md)                         | Wird von beendeten oder angehaltenen Videorenderer gesendet, wenn eine WM \_ -Zeichnungs Nachricht empfangen wird und keine anzuzeigenden Daten vorhanden sind. Dies bewirkt, dass der Filter Graph-Manager einen Frame zum Zeichnen in die Anzeige generiert. |
| [**EC \_ userabort**](ec-userabort.md)                     | Wird von Videorenderer gesendet, um eine vom Benutzer angeforderte Sperre zu signalisieren (z. b. ein Benutzer, der das Videofenster schließt).                                                                               |
| [**Größe des EC- \_ Videos \_ \_ geändert**](ec-video-size-changed.md) | Wird von videorendererarbeitern gesendet, wenn eine Änderung an der systemeigenen Videogröße erkannt wird.                                                                                                                       |
| [**EC- \_ Fenster \_ zerstört**](ec-window-destroyed.md)      | Wird von Videorenderer gesendet, wenn der Filter entfernt oder zerstört wird, sodass Ressourcen, die vom Fenster Fokus abhängen, an andere Filter weitergegeben werden können.                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von Videorenderer](writing-video-renderers.md)
</dt> </dl>

 

 
