---
description: Enthält einen Zeiger auf die streamattribute des verbundenen Streams auf einer hardwarebasierten Media Foundation Transformation (MFT).
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: MFT_CONNECTED_STREAM_ATTRIBUTE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b182cbed78f5f9851b621de72bf691bf698b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863963"
---
# <a name="mft_connected_stream_attribute-attribute"></a>Attribut Attribut des MFT- \_ verbundenen \_ Streams \_

Enthält einen Zeiger auf die streamattribute des verbundenen Streams auf einer hardwarebasierten Media Foundation Transformation (MFT).

## <a name="data-type"></a>Datentyp

**Imfattributes \** _ als " _*IUnknown \** " gespeichert_

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Bemerkungen

Anwendungen verwenden dieses Attribut in der Regel nicht.

Dieses Attribut wird für MFTs verwendet, die als Proxys für ein Hardware Gerät fungieren. Weitere Informationen finden Sie unter [Hardware-MFTs](hardware-mfts.md).

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[mit \_ \_ dem HW- \_ \_ Stream verbundene MFT](mft-connected-to-hw-stream.md)
</dt> <dt>

[Hardware-MFTs](hardware-mfts.md)
</dt> <dt>

[Transformations Attribute](transform-attributes.md)
</dt> </dl>

 

 




