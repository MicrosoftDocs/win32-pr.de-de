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
# <a name="direct3d-11-video-guids"></a><span data-ttu-id="d328b-103">Direct3D 11 Video-GUIDs</span><span class="sxs-lookup"><span data-stu-id="d328b-103">Direct3D 11 Video GUIDs</span></span>

<span data-ttu-id="d328b-104">Die folgenden GUIDs unterstützen Direct3D 11-Video-APIs.</span><span class="sxs-lookup"><span data-stu-id="d328b-104">The following GUIDs support Direct3D 11 Video APIs.</span></span>

<dl> <dt>

<span data-ttu-id="d328b-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11 \_ Schlüssel \_ Austausch- \_ HW- \_ Schutz**</span><span class="sxs-lookup"><span data-stu-id="d328b-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d328b-106">Gibt an, dass der Decoder Daten von einer hardwarebasierten DRM-Komponente empfängt.</span><span class="sxs-lookup"><span data-stu-id="d328b-106">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="d328b-107">**D3D11 \_ Der Schlüssel \_ Austausch- \_ HW- \_ Schutz** kann im Parameter *pkeyexchangetype* der [**ID3D11VideoDevice:: roatecryptosession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) -Funktion angegeben werden, um anzugeben, dass die [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) -Schnittstelle ausschließlich für die Kommunikation zwischen einer DRM-Komponente im Benutzermodus und der sicheren Ausführungsumgebung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d328b-107">**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION** can be specified in the *pKeyExchangeType* parameter of the [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) function to indicate that the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) interface will be used purely for communication between a user mode DRM component and the secure execution environment.</span></span>

<span data-ttu-id="d328b-108">Wenn diese GUID angegeben wird, sollten die folgenden Methoden nicht aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="d328b-108">When this GUID is specified, the following methods should not be called:</span></span>

-   [<span data-ttu-id="d328b-109">**ID3D11CryptoSession:: getcertificesize**</span><span class="sxs-lookup"><span data-stu-id="d328b-109">**ID3D11CryptoSession::GetCertificateSize**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [<span data-ttu-id="d328b-110">**ID3D11CryptoSession:: GetCertificate**</span><span class="sxs-lookup"><span data-stu-id="d328b-110">**ID3D11CryptoSession::GetCertificate**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [<span data-ttu-id="d328b-111">**ID3D11VideoContext:: verschlüsselungsblt**</span><span class="sxs-lookup"><span data-stu-id="d328b-111">**ID3D11VideoContext::EncryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [<span data-ttu-id="d328b-112">**ID3D11VideoContext::D ecryptionblt**</span><span class="sxs-lookup"><span data-stu-id="d328b-112">**ID3D11VideoContext::DecryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [<span data-ttu-id="d328b-113">**ID3D11VideoContext:: starungessionkeyrefresh**</span><span class="sxs-lookup"><span data-stu-id="d328b-113">**ID3D11VideoContext::StartSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [<span data-ttu-id="d328b-114">**ID3D11VideoContext:: finishsessionkeyrefresh**</span><span class="sxs-lookup"><span data-stu-id="d328b-114">**ID3D11VideoContext::FinishSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [<span data-ttu-id="d328b-115">**ID3D11VideoContext:: getencryptionbltkey**</span><span class="sxs-lookup"><span data-stu-id="d328b-115">**ID3D11VideoContext::GetEncryptionBltKey**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span data-ttu-id="d328b-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 \_ - \_ decoderverschlüsselungs- \_ HW \_ Cenc**</span><span class="sxs-lookup"><span data-stu-id="d328b-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11\_DECODER\_ENCRYPTION\_HW\_CENC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d328b-117">Gibt an, dass der Decoder Daten von einer hardwarebasierten DRM-Komponente empfängt.</span><span class="sxs-lookup"><span data-stu-id="d328b-117">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="d328b-118">Durch Festlegen dieser GUID im **guidconfigbitstreamencryption** -Member der [**D3D11- \_ Video \_ Decoder- \_ Konfigurations**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) Struktur, die an die [**ID3D11VideoDevice:: createvideodecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) -API übergeben wird, wird angegeben, dass die folgenden Parameter in den [**ID3D11VideoDevice::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) -aufrufen übergeben werden:</span><span class="sxs-lookup"><span data-stu-id="d328b-118">Setting this GUID in the **guidConfigBitstreamEncryption** member of the [**D3D11\_VIDEO\_DECODER\_CONFIG**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) structure passed to the [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) API indicates that the following parameters will be passed in the [**ID3D11VideoDevice::DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) call:</span></span>



|                  |                                                                                                                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d328b-119">*Contentkeysize*</span><span class="sxs-lookup"><span data-stu-id="d328b-119">*ContentKeySize*</span></span> | <span data-ttu-id="d328b-120">Enthält die Größe der [**\_ \_ \_ \_ \_ kryptografiesitzungsstruktur \_ des D3D11-Video Decoders**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) .</span><span class="sxs-lookup"><span data-stu-id="d328b-120">Contains the size of the [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) structure.</span></span>                                                                                                  |
| <span data-ttu-id="d328b-121">*pcontentkey*</span><span class="sxs-lookup"><span data-stu-id="d328b-121">*pContentKey*</span></span>    | <span data-ttu-id="d328b-122">Ein Zeiger auf einen [**D3D11- \_ Video \_ Decoder beginnt eine Frame- \_ \_ \_ Kryptografiesitzung \_**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) , die [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) und die Schlüsselinformationen bereitstellt, die zum Entschlüsseln des Frames benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="d328b-122">A pointer to a [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) providing the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) and the key information needed to decrypt the frame.</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d328b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d328b-123">Requirements</span></span>



| <span data-ttu-id="d328b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d328b-124">Requirement</span></span> | <span data-ttu-id="d328b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d328b-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d328b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d328b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d328b-127">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d328b-127">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d328b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d328b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d328b-129">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d328b-129">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d328b-130">Header</span><span class="sxs-lookup"><span data-stu-id="d328b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d328b-131"><dt>D3d11. h</dt></span><span class="sxs-lookup"><span data-stu-id="d328b-131"><dt>D3d11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d328b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d328b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d328b-133">Direct3D 11-Video-APIs</span><span class="sxs-lookup"><span data-stu-id="d328b-133">Direct3D 11 Video APIs</span></span>](direct3d-11-video-apis.md)
</dt> </dl>

 

 




