---
description: Gibt die Breite und Höhe des codierten Videos an, wenn das Video zugeschnitten wird.
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: AVEncVideoEncodeDimension-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d99a0c14cbb3f67f7aa1c634a59c5f4cb9184dcd861bc8f14023c4afcebcefa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159319"
---
# <a name="avencvideoencodedimension-property"></a>AVEncVideoEncodeDimension-Eigenschaft

Gibt die Breite und Höhe des codierten Videos an, wenn das Video zugeschnitten wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoEncodeDimension**

## <a name="property-value"></a>Eigenschaftswert

Die oberen 16 Bits des Werts enthalten die Breite in Pixel, und die unteren 16 Bits enthalten die Höhe in Pixel.

## <a name="remarks"></a>Hinweise

Anwendungen können diese Eigenschaft festlegen, um das Eingabevideo zuzuschneiden. Die angegebene Größe muss kleiner als die Größe der Eingabevideoframes sein. Verwenden Sie die [**AVEncVideoEncodeOffsetOrigin-Eigenschaft,**](avencvideoencodeoffsetorigin-property.md) um die linke und obere Ecke des Ausschneiderechtecks anzugeben.

Encoder können diese Eigenschaft als Funktion zurückgeben.

Diese Eigenschaft wird auch mit [H.264 UVC 1.5-Kameraencodern](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)verwendet.

Für UVC 1.5-Kameraencoder wird [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

