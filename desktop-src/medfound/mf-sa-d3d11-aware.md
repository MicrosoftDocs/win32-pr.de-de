---
description: Gibt an, ob eine Media Foundation Transformation (MFT) Microsoft Direct3D 11 unterstützt.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: MF_SA_D3D11_AWARE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d90f560e3d31b80c1b3fbcbb5c25c4e20815f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344178"
---
# <a name="mf_sa_d3d11_aware-attribute"></a>MF \_ sa \_ D3D11 \_ Aware-Attribut

Gibt an, ob eine Media Foundation Transformation (MFT) Microsoft Direct3D 11 unterstützt.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt nur für Video-MFTs. Um dieses Attribut abzufragen, müssen Sie [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) aufrufen, um den MFT-Attribut Speicher zu erhalten. Wenn **GetAttributes** erfolgreich ist, können Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)aufrufen.

-   Wenn das-Attribut ungleich NULL ist, kann der Client dem MFT einen Zeiger auf die [**imfdxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Schnittstelle übergeben, bevor das Streaming gestartet wird. Hierzu sendet der Client die [**MFT \_ Message \_ Set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) -Nachricht an die MFT. Der Client muss diese Nachricht nicht senden.
-   Wenn dieses Attribut NULL (**false**) ist, wird Direct3D 11 von der MFT nicht unterstützt, und der Client sollte die [**MFT- \_ Nachricht \_ Set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) nicht an die MFT senden.

Der Standardwert dieses Attributs ist **false**. Behandeln Sie dieses Attribut als schreibgeschützt. Ändern Sie den Wert nicht. die MFT ignoriert alle Änderungen am Wert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Unterstützung von Direct3D 11 Video Decodierung in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




