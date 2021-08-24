---
description: Gibt die linke und obere Ecke des Clippingrechtecks an, wenn das Video zugeschnitten wird.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: AVEncVideoEncodeOffsetOrigin-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fdc4ffd1f168fa98ce71937b5ddc22d429c573481575432e94964fdfc5205b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119275760"
---
# <a name="avencvideoencodeoffsetorigin-property"></a>AVEncVideoEncodeOffsetOrigin-Eigenschaft

Gibt die linke und obere Ecke des Clippingrechtecks an, wenn das Video zugeschnitten wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoEncodeOffsetOrigin**

## <a name="property-value"></a>Eigenschaftswert

Die oberen 16 Bits des Werts enthalten den Offset vom linken Rand des Eingabeframes in Pixel. Die unteren 16 Bits enthalten den Offset vom oberen Rand des Eingabeframes in Pixel.

## <a name="remarks"></a>Hinweise

Anwendungen können diese Eigenschaft festlegen, um das Eingabevideo zuschneiden. Verwenden Sie die [**AVEncVideoEncodeDimension-Eigenschaft,**](avencvideoencodedimension-property.md) um die Breite und Höhe des Clippingrechtecks anzugeben.

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

 

 




