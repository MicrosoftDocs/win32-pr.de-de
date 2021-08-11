---
description: Gibt an, wie oft der Voice Capture-DSP AES (Acoustic Echo Suppression) für das Restsignal ausführt.
ms.assetid: 409b40f8-38eb-49f7-be30-348ab5cdd33a
title: MFPKEY_WMAAECMA_FEATR_AES-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e842bc3064b431437d8bbdfab06c0081ecdb49a8c38288ba4adb78648363c71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242037"
---
# <a name="mfpkey_wmaaecma_featr_aes-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ AES-Eigenschaft

Gibt an, wie oft der Voice Capture-DSP AES (Acoustic Echo Suppression) für das Restsignal ausführt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mithilfe von [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="applies-to"></a>Gilt für

-   [Voice Capture-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Der Voice Capture-DSP kann AES für das Restsignal nach dem Echoabbruch ausführen. Diese Eigenschaft kann den Wert 0, 1 oder 2 haben. Der Standardwert ist 0. Bevor Sie diese Eigenschaft festlegen, müssen Sie die [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE-Eigenschaft](mfpkey-wmaaecma-feature-modeproperty.md) auf VARIANT \_ TRUE festlegen.

Der DSP verwendet diese Eigenschaft nur, wenn die AEC-Verarbeitung aktiviert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Voice Capture-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
