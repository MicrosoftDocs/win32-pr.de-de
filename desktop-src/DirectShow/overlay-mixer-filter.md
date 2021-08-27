---
description: Filter für Überlagerungsmixer
ms.assetid: e80938b7-31f0-467b-a3fa-c4511d14758d
title: Filter für Überlagerungsmixer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475726607f282ce4b7885ec6c5aea562c0380cb0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476986"
---
# <a name="overlay-mixer-filter"></a>Filter für Überlagerungsmixer

Der Filter Overlay Mixer ist ein Videorenderer, der speziell für die DVD-Wiedergabe und übertragung von Videostreams mit Untertiteln in Zeile 21 entwickelt wurde. Die Overlay-Mixer unterstützt auch Videoporterweiterungen (Video Port Extensions, VPEs), sodass sie mit MPEG-2-Hardwaredecodern oder analogen TV-Tunern arbeiten kann, die Videos direkt an die Grafikkarte senden, anstatt über den PCI-Bus.

> [!Note]  
> Der [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) wird jetzt dem Filter Overlay Mixer bevorzugt, mit Ausnahme von VPE-Szenarien.

 

Der Overlay-Mixer verwendet DirectDraw für das Rendering. Hierfür ist eine Überlagerungsoberfläche auf der Grafikkarte erforderlich. Der primäre Videostream sollte mit Pin 0 verbunden sein. Sekundäre Streams (Untertitelgrafiken oder DVD-Unterbilder) sind mit Pins 1 und höher verbunden. Der Overlay-Mixer blitt die sekundären Streams direkt auf die primäre Oberfläche. sie werden nicht gemischt oder alphanal gemischt.

Der Overlay-Mixer verwendet den Videorenderer für die Fensterverwaltung. Der Videorenderer stellt eine Verbindung mit dem Ausgabepin des Overlay-Mixer her.

Dieser Filter wird dem Filterdiagramm automatisch hinzugefügt, wenn Anwendungen die Schnittstellen [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) und [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) verwenden, um das Diagramm zu erstellen. Der Filter Graph Manager fügt dem Diagramm nicht automatisch die Overlay-Mixer hinzu.

> [!Note]  
> In der folgenden Tabelle sind die Medienuntertypen, die auf Eingabepin 0 akzeptiert werden, hardwareabhängig. Der Overlay-Mixer kann erst bestimmen, ob ein bestimmter Untertyp unterstützt wird, wenn die DirectDraw-Oberfläche erstellt wird. Daher kann ein Upstreamfilter nur ermitteln, ob ein Untertyp unterstützt wird, wenn versucht wird, eine Verbindung mit diesem Untertyp herzustellen.

 




| | | Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> | | Eingabepinmedientypen | Haupttyp: MEDIATYPE_Video<br /> Untertypen:<br /><ul><li>MEDIASUBTYPE_Overlay (nur Pin 0)</li><li>DirectDraw YUV-Formate (nur Pin 0)</li><li>DirectDraw Video Acceleration-Formate (nur Pin 0)</li><li>DirectDraw RGB-Formate (alle Eingabepins)</li></ul>Formattypen:<br /><ul><li>Format_VIDEOINFO</li><li>Format_VIDEOINFO2</li></ul> | | Eingabepinschnittstellen | <a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="ikspin.md"><strong>IKsPin</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>IMixerPinConfig</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (nur Pin 0), <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> | | Ausgabepinmedientypen | MEDIATYPE_Video, MEDIASUBTYPE_Overlay | | Ausgabepinschnittstellen | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtern von CLSID-| CLSID_OverlayMixer | | CLSID-| der Eigenschaftenseite Keine Eigenschaftenseite. | | Ausführbare | qdvd.dll | | <a href="merit.md">|</a> MERIT_DO_NOT_USE | | <a href="filter-categories.md">| "Filterkategorie"</a> CLSID_LegacyAmFilterCategory | 




 

### <a name="remarks"></a>Hinweise

Der Overlay-Mixer verwendet die Zielfarbtaste, um Videooberflächen mit Überlagerungen zu mischen. Es blitt den Farbschlüssel und das sekundäre Video auf die primäre Oberfläche und sendet das primäre Video an die Überlagerungsoberfläche. Die Grafikkarte zusammengesetzt dann die beiden Oberflächen in ihren Rahmenpuffer.

Um zu testen, ob der Grafiktreiber Hardwareüberlagerungen unterstützt, rufen **Sie IDirectDraw7::GetCaps auf.** Wenn das **DwMaxVisibleOverlays-Feld** in der **DDCAPS-Struktur** größer als 0 (null) ist, unterstützt der Treiber die Hardwareüberlagerung.

Anwendungen können einige Verhaltensweisen auf dem Overlay-Mixer über die [**IMixerPinConfig2-Schnittstelle**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) steuern. Spieleentwickler können das Overlay Mixer verwenden, um Videos im exklusiven DirectDraw-Modus anzuzeigen, wie weiter unten in diesem Abschnitt beschrieben. Der [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) bietet jetzt jedoch eine bessere Unterstützung für Videos in Spielen. Weitere Informationen finden Sie unter [Verwenden des VideoMischungsrenderers.](using-the-video-mixing-renderer.md)

Die folgenden Informationen dienen dem Vorteil von Filterentwicklern und Spieleentwicklern, die die Overlay-Mixer im exklusiven DirectDraw-Modus verwenden möchten.

**Überlagern Mixer interne Vorgänge**

Der Overlay-Mixer macht einen Eingabepin für jeden eingehenden Datenstrom verfügbar. In der Regel gibt es drei Eingabepins: Pin 0 für Videodaten und Stecknadeln 1 und 2 für Daten aus Zeile 21 und DVD-Unterbilddaten. Intern erstellt das Overlay-Mixer ein DirectDraw-Objekt mit einer primären Oberfläche, die den gesamten Desktop umfasst, sowie eine Überlagerungsoberfläche, deren Rechteck durch die Größe des Videostreams auf Pin 0 definiert ist. Wenn der Decoder keinen Farbschlüssel angibt, verwendet der Overlay-Mixer Standardfarbtasten: dunkelgrau für neuere Grafikkarten und Magenta für ältere Karten mit 256 Farben.

> [!Note]  
> Die Ergebnisse sind nicht definiert, wenn der Decoder zwei sekundäre Videostreams gleichzeitig an derselben Stelle auf der Überlagerungsoberfläche übermittelt. (Dies tritt manchmal bei DVDs auf, die Unterbild- und Zeilen-21-Streams enthalten.) Das Video kann flackern oder nur einen der Streams anzeigen.

 

Auf Windows Vista oder höher deaktiviert die Overlay-Mixer Desktopfenster-Manager (DWM), wenn der Anzeigetreiber Hardwareüberlagerungen unterstützt. Anwendungen sollten die Verwendung des Filters Overlay Mixer vermeiden. Verwenden Sie stattdessen VMR-9 oder enhanced video renderer (EVR).

**Upstreamverbindung mit dem Videodecoder**

In der Regel stellen die Eingabepins des Overlay-Mixer eine Verbindung mit einem Upstreamvideodecoder her. Der primäre Videostream muss eine Verbindung mit dem Pin 0 herstellen. Die Datenströme der Zeile 21 oder der Unterbilddatenströme stellen eine Verbindung mit Pin 1 oder höher her. Wenn der Decoder ein Softwaredecoder ist, der die Host-CPU ausschließlich verwendet, ist die Verbindung zwischen dem Decoder und dem Pin 0 eine [**IMemInputPin-Verbindung.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) Wenn der Decoder die Hardwarebeschleunigung verwendet, muss die Verbindung mit Pin 0 die [**IAMVideoAccelerator-Rückschlussfläche**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) verwenden. Diese beiden Verbindungstypen schließen sich gegenseitig aus.

Wenn der Decoder direkt auf die Überlagerungsoberfläche zeichnet, sollte er die [**IOverlay-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) an Pin 0 verwenden und die [**IOverlayNotify-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify) implementieren.

Filter, die einen Hardwaredecoder umschließen und über einen Videoport eine Verbindung mit der Overlay-Mixer herstellen, müssen die [**IVPConfig-Schnittstelle**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) implementieren. Der Overlay-Mixer implementiert die [**IVPNotify-Schnittstelle.**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) Diese beiden Schnittstellen ermöglichen es dem Decoder, die benötigten Überlagerungsoberflächen anzugeben, und sie ermöglichen dem Overlay-Mixer, den Decoder über die Position dieser Oberflächen im Videospeicher zu informieren.

Das Overlay Mixer stellt außerdem sicher, dass das Videorechteck ordnungsgemäß skaliert wird. Die Videoaufnahme umfasst bestimmte Probleme in Bezug auf die Skalierung des Vorschaubilds und die Erfassung verschachtelter Videoframes. Wenn Sie einen Filter- oder WDM-Treiber für ein Hardware-Videoaufnahmegerät entwickeln, finden Sie weitere Informationen zu diesen Themen auf den Referenzseiten [**zu IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) und [**IVPNotify.**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify)

Die Overlay-Mixer wird in 1394- oder USB-Erfassungsszenarien nicht verwendet. Sie wird in der Videoaufzeichnung über den PCI-Bus verwendet.

**Downstreamverbindung mit dem Videorenderer**

Der Overlay-Mixer verfügt über einen Ausgabepin, der eine Verbindung mit dem [Videorendererfilter](video-renderer-filter.md) herstellt. Der Videorenderer rendert das Video in diesem Fall nicht. es verwaltet einfach das Videofenster.

Die Pinverbindung verwendet die [**IOverlay-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) anstelle der [**IMemInputPin-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) Der Videorenderer übergibt sein Fensterhandle durch die Überlagerungs-Mixer an DirectDraw, die die Rechteckausschneidung verwaltet. Anwendungen können den Videorenderer über die Schnittstellen [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) und [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2) im Filter Graph Manager steuern.

**Exklusiver DirectDraw-Modus**

Im exklusiven DirectDraw-Modus der Overlay Mixer können Spiele Video auf einem Teil des Bildschirms anzeigen. In diesem Modus rendert das Overlay-Mixer das Video direkt auf einer DirectDraw-Oberfläche, die von der Spielanwendung erstellt wurde, und nicht in einem Fenster, das vom Videorenderer bereitgestellt wird. Dadurch können Spiele den Farbschlüssel steuern. Der Overlay-Mixer macht nur einen Eingabepin im exklusiven DirectDraw-Modus verfügbar. Dies bedeutet, dass in diesem Modus keine Mischung aus Line 21- oder DVD-Unterbild durchgeführt werden kann.

Um die Overlay-Mixer im exklusiven DirectDraw-Modus zu verwenden, erstellen Sie eine Instanz des Overlay-Mixer und fragen sie nach der [**IDDrawExclModeVideo-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo) ab, bevor Sie den Filtergraphen erstellen. Rufen Sie dann [**IDDrawExclModeVideo::SetDDrawSurface**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) auf, um die DirectDraw-Oberfläche für das Rendering anzugeben. Eine wesentliche Einschränkung dieses Modus ist, dass das Spiel keinen Zugriff auf die tatsächlichen Videobits erhält. Wenn Sie **IDDrawExclModeVideo** verwenden, erstellt Ihre Anwendung die primäre Oberfläche und die Overlay-Mixer die Überlagerungsoberfläche.

Sie können auch den exklusiven DirectDraw-Modus verwenden, um fensterloses Rendering durchzuführen , z. B. auf einer Webseite. Dies wird jedoch nicht empfohlen, da das Overlay-Mixer in diesem Modus keine Mischung durchführt. Dies bedeutet, dass keine Zeile 21- oder Unterbilddaten angezeigt werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




