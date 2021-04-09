---
description: Gibt die linke und die obere Ecke des clippingrechtecks an, wenn das Video zugeschnitten ist.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: Avencvideoencodeoffctorigin-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db4d685942b8c21f2d5047003f2172c54b1d50d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124226"
---
# <a name="avencvideoencodeoffsetorigin-property"></a>Avencvideoencodeoffctorigin (Eigenschaft)

Gibt die linke und die obere Ecke des clippingrechtecks an, wenn das Video zugeschnitten ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideoencodeoffantorigin**

## <a name="property-value"></a>Eigenschaftswert

Die oberen 16 Bits des Werts enthalten den Offset vom linken Rand des Eingabe Rahmens in Pixel. Die unteren 16 Bits enthalten den Offset vom oberen Rand des Eingabe Rahmens in Pixel.

## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Eigenschaft festlegen, um das Eingabe Video Zuschneiden. Verwenden Sie die Eigenschaft " [**avencvideoencodedimension**](avencvideoencodedimension-property.md) ", um die Breite und Höhe des clippingrechtecks anzugeben.

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

 

 




