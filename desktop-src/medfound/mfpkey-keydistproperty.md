---
description: Gibt die maximale Zeit (in Millisekunden) zwischen Keyframes in der Codec-Ausgabe an.
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: MFPKEY_KEYDIST-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55925811db71f24cf360113aa6d03a325bcdc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864152"
---
# <a name="mfpkey_keydist-property"></a>Mfpkey \_ keydist (Eigenschaft)

Gibt die maximale Zeit (in Millisekunden) zwischen Keyframes in der Codec-Ausgabe an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvckeyframedistance

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Der Standardwert hängt davon ab, welche Version von Windows ausgeführt wird, wie in der folgenden Tabelle dargestellt.



| Betriebssystem | Standardwert |
|------------------|---------------|
| Windows XP       | 8.000          |
| Windows Vista    | 8.000          |
| Windows 7        | 2000          |



 

## <a name="remarks"></a>Bemerkungen

Die interne Logik des Codecs bestimmt den tatsächlichen Speicherort der einzelnen Keyframes. Der Abstand zwischen zwei Keyframes kann kleiner sein als der Wert dieser Eigenschaft, er ist jedoch nie größer.

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

 

 




