---
description: Die folgenden GUIDs unterstützen Direct3D 11-Video-APIs.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: Direct3D 11 Video-GUIDs (D3d11. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d97a43285a59cf5196584b9be04fc36b02e5243f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041555"
---
# <a name="direct3d-11-video-guids"></a>Direct3D 11 Video-GUIDs

Die folgenden GUIDs unterstützen Direct3D 11-Video-APIs.

<dl> <dt>

<span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11 \_ Schlüssel \_ Austausch- \_ HW- \_ Schutz**
</dt> <dd> <dl> <dt>



Gibt an, dass der Decoder Daten von einer hardwarebasierten DRM-Komponente empfängt.

**D3D11 \_ Der Schlüssel \_ Austausch- \_ HW- \_ Schutz** kann im Parameter *pkeyexchangetype* der [**ID3D11VideoDevice:: roatecryptosession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) -Funktion angegeben werden, um anzugeben, dass die [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) -Schnittstelle ausschließlich für die Kommunikation zwischen einer DRM-Komponente im Benutzermodus und der sicheren Ausführungsumgebung verwendet wird.

Wenn diese GUID angegeben wird, sollten die folgenden Methoden nicht aufgerufen werden:

-   [**ID3D11CryptoSession:: getcertificesize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [**ID3D11CryptoSession:: GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [**ID3D11VideoContext:: verschlüsselungsblt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [**ID3D11VideoContext::D ecryptionblt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [**ID3D11VideoContext:: starungessionkeyrefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [**ID3D11VideoContext:: finishsessionkeyrefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [**ID3D11VideoContext:: getencryptionbltkey**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 \_ - \_ decoderverschlüsselungs- \_ HW \_ Cenc**
</dt> <dd> <dl> <dt>



Gibt an, dass der Decoder Daten von einer hardwarebasierten DRM-Komponente empfängt.

Durch Festlegen dieser GUID im **guidconfigbitstreamencryption** -Member der [**D3D11- \_ Video \_ Decoder- \_ Konfigurations**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) Struktur, die an die [**ID3D11VideoDevice:: createvideodecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) -API übergeben wird, wird angegeben, dass die folgenden Parameter in den [**ID3D11VideoDevice::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) -aufrufen übergeben werden:



|                  |                                                                                                                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Contentkeysize* | Enthält die Größe der [**\_ \_ \_ \_ \_ kryptografiesitzungsstruktur \_ des D3D11-Video Decoders**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) .                                                                                                  |
| *pcontentkey*    | Ein Zeiger auf einen [**D3D11- \_ Video \_ Decoder beginnt eine Frame- \_ \_ \_ Kryptografiesitzung \_**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) , die [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) und die Schlüsselinformationen bereitstellt, die zum Entschlüsseln des Frames benötigt werden. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>D3d11. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 11-Video-APIs](direct3d-11-video-apis.md)
</dt> </dl>

 

 




