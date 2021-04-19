---
description: In diesem Thema wird beschrieben, wie Microsoft Direct3D 11 in einem Microsoft Media Foundation Decoder unterstützt wird.
ms.assetid: 656556AA-0266-4318-9D3C-AED75BD728F6
title: Unterstützung von Direct3D 11 Video Decodierung in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542f7244922dc7947f22e4d33027fdcac1962fe5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355107"
---
# <a name="supporting-direct3d-11-video-decoding-in-media-foundation"></a>Unterstützung von Direct3D 11 Video Decodierung in Media Foundation

In diesem Thema wird beschrieben, wie Microsoft Direct3D 11 in einem Microsoft Media Foundation Decoder unterstützt wird. Insbesondere wird die Kommunikation zwischen dem Decoder und dem Videorenderer beschrieben. In diesem Thema wird nicht beschrieben, wie die Decodierungs Vorgänge implementiert werden.

-   [Übersicht](#overview)
-   [Öffnen eines Geräte Handles](#open-a-device-handle)
-   [Suchen einer decoderkonfiguration](#find-a-decoder-configuration)
-   [Fallback auf Software Decodierung](#fallback-to-software-decoding)
-   [Zuordnen von nicht komprimierten Puffern](#allocating-uncompressed-buffers)
-   [Decodierung](#supporting-direct3d-11-video-decoding-in-media-foundation)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Im restlichen Teil dieses Themas werden die folgenden Begriffe verwendet:

-   **Software Decoder**. Der Software Decoder ist die Media Foundation Transformation (MFT), die komprimierte Videobeispiele empfängt und unkomprimierte Video Frames ausgibt.
-   **Decoder-Gerät**. Das Decoder-Gerät ist die Video Zugriffstaste und wird von dem Grafiktreiber implementiert. Das Decoder-Gerät führt beschleunigte Decodierungs Vorgänge aus.
-   **Pipeline**. Die Pipeline hostet den Software Decoder und übermittelt Puffer an den und aus dem Software Decoder. Abhängig von der Anwendung ist die Pipeline möglicherweise die [Medien Sitzung](media-session.md), der [Quell Leser](source-reader.md)oder der Anwendungscode, der die MFT direkt aufruft.

Um die Decodierung mit Direct3D 11 auszuführen, muss der Software Decoder über einen Zeiger auf ein Direct3D 11-Gerät verfügen. Das Gerät Direct3D 11 wird extern zum Software Decoder erstellt. In einem [Medien Sitzungs](media-session.md) Szenario erstellt der Videorenderer das Gerät Direct3D 11. In einem [Quell Leser](source-reader.md) Szenario erstellt die Anwendung normalerweise das Gerät Direct3D 11.

Der DXGI-Device Manager wird verwendet, um Direct3D 11 zwischen Komponenten gemeinsam zu nutzen. Der DXGI-Device Manager macht die [**IMF dxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Schnittstelle verfügbar. Die Pipeline legt den **imfdxgidevicemanager** -Zeiger auf den Software Decoder fest, indem die [**MFT \_ Message \_ Set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) -Nachricht gesendet wird.

Das folgende Diagramm zeigt die Beziehung zwischen dem Software Decoder, Direct3D 11 und der Pipeline.

![ein Diagramm, in dem der Software Decoder und der DXGI-Geräte-Manager angezeigt werden.](images/d3d11video01.png)

Im folgenden finden Sie die grundlegenden Schritte, die ein Software Decoder ausführen muss, um Direct3D 11 in Media Foundation zu unterstützen:

1.  Öffnen Sie ein Handle für das Gerät Direct3D 11.
2.  Suchen Sie eine Decoder-Konfiguration.
3.  Nicht komprimierte Puffer zuordnen.
4.  Decodieren von Frames.

Diese Schritte werden im weiteren Verlauf dieses Themas ausführlicher beschrieben.

## <a name="open-a-device-handle"></a>Öffnen eines Geräte Handles

Der Decoder-MFT verwendet den DXGI-Geräte-Manager, um ein Handle für das Direct3D 11-Gerät zu erhalten. Führen Sie die folgenden Schritte aus, um das Geräte Handle zu öffnen:

1.  Der Decoder-MFT muss das Attribut [MF \_ sa \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md) mit dem Wert **true** verfügbar machen.
2.  Das topologielader fragt dieses Attribut durch Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)ab. Der Wert **true** gibt an, dass der MFT Direct3D 11 unterstützt.
3.  Das topologielader ruft [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der Meldung [**MFT \_ Message \_ Set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) auf. Der *ulparam* -Parameter ist ein [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger auf den DXGI-Geräte-Manager. Fragen Sie diesen Zeiger nach der [**imbodxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Schnittstelle ab.
4.  Wenn Sie [**imfdxgidebug Manager:: opentovicehandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle) abrufen, erhalten Sie ein Handle für das Gerät Direct3D 11.
5.  Um einen Zeiger auf das Direct3D 11-Gerät abzurufen, nennen Sie [**imfdxgidevicemanager:: getvideoservice**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice). Übergeben Sie das Geräte Handle und den Wert **IID \_ ID3D11Device**. Die-Methode gibt einen Zeiger auf die [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) -Schnittstelle zurück.
6.  Zum Abrufen eines Zeigers auf die Video Zugriffstaste müssen Sie [**imfdxgidevicemanager:: getvideoservice**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice) erneut aufrufen. Übergeben Sie dieses Mal das Geräte Handle und den Wert **IID \_ ID3D11VideoDevice**. Die-Methode gibt einen Zeiger auf die [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) -Schnittstelle zurück.
7.  Aufrufen von [**ID3D11Device:: getimmediatecontext**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-getimmediatecontext) zum Abrufen eines [**Verknüpfung id3d11devicecontext aus**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) -Zeigers.
8.  Ruft [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den [**Verknüpfung id3d11devicecontext aus**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) auf, um einen [**ID3D11VideoContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext) -Zeiger zu erhalten.
9.  Es wird empfohlen, dass Sie den Multithread-Schutz für den Gerätekontext verwenden, um Deadlock-Probleme zu vermeiden, die manchmal auftreten können, wenn Sie [**ID3D11VideoContext:: getdecoderbuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) oder [**ID3D11VideoContext:: releasedecoderbuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer)aufrufen. Um den Multithread-Schutz festzulegen, müssen Sie zuerst [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) abrufen, um einen [**ID3D10Multithread**](/windows/win32/api/d3d10/nn-d3d10-id3d10multithread) -Zeiger zu erhalten. Dann rufe ich [**ID3D10Multithread:: setmultithreadprotected**](/windows/win32/api/d3d10/nf-d3d10-id3d10multithread-setmultithreadprotected)auf und übergebe **true** für *bmtprotect*.

## <a name="find-a-decoder-configuration"></a>Suchen einer decoderkonfiguration

Um die Decodierung auszuführen, muss der Software Decoder eine kompatible Konfiguration finden, die vom Decoder-Gerät unterstützt wird, einschließlich eines renderzielformats. Dieser Schritt erfolgt in der [**IMF Transform::**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) *-Methode wie folgt.

1.  Überprüfen Sie den Eingabe Medientyp. Wenn der Typ abgelehnt wird, überspringen Sie die restlichen Schritte, und geben Sie einen Fehlercode zurück.
2.  Aufrufen von [**ID3D11VideoDevice:: getvideodecoderprofilecount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) , um die Anzahl unterstützter Profile zu erhalten.
3.  Aufrufen von [**ID3D11VideoDevice:: getvideodecoderprofile**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) zum Auflisten der Profile und Abrufen der Profil-GUIDs.
4.  Suchen Sie nach einer Profil-GUID, die dem Videoformat und den Funktionen des Software Decoders entspricht. Ein MPEG-2-Decoder würde z. b. nach **D3D11 \_ Decoder \_ profile \_ MPEG2 \_ mucomp**,**D3D11 \_ Decoder \_ profile \_ MPEG2 \_ IDCT** und **D3D11 \_ Decoder \_ profile \_ MPEG2 \_ VLD** suchen.
5.  Wenn eine passende decoderguid gefunden wird, überprüfen Sie das Ausgabeformat, indem Sie die [**ID3D11VideoDevice:: checkvideodecoderformat**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) -Methode aufrufen. Übergeben Sie die decoderguid und einen **DXGI- \_ Format** Wert, der das renderzielformat angibt.
6.  Suchen Sie als nächstes eine passende Konfiguration für den Decoder.
    1.  Aufrufen von [**ID3D11VideoDevice:: getvideodecoderconfigcount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) zum Abrufen der Anzahl von Decoder-Konfigurationen. Übergeben Sie dieselbe Decoder-Geräte-GUID, zusammen mit einer [**D3D11- \_ Video- \_ decoderstruktur \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc) , die das vorgeschlagene renderzielformat beschreibt.
    2.  Aufrufen von [**ID3D11VideoDevice:: getvideodecoderconfig zum Auflisten der decoderkonfigurationen**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) .

Geben Sie in der [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) -Methode ein unkomprimiertes Videoformat basierend auf dem vorgeschlagenen renderzielformat zurück.

Überprüfen Sie in der [**IMF Transform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) -Methode den Medientyp auf das renderzielformat.

## <a name="fallback-to-software-decoding"></a>Fallback auf Software Decodierung

Die MFT kann möglicherweise keine Konfiguration finden. Der Grafiktreiber unterstützt z. b. möglicherweise nicht die richtigen Funktionen. In diesem Fall muss der MFT wie folgt auf die Software Decodierung zurückgreifen.

1.  Die [**setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) -Methode und die [**setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) -Methode sollten sowohl den **\_ \_ nicht unterstützten MF- \_ D3D- \_ Typ** zurückgeben.
2.  Als Antwort sendet das topologielader die [**MFT \_ Message \_ Set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) -Nachricht mit dem Wert **null** für den *ulparam* -Parameter.
3.  Der MFT gibt seinen Zeiger auf die [**imfdxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Schnittstelle frei.
4.  Der topologielader verhandelt den Medientyp erneut.

An diesem Punkt kann der MFT Software Decodierung verwenden.

## <a name="allocating-uncompressed-buffers"></a>Zuordnen von nicht komprimierten Puffern

Der Decoder ist dafür verantwortlich, Direct3D 11-Texturen zuzuordnen, die als unkomprimierte Video Puffer verwendet werden. Das Attribut für die [ \_ \_ minimale \_ Ausgabe \_ Stichproben \_ Anzahl der MF-Ausgabe](mf-sa-minimum-output-sample-count.md) in den ausgabestreamattributen (siehe [**imftransform:: getoutputstreamtribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)) wird verwendet, um zu bestimmen, wie viele Oberflächen der Decoder dem Videorenderer zuweisen soll, der für Deinterlacing verwendet werden soll. Ein Decoder sollte diesen Wert verwenden, um ihn für einige sinnvolle obere und untere Grenzwerte zu verwenden, z. b. 3-32. Informationen zu progressivem Inhalt finden Sie unter die [ \_ \_ minimale \_ Anzahl von Ausgabe \_ Beispielen \_ \_ für MF SA](mf-sa-minimum-output-sample-count-progressive.md).

Legen Sie in der [**imftransform:: getoutputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) -Methode den **MFT- \_ Ausgabestream \_ \_ enthält \_** ein beispielflag in der [**MFT- \_ Ausgabestream- \_ \_ Informations**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) Struktur fest. Dieses Flag benachrichtigt die Medien Sitzung, dass der MFT seine eigenen Ausgabe Beispiele zuweist. Zum Zuordnen der Ausgabe Beispiele führt der MFT die folgenden Schritte aus:

1.  Erstellen Sie ein 2D-Textur Array durch Aufrufen von [**ID3D11Device:: CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d). Legen Sie **arraySize** in der [**D3D11 \_ TEXTURE2D \_**](/windows/win32/api/d3d11/ns-d3d11-d3d11_texture2d_desc) -Struktur auf die Anzahl der vom Decoder benötigten Oberflächen fest. Dies schließt Folgendes ein:
    -   Oberflächen für Bezugs Frames.
    -   Oberflächen für Deinterlacing (drei Oberflächen).
    -   Oberflächen, die der Decoder für die Pufferung benötigt.

    Die **Bindungsflags (bindflags**) müssen das **D3D11 \_ Bind- \_ decoderflag** und alle Bindungsflags enthalten, die über das [MF \_ sa \_ D3D11 \_ bindflags](mf-sa-d3d11-bindflags.md) -Attribut in den ausgabestreamattributen festgelegt wurden.
2.  Rufen Sie für jede Oberfläche im Textur Array [**ID3D11VideoDevice:: createvideodecoderoutputview**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) auf, um eine Video Decoder-Ausgabe Ansicht zu erstellen. Beim Decodieren werden diese Ausgabe Sichten an die [**ID3D11VideoContext::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) -Methode übermittelt.
3.  Erstellen Sie für jede Oberfläche im Textur Array ein Medien Beispiel wie folgt:
    1.  Erstellen Sie einen DXGI-Medien Puffer, indem Sie die [**mfcreatedxgisurfacebuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer) -Funktion aufrufen. Übergeben Sie den [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) -Zeiger und den Offset für jedes Element im Textur Array. Die-Funktion gibt einen [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Zeiger zurück.
    2.  Erstellen Sie ein leeres Medien Beispiel, indem Sie die [**mfcreatevideosamplefromsurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) -Funktion aufrufen. Legen Sie den Parameter " *punksurface* " auf **null** fest. Die-Funktion gibt einen [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Zeiger zurück.
    3.  Zum Hinzufügen des Medien Puffers zum Beispiel wird [**imfsample:: addbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) aufgerufen.

Sie sollten alle Texturen, die Sie gleichzeitig erstellen, zerstören, anstatt nur einige zu zerstören und die Erinnerung weiterhin zu verwenden.

## <a name="decoding"></a>Decodierung

Um das Decoder-Gerät zu erstellen, rufen Sie [**ID3D11VideoDevice:: createvideodecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder)auf. Die-Methode gibt einen Zeiger auf die [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) -Schnittstelle zurück. Die Decodierung sollte in der [**IMF Transform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode erfolgen. Bei jedem Frame wird [**imfdxgiabvicemanager:: testdevice**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-testdevice) aufgerufen, um die Verfügbarkeit des DXGI zu testen. Wenn sich das Gerät geändert hat, muss der Software Decoder das Decoder-Gerät wie folgt neu erstellen:

1.  Schließen Sie das Geräte handle, indem Sie [**imfdxgidevicemanager:: closedevicehandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-closedevicehandle)aufrufen.
2.  Gibt alle dem früheren Direct3D 11-Gerät zugeordneten Ressourcen frei, einschließlich der [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder)-, [**ID3D11VideoContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext)-, [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d)-und [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) -Schnittstellen.
3.  Öffnen Sie ein neues Geräte handle.
4.  Aushandeln Sie eine neue decoderkonfiguration, wie zuvor in [Suchen einer decoderkonfiguration](#find-a-decoder-configuration)beschrieben. Dieser Schritt ist erforderlich, da sich die Gerätefunktionen möglicherweise geändert haben.
5.  Erstellen Sie ein neues Decoder-Gerät.

Wenn das Geräte Handle gültig ist, funktioniert der Decodierungs Prozess wie folgt:

1.  Sie erhalten eine verfügbare Oberfläche, die derzeit nicht verwendet wird. Anfänglich sind alle Oberflächen verfügbar.
2.  Fragen Sie das Medien Beispiel nach der [**IMF trackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) -Schnittstelle ab.
3.  Aufrufen von [**imftrackedsample:: abtallocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) und Bereitstellen eines Zeigers auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle. (Der Software Decoder muss diese Schnittstelle implementieren.) Wenn der Videorenderer das Beispiel freigibt, wird der Rückruf aufgerufen. Verwenden Sie diesen Rückruf, um nachzuverfolgen, welche Beispiele derzeit verfügbar sind und welche verwendet werden.
4.  Aufrufen von [**ID3D11VideoContext::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe). Übergeben Sie die Zeiger auf die [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) -Schnittstelle für das Decoder-Gerät und die [**ID3D11VideoDecoderOutputView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) -Schnittstelle für die Ausgabe Ansicht.
5.  Führen Sie die folgenden Schritte aus:
    1.  Aufrufen von [**ID3D11VideoContext:: getdecoderbuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) zum Abrufen eines Puffers.
    2.  Füllen Sie den Puffer aus.
    3.  Aufrufen von [**ID3D11VideoContext:: releasedecoderbuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer).
    4.  [**ID3D11VideoContext:: submitdecoderbuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers)aufzurufen. Diese Methode weist das Decoder-Gerät an, die Decodierungs Vorgänge für den Frame auszuführen.
6.  [**ID3D11VideoContext::D ecoderendframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) , um das Ende der Decodierung für den aktuellen Frame zu signalisieren.

Direct3D 11 verwendet die gleichen Datenstrukturen wie DXVA 2,0 für Decodierungs Vorgänge. Für den ursprünglichen Satz von DXVA-Profilen (für h. 261, h. 263 und MPEG-2) werden diese Datenstrukturen in der [Spezifikation DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration)beschrieben.

In jedem Paar von [**decoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) -und [**submitdecoderbuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) -aufrufen können Sie [**getdecoderbuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) mehrmals aufrufen, aber nur einmal für jeden Puffertyp. Wenn Sie den gleichen Puffertyp zweimal verwenden, ohne **submitdecoderbuffer** zu aufrufen, überschreiben Sie die Daten im Puffer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11-Video-APIs](direct3d-11-video-apis.md)
</dt> <dt>

[DirectX-Video Beschleunigung 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
