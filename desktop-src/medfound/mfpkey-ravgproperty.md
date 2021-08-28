---
description: Gibt die durchschnittliche Bitrate in Bits pro Sekunde an, die für die VBR-Codierung (Variable-Bit-Rate) mit zwei Durchlaufwerten verwendet wird.
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: MFPKEY_RAVG-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90fd5435498a8a0c247d9363f02e2e767b46c5ab17ce36cc5a41feab54ed5277
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113290"
---
# <a name="mfpkey_ravg-property"></a>\_MFPKEY-EIGENSCHAFT "MICG"

Gibt die durchschnittliche Bitrate in Bits pro Sekunde an, die für die VBR-Codierung (Variable-Bit-Rate) mit zwei Durchlaufwerten verwendet wird.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCAvgBitrate

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Hinweise

Sowohl in eingeschränktem als auch in uneingeschränktem VBR ist dieser Wert die durchschnittliche Bitrate für die Dauer des Inhalts.

Sie müssen diesen Wert für beide Modi der VBR-Codierung mit zwei Durchlaufwerten festlegen. Nachdem Sie mit der Verarbeitung von Beispielen begonnen haben, dürfen Sie diesen Wert erst abfragen, nachdem Sie die Codierung des Streams abgeschlossen haben. Der Encoder interpretiert eine Anforderung für diesen Wert als Signal, dass die Codierungssitzung beendet ist. Das nächste Beispiel, das Sie verarbeiten, wird als Anfang einer neuen Sitzung behandelt.

Diese Eigenschaft kann auch am Ende einer 1-Pass-VBR-Codierungssitzung gelesen werden.

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

 

 




