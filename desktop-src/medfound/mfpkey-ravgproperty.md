---
description: Gibt die durchschnittliche Bitrate in Bits pro Sekunde an, die für die 2-Pass-, Variable-Bit-Rate (VBR)-Codierung verwendet wird.
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: MFPKEY_RAVG-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad15d2445dc2acea1e91f4d01fad6e7bd83edb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367867"
---
# <a name="mfpkey_ravg-property"></a>Mfpkey \_ Ravg (Eigenschaft)

Gibt die durchschnittliche Bitrate in Bits pro Sekunde an, die für die 2-Pass-, Variable-Bit-Rate (VBR)-Codierung verwendet wird.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcavgbitrate

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Bemerkungen

In eingeschränkter und uneingeschränkter VBR ist dieser Wert die durchschnittliche Bitrate während der gesamten Dauer des Inhalts.

Sie müssen diesen Wert für beide Modi der zweistufigen VBR-Codierung festlegen. Nachdem Sie mit dem Verarbeiten von Beispielen begonnen haben, müssen Sie diesen Wert erst Abfragen, wenn Sie mit dem Codieren des Streams fertig sind. Der Encoder interpretiert eine Anforderung für diesen Wert als Signal, dass die Codierungs Sitzung übersteigt. Das nächste Beispiel, das Sie verarbeiten, wird als Anfang einer neuen Sitzung behandelt.

Diese Eigenschaft kann auch am Ende einer 1-Pass-VBR-Codierungs Sitzung gelesen werden.

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

 

 




