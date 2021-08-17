---
description: Gibt eine zwischengeschaltete Framehöhe für codiertes Video an.
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: MFPKEY_FORCEFRAMEHEIGHT-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6e3d423fe96173829b31a889764d5423db88b5c882d853b3e0f770d17dd4691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463450"
---
# <a name="mfpkey_forceframeheight-property"></a>MFPKEY \_ FORCEFRAMEHEIGHT-Eigenschaft

Gibt eine zwischengeschaltete Framehöhe für codiertes Video an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCForceFrameHeight

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Hinweise

Sie können diesen Wert und die [MFPKEY \_ FORCEFRAMEWIDTH-Eigenschaft](mfpkey-forceframewidthproperty.md) festlegen, um zu erzwingen, dass der Encoder den Videostream mit einer Framegröße codiert, die kleiner als die Größe des Eingabe- oder Ausgabeframes ist. Bei der Decodierung wird die Größe des Videos auf die ursprüngliche Eingabeauflösung geändert.

Gültige Rahmendimensionen auf beiden Achsen sind 2 bis 8192 Pixel. Rahmendimensionen müssen durch 2 teilbar sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




