---
description: Gibt die kostenmethode an, die vom Codec verwendet wird, um zu bestimmen, welcher Makroblock Modus verwendet werden soll.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: MFPKEY_MACROBLOCKMODECOSTMETHOD-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289219300a79c67565891c48cec848851c17bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360197"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a>Mfpkey \_ makroblockmodecostmethod (Eigenschaft)

Gibt die kostenmethode an, die vom Codec verwendet wird, um zu bestimmen, welcher Makroblock Modus verwendet werden soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcmacroblockmodecostmethod

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.



| Wert | Verwendete Methode                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| 0     | Traurig/Hadamard. Mit dieser Option wird der Codec so konfiguriert, dass nur die Verzerrung beim Berechnen der Kosten verwendet wird.             |
| 1     | RD-Kosten. Mit dieser Option wird der Codec so konfiguriert, dass sowohl die Rate als auch die Verzerrung beim Berechnen der Kosten berücksichtigt werden. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[mfpkey- \_ Methode "mutionmatchmethod"](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




