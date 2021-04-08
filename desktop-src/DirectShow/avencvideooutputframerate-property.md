---
description: Gibt die Framerate für den Ausgabestream des Encoders in Frames pro Sekunde an.
ms.assetid: 72e16c7d-977e-4269-9576-afc789e31826
title: Avencvideooutputframerate-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4cb675c266d146936a3402934e51486ded5b02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746232"
---
# <a name="avencvideooutputframerate-property"></a>Avencvideooutputframerate (Eigenschaft)

Gibt die Framerate für den Ausgabestream des Encoders in Frames pro Sekunde an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideooutputframerate**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Verhältnis, das die Framerate definiert. Die oberen 32 Bits enthalten den Zähler, und die unteren 32 Bits enthalten den Nenner. In der folgenden Tabelle werden allgemeine Frameraten in Frames pro Sekunde angezeigt.



| Bildfrequenz | Seitenverhältnis      |
|------------|------------|
| 23,97      | 24000/1001 |
| 24         | 24/1       |
| 25         | 25/1       |
| 29,97      | 30000/1001 |
| 30         | 30/1       |
| 50         | 50/1       |
| 59,94      | 60000/1001 |
| 60         | 60/1       |



 

## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Eigenschaft festlegen, um die Ausgabe Frame Rate anzugeben. Encoder können diese Eigenschaft auch als Funktion zurückgeben. Abhängig vom Encoder ist der Wert möglicherweise auf die Eingabe Frame Rate beschränkt. Wenn dies nicht der Fall ist, kann der Encoder die Framerate intern konvertieren. Siehe die [**Eigenschaft "avencvideooutputframerateconversion**](avencvideooutputframerateconversion-property.md)".

Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)verwendet.

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

 

