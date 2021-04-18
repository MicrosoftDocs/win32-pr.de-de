---
description: Gibt die Breite und Höhe des codierten Videos an, wenn das Video zugeschnitten ist.
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: Avencvideoencodedimension-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f63d0a5c0d1c6af7c20620c315ad25c16eac528
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341090"
---
# <a name="avencvideoencodedimension-property"></a>Avencvideoencodedimension (Eigenschaft)

Gibt die Breite und Höhe des codierten Videos an, wenn das Video zugeschnitten ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideoencodedimension**

## <a name="property-value"></a>Eigenschaftswert

Die oberen 16 Bits des Werts enthalten die Breite in Pixel, die unteren 16 Bits enthalten die Höhe in Pixel.

## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Eigenschaft festlegen, um das Eingabe Video Zuschneiden. Die angegebene Größe muss kleiner sein als die Größe der Eingabe Video Frames. Verwenden Sie die Eigenschaft " [**avencvideoencodeoffsetorigin**](avencvideoencodeoffsetorigin-property.md) ", um die linke und die obere Ecke des clippingrechtecks anzugeben.

Encoder können diese Eigenschaft als Funktion zurückgeben.

Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)verwendet.

Für UVC 1,5-Kamera Encoder wird " [avencvideoencodeoffot torigin](avencvideoencodeoffsetorigin-property.md) " nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften der Codec-API](codec-api-properties.md)
</dt> <dt>

[**Icodecapi-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

