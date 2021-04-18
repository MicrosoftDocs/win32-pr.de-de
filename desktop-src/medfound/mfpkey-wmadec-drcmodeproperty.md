---
description: Gibt den dynamischen Bereichs Steuerungs Modus an, den der Audiodecoder verwendet.
ms.assetid: 0dbe0c40-39ac-4c1b-9da2-9b142b5bb0eb
title: MFPKEY_WMADEC_DRCMODE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb612e08ff8bd799ec94faae68763f04db8ad052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215045"
---
# <a name="mfpkey_wmadec_drcmode-property"></a>Mfpkey \_ wmadec \_ drcmode (Eigenschaft)

Gibt den dynamischen Bereichs Steuerungs Modus an, den der Audiodecoder verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmacdrcsetting

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Dieser ganzzahlige Wert liegt zwischen 0 und 2. Umso größer der Wert, desto kleiner der dynamische Bereich der nicht komprimierten Audioausgabe. Der Wert 0 signalisiert dem Codec, dass kein dynamisches Bereichs Steuerelement durchgeführt werden soll, d. h., der Codec ändert nicht den inhärenten dynamischen Bereich des codierten Inhalts.

Wenn dieser Wert auf 1 oder 2 festgelegt ist, verwendet der Codec die folgenden Eigenschaften, um das erforderliche dynamische Bereichs Steuerelement zu bestimmen:

-   [mfpkey \_ wmadrc \_ avgref](mfpkey-wmadrc-avgrefproperty.md)
-   [mfpkey \_ wmadrc- \_ Peer-Ref](mfpkey-wmadrc-peakrefproperty.md)
-   [mfpkey \_ wmademokratische \_ avgtarget](mfpkey-wmadrc-avgtargetproperty.md)
-   [mfpkey \_ wmadrc- \_ Peer Ziel](mfpkey-wmadrc-peaktargetproperty.md)

Wenn Sie keine Zielwerte angeben, stellt der Codec seinen eigenen bereit.

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

 

 




