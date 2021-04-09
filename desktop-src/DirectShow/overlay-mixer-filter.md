---
description: Filter für Überlagerungsmixer
ms.assetid: e80938b7-31f0-467b-a3fa-c4511d14758d
title: Filter für Überlagerungsmixer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26ad8ba8a41a1cdb94eec0f4406c4845f25cda5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859980"
---
# <a name="overlay-mixer-filter"></a>Filter für Überlagerungsmixer

Der Überlagerungs-Mischungs Filter ist ein Videorenderer, der speziell für die DVD-Wiedergabe und Broadcast-Videostreams mit Zeilen 21 Untertiteln entwickelt wurde. Der Überlagerungs-Mixer unterstützt auch Video Port Erweiterungen (vpes) und ermöglicht es, mit Hardware-MPEG-2-Decodern oder analogen TV-Tunern zu arbeiten, die Videos direkt an die Grafikkarte anstatt über den PCI-Bus senden.

> [!Note]  
> Der [Video Mischungs-Renderer 9](video-mixing-renderer-filter-9.md) wird jetzt über den Überlagerungs-Mischungs Filter bevorzugt, außer in VPE-Szenarios.

 

Der Overlay-Mixer verwendet DirectDraw zum Rendern. Es ist eine Überlagerungs Oberfläche auf der Grafikkarte erforderlich. Der primäre Videostream sollte mit PIN 0 verbunden sein. Sekundäre Datenströme (geschlossene Beschriftungs Grafiken oder DVD-Teilbilder) sind mit Pins 1 und höher verbunden. Der Overlay-Mixer blitet die sekundären Datenströme direkt auf das primäre untergeordnete Element. Sie werden nicht gemischt oder Alpha gemischt.

Der Overlay-Mixer verwendet den Videorenderer für die Fensterverwaltung. Der Videorenderer stellt eine Verbindung mit dem Auslagerungs-PIN des Überlagerungs-

Dieser Filter wird automatisch dem Filter Diagramm hinzugefügt, wenn Anwendungen die [**idvdgraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) -Schnittstelle und die [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle zum Erstellen des Diagramms verwenden. Der Diagramm-Manager des Filters fügt dem Diagramm nicht automatisch den Overlay-Mixer hinzu.

> [!Note]  
> In der folgenden Tabelle sind die für die Eingabe-PIN 0 zulässigen Medien Teil Typen Hardware abhängig. Der Überlagerungs Mixer kann nicht bestimmen, ob ein bestimmter Untertyp unterstützt wird, bis die DirectDraw-Oberfläche erstellt wird. Daher kann ein upstreamfilter nur dann ermitteln, ob ein Untertyp unterstützt wird, indem versucht wird, eine Verbindung mit diesem Untertyp herzustellen.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>Iamoverlayfx</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>iamvideodecimationproperties</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ibasefilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>iddrawexclmodevideo</strong></a>, <a href="ikspropertyset.md"><strong>ikspropertyset</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>imixerocx</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>iqualprop</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>ivpnotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td>Haupttyp: MEDIATYPE_Video<br/> Untertypen<br/>
<ul>
<li>MEDIASUBTYPE_Overlay (nur Pin 0)</li>
<li>DirectDraw-YUV-Formate (nur Pin 0)</li>
<li>DirectDraw-Video Beschleunigungs Formate (nur Pin 0)</li>
<li>DirectDraw RGB-Formate (alle Eingabe Pins)</li>
</ul>
Format Typen:<br/>
<ul>
<li>Format_VIDEOINFO</li>
<li>Format_VIDEOINFO2</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>Iamvideoaccelerator</strong></a>, <a href="ikspin.md"><strong>ikspin</strong></a>, <a href="ikspropertyset.md"><strong>ikspropertyset</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>imixerpinconfig</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (nur Pin 0), <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>ipinconnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>ivpnotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td>MEDIATYPE_Video MEDIASUBTYPE_Overlay</td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_OverlayMixer</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td>Keine Eigenschaften Seite.</td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Verdienst</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a>Bemerkungen

Der Overlay-Mixer verwendet die Zielfarbe, um Video Oberflächen mit Überlagerungen zu kombinieren. Es blierte den Farbschlüssel und das sekundäre Video auf die primäre Oberfläche und sendet das primäre Video an die über Lagerungs Oberfläche. Die Grafikkarte kombiniert dann die beiden Oberflächen in ihren Frame Puffer.

Um zu testen, ob der Grafiktreiber die Hardware Überlagerung unterstützt, müssen Sie **IDirectDraw7:: getcaps** aufrufen. Wenn das Feld **dwmaxvisibleoverlays** in der **ddcaps** -Struktur größer als 0 (null) ist, unterstützt der Treiber die Hardware Überlagerung.

Anwendungen können einige Verhaltensweisen auf dem Überlagerungs Mixer über die [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) -Schnittstelle steuern. Spieleentwickler können den Overlay-Mixer zum Anzeigen von Videos im exklusiven DirectDraw-Modus verwenden, wie weiter unten in diesem Abschnitt beschrieben. Der [Video Mischungs Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) bietet jetzt bessere Unterstützung für Videos in spielen. Weitere Informationen finden Sie unter [using the Video mischungsrenderer](using-the-video-mixing-renderer.md).

Die folgenden Informationen werden für den Vorteil der Filter Entwickler und Spielentwickler bereitgestellt, die den Overlay-Mixer im exklusiven DirectDraw-Modus verwenden möchten.

**Interne Überlagerungs Mixer-Vorgänge**

Der Overlay-Mixer macht eine Eingabe-PIN für jeden eingehenden Stream verfügbar. In der Regel gibt es drei Eingabe Pins: Pin 0 für Videodaten und Pins 1 und 2 für die Daten in Zeile 21 und DVD-subbild. Intern erstellt der Overlay-Mixer ein DirectDraw-Objekt mit einer primären Oberfläche, die den gesamten Desktop umfasst, sowie eine Überlagerungs Oberfläche, deren Rechteck durch die Größe des Videodaten Stroms auf Pin 0 definiert wird. Wenn der Decoder keinen Farbschlüssel angibt, verwendet der Überlagerungs Mixer Standard Farbtasten: dunkelgrau für neuere Grafikkarten und Magenta für ältere 256-farbige Karten.

> [!Note]  
> Die Ergebnisse sind nicht definiert, wenn der Decoder zwei sekundäre Videostreams gleichzeitig an derselben Stelle auf der über Lagerungs Oberfläche bereitstellt. (Dies tritt manchmal bei DVDs auf, die subbild-und Zeile 21-Streams enthalten.) Das Video kann Flimmern oder nur einen der Streams anzeigen.

 

Unter Windows Vista oder höher deaktiviert der Überlagerungs-Mixer die Komposition von Desktopfenster-Manager (DWM), wenn der Anzeigetreiber die Hardware Überlagerung unterstützt. Anwendungen sollten die Verwendung des Überlagerungs-Mischungs Filters vermeiden. Verwenden Sie stattdessen VMR-9 oder den erweiterten Videorenderer (EVR).

**Upstreamverbindung mit dem Video Decoder**

In der Regel stellen die Eingabe Pins des Overlay-Mixers eine Verbindung mit einem upstreamvideodecoder her Der primäre Videostream muss eine Verbindung mit der PIN 0 herstellen. Die Zeilen 21-oder subbildstreams stellen eine Verbindung mit PIN 1 oder höher her. Wenn der Decoder ein Software Decoder ist, der die Host-CPU exklusiv verwendet, ist die Verbindung zwischen dem Decoder und der PIN 0 eine [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Verbindung. Wenn der Decoder die Hardwarebeschleunigung verwendet, muss für die Verbindung mit PIN 0 das Inferface [**iamvideoaccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) verwendet werden. Diese beiden Verbindungstypen schließen sich gegenseitig aus.

Wenn der Decoder direkt auf die Überlagerungs Oberfläche verweist, sollte er die [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) -Schnittstelle für PIN 0 verwenden und die [**ioverlaynotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify) -Schnittstelle implementieren.

Filter, bei denen ein Hardware Decoder umschlossen und über einen Videoport eine Verbindung mit dem Overlay-Mixer hergestellt wird, müssen die [**ivpconfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) -Schnittstelle implementieren Der Overlay-Mixer implementiert die [**ivpnotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) -Schnittstelle. Diese beiden Schnittstellen ermöglichen es dem Decoder, die erforderlichen Überlagerungs Oberflächen anzugeben, und ermöglichen dem Überlagerungs-Mixer, den Decoder über den Speicherort dieser Oberflächen im Videospeicher zu informieren.

Der Overlay-Mixer stellt außerdem sicher, dass das Video Rechteck ordnungsgemäß skaliert wird. Die Video Erfassung umfasst bestimmte Probleme in Bezug auf das Skalieren des Vorschaubilds und das Erfassen von verschachtelten Video Frames. Wenn Sie einen Filter oder einen WDM-Treiber für ein Hardware Video Erfassungsgerät entwickeln, finden Sie weitere Informationen zu diesen Themen in den Referenzseiten [**ivpconfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) und [**ivpnotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) .

Der Overlay-Mixer wird nicht in 1394-oder USB-Aufzeichnungs Szenarien verwendet. Sie wird bei der Video Erfassung über den PCI-Bus verwendet.

**Downstream-Verbindung mit dem Videorenderer**

Der Overlay-Mixer verfügt über eine Ausgabe-PIN, die eine Verbindung mit dem [Videorenderer](video-renderer-filter.md) -Filter herstellt. Der Videorenderer in diesem Fall renderdas Video nicht. das Videofenster wird einfach verwaltet.

Die PIN-Verbindung verwendet anstelle der [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle die [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) -Schnittstelle. Der Videorenderer übergibt seinen Fenster Handle über den Überlagerungs Mixer an DirectDraw, das das Rechteck Clipping verwaltet. Anwendungen können den Videorenderer über die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -und [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2) -Schnittstellen im Filter Graph-Manager steuern.

**Exklusiver DirectDraw-Modus**

Der exklusive DirectDraw-Modus des Overlay-Mischers ermöglicht spielen, Videos in einem Teil des Bildschirms anzuzeigen. In diesem Modus rendert der Überlagerungs-Mixer das Video direkt in eine von der Spiel Anwendung erstellte DirectDraw-Oberfläche und nicht in ein Fenster, das vom Videorenderer bereitgestellt wird. Dies ermöglicht spielen, den Farbschlüssel zu steuern. Der Overlay-Mixer macht nur eine Eingabe-PIN im exklusiven DirectDraw-Modus verfügbar. Dies bedeutet, dass in diesem Modus keine Mischung aus Zeile 21 oder DVD-subbild ausgeführt werden kann.

Um den Overlay-Mixer im exklusiven DirectDraw-Modus zu verwenden, erstellen Sie eine Instanz des Overlay-Mischers und Fragen Sie diese nach der [**iddrawexclmodevideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo) -Schnittstelle ab, bevor Sie das Filter Diagramm erstellen. Anschließend können Sie [**iddrawexclmodevideo:: setddrawsurface**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) aufrufen, um die DirectDraw-Oberfläche für das Rendering anzugeben. Eine wesentliche Einschränkung dieses Modus besteht darin, dass das Spiel keinen Zugriff auf die eigentlichen Video Bits erhält. Wenn Sie **iddrawexclmodevideo** verwenden, wird die primäre Oberfläche von der Anwendung erstellt, und der Überlagerungs-Mixer erstellt die Überlagerungs Oberfläche.

Sie können auch den exklusiven DirectDraw-Modus verwenden, um fensterlose Rendering auszuführen – z. b. auf einer Webseite – aber dies wird nicht empfohlen, da der Überlagerungs-Mixer in diesem Modus keine Vermischung ausführt. Dies bedeutet, dass keine Daten der Zeile 21 oder eines teilbilds angezeigt werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




