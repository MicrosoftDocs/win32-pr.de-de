---
description: Gibt an, ob der Codec die Optimierung der Videoskalierung verwendet.
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: MFPKEY_VIDEOSCALING-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2dc069d70b167dd8da6cb308d70149aec1028f3aaf4e50b5c1cc8ab11104c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887651"
---
# <a name="mfpkey_videoscaling-property"></a>MFPKEY \_ VIDEOSCALING-Eigenschaft

Gibt an, ob der Codec die Optimierung der Videoskalierung verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCVideoScaling

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Hinweise

Die Videoskalierung ist eine Art von wahrnehmbarer Optimierung, die die visuelle Qualität von Video, das mit niedrigen Bitraten codiert ist, verbessern kann. Die Optimierung der Videoskalierung reduziert ausgesprochene Artefakte, kann aber Bilddetails verungern. Diese Optimierung wirkt sich wie unten beschrieben auf den Lumabereich des codierten Videos aus, wirkt sich jedoch nicht auf die physische Auflösung des Ausgabevideos aus.

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.



| Wert | BESCHREIBUNG                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| 0     | Die Videoskalierung wird nicht verwendet.                                                                                       |
| 1     | Der Encoder verwendet die konservative Videoskalierungsoptimierung. Der Lumabereich wird von 0...255 auf 26...229 skaliert. |
| 2     | Der Encoder verwendet eine aggressive Videoskalierungsoptimierung. Der Lumabereich wird von 0...255 auf 31...224 skaliert.   |



 

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

 

 




