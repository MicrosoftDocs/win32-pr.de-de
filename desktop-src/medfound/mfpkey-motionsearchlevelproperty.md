---
description: Gibt an, wie Farbinformationen in Bewegungssuchvorgängen verwendet werden.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: MFPKEY_MOTIONSEARCHLEVEL-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b53c6bf8f94b2b9817249d96cffbfa0da251dbbcb0545c141230de90f80485af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555410"
---
# <a name="mfpkey_motionsearchlevel-property"></a>MFPKEY \_ MOTIONSEARCHLEVEL-Eigenschaft

Gibt an, wie Farbinformationen in Bewegungssuchvorgängen verwendet werden.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCMotionSearchLevel

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.



| Wert | Verwendete Videoinformationen                           |
|-------|--------------------------------------------------|
| 0     | Nur Luma.                                       |
| 1     | Luma mit nächster ganzzahliger Zahl.                |
| 2     | Luma mit echtem Chroma.                           |
| –1    | Macroblock-adaptive mit true-Blockierung.            |
| –2    | Macroblock-adaptive mit nächster ganzzahliger Zahl. |



 

Standardmäßig führt der Codec die Bewegungssuche nur im Lumakanal aus. Die Einbeziehung von Farbinformationen in die Bewegungsschätzung kann die Qualität codierter Videos erheblich verbessern. Die Bewegungssuche mit Luma und true-Brille ergibt die beste Videoqualität, aber zu den höchsten Leistungskosten. Die beiden dynamischen Modi (-1 und -2) und der Luma mit dem Modus für ganzzahlige Ganzzahlen stellen sinnvolle Kompromisse zwischen Qualität und Leistung dar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




