---
description: Gibt das Puffer Fenster (in Millisekunden) eines eingeschränkten VBR-Streams (Variable-Bitrate) mit der durchschnittlichen Bitrate an (angegeben durch mfpkey \_ Ravg).
ms.assetid: 7eabceb5-976e-4ebc-9042-9c203044634c
title: MFPKEY_BAVG-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cc9984b803fc37c84fee032f95098c52a9b47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349390"
---
# <a name="mfpkey_bavg-property"></a>Mfpkey- \_ bavg (Eigenschaft)

Gibt das Puffer Fenster (in Millisekunden) eines eingeschränkten VBR-Streams (Variable-Bitrate) mit der durchschnittlichen Bitrate an (angegeben durch [mfpkey \_ Ravg](mfpkey-ravgproperty.md)).

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcbavg

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Kein Standardwert, aber der Codec berechnet einen entsprechenden Wert auf der Grundlage der anderen eingeschränkten VBR-Einstellungen.

## <a name="remarks"></a>Bemerkungen

Dieser Wert wird nach dem letzten Codierungs Durchlauf durch den Codec berechnet. Sie sollten diesen Wert erst Abfragen, wenn die Codierung beendet ist. Der Codec interpretiert eine Anforderung für diesen Wert als Signal, dass die Codierungs Sitzung übersteigt. Das nächste Beispiel, das Sie verarbeiten, wird als Anfang einer neuen Sitzung behandelt.

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

 

 




