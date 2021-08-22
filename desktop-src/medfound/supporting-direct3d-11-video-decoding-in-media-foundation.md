---
description: In diesem Thema wird beschrieben, wie Microsoft Direct3D 11 in einem Microsoft Media Foundation Decoder unterstützt wird.
ms.assetid: 656556AA-0266-4318-9D3C-AED75BD728F6
title: Unterstützung der Direct3D 11-Videodecodierung in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95a1d1bc1dd9987fe59fe807e56aa9af1ea4ad597b72c077906483d623e11e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972883"
---
# <a name="supporting-direct3d-11-video-decoding-in-media-foundation"></a>Unterstützung der Direct3D 11-Videodecodierung in Media Foundation

In diesem Thema wird beschrieben, wie Microsoft Direct3D 11 in einem Microsoft Media Foundation Decoder unterstützt wird. Insbesondere wird die Kommunikation zwischen dem Decoder und dem Videorenderer beschrieben. In diesem Thema wird nicht beschrieben, wie die Decodierungsvorgänge implementiert werden.

-   [Übersicht](#overview)
-   [Öffnen eines Gerätehandle](#open-a-device-handle)
-   [Suchen einer Decoderkonfiguration](#find-a-decoder-configuration)
-   [Fallback zur Softwaredecodierung](#fallback-to-software-decoding)
-   [Zuordnen von nicht komprimierten Puffern](#allocating-uncompressed-buffers)
-   [Decodierung](#supporting-direct3d-11-video-decoding-in-media-foundation)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Im weiteren Verlauf dieses Themas werden die folgenden Begriffe verwendet:

-   **Softwaredecoder**. Der Softwaredecoder ist die Media Foundation-Transformation (MFT), die komprimierte Videobeispiele empfängt und unkomprimierte Videoframes ausgibt.
-   **Decodergerät**. Das Decodergerät ist die Videobeschleunigung und wird vom Grafiktreiber implementiert. Das Decodergerät führt beschleunigte Decodierungsvorgänge aus.
-   **Pipeline**. Die Pipeline hostet den Softwaredecoder und übermittelt Puffer an den und aus dem Softwaredecoder. Je nach Anwendung kann die Pipeline die [Mediensitzung,](media-session.md)der [Quellleser](source-reader.md)oder Anwendungscode sein, der direkt den MFT aufruft.

Um die Decodierung mit Direct3D 11 durchzuführen, muss der Softwaredecoder einen Zeiger auf ein Direct3D 11-Gerät haben. Das Direct3D 11-Gerät wird extern für den Softwaredecoder erstellt. In einem [Mediensitzungsszenario](media-session.md) erstellt der Videorenderer das Direct3D 11-Gerät. In einem [Quellleseszenario](source-reader.md) erstellt die Anwendung in der Regel das Direct3D 11-Gerät.

Die DXGI-Geräte-Manager wird verwendet, um Direct3D 11 zwischen Komponenten freizugeben. Der DXGI-Geräte-Manager macht die [**INTERFACESDXGIDeviceManager-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) verfügbar. Die Pipeline legt den **POINTERXGIDeviceManager** auf den Softwaredecoder fest, indem die [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER-Nachricht**](mft-message-set-d3d-manager.md) gesendet wird.

Das folgende Diagramm zeigt die Beziehung zwischen dem Softwaredecoder, Direct3D 11 und der Pipeline.

![Ein Diagramm, das den Softwaredecoder und den Dxgi-Geräte-Manager zeigt.](images/d3d11video01.png)

Hier sind die grundlegenden Schritte, die ein Softwaredecoder ausführen muss, um Direct3D 11 in Media Foundation zu unterstützen:

1.  Öffnen Sie ein Handle für das Direct3D 11-Gerät.
2.  Suchen sie nach einer Decoderkonfiguration.
3.  Zuordnen von nicht komprimierten Puffern.
4.  Decodieren von Frames.

Diese Schritte werden im weiteren Verlauf dieses Themas ausführlicher beschrieben.

## <a name="open-a-device-handle"></a>Öffnen eines Gerätehandle

Der Decoder-MFT verwendet den DXGI-Geräte-Manager, um ein Handle für das Direct3D 11-Gerät abzurufen. Führen Sie die folgenden Schritte aus, um das Gerätehandle zu öffnen:

1.  Der Decoder-MFT muss das [MF \_ SA \_ D3D11 \_ AWARE-Attribut](mf-sa-d3d11-aware.md) mit dem Wert **TRUE** verfügbar machen.
2.  Das Topologieladeprogramm fragt dieses Attribut ab, indem [**ESSTRANSFORM::GetAttributes aufruft.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Der Wert **TRUE** gibt an, dass der MFT Direct3D 11 unterstützt.
3.  Das Topologieladeprogramm ruft [**ÜBERTRANSFORM::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER-Nachricht**](mft-message-set-d3d-manager.md) auf. Der *ulParam-Parameter* ist ein [**IUnknown-Zeiger**](/windows/win32/api/unknwn/nn-unknwn-iunknown) auf den DXGI-Geräte-Manager. Fragen Sie diesen Zeiger nach der [**INTERFACESDXGIDeviceManager-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) ab.
4.  Rufen Sie [**DIE DATEI 3DXGIDeviceManager::OpenDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle) auf, um ein Handle für das Direct3D 11-Gerät abzurufen.
5.  Um einen Zeiger auf das Direct3D 11-Gerät zu erhalten, rufen [**Sie DIE DATEI ÜBERDXGIDeviceManager::GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice)auf. Übergeben Sie das Gerätehandle und den Wert **IID \_ ID3D11Device**. Die -Methode gibt einen Zeiger auf die [**ID3D11Device-Schnittstelle**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) zurück.
6.  Um einen Zeiger auf die Videobeschleunigung zu erhalten, rufen Sie NOCH mal [**ÜBERDXGIDeviceManager::GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice) auf. Übergeben Sie dieses Mal das Gerätehandle und den Wert **IID \_ ID3D11VideoDevice**. Die -Methode gibt einen Zeiger auf die [**ID3D11VideoDevice-Schnittstelle**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) zurück.
7.  Rufen Sie [**ID3D11Device::GetImmediateContext**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-getimmediatecontext) auf, um einen [**ID3D11DeviceContext-Zeiger**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) abzurufen.
8.  Rufen Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für [**id3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) auf, um einen [**ID3D11VideoContext-Zeiger**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext) abzurufen.
9.  Es wird empfohlen, den Multithreadschutz im Gerätekontext zu verwenden, um Deadlockprobleme zu vermeiden, die manchmal auftreten können, wenn Sie [**ID3D11VideoContext::GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) oder [**ID3D11VideoContext::ReleaseDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer)aufrufen. Rufen Sie zum Festlegen des Multithreadschutzes zunächst [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) auf, um einen [**ID3D10Multithread-Zeiger**](/windows/win32/api/d3d10/nn-d3d10-id3d10multithread) abzurufen. Rufen Sie dann [**ID3D10Multithread::SetMultithreadProtected**](/windows/win32/api/d3d10/nf-d3d10-id3d10multithread-setmultithreadprotected)auf, und übergeben Sie **true** für *bMTProtect.*

## <a name="find-a-decoder-configuration"></a>Suchen einer Decoderkonfiguration

Um die Decodierung durchzuführen, muss der Softwaredecoder eine kompatible Konfiguration finden, die vom Decodergerät unterstützt wird, einschließlich eines Renderzielformats. Dieser Schritt erfolgt innerhalb der [**METHODE VONTRANSFORM::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) wie folgt.

1.  Überprüfen Sie den Eingabemedientyp. Wenn der Typ abgelehnt wird, überspringen Sie die verbleibenden Schritte, und geben Sie einen Fehlercode zurück.
2.  Rufen Sie [**ID3D11VideoDevice::GetVideoDecoderProfileCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofilecount) auf, um die Anzahl der unterstützten Profile abzurufen.
3.  Rufen Sie [**ID3D11VideoDevice::GetVideoDecoderProfile**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderprofile) auf, um die Profile aufzuzählen und die Profil-GUIDs abzurufen.
4.  Suchen Sie nach einer Profil-GUID, die dem Videoformat und den Funktionen des Softwaredecoders entspricht. Beispielsweise würde ein MPEG-2-Decoder nach **D3D11 \_ DECODER \_ PROFILE \_ MPEG2 \_ MOCOMP,****D3D11 \_ DECODER PROFILE \_ \_ MPEG2 \_ IDCT** und **D3D11 \_ DECODER PROFILE \_ \_ MPEG2 \_ VLD** suchen.
5.  Wenn eine geeignete Decoder-GUID gefunden wird, überprüfen Sie das Ausgabeformat, indem Sie die [**ID3D11VideoDevice::CheckVideoDecoderFormat-Methode**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkvideodecoderformat) aufrufen. Übergeben Sie die Decoder-GUID und einen **DXGI \_ FORMAT-Wert,** der das Renderzielformat angibt.
6.  Suchen Sie als Nächstes eine geeignete Konfiguration für den Decoder.
    1.  Rufen Sie [**ID3D11VideoDevice::GetVideoDecoderConfigCount**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfigcount) auf, um die Anzahl der Decoderkonfigurationen abzurufen. Übergeben Sie die gleiche Decodergeräte-GUID zusammen mit einer [**D3D11 \_ VIDEO \_ DECODER \_ DESC-Struktur,**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc) die das vorgeschlagene Renderzielformat beschreibt.
    2.  Rufen Sie [**ID3D11VideoDevice::GetVideoDecoderConfig**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getvideodecoderconfig) auf, um die Decoderkonfigurationen aufzuzählen.

Geben Sie in der [**FORMATSTransform::GetOutputAvailableType-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) ein nicht komprimiertes Videoformat zurück, das auf dem vorgeschlagenen Renderzielformat basiert.

Überprüfen Sie in der [**FORMATSTransform::SetOutputType-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) den Medientyp anhand des Renderzielformats.

## <a name="fallback-to-software-decoding"></a>Fallback zur Softwaredecodierung

Der MFT kann möglicherweise keine Konfiguration finden. Beispielsweise unterstützt der Grafiktreiber möglicherweise nicht die richtigen Funktionen. In diesem Fall muss der MFT wie folgt auf die Softwaredecodierung zurückgreifen.

1.  Die [**Methoden SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) und [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) sollten beide **MF E \_ \_ UNSUPPORTED \_ D3D \_ TYPE** zurückgeben.
2.  Als Reaktion sendet das Topologieladeprogramm die [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER-Nachricht**](mft-message-set-d3d-manager.md) mit dem Wert **NULL** für den *ulParam-Parameter.*
3.  Der MFT gibt seinen Zeiger auf die [**INTERFACESDXGIDeviceManager-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) frei.
4.  Mit dem Topologieladeprogramm wird der Medientyp neu ausgehandelt.

An diesem Punkt kann der MFT die Softwaredecodierung verwenden.

## <a name="allocating-uncompressed-buffers"></a>Zuordnen von nicht komprimierten Puffern

Der Decoder ist für die Zuweisung von Direct3D 11-Texturen für die Verwendung als unkomprimierte Videopuffer verantwortlich. Mit dem [MF SA MINIMUM OUTPUT SAMPLE \_ \_ \_ \_ \_ COUNT-Attribut](mf-sa-minimum-output-sample-count.md) in den Ausgabestreamattributen (siehe [**ÜBERTRANSFORM::GetOutputStreamAttributes)**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)wird bestimmt, wie viele Oberflächen der Decoder dem Videorenderer für die Deinterlacing zuordnen soll. Ein Decoder sollte diesen Wert verwenden, um ihn für einige sinnvolle Ober- und Untergrenzen zu begrenzen, z.B. 3-32. Informationen zu progressivem Inhalt finden Sie unter [MF SA MINIMUM OUTPUT SAMPLE COUNT \_ \_ \_ \_ \_ \_ PROGRESSIVE](mf-sa-minimum-output-sample-count-progressive.md).

Legen Sie in der [**METHODE ÜBERTRANSFORM::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) das **Flag MFT OUTPUT STREAM PROVIDES \_ \_ \_ \_ SAMPLES** in der [**MFT OUTPUT STREAM \_ \_ \_ INFO-Struktur**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) fest. Dieses Flag benachrichtigt die Mediensitzung, dass der MFT eigene Ausgabebeispiele zuordnet. Um die Ausgabebeispiele zuzuordnen, führt der MFT die folgenden Schritte aus:

1.  Erstellen Sie ein 2D-Texturarray, indem Sie [**ID3D11Device::CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d)aufrufen. Legen Sie in der [**D3D11 \_ TEXTURE2D \_ DESC-Struktur**](/windows/win32/api/d3d11/ns-d3d11-d3d11_texture2d_desc) **ArraySize** auf die Anzahl von Oberflächen fest, die der Decoder benötigt. Dies schließt Folgendes ein:
    -   Oberflächen für Verweisframes.
    -   Oberflächen für das Deinterlacing (drei Oberflächen).
    -   Oberflächen, die der Decoder für die Pufferung benötigt.

    Die Bindungsflags (**BindFlags**) sollten das **D3D11 \_ BIND \_ DECODER-Flag** und alle Bindungsflags enthalten, die über das [MF SA \_ \_ D3D11 \_ BINDFLAGS-Attribut](mf-sa-d3d11-bindflags.md) in den Ausgabestreamattributen festgelegt werden.
2.  Rufen Sie für jede Oberfläche im Texturarray [**ID3D11VideoDevice::CreateVideoDecoderOutputView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview) auf, um eine Videodecoder-Ausgabeansicht zu erstellen. Während der Decodierung werden diese Ausgabeansichten an die [**ID3D11VideoContext::D ecoderBeginFrame-Methode**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) übergeben.
3.  Erstellen Sie für jede Oberfläche im Texturarray wie folgt ein Medienbeispiel:
    1.  Erstellen Sie einen DXGI-Medienpuffer, indem Sie die [**MFCreateDXGISurfaceBuffer-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer) aufrufen. Übergeben Sie den [**ID3D11Texture2D-Zeiger**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) und den Offset für jedes Element im Texturarray. Die Funktion gibt einen [**POINTERMediaBuffer-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) zurück.
    2.  Erstellen Sie ein leeres Medienbeispiel, indem Sie die [**MFCreateVideoSampleFromSurface-Funktion**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) aufrufen. Legen Sie den *pUnkSurface-Parameter* auf **NULL** fest. Die Funktion gibt einen [**POINTERSample-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) zurück.
    3.  Rufen Sie [**DEN AUFRUF VON SAMPLESample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) auf, um dem Beispiel den Medienpuffer hinzuzufügen.

Sie sollten alle Texturen, die Sie gleichzeitig erstellen, zerstören, anstatt nur einige zu zerstören und die Erinnerung weiterhin zu verwenden.

## <a name="decoding"></a>Decodierung

Rufen Sie zum Erstellen des Decodergeräts [**ID3D11VideoDevice::CreateVideoDecoder auf.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) Die -Methode gibt einen Zeiger auf die [**ID3D11VideoDecoder-Schnittstelle**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) zurück. Die Decodierung sollte innerhalb der [**ROCTRANSFORM::P rocessOutput-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) erfolgen. Rufen Sie in jedem Frame [**DIE NDXGIDeviceManager::TestDevice**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-testdevice) auf, um die Verfügbarkeit von DXGI zu testen. Wenn sich das Gerät geändert hat, muss der Softwaredecoder das Decodergerät wie folgt neu erstellen:

1.  Schließen Sie das Gerätehandle, indem Sie [**DENDXGIDeviceManager::CloseDeviceHandle**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-closedevicehandle)aufrufen.
2.  Geben Sie alle Ressourcen frei, die dem vorherigen Direct3D 11-Gerät zugeordnet sind, einschließlich der Schnittstellen [**ID3D11VideoDecoder,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) [**ID3D11VideoContext,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext) [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d)und [**ID3D11VideoDecoderOutputView.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview)
3.  Öffnen Sie ein neues Gerätehandle.
4.  Aushandeln einer neuen Decoderkonfiguration, wie zuvor unter [Suchen einer Decoderkonfiguration](#find-a-decoder-configuration)beschrieben. Dieser Schritt ist erforderlich, da sich die Gerätefunktionen möglicherweise geändert haben.
5.  Erstellen Sie ein neues Decodergerät.

Vorausgesetzt, dass das Gerätehandle gültig ist, funktioniert der Decodierungsprozess wie folgt:

1.  Abrufen einer verfügbaren Oberfläche, die derzeit nicht verwendet wird. Anfänglich sind alle Oberflächen verfügbar.
2.  Fragen Sie das Medienbeispiel für die [**SCHNITTSTELLE ZUTRACKEDSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) ab.
3.  Rufen Sie [**DIE NURTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) auf, und stellen Sie einen Zeiger auf die [**SCHNITTSTELLE "POINTERAsyncCallback"**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) bereit. (Der Softwaredecoder muss diese Schnittstelle implementieren.) Wenn der Videorenderer das Beispiel freigibt, wird der Rückruf aufgerufen. Verwenden Sie diesen Rückruf, um nachzuverfolgen, welche Beispiele derzeit verfügbar sind und welche verwendet werden.
4.  Rufen Sie [**ID3D11VideoContext::D ecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)auf. Übergeben Sie die Zeiger an die [**ID3D11VideoDecoder-Schnittstelle**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder) für das Decodergerät und die [**ID3D11VideoDecoderOutputView-Schnittstelle**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoderoutputview) für die Ausgabeansicht.
5.  Gehen Sie wie folgt vor:
    1.  Rufen Sie [**ID3D11VideoContext::GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) auf, um einen Puffer abzurufen.
    2.  Füllen Sie den Puffer aus.
    3.  Rufen Sie [**ID3D11VideoContext::ReleaseDecoderBuffer auf.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer)
    4.  Rufen Sie [**ID3D11VideoContext::SubmitDecoderBuffer auf.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) Diese Methode weist das Decodergerät an, die Decodierungsvorgänge für den Frame auszuführen.
6.  Rufen Sie [**ID3D11VideoContext::D ecoderEndFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderendframe) auf, um das Ende der Decodierung für den aktuellen Frame zu signalisieren.

Direct3D 11 verwendet die gleichen Datenstrukturen wie DXVA 2.0 für Decodierungsvorgänge. Für den ursprünglichen Satz von DXVA-Profilen (für H.261, H.263 und MPEG-2) werden diese Datenstrukturen in der [DXVA 1.0-Spezifikation](/windows-hardware/drivers/display/directx-video-acceleration)beschrieben.

Innerhalb jedes [**DecoderBeginFrame-**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) und [**SubmitDecoderBuffer-Aufrufpaars**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-submitdecoderbuffers) können Sie [**GetDecoderBuffer**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer) mehrmals aufrufen, jedoch nur einmal für jeden Puffertyp. Wenn Sie denselben Puffertyp zweimal verwenden, ohne **SubmitDecoderBuffer** aufzurufen, überschreiben Sie die Daten im Puffer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11 Video-APIs](direct3d-11-video-apis.md)
</dt> <dt>

[DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
