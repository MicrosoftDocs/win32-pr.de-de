---
description: Gibt an, ob der codierte videobit-Stream einen Puffer Füllwert mit jedem Keyframe enthält.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: MFPKEY_BUFFERFULLNESSINFIRSTBYTE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350922"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a>Mfpkey \_ bufferfullnessinfirstbyte (Eigenschaft)

Gibt an, ob der codierte videobit-Stream einen Puffer Füllwert mit jedem Keyframe enthält.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcbufferfullnessinfirstbyte

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="remarks"></a>Bemerkungen

Sie müssen einen Ausgabetyp festlegen, bevor Sie diesen Wert erhalten.

Sie können den Wert dieser Eigenschaft mithilfe von [iwmcodecprop:: getcodecprop](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop)erhalten. Wenn Sie **IPropertyBag** verwenden, müssen Sie zuerst den FourCC-Wert des gewünschten komprimierten Formats mit der Eigenschaft " [mfpkey \_ FourCC](mfpkey-fourccproperty.md) " festlegen.

Wenn Sie die Puffergröße im ersten Byte aller Keyframes haben, können Sie die erforderliche Puffergröße beim Verketten komprimierter Videostreams ermitteln.

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

 

 




