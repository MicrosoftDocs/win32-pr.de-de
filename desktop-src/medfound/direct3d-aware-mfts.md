---
description: In diesem Thema wird beschrieben, wie Sie eine Direct3D-fähige Media Foundation Transformation (MFT) für Videos implementieren.
ms.assetid: 8ec7e678-8477-41fa-9726-54df5ed187cd
title: Direct3D-Aware MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae3bc071ee707505fd7412cba6f0a5aa397fd4c3f623225da28cc5490bf3323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958737"
---
# <a name="direct3d-aware-mfts"></a>Direct3D-Aware MFTs

In diesem Thema wird beschrieben, wie Sie eine *Direct3D-fähige* Media Foundation Transformation (MFT) für Videos implementieren.

Ein Video-MFT gilt als *Direct3D-fähiges* Video, wenn es Beispiele verarbeiten kann, die Direct3D-Oberflächen enthalten. Der typische Grund für die Unterstützung von Direct3D in einem Video-MFT ist die Aktivierung der hardwarebeschleunigen Decodierung mithilfe von DirectX Video Acceleration (DXVA).

In diesem Thema werden die Schritte beschrieben, die erforderlich sind, um Ihre MFT Direct3D-Fähige zu machen. In diesem Thema werden die Mechanismen der DXVA-Decodierung nicht behandelt. Informationen zu DXVA finden Sie unter [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md).

> [!IMPORTANT]
> Ab Windows 8 kann anstatt [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) [**DERDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) verwendet werden. Für Windows Store-Apps müssen Sie DIE APPS **UND DIRECTDXGIDeviceManager** und Microsoft Direct3D 11 verwenden. Weitere Informationen finden Sie in den [Direct3D 11 Video-APIs.](direct3d-11-video-apis.md)

 

1.  Implementieren Sie die [**METHODE VONTRANSFORM::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Diese Methode gibt einen Zeiger auf einen Attributspeicher zurück.
2.  Der MFT muss den Wert des [**MF \_ SA \_ D3D \_ AWARE-Attributs**](mf-sa-d3d-aware-attribute.md) im eigenen Attributspeicher auf **TRUE** festlegen. Verwenden Sie ab Windows 8 bei Verwendung von Direct3D 11 [MF \_ SA \_ D3D11 \_ AWARE](mf-sa-d3d11-aware.md).
3.  Wenn während der Formataushandlung das [**ATTRIBUT MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md) (oder [MF SA \_ \_ D3D11 \_ AWARE](mf-sa-d3d11-aware.md) bei Verwendung von Direct3D 11) **TRUE** ist, kann der Client die [**MFT MESSAGE \_ SET \_ \_ D3D \_ MANAGER-Nachricht**](mft-message-set-d3d-manager.md) an den MFT senden. Der *ulParam-Ereignisparameter* ist ein Zeiger auf die [**IDirect3DDeviceManager9-Schnittstelle.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) Ab Windows 8 können Sie anstatt **"IDirect3DDeviceManager9"** DIE DATEI [**"DIRECTDXGIDeviceManager"**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) verwenden. Der Client muss diese Nachricht nicht senden.
4.  Der MFT ruft [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) auf, um den benötigten DXVA-Dienst abzufragen. Wenn [**DER**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) MFT verwendet wurde, ruft der MFT ab Windows 8 [**DENKDXGIDeviceManager::GetVideoService**](/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice)auf. In der Regel würde ein Decoder [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice)abfragen, und ein Videoprozessor würde [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)abfragen.
5.  Vorausgesetzt, der vorherige Schritt ist erfolgreich, müssen die METHODEN DXVA-kompatible Formate für DIE Methoden [**"DXTRANSFORM::GetInputAvailableType"**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) und [**"DXTransform::GetOutputAvailableType"**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) zurückgeben.
6.  Der Client konfiguriert die Medientypen auf dem MFT. Wenn ein Medientyp nicht mit DXVA kompatibel ist, muss der MFT den Fehlercode **MF \_ E \_ UNSUPPORTED \_ D3D \_ TYPE** zurückgeben.
7.  An diesem Punkt gibt es zwei Optionen, je nachdem, ob der Client ein geeignetes DXVA-Format findet.
    -   Wenn der Client erfolgreich ein DXVA-Format konfiguriert, beginnt er möglicherweise mit der Verarbeitung. An diesem Punkt kann der MFT DXVA für die Verarbeitung verwenden oder auf die Softwareverarbeitung zurückgreifen.
    -   Wenn der Client kein akzeptables DXVA-Format findet, kann der Client auch eine weitere [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER-Nachricht**](mft-message-set-d3d-manager.md) senden. Dieses Mal wird *ulParam* auf **NULL** festgelegt. Der MFT muss den [**IDirect3DDeviceManager9-Zeiger**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) (den [**POINTERDXGIDeviceManager-Zeiger,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) wenn **DER CURSORDXGIDeviceManager** verwendet wurde) und andere DXVA-Schnittstellen freigeben und zur Softwareverarbeitung kehren. An diesem Punkt darf der MFT keine DXVA-Verarbeitung verwenden.

Ein Direct3D-fähiges MFT muss für die Verarbeitung von Stichproben vorbereitet sein, die eine Direct3D-Oberfläche enthalten. Das Beispiel enthält genau einen Medienpuffer. Um die Direct3D-Oberfläche aus dem Puffer abzurufen, rufen Sie die [**MFGetService-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) auf, und geben Sie den **MR BUFFER \_ \_ SERVICE-Dienst** an. Weitere Informationen finden Sie unter [DirectX Surface Buffer](directx-surface-buffer.md).

Ein MFT, der DXVA verwendet, muss wie folgt eigene Ausgabebeispiele zuordnen:

1.  Legen Sie in der [**METHODE ÜBERTRANSFORM::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) das **Flag MFT OUTPUT STREAM PROVIDES \_ \_ \_ \_ SAMPLES** fest.
2.  Erstellen Sie einen Pool von DXVA-Oberflächen, wie in der DXVA-Spezifikation beschrieben.
3.  Erstellen Sie Medienbeispiele, indem Sie [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface)aufrufen.

Der MFT sollte immer die Softwareverarbeitung als Fallback unterstützen, da die DXVA-Verarbeitung aus verschiedenen Gründen möglicherweise nicht verfügbar ist:

-   Die GPU unterstützt DXVA möglicherweise nicht.
-   Der Client verwendet direct3D möglicherweise nicht.
-   DXVA-Profile sind nicht für jedes Videoformat definiert.

Ein Direct3D-fähiges MFT muss über einen einzelnen Ausgabestream verfügen. Es dürfen nicht mehrere Ausgaben verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



