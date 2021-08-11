---
description: Gibt an, ob der codierte Videobitstream einen Pufferfüllwert mit jedem Keyframe enthält.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: MFPKEY_BUFFERFULLNESSINFIRSTBYTE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 087b505680dfc3c51fe2cb50cdae76a425ca2ff5798356e9893794d47a7e22e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242999"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a>MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE-Eigenschaft

Gibt an, ob der codierte Videobitstream einen Pufferfüllwert mit jedem Keyframe enthält.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCBufferFullnessInFirstByte

## <a name="data-type"></a>Datentyp

VT \_ BOOL

## <a name="remarks"></a>Hinweise

Sie müssen einen Ausgabetyp festlegen, bevor Sie diesen Wert abrufen.

Sie können den Wert dieser Eigenschaft mithilfe von [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop)abrufen. Wenn Sie **IPropertyBag** verwenden, müssen Sie zuerst den FOURCC-Wert des gewünschten komprimierten Formats mit der [MFPKEY \_ FOURCC-Eigenschaft](mfpkey-fourccproperty.md) festlegen.

Wenn die Pufferfülle im ersten Byte aller Keyframes vorhanden ist, können Sie die Puffergröße bestimmen, die beim Verketten komprimierter Videostreams erforderlich ist.

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

 

 




