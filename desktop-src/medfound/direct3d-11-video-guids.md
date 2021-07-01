---
description: Die folgenden GUIDs unterstützen Direct3D 11-Video-APIs.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: Direct3D 11-Video-GUIDs (D3d11.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16f5277123c3d174427debc3f0ad5e184e49a6c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118635"
---
# <a name="direct3d-11-video-guids"></a>Direct3D 11-Video-GUIDs

Die folgenden GUIDs unterstützen Direct3D 11-Video-APIs.

<dl> <dt>

<span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11 \_ KEY \_ EXCHANGE \_ HW \_ PROTECTION**
</dt> <dd> <dl> <dt>



Gibt an, dass der Decoder Daten von einer hardwarebasierten DRM-Komponente erhält.

**D3D11 \_ KEY \_ EXCHANGE \_ HW \_ PROTECTION** kann im *pKeyExchangeType-Parameter* der [**ID3D11VideoDevice::CreateCryptoSession-Funktion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) angegeben werden, um anzugeben, dass die [**ID3D11CryptoSession-Schnittstelle**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) ausschließlich für die Kommunikation zwischen einer DRM-Komponente im Benutzermodus und der sicheren Ausführungsumgebung verwendet wird.

Wenn diese GUID angegeben wird, sollten die folgenden Methoden nicht aufgerufen werden:

-   [**ID3D11CryptoSession::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [**ID3D11CryptoSession::GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [**ID3D11VideoContext::EncryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [**ID3D11VideoContext::D ecryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [**ID3D11VideoContext::StartSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [**ID3D11VideoContext::FinishSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [**ID3D11VideoContext::GetEncryptionBltKey**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 \_ DECODER \_ ENCRYPTION \_ HW \_ CENC**
</dt> <dd> <dl> <dt>



Gibt an, dass der Decoder Daten von einer hardwarebasierten DRM-Komponente erhält.

Das Festlegen dieser GUID im **guidConfigBitstreamEncryption-Member** der [**\_ \_ \_ CONFIG-Struktur des D3D11 VIDEO DECODER,**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) das an die [**ID3D11VideoDevice::CreateVideoDecoder-API**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) übergeben wird, gibt an, dass die folgenden Parameter im [**ID3D11VideoDevice::D ecoderBeginFrame-Aufruf übergeben**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) werden:



| Wert                 | Beschreibung                                                                                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ContentKeySize* | Enthält die Größe der [**BEGIN FRAME CRYPTO \_ \_ \_ \_ \_ \_ SESSION-Struktur des D3D11-VIDEODECODERS.**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session)                                                                                                  |
| *pContentKey*    | Ein Zeiger auf einen [**D3D11-VIDEODECODER \_ BEGIN FRAME CRYPTO \_ \_ \_ \_ \_ SESSION,**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) der die [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) und die zum Entschlüsseln des Frames erforderlichen Schlüsselinformationen enthält. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2016-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>D3d11.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 11-Video-APIs](direct3d-11-video-apis.md)
</dt> </dl>

 

 




