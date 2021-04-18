---
description: Gibt die gewünschte maximale Volumeebene der Ausgabe Audioinhalte an.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: MFPKEY_WMADRC_PEAKTARGET-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c40fa68e2b580c5d3e8550d6e46c9f6b9fe4bfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345267"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a>Mfpkey \_ wmadrc- \_ Eigenschaft "Peer Ziel"

Gibt die gewünschte maximale Volumeebene der Ausgabe Audioinhalte an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmadrcpeer Target

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Siehe Hinweise.

## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert für den Decoder für das dynamische Bereichs Steuerelement festlegen, aber er wirkt sich nur dann aus, wenn die Eigenschaft [mfpkey \_ wmadec \_ drcmode](mfpkey-wmadec-drcmodeproperty.md) festgelegt ist.

Wenn Sie das dynamische Bereichs Steuerelement vom Decoder anfordern, wenn diese Eigenschaft nicht festgelegt ist, berechnet der Codec einen Standardwert.

Verwenden Sie die Eigenschaften [mfpkey \_ wmadrc \_ avgref](mfpkey-wmadrc-avgrefproperty.md) und [mfpkey \_ wmadrc \_ ](mfpkey-wmadrc-peakrefproperty.md) -Eigenschaft, um die entsprechenden Werte für diese Eigenschaft zu berechnen.

Weitere Informationen zur Steuerung des dynamischen Bereichs finden Sie im Webartikel [Windows Media Audio Professional-Codec-Features](/previous-versions/ms867218(v=msdn.10)).

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

 

 
