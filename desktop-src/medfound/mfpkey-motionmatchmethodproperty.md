---
description: Gibt die Methode an, die für den Bewegungs Vergleich verwendet werden soll.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: MFPKEY_MOTIONMATCHMETHOD-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09496e714633dd394f55122b7461f29a2daa3656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959416"
---
# <a name="mfpkey_motionmatchmethod-property"></a>Mfpkey- \_ Eigenschaft "mutionmatchmethod"

Gibt die Methode an, die für den Bewegungs Vergleich verwendet werden soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcmutionmatchmethod

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.



| Wert | Verwendete Methode                       |
|-------|-----------------------------------|
| 0     | Summe der absoluten Unterschiede (traurig) |
| 1     | Hadamard                          |
| -1    | Makroblock-Adaptive.              |



 

Die Summe der absoluten Unterschiede (Sad) ist eine schnellere, aber weniger genaue Methode als die Hadamard-Transformation. Die Hadamard-Transformation ist präziser, aber Rechen intensiv. Der Makroblock-Adaptive Modus stellt einen angemessenen Kompromiss zwischen den beiden Methoden dar, indem zwischen den beiden Transformationen dynamisch ausgewählt wird, wobei die Hadamard-Transformation nur bei Bedarf ausgewählt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




