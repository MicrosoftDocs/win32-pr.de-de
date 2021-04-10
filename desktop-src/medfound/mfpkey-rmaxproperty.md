---
description: Gibt die Spitzen Bitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-VBR-Wiedergabe verwendet wird.
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: MFPKEY_RMAX-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3568e0a3ee506640200413a5dc222c7cccec2215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215483"
---
# <a name="mfpkey_rmax-property"></a>Mfpkey- \_ Rmax-Eigenschaft

Gibt die Spitzen Bitrate in Bits pro Sekunde an, die für die eingeschränkte 2-Pass-VBR-Wiedergabe verwendet wird.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcmaxbitrate

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Keine Standardeinstellung.

## <a name="remarks"></a>Bemerkungen

Dieser Wert stellt die Spitzen Bitrate für die Wiedergabe dar. Der Wert von [mfpkey \_ bmax](mfpkey-bmaxproperty.md) wird verwendet, um den Puffer in Bezug auf diese Bitrate zu beschreiben. der eingeschränkte VBR ähnelt der konstanten Bitrate (CBR) und verwendet diesen Wert als Bitrate. Ein eingeschränkter VBR-Datenstrom kann jedoch mit einer niedrigeren Bitrate wiedergegeben werden, solange der Puffer erweitert wird.

Sie müssen diesen Wert für die mit hoher Last beschränkte VBR-Codierung mit zwei bestanden festlegen. Nachdem Sie mit dem Verarbeiten von Beispielen begonnen haben, müssen Sie diesen Wert erst Abfragen, wenn Sie mit dem Codieren des Streams fertig sind. Der Encoder interpretiert eine Anforderung für diesen Wert als Signal, dass die Codierungs Sitzung übersteigt. Das nächste Beispiel, das Sie verarbeiten, wird als Anfang einer neuen Sitzung behandelt.

In der Regel ist dieser Wert zwei bis dreimal größer als der Wert von [mfpkey \_ Ravg](mfpkey-ravgproperty.md).

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

 

 




