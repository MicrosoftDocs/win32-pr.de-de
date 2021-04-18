---
description: Unterstützung von DXVA 2,0 in Media Foundation
ms.assetid: d7330370-adb3-4c6a-962a-7b46c344500c
title: Unterstützung von DXVA 2,0 in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce144c24a1aeeda6281ddb423757f3e339903440
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106364999"
---
# <a name="supporting-dxva-20-in-media-foundation"></a>Unterstützung von DXVA 2,0 in Media Foundation

In diesem Thema wird beschrieben, wie Sie die DirectX-Video Beschleunigung (DXVA) 2,0 in einer Media Foundation Transformation (MFT) mit Microsoft Direct3D 9 unterstützen, insbesondere die Kommunikation zwischen dem Decoder und dem Videorenderer, der vom topologielader vermittelt wird. In diesem Thema wird nicht beschrieben, wie DXVA-Decodierung implementiert wird.

Im restlichen Teil dieses Themas verweist der Begriff " *Decoder* " auf den Decoder-MFT, der komprimierte Videos empfängt und unkomprimierte Videos ausgibt. Der Begriff " *Decoder-Gerät* " bezieht sich auf einen Hardware-Video Beschleuniger, der vom Grafiktreiber implementiert wird.

> [!TIP]
> Weitere Informationen zur Video Decodierung von Microsoft Direct3D 11 finden Sie unter [Unterstützung von Direct3D 11 Video Decodierung in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).

 

> [!Note]  
> Für Windows Store-Apps muss Direct3D 11 verwendet werden.

 

Im folgenden finden Sie die grundlegenden Schritte, die ein Decoder ausführen muss, um DXVA 2,0 in Media Foundation zu unterstützen:

1.  Öffnen Sie ein Handle für das Gerät Direct3D 9.
2.  Suchen Sie die Konfiguration des DXVA-Decoders.
3.  Nicht komprimierte Puffer zuordnen.
4.  Decodieren von Frames.

Diese Schritte werden im weiteren Verlauf dieses Themas ausführlicher beschrieben.

## <a name="opening-a-direct3d-device-handle"></a>Öffnen eines Direct3D-Geräte Handles

Der MFT verwendet den Microsoft Direct3D-Geräte-Manager, um ein Handle für das Direct3D 9-Gerät zu erhalten. Führen Sie die folgenden Schritte aus, um das Geräte Handle zu öffnen:

1.  Machen Sie das Attribut [MF \_ sa \_ D3D \_ Aware](mf-sa-d3d-aware-attribute.md) mit dem Wert **true** verfügbar. Das topologielader fragt dieses Attribut durch Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)ab. Wenn das-Attribut auf **true** festgelegt wird, wird der topologielader benachrichtigt, dass der MFT DXVA unterstützt.
2.  Wenn die Format Aushandlung beginnt, ruft das topologieloader " [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) " mit der Meldung " [**MFT \_ Message \_ Set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) " auf. Der *ulparam* -Parameter ist ein **IUnknown** -Zeiger auf den Direct3D-Geräte-Manager des Video-Renderers. Fragen Sie diesen Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle ab.
3.  Wenn Sie [**IDirect3DDeviceManager9:: opentovicehandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) aufzurufen, erhalten Sie ein Handle für das Direct3D-Gerät des Renderers.
4.  Aufrufen von [**IDirect3DDeviceManager9:: getvideoservice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) und übergeben des Geräte Handles. Diese Methode gibt einen Zeiger auf die [**idirectxvideodecoderservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) -Schnittstelle zurück.
5.  Zwischenspeichern der Zeiger und des Geräte Handles.

## <a name="finding-a-decoder-configuration"></a>Suchen einer decoderkonfiguration

Der MFT muss eine kompatible Konfiguration für das DXVA-Decodergerät finden. Führen Sie nach der Überprüfung des Eingabe Typs die folgenden Schritte innerhalb der [**IMF Transform:: abktinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) -Methode aus:

1.  Aufrufen von [**idirectxvideodecoderservice:: getdecoderdeviceguids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids). Diese Methode gibt ein Array von Decoder-Geräte-GUIDs zurück.
2.  Durchlaufen Sie das Array von decoderguids, um diejenigen zu finden, die der Decoder unterstützt. Für einen MPEG-2-Decoder würden Sie z. b. nach **DXVA2 \_ ModeMPEG2 \_ mucomp**, **DXVA2 \_ ModeMPEG2 \_ IDCT** oder **DXVA2 \_ ModeMPEG2 \_ VLD** suchen.

3.  Wenn Sie eine Geräte-GUID für den Kandidaten Decoder finden, übergeben Sie die GUID an die [**idirectxvideodecoderservice:: getdecoderrendertargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) -Methode. Diese Methode gibt ein Array von renderzielformaten zurück, die als **D3DFORMAT** -Werte angegeben werden.
4.  Durchlaufen Sie die renderzielformate, und suchen Sie nach einem Format, das vom Decoder unterstützt wird.
5.  Aufrufen von [**idirectxvideodecoderservice:: getdecoderkonfigurationen**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Übergeben Sie dieselbe Decoder-Geräte-GUID, zusammen mit einer [**DXVA2 \_ videodesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) -Struktur, die das vorgeschlagene Ausgabeformat beschreibt. Die-Methode gibt ein Array von [**DXVA2 \_ configpicturedecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) -Strukturen zurück. Jede Struktur beschreibt eine mögliche Konfiguration für das Decoder-Gerät. Suchen Sie nach einer Konfiguration, die vom Decoder unterstützt wird.
6.  Speichert das renderzielformat und die Konfiguration.

Geben Sie in der [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) -Methode basierend auf dem vorgeschlagenen renderzielformat ein unkomprimiertes Videoformat zurück.

Überprüfen Sie in der [**IMF Transform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) -Methode den Medientyp auf das renderzielformat.

### <a name="fallback-to-software-decoding"></a>Fallback auf Software Decodierung

Wenn die MFT eine DXVA-Konfiguration nicht finden kann (z. b. wenn der Grafiktreiber nicht über die richtigen Funktionen verfügt), sollte der Fehlercode **MF \_ E \_ nicht unterstützter \_ D3D- \_ Typ** aus den Methoden [**setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) und [**setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) zurückgegeben werden. Das topologielader antwortet, indem er die [**MFT \_ Message \_ Set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) -Nachricht mit dem Wert **null** für den *ulparam* -Parameter sendet. Der MFT sollte seinen Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle freigeben. Das topologielader wird dann den Medientyp erneut aushandeln, und die MFT kann Software Decodierung verwenden.

## <a name="allocating-uncompressed-buffers"></a>Zuordnen von nicht komprimierten Puffern

In DXVA 2,0 ist der Decoder für das Zuordnen von Direct3D-Oberflächen zur Verwendung als nicht komprimierte Video Puffer verantwortlich. Der Decoder sollte drei Oberflächen zuordnen, die der EVR für Deinterlacing verwenden soll. Diese Zahl ist korrigiert, da Media Foundation keine Möglichkeit bietet, den EVR anzugeben, wie viele Oberflächen der Grafiktreiber für Deinterlacing benötigt. Für jeden Treiber sollten drei Oberflächen ausreichen.

Legen Sie in der [**imftransform:: getoutputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) -Methode den **MFT- \_ Ausgabestream \_ \_ enthält \_** ein beispielflag in der [**MFT- \_ Ausgabestream- \_ \_ Informations**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) Struktur fest. Dieses Flag benachrichtigt die Medien Sitzung, dass der MFT seine eigenen Ausgabe Beispiele zuweist.

Rufen Sie zum Erstellen der Oberflächen [**idirectxvideoaccelerationservice:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface)auf. (Die [**idirectxvideodecoderservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) -Schnittstelle erbt diese Methode von [**idirectxvideoaccelerationservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).) Sie können dies in [**setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)tun, nachdem Sie das renderzielformat gefunden haben.

Rufen Sie für jede Oberfläche [**mfcreatevideosamplefromsurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) auf, um ein Medien Beispiel zu erstellen, das die Oberfläche enthält. Die-Methode gibt einen Zeiger auf die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle zurück.

## <a name="decoding"></a>Decodierung

Um das Decoder-Gerät zu erstellen, rufen Sie [**idirectxvideodecoderservice:: createvideodecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder)auf. Die-Methode gibt einen Zeiger auf die [**idirectxvideodecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) -Schnittstelle des Decoder-Geräts zurück.

Die Decodierung sollte in der [**IMF Transform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode erfolgen. Bei jedem Frame wird [**IDirect3DDeviceManager9:: testdevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) aufgerufen, um das Geräte Handle zu testen. Wenn sich das Gerät geändert hat, gibt die Methode **DXVA2 \_ E \_ New \_ Video \_ Device** zurück. Wenn dies der Fall ist, gehen Sie wie folgt vor:

1.  Schließen Sie das Geräte Handle durch Aufrufen von [**IDirect3DDeviceManager9:: closedevicehandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Geben Sie die Zeiger [**idirectxvideodecoderservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) und [**idirectxvideodecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) frei.
3.  Öffnen Sie ein neues Geräte handle.
4.  Aushandeln Sie eine neue decoderkonfiguration, wie unter "Suchen einer decoderkonfiguration" weiter oben auf dieser Seite beschrieben.
5.  Erstellen Sie ein neues Decoder-Gerät.

Wenn das Geräte Handle gültig ist, funktioniert der Decodierungs Prozess wie folgt:

1.  Sie erhalten eine verfügbare Oberfläche, die derzeit nicht verwendet wird. (Anfänglich sind alle Oberflächen verfügbar.)
2.  Fragen Sie das Medien Beispiel nach der [**IMF trackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) -Schnittstelle ab.
3.  Aufrufen von [**imftrackedsample:: abtallocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) und Bereitstellen eines Zeigers auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle, die vom Decoder implementiert wird. Wenn der Videorenderer das Beispiel freigibt, wird der Rückruf des Decoders aufgerufen.
4.  Aufrufen von [**idirectxvideodecoder:: beginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).
5.  Führen Sie die folgenden Schritte aus:
    1.  Aufrufen von [**idirectxvideodecoder:: GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) zum Abrufen eines DXVA-decoderpuffers.
    2.  Füllen Sie den Puffer aus.
    3.  Nennen Sie [**idirectxvideodecoder:: ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).
    4.  Nennen Sie [**idirectxvideodecoder:: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) , um die Decodierungs Vorgänge für den Frame auszuführen.

DXVA 2,0 verwendet die gleichen Datenstrukturen wie DXVA 1,0 für Decodierungs Vorgänge. Für den ursprünglichen Satz von DXVA-Profilen (für h. 261, h. 263 und MPEG-2) werden diese Datenstrukturen in der [Spezifikation DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration)beschrieben.

In jedem Paar von [**beginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)- / [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) -aufrufen können Sie [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) mehrmals aufrufen, aber nur einmal für jeden DXVA-Puffer. Wenn Sie es zweimal mit dem gleichen Puffertyp aufzurufen, überschreiben Sie die Daten.

Verwenden [**Sie den Rückruf der Methode "**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) -Methode" (Schritt 3), um nachzuverfolgen, welche Beispiele derzeit verfügbar sind und welche verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Video Beschleunigung 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 
