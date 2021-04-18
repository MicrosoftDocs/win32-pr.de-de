---
description: Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der maximalen Bitrate (angegeben durch mfpkey Rmax) in Millisekunden an \_ .
ms.assetid: ef27b179-4d9b-4ce7-867a-f62b0f9b735d
title: MFPKEY_BMAX-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaca172e97c27e6e8d97902fbe3c969efc933eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351549"
---
# <a name="mfpkey_bmax-property"></a>Mfpkey ( \_ bmax-Eigenschaft)

Gibt das Puffer Fenster eines eingeschränkten VBR (Variable-Bit-Rate)-Streams mit der maximalen Bitrate (angegeben durch [mfpkey \_ Rmax](mfpkey-rmaxproperty.md)) in Millisekunden an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcbmax

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Keine Standardeinstellung.

## <a name="remarks"></a>Bemerkungen

Sie müssen diesen Wert für die VBR-Codierung mit hoher Einschränkung festlegen. Nachdem Sie mit dem Verarbeiten von Beispielen begonnen haben, müssen Sie diesen Wert erst Abfragen, wenn Sie mit dem Codieren des Streams fertig sind. Der Codec interpretiert eine Anforderung für diesen Wert als Signal, dass die Codierungs Sitzung übersteigt. Das nächste Beispiel, das Sie verarbeiten, wird als Anfang einer neuen Sitzung behandelt.

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

 

 




