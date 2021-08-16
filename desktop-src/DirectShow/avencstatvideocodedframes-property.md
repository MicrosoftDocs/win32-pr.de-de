---
description: Gibt die Anzahl der codierten Videoframes zurück.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: AVEncStatVideoCodedFrames-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f8858aba7a36d79096eccad40990e1859d4073695aaf80910587bac4005d6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342560"
---
# <a name="avencstatvideocodedframes-property"></a>AVEncStatVideoCodedFrames (Eigenschaft)

Gibt die Anzahl der codierten Videoframes zurück.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncStatVideoCodedFrames**

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist verfügbar, nachdem die Codierung abgeschlossen wurde.

Der Wert dieser Eigenschaft entspricht der [**AVEncStatVideoTotalFrames-Eigenschaft**](avencstatvideototalframes-property.md) abzüglich der Anzahl der gelöschten Frames. Der Encoder kann Frames ablegen, um innerhalb der angegebenen Bitrateneinschränkungen zu bleiben. Sie kann auch Frames am Ende des Streams ablegen (siehe [**AVEncCommonStreamEndHandling-Eigenschaft).**](avenccommonstreamendhandling-property.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




