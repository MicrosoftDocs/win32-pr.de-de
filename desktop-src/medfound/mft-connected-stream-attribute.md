---
description: Enthält einen Zeiger auf die Streamattribute des verbundenen Streams auf einer hardwarebasierten Media Foundation Transform (MFT).
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: MFT_CONNECTED_STREAM_ATTRIBUTE -Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2289b8f1e8d5d751f7aa69564b8bbd26d865b43efedb474529147385b1851bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722566"
---
# <a name="mft_connected_stream_attribute-attribute"></a>Attribut "MFT \_ CONNECTED \_ STREAM \_ ATTRIBUTE"

Enthält einen Zeiger auf die Streamattribute des verbundenen Streams auf einer hardwarebasierten Media Foundation Transform (MFT).

## <a name="data-type"></a>Datentyp

**ATTRIBUTE _ \* *gespeichert als _* IUnknown\***

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DANNATTRIBUTEs::GetUnknown auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)

Rufen Sie ZUM Festlegen dieses [**Attributs DEN WERTATTRIBUTEs::SetUnknown auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)

## <a name="remarks"></a>Hinweise

Anwendungen verwenden dieses Attribut in der Regel nicht.

Dieses Attribut wird für MFTs verwendet, die als Proxys für ein Hardwaregerät fungieren. Weitere Informationen finden Sie unter [Hardware-MFTs](hardware-mfts.md).

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT \_ MIT \_ \_ HW-STREAM \_ VERBUNDEN](mft-connected-to-hw-stream.md)
</dt> <dt>

[Hardware-MFTs](hardware-mfts.md)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 




