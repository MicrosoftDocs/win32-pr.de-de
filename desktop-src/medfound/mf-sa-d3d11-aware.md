---
description: Gibt an, ob eine Media Foundation-Transformation (MFT) Microsoft Direct3D 11 unterstützt.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: MF_SA_D3D11_AWARE-Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59a996493ace387d1c6e93c734110772274986c6e5490b9e0e08567024d47c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955400"
---
# <a name="mf_sa_d3d11_aware-attribute"></a>MF \_ SA \_ D3D11 \_ AWARE-Attribut

Gibt an, ob eine Media Foundation-Transformation (MFT) Microsoft Direct3D 11 unterstützt.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt nur für Video-MFTs. Um dieses Attribut abzufragen, rufen [**Sie ÜBERTRANSFORM::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) auf, um den MFT-Attributspeicher abzurufen. Wenn **GetAttributes** erfolgreich ist, rufen [**Sie DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

-   Wenn das Attribut ungleich 0 (null) ist, kann der Client dem MFT einen Zeiger auf die [**INTERFACESDXGIDeviceManager-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) geben, bevor das Streaming gestartet wird. Hierzu sendet der Client die [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER-Nachricht**](mft-message-set-d3d-manager.md) an den MFT. Der Client muss diese Nachricht nicht senden.
-   Wenn dieses Attribut 0 **(FALSE)** ist, unterstützt der MFT Direct3D 11 nicht, und der Client sollte die [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER-Nachricht**](mft-message-set-d3d-manager.md) nicht an den MFT senden.

Der Standardwert dieses Attributs ist **FALSE.** Behandeln Sie dieses Attribut als schreibgeschützt. Ändern Sie den Wert nicht. Der MFT ignoriert alle Änderungen am Wert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Unterstützung der Direct3D 11-Videodecodierung in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




