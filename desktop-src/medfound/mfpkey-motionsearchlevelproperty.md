---
description: Gibt an, wie Farbinformationen in Bewegungs Such Vorgängen verwendet werden.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: MFPKEY_MOTIONSEARCHLEVEL-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231c2c0ae70466d41f4bf348ec47ee0a74cb135b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042082"
---
# <a name="mfpkey_motionsearchlevel-property"></a>Mfpkey- \_ Eigenschaft "mutionsearchlevel"

Gibt an, wie Farbinformationen in Bewegungs Such Vorgängen verwendet werden.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcmutionsearchlevel

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.



| Wert | Verwendete Video Informationen                           |
|-------|--------------------------------------------------|
| 0     | Nur Luma.                                       |
| 1     | Luma mit nächster ganzzahligen Chroma.                |
| 2     | Luma mit echtem Chroma.                           |
| -1    | Makroblock-Adaptive mit True Chroma.            |
| -2    | Makroblock-Adaptive mit dem nächstgelegenen ganzzahligen Chroma. |



 

Standardmäßig führt der Codec die Bewegungssuche nur im Luma-Kanal durch. Das Einschließen von Chroma-Informationen in die Bewegungs Schätzung kann die Qualität codierter Videos erheblich verbessern. Die Bewegungssuche mit Luma und True Chroma ergibt die beste Videoqualität, aber mit den höchsten Leistungseinbußen. Die beiden dynamischen Modi (-1 und-2) und die-Eigenschaft mit dem Wert "Luma" mit dem nächstliegenden ganzzahligen Chroma-Modus bietet angemessene Kompromisse zwischen Qualität und Leistung.

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

 

 




