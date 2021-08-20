---
description: In diesem Thema wird beschrieben, wie Sie einen benutzerdefinierten Videorenderer für DirectShow schreiben.
ms.assetid: abba5113-125f-4dac-b566-99c0d9b5978c
title: Alternative Videorenderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd105f406e1b39d998a027a915621f214ec2e769f373912a1e9e8525573f31aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074804"
---
# <a name="alternative-video-renderers"></a>Alternative Videorenderer

In diesem Thema wird beschrieben, wie Sie einen benutzerdefinierten Videorenderer für DirectShow schreiben.

> [!Note]  
> Anstatt einen benutzerdefinierten Videorenderer zu schreiben, wird empfohlen, ein Plug-In allocator-presenter für den Video Mixing Renderer (VMR) oder [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) zu schreiben. Dieser Ansatz bietet Ihnen alle Vorteile von VMR/EVR, einschließlich Unterstützung für DirectX Video Acceleration (DXVA), Hardwaredeinterlacing und Frameschritte, und ist wahrscheinlich stabiler als ein benutzerdefinierter Videorenderer. Weitere Informationen finden Sie in den folgenden Themen:
>
> -   [VMR Renderless Playback Mode (Custom Allocator-Presenters)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
> -   [Schreiben eines EVR-Presenters](/windows/desktop/medfound/how-to-write-an-evr-presenter)

 

## <a name="writing-an-alternative-renderer"></a>Schreiben eines alternativen Renderers

Microsoft DirectShow bietet einen fensterbasierten Videorenderer. Es stellt auch einen Vollbildrenderer in der Laufzeitinstallation bereit. Sie können die DirectShow-Basisklassen verwenden, um alternative Videorenderer zu schreiben. Damit alternative Renderer ordnungsgemäß mit DirectShow-basierten Anwendungen interagieren können, müssen die Renderer die in diesem Artikel beschriebenen Richtlinien einhalten. Sie können die [**Klassen CBaseRenderer**](cbaserenderer.md) und [**CBaseVideoRenderer**](cbasevideorenderer.md) verwenden, um diese Richtlinien beim Implementieren eines alternativen Videorenderings zu befolgen. Überprüfen Sie ihre Implementierung aufgrund der laufenden Entwicklung von DirectShow regelmäßig, um sicherzustellen, dass die Renderer mit der neuesten Version von DirectShow kompatibel sind.

In diesem Thema werden viele Benachrichtigungen erläutert, die von einem Renderer verarbeitet werden. Eine kurze Überprüfung der DirectShow-Benachrichtigungen kann beim Festlegen der Phase hilfreich sein. Es gibt im Wesentlichen drei Arten von Benachrichtigungen, die in DirectShow auftreten:

-   *Streambenachrichtigungen* sind Ereignisse, die im Medienstream auftreten und von einem Filter an den nächsten übergeben werden. Hierbei kann es sich um Benachrichtigungen zum Starten, Beenden oder Streamende handelt, und sie werden gesendet, indem die entsprechende Methode auf dem Eingabepin des Downstreamfilters aufgerufen wird (z. B. [**IPin::BeginFlush).**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)
-   *Filterdiagrammbenachrichtigungen,* bei denen es sich um Ereignisse handelt, die von einem Filter an den Filter Graph Manager gesendet werden, z. [**B. EC \_ COMPLETE**](ec-complete.md). Dies wird erreicht, indem die [**IMediaEventSink::Notify-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) im Filter Graph Manager aufgerufen wird.
-   *Anwendungsbenachrichtigungen,* die vom Filter Graph Manager von der steuernden Anwendung abgerufen werden. Eine Anwendung ruft die [**IMediaEvent::GetEvent-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) im Filter-Graph-Manager auf, um diese Ereignisse abzurufen. Häufig übergibt der Filter Graph Manager die empfangenen Ereignisse an die Anwendung.

In diesem Thema wird die Verantwortung des Rendererfilters bei der Verarbeitung von empfangenen Streambenachrichtigungen und beim Senden geeigneter Filterdiagrammbenachrichtigungen erläutert.

## <a name="handling-end-of-stream-and-flushing-notifications"></a>Verarbeiten des Endes des Streams und Leeren von Benachrichtigungen

Eine End-of-Stream-Benachrichtigung beginnt bei einem Upstreamfilter (z. B. dem Quellfilter), wenn dieser Filter erkennt, dass keine weiteren Daten gesendet werden können. Er wird durch jeden Filter im Diagramm übergeben und endet schließlich beim Renderer, der anschließend eine [**EC \_ COMPLETE-Benachrichtigung**](ec-complete.md) an den Filter Graph Manager sendet. Renderer haben besondere Zuständigkeiten bei der Behandlung dieser Benachrichtigungen.

Ein Renderer empfängt eine End-of-Stream-Benachrichtigung, wenn die [**IPin::EndOfStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) des Eingabepins vom Upstreamfilter aufgerufen wird. Ein Renderer sollte diese Benachrichtigung notieren und weiterhin alle bereits empfangenen Daten rendern. Sobald alle verbleibenden Daten empfangen wurden, sollte der Renderer eine [**EC \_ COMPLETE-Benachrichtigung**](ec-complete.md) an den Filter Graph Manager senden. Die **EC \_ COMPLETE-Benachrichtigung** sollte von einem Renderer nur einmal gesendet werden, wenn sie das Ende eines Streams erreicht. Darüber hinaus dürfen **EC COMPLETE-Benachrichtigungen \_** nur gesendet werden, wenn das Filterdiagramm ausgeführt wird. Wenn das Filterdiagramm daher angehalten wird, wenn ein Quellfilter eine Benachrichtigung über das Ende des Streams sendet, sollte **EC \_ COMPLETE** erst gesendet werden, wenn das Filterdiagramm schließlich ausgeführt wird.

Alle Aufrufe der [**Methoden IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) oder [**IMemInputPin::ReceiveMultiple,**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) nachdem eine Benachrichtigung über das Ende des Streams signalisiert wurde, sollten abgelehnt werden. **E \_ UNEXPECTED** ist die am besten geeignete Fehlermeldung, die in diesem Fall zurückgegeben werden soll.

Wenn ein Filterdiagramm beendet wird, sollten alle zwischengespeicherten End-of-Stream-Benachrichtigungen gelöscht und beim nächsten Start nicht erneut übermittelt werden. Dies liegt daran, dass der Filter-Graph-Manager alle Filter immer unmittelbar vor der Ausführung annimmt, sodass eine ordnungsgemäße Leerung erfolgt. Wenn also beispielsweise das Filterdiagramm angehalten wird und eine Benachrichtigung über das Ende des Streams empfangen wird und dann das Filterdiagramm beendet wird, sollte der Renderer bei der anschließenden Ausführung keine [**EC \_ COMPLETE-Benachrichtigung**](ec-complete.md) senden. Wenn keine Suchläufe aufgetreten sind, sendet der Quellfilter während des Pausenzustands, der einem Ausführungszustand vorausgeht, automatisch eine weitere Benachrichtigung über das Ende des Streams. Wenn andererseits eine Suche erfolgt ist, während das Filterdiagramm beendet wird, verfügt der Quellfilter möglicherweise über zu sendende Daten, sodass keine Benachrichtigung über das Ende des Streams gesendet wird.

Videorenderer sind häufig für mehr als das Senden von [**EC COMPLETE-Benachrichtigungen \_**](ec-complete.md) von End-of-Stream-Benachrichtigungen abhängig. Wenn beispielsweise die Wiedergabe eines Streams abgeschlossen ist (d. h. eine Benachrichtigung über das Ende des Streams gesendet wird) und ein anderes Fenster über ein Videorendererfenster gezogen wird, werden eine Reihe von [**WM \_ PAINT-Fenstermeldungen**](/windows/desktop/gdi/wm-paint) generiert. Die übliche Vorgehensweise beim Ausführen von Videorenderern besteht darin, den aktuellen Frame bei Empfang von **WM \_ PAINT-Nachrichten** neu zu zeichnen (basierend auf der Annahme, dass ein anderer zu zeichnender Frame empfangen wird). Wenn jedoch die Benachrichtigung zum Ende des Streams gesendet wurde, befindet sich der Renderer im Wartezustand. sie wird weiterhin ausgeführt, aber sie ist sich bewusst, dass sie keine zusätzlichen Daten empfängt. Unter diesen Umständen zeichnet der Renderer den Wiedergabebereich üblicherweise schwarz.

Die Behandlung von Leerungen ist eine zusätzliche Komplizierung für Renderer. Das Leeren erfolgt über ein Paar von [**IPin-Methoden**](/windows/desktop/api/Strmif/nn-strmif-ipin) namens [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) und [**EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) Das Leeren ist im Wesentlichen ein zusätzlicher Zustand, den der Renderer behandeln muss. Es ist unzulässig, dass ein Quellfilter **BeginFlush aufruft,** ohne **EndFlush** aufzurufen, sodass der Zustand hoffentlich kurz und diskret ist. Der Renderer muss jedoch Daten oder Benachrichtigungen, die er während des Leerungsübergangs empfängt, ordnungsgemäß verarbeiten.

Alle Daten, die nach dem Aufruf von [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) empfangen werden, sollten sofort abgelehnt werden, indem **S \_ FALSE** zurückgegeben wird. Darüber hinaus sollten alle zwischengespeicherten End-of-Stream-Benachrichtigungen auch gelöscht werden, wenn ein Renderer geleert wird. Ein Renderer wird in der Regel als Antwort auf eine Suche geleert. Durch die Leerung wird sichergestellt, dass alte Daten aus dem Filterdiagramm gelöscht werden, bevor neue Stichproben gesendet werden. (In der Regel wird die Wiedergabe von zwei Abschnitten eines Streams nacheinander am besten über verzögerte Befehle verarbeitet, anstatt auf den Abschluss eines Abschnitts zu warten und dann einen Seek-Befehl auszugeben.)

## <a name="handling-state-changes-and-pause-completion"></a>Behandeln von Zustandsänderungen und Anhalten der Vervollständigung

Ein Rendererfilter verhält sich mit der folgenden Ausnahme wie jeder andere Filter im Filterdiagramm, wenn sein Zustand geändert wird. Nachdem der Renderer angehalten wurde, werden einige Daten in die Warteschlange eingereiht, die bei der anschließenden Ausführung gerendert werden können. Wenn der Videorenderer beendet wird, wird er für diese Daten in der Warteschlange gespeichert. Dies ist eine Ausnahme von der DirectShow-Regel, dass keine Ressourcen von Filtern aufbewahrt werden sollen, während das Filterdiagramm beendet wird.

Der Grund für diese Ausnahme ist, dass der Renderer durch das Halten von Ressourcen immer über ein Bild verfügt, mit dem das Fenster neu malt werden kann, wenn er eine [**WM \_ PAINT-Nachricht**](/windows/desktop/gdi/wm-paint) empfängt. Es verfügt auch über ein Image, um Methoden wie [**CBaseControlVideo::GetStaticImage**](cbasecontrolvideo-getstaticimage.md)zu erfüllen, die eine Kopie des aktuellen Images anfordern. Eine weitere Auswirkung des Haltens von Ressourcen besteht darin, dass durch das Halten am Image verhindert wird, dass die Zuweisung aufgehoben wird. Dies führt wiederum dazu, dass die nächste Zustandsänderung viel schneller erfolgt, da die Imagepuffer bereits zugeordnet sind.

Ein Videorenderer sollte Beispiele nur während der Ausführung rendern und freigeben. Während der Filter angehalten wurde, kann er sie rendern (z. B. beim Zeichnen eines statischen Posterbilds in einem Fenster), sollte sie jedoch nicht freigeben. Audiorenderer führen während der Pause kein Rendering durch (obwohl sie andere Aktivitäten ausführen können, z. B. die Vorbereitung des Wellengeräts). Die Zeit, zu der die Beispiele gerendert werden sollen, wird abgerufen, indem die Streamzeit im Beispiel mit der Referenzzeit kombiniert wird, die als Parameter an die [**IMediaControl::Run-Methode**](/windows/desktop/api/Control/nf-control-imediacontrol-run) übergeben wird. Renderer sollten Stichproben mit Startzeiten ablehnen, die kleiner oder gleich enden.

Wenn eine Anwendung ein Filterdiagramm anzuhalten, gibt das Filterdiagramm erst dann von seiner [**IMediaControl::P ause-Methode**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) zurück, wenn daten in die Warteschlange der Renderer eingereiht werden. Um dies sicherzustellen, sollte beim Anhalten eines Renderers S FALSE zurückgegeben \_ werden, wenn keine Daten auf das Rendern warten. Wenn Daten in die Warteschlange eingereiht sind, kann S **\_ OK** zurückgegeben werden.

Der Filter Graph Manager überprüft beim Anhalten eines Filterdiagramms alle Rückgabewerte, um sicherzustellen, dass die Renderer daten in die Warteschlange eingereiht haben. Wenn mindestens ein Filter nicht bereit ist, fragt der Filter Graph Manager die Filter im Diagramm ab, indem [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)aufgerufen wird. Die **GetState-Methode** verwendet einen Time out-Parameter. Ein Filter (in der Regel ein Renderer), der noch auf das Eintreffen der Daten wartet, bevor die Zustandsänderung abgeschlossen ist, gibt **VFW \_ S \_ STATE \_ INTERMEDIATE** zurück, wenn die **GetState-Methode** abläuft. Sobald die Daten beim Renderer eintreffen, sollte **GetState** sofort mit **S \_ OK** zurückgegeben werden.

Sowohl im Zwischen- als auch im Abgeschlossen-Zustand ist der gemeldete Filterzustand Zustand \_ angehalten. Nur der Rückgabewert gibt an, ob der Filter wirklich bereit ist oder nicht. Wenn ein Renderer auf das Eintreffen von Daten wartet, sendet sein Quellfilter eine Benachrichtigung über das Ende des Streams, dann sollte auch die Zustandsänderung abgeschlossen werden.

Sobald alle Filter tatsächlich Daten enthalten, die auf das Rendern warten, schließt das Filterdiagramm die Änderung des Pausenzustands ab.

## <a name="handling-termination"></a>Behandeln der Beendigung

Videorenderer müssen Beendigungsereignisse des Benutzers ordnungsgemäß verarbeiten. Dies bedeutet, dass das Fenster ordnungsgemäß ausgeblendet wird und bekannt ist, was zu tun ist, wenn ein Fenster anschließend angezeigt werden muss. Außerdem müssen Videorenderer den Filter Graph Manager benachrichtigen, wenn sein Fenster zerstört wird (oder genauer gesagt, wenn der Renderer aus dem Filterdiagramm entfernt wird), um Ressourcen freizugeben.

Wenn der Benutzer das Videofenster schließt (z. B. durch Drücken von ALT+F4), besteht die Konvention darin, das Fenster sofort auszublenden und eine [**EC \_ USERABORT-Benachrichtigung**](ec-userabort.md) an den Filter Graph Manager zu senden. Diese Benachrichtigung wird an die Anwendung übergeben, wodurch das Wiedergeben des Graphen beendet wird. Nach dem Senden von **EC \_ USERABORT** sollte ein Videorenderer alle weiteren bereitgestellten Beispiele ablehnen.

Das Graphstoppflag sollte vom Renderer beibehalten werden, bis es anschließend beendet wird. An diesem Punkt sollte es zurückgesetzt werden, damit eine Anwendung die Benutzeraktion überschreiben und das Diagramm bei Bedarf weiterhin wiedergeben kann. Wenn ALT+F4 gedrückt wird, während das Video ausgeführt wird, wird das Fenster ausgeblendet, und alle weiteren übermittelten Beispiele werden abgelehnt. Wenn das Fenster anschließend angezeigt wird (möglicherweise über [**IVideoWindow::p ut \_ Visible),**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible)sollten keine [**EC \_ REPAINT-Benachrichtigungen**](ec-repaint.md) generiert werden.

Der Videorenderer sollte auch die [**EC \_ WINDOW \_ DESTROYED-Benachrichtigung**](ec-window-destroyed.md) an den Filtergraphen senden, wenn der Videorenderer beendet wird. Tatsächlich empfiehlt es sich, dies zu behandeln, wenn die [**IBaseFilter::JoinFilterGraph-Methode**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) des Renderers mit einem NULL-Parameter aufgerufen wird (der angibt, dass der Renderer im Begriff ist, aus dem Filterdiagramm entfernt zu werden), anstatt zu warten, bis das tatsächliche Videofenster zerstört wird. Durch das Senden dieser Benachrichtigung kann der Plug-In-Verteiler im Filter Graph Manager Ressourcen, die vom Fensterfokus abhängig sind, an andere Filter wie Audiogeräte übergeben.

## <a name="handling-dynamic-format-changes"></a>Verarbeiten dynamischer Formatänderungen

In einigen Fällen versucht der Upstreamfilter des Renderers möglicherweise, das Videoformat zu ändern, während das Video wiedergegeben wird. In den meisten Fällen initiiert der Videodekomprimierer eine dynamische Formatänderung.

Ein Upstreamfilter, der versucht, Formate dynamisch zu ändern, sollte immer die [**IPin::QueryAccept-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) auf dem Eingabepin des Renderers aufrufen. Ein Videorenderer hat einen Gewissensraum, um zu erfahren, welche Arten von dynamischen Formatänderungen er unterstützen soll. Mindestens sollte der Upstreamfilter Paletten ändern können. Wenn ein Upstreamfilter Medientypen ändert, fügt er den Medientyp an das erste Im neuen Format übermittelte Beispiel an. Wenn der Renderer Beispiele in einer Warteschlange für das Rendering enthält, sollte er das Format erst ändern, wenn er das Beispiel mit der Typänderung rendert.

Ein Videorenderer kann auch eine Formatänderung vom Decoder anfordern. Beispielsweise kann der Decoder aufgefordert werden, ein DirectDraw-kompatibles Format mit einem negativen **biHeight** bereitzustellen. Wenn der Renderer angehalten wird, sollte er [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) auf dem Upstreampin aufrufen, um zu sehen, welche Formate der Decoder bereitstellen kann. Der Decoder kann jedoch möglicherweise nicht alle Typen aufzählen, die er akzeptieren kann. Daher sollte der Renderer einige Typen auch dann anbieten, wenn der Decoder sie nicht ankündigt.

Wenn der Decoder zum angeforderten Format wechseln kann, gibt er **S \_ OK** von [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept)zurück. Der Renderer fügt dann den neuen Medientyp an das nächste Medienbeispiel auf der Upstreamzuweisung an. Damit dies funktioniert, muss der Renderer eine benutzerdefinierte Zuweisung bereitstellen, die eine private Methode zum Anfügen des Medientyps an das nächste Beispiel implementiert. (Rufen Sie in dieser privaten Methode [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) auf, um den Typ festzulegen.)

Der Eingabepin des Renderers sollte die benutzerdefinierte Zuweisung des Renderers in der [**IMemInputPin::GetAllocator-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) zurückgeben. Überschreiben Sie [**IMemInputPin::NotifyAllocator,**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) sodass ein Fehler auftritt, wenn der Upstreamfilter die Zuweisung des Renderers nicht verwendet.

Bei einigen Decodern führt das Festlegen von **biHeight** auf eine positive Zahl für YUV-Typen dazu, dass der Decoder das Bild um den Kopf zeichnet. (Dies ist falsch und sollte als Fehler im Decoder betrachtet werden.)

Wenn vom Videorenderer eine Formatänderung erkannt wird, sollte eine [**EC \_ DISPLAY \_ CHANGED-Benachrichtigung**](ec-display-changed.md) gesendet werden. Die meisten Videorenderer wählen während der Verbindung ein Format aus, damit das Format effizient über GDI gezeichnet werden kann. Wenn der Benutzer den aktuellen Anzeigemodus ändert, ohne den Computer neu zu starten, befindet sich ein Renderer möglicherweise mit einer fehlerhaften Imageformatverbindung und sollte diese Benachrichtigung senden. Der erste Parameter sollte der Pin sein, der erneut eine Verbindung herstellen muss. Der Filter-Graph-Manager sorgt dafür, dass das Filterdiagramm beendet und die Verbindung mit dem Pin wiederhergestellt wird. Während der nachfolgenden erneuten Verbindung kann der Renderer ein geeigneteres Format akzeptieren.

Wenn ein Videorenderer eine Palettenänderung im Stream erkennt, sollte er die [**EC \_ PALETTE \_ CHANGED-Benachrichtigung**](ec-palette-changed.md) an den Filter Graph Manager senden. Die DirectShow-Videorenderer erkennen, ob sich eine Palette im dynamischen Format geändert hat oder nicht. Die Videorenderer führen dies nicht nur aus, um die Anzahl der gesendeten EC PALETTE CHANGED-Benachrichtigungen **herauszufiltern, \_ \_** sondern auch, um die Erforderliche Menge an Palettenerstellung, Installation und Löschung zu reduzieren.

Schließlich erkennt der Videorenderer möglicherweise auch, dass sich die Größe des Videos geändert hat. In diesem Fall sollte er die [**EC \_ VIDEO SIZE \_ \_ CHANGED-Benachrichtigung**](ec-video-size-changed.md) senden. Eine Anwendung kann diese Benachrichtigung verwenden, um Speicherplatz in einem zusammengesetzten Dokument auszuhandeln. Die tatsächlichen Videodimensionen sind über die [**IBasicVideo-Steuerelementschnittstelle**](/windows/desktop/api/Control/nn-control-ibasicvideo) verfügbar. Die DirectShow-Renderer erkennen, ob sich die Größe des Videos vor dem Senden dieser Ereignisse tatsächlich geändert hat oder nicht.

## <a name="handling-persistent-properties"></a>Behandeln persistenter Eigenschaften

Alle Eigenschaften, die über die [**Schnittstellen IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) und [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) festgelegt werden, sind verbindungsübergreifend persistent. Daher sollte das Trennen und erneute Verbinden eines Renderers keine Auswirkungen auf die Fenstergröße, -position oder -stile haben. Wenn sich die Videodimensionen jedoch zwischen Verbindungen ändern, sollte der Renderer die Quell- und Zielrechtecke auf ihre Standardwerte zurücksetzen. Die Quell- und Zielpositionen werden über die **IBasicVideo-Schnittstelle** festgelegt.

[**Sowohl IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) als [**auch IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) bieten ausreichend Zugriff auf Eigenschaften, damit eine Anwendung alle Daten in der Schnittstelle in einem persistenten Format speichern und wiederherstellen kann. Dies ist nützlich für Anwendungen, die die genaue Konfiguration und die Eigenschaften von Filterdiagrammen während einer Bearbeitungssitzung speichern und später wiederherstellen müssen.

## <a name="handling-ec_repaint-notifications"></a>Behandeln von \_ EC-REPAINT-Benachrichtigungen

Die [**EC \_ REPAINT-Benachrichtigung**](ec-repaint.md) wird nur gesendet, wenn der Renderer angehalten oder beendet wird. Diese Benachrichtigung signalisiert dem Filter Graph Manager, dass der Renderer Daten benötigt. Wenn das Filterdiagramm beendet wird, wenn es eine dieser Benachrichtigungen empfängt, hält es das Filterdiagramm an, wartet, bis alle Filter Daten empfangen (durch Aufrufen von [**GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)), und beendet es dann erneut. Wenn er beendet wird, sollte ein Videorenderer das Bild speichern, damit nachfolgende [**WM \_ PAINT-Meldungen**](/windows/desktop/gdi/wm-paint) verarbeitet werden können.

Wenn ein Videorenderer daher eine [**WM \_ PAINT-Nachricht**](/windows/desktop/gdi/wm-paint) empfängt, wenn er angehalten oder angehalten wurde, und er über nichts verfügt, um sein Fenster zu zeichnen, sollte er [**EC \_ REPAINT**](ec-repaint.md) an den Filter Graph Manager senden. Wenn eine **EC \_ REPAINT-Benachrichtigung** empfangen wird, während sie angehalten wird, ruft der Filter Graph Manager [**IMediaPosition::p ut \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) mit der aktuellen Position auf (d.h. sucht nach der aktuellen Position). Dies bewirkt, dass die Quellfilter das Filterdiagramm leeren und neue Daten über das Filterdiagramm gesendet werden.

Ein Renderer darf jeweils nur eine dieser Benachrichtigungen senden. Sobald der Renderer eine Benachrichtigung sendet, sollte er daher sicherstellen, dass erst dann mehr gesendet werden, wenn einige Beispiele übermittelt werden. Die herkömmliche Möglichkeit hierfür besteht darin, ein Flag zu haben, das angibt, dass ein Repaint gesendet werden kann, der nach dem Senden einer [**EC \_ REPAINT-Benachrichtigung**](ec-repaint.md) deaktiviert wird. Dieses Flag sollte zurückgesetzt werden, sobald Daten übermittelt wurden oder wenn der Eingabepin geleert wird, aber nicht, wenn das Ende des Streams auf dem Eingabepin signalisiert wird.

Wenn der Renderer seine [**EC \_ REPAINT-Benachrichtigungen**](ec-repaint.md) nicht überwacht, überflutet er den Filter Graph Manager mit **EC \_ REPAINT-Anforderungen** (die relativ teuer zu verarbeiten sind). Wenn ein Renderer beispielsweise kein zu zeichnendes Bild hat und ein anderes Fenster in einem vollständigen Ziehvorgang über das Fenster des Renderers gezogen wird, empfängt der Renderer mehrere [**WM \_ PAINT-Meldungen.**](/windows/desktop/gdi/wm-paint) Nur die erste dieser Ereignisse sollte eine **EC \_ REPAINT-Ereignisbenachrichtigung** vom Renderer an den Filter Graph Manager generieren.

Ein Renderer sollte seinen Eingabepin als ersten Parameter an die [**EC \_ REPAINT-Benachrichtigung**](ec-repaint.md) senden. Auf diese Weise wird der angefügte Ausgabepin nach [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)abgefragt, und wenn dies unterstützt wird, wird die **EC \_ REPAINT-Benachrichtigung** zuerst dort gesendet. Dadurch können Ausgabepins Neustriche verarbeiten, bevor das Filterdiagramm berührt werden muss. Dies geschieht nicht, wenn das Filterdiagramm beendet wird, da keine Puffer über die Zuweisung des decommitted-Renderers verfügbar wären.

Wenn der Ausgabepin die Anforderung nicht verarbeiten kann und der Filtergraph ausgeführt wird, wird die [**EC \_ REPAINT-Benachrichtigung**](ec-repaint.md) ignoriert. Ein Ausgabepin muss **S \_ OK** von [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) zurückgeben, um zu signalisieren, dass die Anforderung zum erneuten Anheften erfolgreich verarbeitet wurde. Der Ausgabepin wird im Workerthread Filter Graph Manager aufgerufen. Dadurch wird vermieden, dass der Renderer den Ausgabepin direkt aufruft, sodass Deadlockprobleme umgangen werden. Wenn das Filterdiagramm beendet oder angehalten wird und die Ausgabe die Anforderung nicht verarbeitet, erfolgt die Standardverarbeitung.

## <a name="handling-notifications-in-full-screen-mode"></a>Behandeln von Benachrichtigungen im Full-Screen-Modus

Der [](/windows/desktop/api/Control/nn-control-ivideowindow) IVideoWindow-Plug-In-Verteiler (PID) im Filterdiagramm verwaltet die Vollbildwiedergabe. Es tauscht einen Videorenderer für einen spezialisierten Vollbildrenderer aus, streckt ein Fenster eines Renderers auf den Vollbildmodus oder lässt den Renderer die Vollbildwiedergabe direkt implementieren. Für die Interaktion mit Vollbildprotokollen sollte ein Videorenderer immer dann eine [**EC \_ ACTIVATE-Benachrichtigung**](ec-activate.md) senden, wenn das Fenster aktiviert oder deaktiviert wird. Anders ausgedrückt: Für jede WM ACTIVATEAPP-Nachricht, die ein Renderer empfängt, sollte eine **EC \_ ACTIVATE-Benachrichtigung** gesendet \_ werden.

Wenn ein Renderer im Vollbildmodus verwendet wird, verwalten diese Benachrichtigungen das Ein- und Ausschalten dieses Vollbildmodus. Die Fensterdeaktivierung tritt in der Regel auf, wenn ein Benutzer ALT+TAB drückt, um zu einem anderen Fenster zu wechseln, das der DirectShow-Vollbildrenderer als Hinweis verwendet, um zum typischen Renderingmodus zurückzukehren.

Wenn die [**EC \_ ACTIVATE-Benachrichtigung**](ec-activate.md) beim Ausschalten des Vollbildmodus an den Filter Graph Manager gesendet wird, sendet der Filter Graph Manager eine [**EC \_ FULLSCREEN \_ LOST-Benachrichtigung**](ec-fullscreen-lost.md) an die steuernde Anwendung. Die Anwendung kann diese Benachrichtigung verwenden, um z. B. den Zustand einer Vollbildschaltfläche wiederherzustellen. Die **EC ACTIVATE-Benachrichtigungen \_** werden intern von DirectShow verwendet, um Denkhinweise von Videorenderern im Vollbildmodus zu verwalten.

## <a name="summary-of-notifications"></a>Zusammenfassung der Benachrichtigungen

In diesem Abschnitt werden die Filterdiagrammbenachrichtigungen aufgelistet, die ein Renderer senden kann.



| Ereignisbenachrichtigung                                        | Beschreibung                                                                                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EC \_ ACTIVATE**](ec-activate.md)                       | Wird von Videorenderern im Vollbildrenderingmodus für jede empfangene WM \_ ACTIVATEAPP-Nachricht gesendet.                                                                                                  |
| [**EC \_ COMPLETE**](ec-complete.md)                       | Wird von Renderern gesendet, nachdem alle Daten gerendert wurden.                                                                                                                                               |
| [**\_EC-ANZEIGE \_ GEÄNDERT**](ec-display-changed.md)        | Wird von Videorenderern gesendet, wenn sich ein Anzeigeformat ändert.                                                                                                                                            |
| [**EC \_ PALETTE \_ GEÄNDERT**](ec-palette-changed.md)        | Wird gesendet, wenn ein Videorenderer eine Palettenänderung im Stream erkennt.                                                                                                                            |
| [**EC \_ REPAINT**](ec-repaint.md)                         | Wird von angehaltenen oder angehaltenen Videorenderern gesendet, wenn eine WM \_ PAINT-Nachricht empfangen wird und keine Anzuzeigenden Daten vorhanden sind. Dies bewirkt, dass der Filter Graph Manager einen Rahmen generiert, der auf die Anzeige malt. |
| [**EC \_ USERABORT**](ec-userabort.md)                     | Wird von Videorenderern gesendet, um einen Abschluss zu signalisieren, den der Benutzer angefordert hat (z. B. ein Benutzer, der das Videofenster schließt).                                                                               |
| [**\_EC-VIDEOGRÖßE \_ \_ GEÄNDERT**](ec-video-size-changed.md) | Wird von Videorenderern gesendet, wenn eine Änderung der nativen Videogröße erkannt wird.                                                                                                                       |
| [**\_EC-FENSTER \_ ZERSTÖRT**](ec-window-destroyed.md)      | Wird von Videorenderern gesendet, wenn der Filter entfernt oder zerstört wird, sodass Ressourcen, die vom Fensterfokus abhängen, an andere Filter übergeben werden können.                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von Videorenderern](writing-video-renderers.md)
</dt> </dl>

 

 
