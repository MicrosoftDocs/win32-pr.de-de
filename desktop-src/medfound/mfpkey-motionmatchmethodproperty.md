---
description: Gibt die Methode an, die für den Bewegungsabgleich verwendet werden soll.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: MFPKEY_MOTIONMATCHMETHOD-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec0604acc7dc0634be296e5097c3594dc74e5ceb7bdb7563b48a164cd13b164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119355730"
---
# <a name="mfpkey_motionmatchmethod-property"></a>MFPKEY \_ MOTIONMATCHMETHOD-Eigenschaft

Gibt die Methode an, die für den Bewegungsabgleich verwendet werden soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCMotionMatchMethod

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.



| Wert | Verwendete Methode                       |
|-------|-----------------------------------|
| 0     | Summe der absoluten Unterschiede (SAD) |
| 1     | Hadamard                          |
| –1    | Macroblock-adaptive.              |



 

Die Summe der absoluten Unterschiede (SAD) ist eine schnellere, aber weniger genaue Methode als die Hadamard-Transformation. Die Hadamard-Transformation ist genauer, aber rechenintensiv. Der macroblock-adaptive-Modus bietet eine angemessene Kompromittierung zwischen den beiden Methoden, indem dynamisch zwischen den beiden Transformationen ausgewählt wird und die Hadamard-Transformation nur bei Bedarf ausgewählt wird.

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

 

 




