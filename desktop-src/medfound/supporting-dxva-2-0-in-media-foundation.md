---
description: Unterstützung von DXVA 2.0 in Media Foundation
ms.assetid: d7330370-adb3-4c6a-962a-7b46c344500c
title: Unterstützung von DXVA 2.0 in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170b9c8ccdbdb7e0844b79e5743c4a84b033b7d504378dba083be5adfb244fcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721929"
---
# <a name="supporting-dxva-20-in-media-foundation"></a>Unterstützung von DXVA 2.0 in Media Foundation

In diesem Thema wird beschrieben, wie DirectX Video Acceleration (DXVA) 2.0 in einer Media Foundation-Transformation (MFT) mithilfe von Microsoft Direct3D 9 unterstützt wird. Insbesondere wird die Kommunikation zwischen dem Decoder und dem Videorenderer beschrieben, der vom Topologielader vermittelt wird. In diesem Thema wird nicht beschrieben, wie die DXVA-Decodierung implementiert wird.

Im restlichen Teil dieses  Themas bezieht sich der Begriff Decoder auf den Decoder MFT, der komprimiertes Video empfängt und unkomprimiertes Video ausausgabet. Der Begriff *Decodergerät bezieht* sich auf eine Hardwarevideobeschleunigung, die vom Grafiktreiber implementiert wird.

> [!TIP]
> Informationen zur Videodecodierung von Microsoft Direct3D 11 finden Sie unter [Supporting Direct3D 11 Video Decoding in Media Foundation.](supporting-direct3d-11-video-decoding-in-media-foundation.md)

 

> [!Note]  
> Windows Store Müssen Direct3D 11 verwenden.

 

Hier sind die grundlegenden Schritte, die ein Decoder ausführen muss, um DXVA 2.0 in Media Foundation:

1.  Öffnen Sie ein Handle für das Direct3D 9-Gerät.
2.  Suchen sie nach einer DXVA-Decoderkonfiguration.
3.  Ordnen Sie unkomprimierte Puffer zu.
4.  Decodieren von Frames.

Diese Schritte werden im weiteren Verlauf dieses Themas ausführlicher beschrieben.

## <a name="opening-a-direct3d-device-handle"></a>Öffnen eines Direct3D-Gerätehandpunkts

MFT verwendet den Microsoft Direct3D-Geräte-Manager, um ein Handle für das Direct3D 9-Gerät zu erhalten. Führen Sie die folgenden Schritte aus, um das Gerätehand handle zu öffnen:

1.  Machen Sie das [MF \_ SA \_ D3D \_ AWARE-Attribut](mf-sa-d3d-aware-attribute.md) mit dem Wert **TRUE verfügbar.** Das Topologielader fragt dieses Attribut ab, indem [**ESGETRANSFORM::GetAttributes aufruft.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Wenn Sie das -Attribut **auf TRUE** festlegen, wird das Topologielader benachrichtigt, dass das MFT DXVA unterstützt.
2.  Wenn die Formatierungsaushandlung beginnt, ruft das Topologielader mit der [**MFT \_ MESSAGE \_ SET \_ D3D \_ MANAGER-Nachricht**](mft-message-set-d3d-manager.md) [**DEN AUFRUF VON DURCHSICHTTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) auf. Der *ulParam-Parameter* ist ein **IUnknown-Zeiger** auf den Direct3D-Geräte-Manager des Videorenderers. Fragen Sie diesen Zeiger für die [**IDirect3DDeviceManager9-Schnittstelle**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) ab.
3.  Rufen [**Sie IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) auf, um ein Handle für das Direct3D-Gerät des Renderers abzurufen.
4.  Rufen [**Sie IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) auf, und übergeben Sie das Gerätehand handle. Diese Methode gibt einen Zeiger auf die [**IDirectXVideoDecoderService-Schnittstelle**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) zurück.
5.  Speichern Sie die Zeiger und das Gerätehandler zwischen.

## <a name="finding-a-decoder-configuration"></a>Suchen einer Decoderkonfiguration

MFT muss eine kompatible Konfiguration für das DXVA-Decodergerät finden. Führen Sie nach der Validierung des Eingabetyps die folgenden Schritte in der [**METHODE VEREERTRANSFORM::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) aus:

1.  Rufen [**Sie IDirectXVideoDecoderService::GetDecoderDeviceGuids auf.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids) Diese Methode gibt ein Array von Decodergeräte-GUIDs zurück.
2.  Schleife durch das Array von Decoder-GUIDs, um diejenigen zu finden, die der Decoder unterstützt. Für einen MPEG-2-Decoder würden Sie beispielsweise nach **DXVA2 \_ ModeMPEG2 \_ MOCOMP,** **DXVA2 \_ ModeMPEG2 \_ IDCT** oder **DXVA2 \_ ModeMPEG2 \_ VLD** suchen.

3.  Wenn Sie eine kandidatenweise Decodergeräte-GUID finden, übergeben Sie die GUID an die [**IDirectXVideoDecoderService::GetDecoderRenderTargets-Methode.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) Diese Methode gibt ein Array von Renderzielformaten zurück, die als **D3DFORMAT-Werte angegeben** werden.
4.  Schleife durch die Renderzielformate, und suchen Sie nach einem Format, das vom Decoder unterstützt wird.
5.  Rufen [**Sie IDirectXVideoDecoderService::GetDecoderConfigurations auf.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations) Übergeben Sie die gleiche Decodergeräte-GUID zusammen mit einer [**DXVA2 \_ VideoDesc-Struktur,**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) die das vorgeschlagene Ausgabeformat beschreibt. Die -Methode gibt ein Array von [**DXVA2-ConfigPictureDecode-Strukturen \_**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) zurück. Jede Struktur beschreibt eine mögliche Konfiguration für das Decodergerät. Suchen Sie nach einer Konfiguration, die der Decoder unterstützt.
6.  Store das Format und die Konfiguration des Renderziels.

Geben Sie [**in der METHODE DURCHSICHTTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) basierend auf dem vorgeschlagenen Renderzielformat ein unkomprimiertes Videoformat zurück.

Überprüfen Sie den Medientyp in [**der METHODE VERTRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) mit dem Renderzielformat.

### <a name="fallback-to-software-decoding"></a>Fallback auf Softwaredecodierung

Wenn MFT keine DXVA-Konfiguration finden kann (z. B. wenn der Grafiktreiber nicht über die richtigen Funktionen verfügt), sollte er den Fehlercode **MF \_ E \_ UNSUPPORTED \_ D3D \_ TYPE** aus den [**Methoden SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) und [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) zurückgeben. Das Topologielader antwortet, indem es die [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER-Nachricht**](mft-message-set-d3d-manager.md) mit dem Wert **NULL** für den *ulParam-Parameter* sendet. Der MFT sollte seinen Zeiger auf die [**IDirect3DDeviceManager9-Schnittstelle**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) frei geben. Der Medientyp wird dann vom Topologielader neu ausgehandelt, und MFT kann die Softwaredecodierung verwenden.

## <a name="allocating-uncompressed-buffers"></a>Zuordnen von unkomprimierten Puffern

In DXVA 2.0 ist der Decoder dafür verantwortlich, Direct3D-Oberflächen als unkomprimierte Videopuffer zu verwenden. Der Decoder sollte 3 Oberflächen zuordnen, die der EVR für das Deinterlacing verwenden kann. Diese Zahl ist fest, da Media Foundation evr keine Möglichkeit bietet, anzugeben, wie viele Oberflächen der Grafiktreiber für das Deinterlacing benötigt. Drei Oberflächen sollten für jeden Treiber ausreichend sein.

Legen Sie [**in der METHODE VERFORMTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) das **Flag MFT OUTPUT STREAM PROVIDES \_ \_ \_ \_ SAMPLES** in der [**MFT \_ OUTPUT STREAM \_ \_ INFO-Struktur**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) fest. Dieses Flag benachrichtigt die Mediensitzung, dass MFT eigene Ausgabebeispiele zuteilen.

Rufen Sie zum Erstellen der Oberflächen [**IDirectXVideoAccelerationService::CreateSurface auf.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) (Die [**IDirectXVideoDecoderService-Schnittstelle**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) erbt diese Methode von [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).) Sie können dies in [**SetInputType nach**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)dem Suchen des Renderzielformats tun.

Rufen Sie für jede Oberfläche [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) auf, um ein Medienbeispiel für die Oberfläche zu erstellen. Die -Methode gibt einen Zeiger auf die [**NSSAMPLE-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) zurück.

## <a name="decoding"></a>Decodierung

Rufen Sie zum Erstellen des Decodergeräts [**IDirectXVideoDecoderService::CreateVideoDecoder auf.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder) Die -Methode gibt einen Zeiger auf die [**IDirectXVideoDecoder-Schnittstelle**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) des Decodergeräts zurück.

Die Decodierung sollte innerhalb der [**METHODE 10::P ROCTransform::P Output erfolgen.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) Rufen Sie in jedem Frame [**IDirect3DDeviceManager9::TestDevice auf,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) um das Gerätehandchen zu testen. Wenn das Gerät geändert wurde, gibt die Methode **DXVA2 \_ E NEW VIDEO DEVICE \_ \_ \_ zurück.** Gehen Sie in diesem Fall wie folgt vor:

1.  Schließen Sie das Gerätehandle, indem [**Sie IDirect3DDeviceManager9::CloseDeviceHandle aufrufen.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle)
2.  Geben Sie [**die Zeiger IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) [**und IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) frei.
3.  Öffnen Sie ein neues Gerätehand handle.
4.  Aushandeln einer neuen Decoderkonfiguration, wie weiter oben auf dieser Seite unter "Finding a Decoder Configuration" (Suchen einer Decoderkonfiguration) beschrieben.
5.  Erstellen Sie ein neues Decodergerät.

Unter der Annahme, dass das Gerätehandy gültig ist, funktioniert der Decodierungsprozess wie folgt:

1.  Hier erhalten Sie eine verfügbare Oberfläche, die derzeit nicht verwendet wird. (Anfänglich sind alle Oberflächen verfügbar.)
2.  Fragen Sie das Medienbeispiel für die [**BENUTZEROBERFLÄCHETrackedSample-Schnittstelle**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) ab.
3.  Rufen [**Sie DIEDOKTrackedSample::SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) auf, und stellen Sie einen Zeiger auf die [**DURCHDNASYNCCallback-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) bereit, die vom Decoder implementiert wird. Wenn der Videorenderer das Beispiel frei gibt, wird der Rückruf des Decoders aufgerufen.
4.  Rufen [**Sie IDirectXVideoDecoder::BeginFrame auf.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)
5.  Führen Sie die folgenden Schritte mindestens einmal aus:
    1.  Rufen [**Sie IDirectXVideoDecoder::GetBuffer auf,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) um einen DXVA-Decoderpuffer zu erhalten.
    2.  Füllen Sie den Puffer aus.
    3.  Rufen [**Sie IDirectXVideoDecoder::ReleaseBuffer auf.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer)
    4.  Rufen [**Sie IDirectXVideoDecoder::Execute auf,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) um die Decodierungsvorgänge für den Frame auszuführen.

DXVA 2.0 verwendet dieselben Datenstrukturen wie DXVA 1.0 für Decodierungsvorgänge. Für den ursprünglichen Satz von DXVA-Profilen (für H.261, H.263 und MPEG-2) werden diese Datenstrukturen in der [DXVA 1.0-Spezifikation beschrieben.](/windows-hardware/drivers/display/directx-video-acceleration)

Innerhalb jedes [**BeginFrame Execute-Aufrufpaars**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)können Sie GetBuffer mehrmals aufrufen, jedoch nur einmal für jeden / [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) DXVA-Puffertyp. Wenn Sie ihn zweimal mit dem gleichen Puffertyp aufrufen, überschreiben Sie die Daten.

Verwenden Sie den Rückruf der [**SetAllocator-Methode**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) (Schritt 3), um zu verfolgen, welche Beispiele derzeit verfügbar sind und welche verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Videobeschleunigung 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 
