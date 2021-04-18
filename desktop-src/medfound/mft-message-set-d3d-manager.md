---
description: Legt die Direct3D-Device Manager für die DirectX-Video-accereration (DXVA) fest oder löscht sie.
ms.assetid: fd346d56-1f80-488a-94c8-4e4e36d72890
title: MFT_MESSAGE_SET_D3D_MANAGER (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef8ecb5db474935bb25138a960b6df1c2109c16c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343808"
---
# <a name="mft_message_set_d3d_manager"></a>MFT- \_ Nachrichten \_ Satz \_ D3D \_ Manager

Legt die Direct3D- [Device Manager](direct3d-device-manager.md) für die DirectX-Video-accereration (DXVA) fest oder löscht sie.

## <a name="message-parameter"></a>Message-Parameter

Wenn das Streaming beginnt, enthält der *ulparam* -Parameter einen **IUnknown** -Zeiger. Der MFT fragt diesen Zeiger nach der [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle für Direct3D 9 und der [**imfdxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Schnittstelle für Direct3D 11 ab. Wenn das Streaming beendet wird, enthält der *ULParameter* den Wert **null**.

## <a name="remarks"></a>Bemerkungen

Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Diese Meldung gilt nur für Video Transformationen. Der Client sollte diese Nachricht nicht senden, es sei denn, der MFT gibt **true** für das [**MF \_ sa \_ D3D \_ Aware**](mf-sa-d3d-aware-attribute.md) -Attribut zurück ([MF \_ sa \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md) für Direct3D 11).

Senden Sie diese Nachricht nicht mit mehreren ouputs an einen MFT.

### <a name="implementation"></a>Implementierung

Eine MFT sollte diese Nachricht nur unterstützen, wenn die MFT eine DirectX-Videobeschleunigung für die Videoverarbeitung oder Decodierung verwendet.

Wenn eine MFT diese Nachricht unterstützt, sollte Sie auch die [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode implementieren und den Wert " **true** " für das Attribut " [**MF \_ sa \_ D3D \_ Aware**](mf-sa-d3d-aware-attribute.md) " ([MF \_ sa \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md) für Direct3D 11) zurückgeben. Dieses Attribut informiert den Client darüber, dass der Client die **MFT \_ Message \_ Set \_ D3D \_ Manager** -Nachricht an die MFT senden soll, bevor das Streaming beginnt.

Wenn eine MFT diese Nachricht nicht unterstützt, sollte Sie **E \_ notimpl** von [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)zurückgeben. Dies ist eine Ausnahme von der allgemeinen Regel, dass eine MFT von jeder ignoriernachricht aus **\_ OK** zurückgeben kann.

Weitere Informationen finden Sie unter [Direct3D-Aware MFTs](direct3d-aware-mfts.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-kompatible MFTs](direct3d-aware-mfts.md)
</dt> <dt>

[Unterstützung von DXVA 2,0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Unterstützung von Direct3D 11 Video Decodierung in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[**MFT \_ - \_ Nachrichtentyp**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




