---
description: Gibt eine zwischengeschaltete Framebreite für codiertes Video an.
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: MFPKEY_FORCEFRAMEWIDTH-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d04e30f5fd5d2ecc7055553e17eaf86199b62be8d3dd861b9f82246947212f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939835"
---
# <a name="mfpkey_forceframewidth-property"></a>MFPKEY \_ FORCEFRAMEWIDTH-Eigenschaft

Gibt eine zwischengeschaltete Framebreite für codiertes Video an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCForceFrameWidth

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Hinweise

Sie können diesen Wert und die [MFPKEY \_ FORCEFRAMEHEIGHT-Eigenschaft](mfpkey-forceframeheightproperty.md) festlegen, um zu erzwingen, dass der Encoder den Videostream mit einer Framegröße codiert, die kleiner als die Größe des Eingabe- oder Ausgabeframes ist. Bei der Decodierung wird die Größe des Videos auf die ursprüngliche Eingabeauflösung geändert.

Gültige Rahmendimensionen auf beiden Achsen sind 2 bis 8192 Pixel. Rahmendimensionen müssen durch 2 teilbar sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




