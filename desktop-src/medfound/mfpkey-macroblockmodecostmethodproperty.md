---
description: Gibt die Kostenmethode an, die vom Codec verwendet wird, um zu bestimmen, welcher Makroblockmodus verwendet werden soll.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: MFPKEY_MACROBLOCKMODECOSTMETHOD-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe61be79b07a09d1f55c09b1970c4becbf7aca9818c525420712952bac40db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873284"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a>MFPKEY \_ MACROBLOCKMODECOSTMETHOD-Eigenschaft

Gibt die Kostenmethode an, die vom Codec verwendet wird, um zu bestimmen, welcher Makroblockmodus verwendet werden soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCMacroblockModeCostMethod

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.



| Wert | Verwendete Methode                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| 0     | SAD/Hadamard. Mit dieser Option wird der Codec so konfiguriert, dass bei der Berechnung der Kosten nur Verzerrung verwendet wird.             |
| 1     | RD-Kosten. Mit dieser Option wird der Codec so konfiguriert, dass sowohl die Rate als auch die Verzerrung bei der Berechnung der Kosten berücksichtigt wird. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MFPKEY \_ MOTIONMATCHMETHOD](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




