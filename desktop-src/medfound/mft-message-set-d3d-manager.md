---
description: Legt die Direct3D-Geräte-Manager für DirectX Video Accereration (DXVA) fest oder löscht sie.
ms.assetid: fd346d56-1f80-488a-94c8-4e4e36d72890
title: MFT_MESSAGE_SET_D3D_MANAGER (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a0e7ccbf9f28615b17e6acded6ecc932334b4fb0fa4a607d6fd6213ba2cd214
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848065"
---
# <a name="mft_message_set_d3d_manager"></a>MFT \_ MESSAGE \_ SET \_ D3D \_ MANAGER

Legt die [Direct3D-Geräte-Manager](direct3d-device-manager.md) für DirectX Video Accereration (DXVA) fest oder löscht sie.

## <a name="message-parameter"></a>Message-Parameter

Wenn das Streaming beginnt, enthält der *ulParam-Parameter* einen **IUnknown-Zeiger.** Der MFT fragen diesen Zeiger nach der [**IDirect3DDeviceManager9-Schnittstelle**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) für Direct3D 9 und der [**INTERFACESDXGIDeviceManager-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) für Direct3D 11 ab. Wenn das Streaming beendet wird, enthält *ulParameter* den Wert **NULL**.

## <a name="remarks"></a>Hinweise

Um diese Nachricht zu senden, rufen Sie [**ÜBERTRANSFORM::P rocessMessage auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)

Diese Meldung gilt nur für Videotransformationen. Der Client sollte diese Nachricht nur senden, wenn der MFT **TRUE** für das [**MF SA \_ \_ D3D \_ AWARE-Attribut**](mf-sa-d3d-aware-attribute.md) [(MF SA \_ \_ D3D11 \_ AWARE](mf-sa-d3d11-aware.md) für Direct3D 11) zurückgibt.

Senden Sie diese Nachricht nicht an einen MFT mit mehreren Ouputs.

### <a name="implementation"></a>Implementierung

Ein MFT sollte diese Nachricht nur unterstützen, wenn der MFT DirectX Video Acceleration für die Videoverarbeitung oder -decodierung verwendet.

Wenn ein MFT diese Nachricht unterstützt, sollte er auch die [**METHODE DERTRANSFORM::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) implementieren und den Wert **TRUE** für das [**MF SA \_ \_ D3D \_ AWARE-Attribut**](mf-sa-d3d-aware-attribute.md) zurückgeben (([MF SA \_ \_ D3D11 \_ AWARE](mf-sa-d3d11-aware.md) für Direct3D 11). Dieses Attribut informiert den Client, dass der Client die **MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER-Nachricht** an den MFT senden soll, bevor das Streaming beginnt.

Wenn ein MFT diese Nachricht nicht unterstützt, sollte E **\_ NOTIMPL** von [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)zurückgegeben werden. Dies ist eine Ausnahme von der allgemeinen Regel, dass ein MFT **S \_ OK** aus jeder ignorierten Nachricht zurückgeben kann.

Weitere Informationen finden Sie unter [Direct3D-fähige MFTs.](direct3d-aware-mfts.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-fähige MFTs](direct3d-aware-mfts.md)
</dt> <dt>

[Unterstützung von DXVA 2.0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Unterstützung der Direct3D 11-Videodecodierung in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[**\_MFT-NACHRICHTENTYP \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




