---
description: Gibt die gewünschte durchschnittliche Volumeebene der Ausgabe Audioinhalte an.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: MFPKEY_WMADRC_AVGTARGET-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4503161ac6e392a50fd7535592b84ea92d6136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215422"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a>Avgtarget-Eigenschaft für mfpkey \_ wmadrc \_

Gibt die gewünschte durchschnittliche Volumeebene der Ausgabe Audioinhalte an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmadrcaveragetarget

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Siehe Hinweise.

## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert für den Decoder für das dynamische Bereichs Steuerelement festlegen, aber er wirkt sich nur dann aus, wenn die Eigenschaft [mfpkey \_ wmadec \_ drcmode](mfpkey-wmadec-drcmodeproperty.md) festgelegt ist.

> [!Note]  
> Es wird nicht empfohlen, den durchschnittlichen Zielwert festzulegen. Die Anpassung des durchschnittlichen Werts wirkt sich nicht auf den Unterschied zwischen lautstarkem und weichem Sound aus. Stattdessen wird das gesamte durchschnittliche Volume, das während der Wiedergabe unerwünschte Verzerrung verursachen kann, reduziert oder erhöht.

 

Wenn Sie das dynamische Bereichs Steuerelement vom Decoder anfordern, wenn diese Eigenschaft nicht festgelegt ist, berechnet der Codec einen Standardwert.

Verwenden Sie die Eigenschaften [mfpkey \_ wmadrc \_ avgref](mfpkey-wmadrc-avgrefproperty.md) und [mfpkey \_ wmadrc \_ ](mfpkey-wmadrc-peakrefproperty.md) -Eigenschaft, um die entsprechenden Werte für diese Eigenschaft zu berechnen.

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

 

 




