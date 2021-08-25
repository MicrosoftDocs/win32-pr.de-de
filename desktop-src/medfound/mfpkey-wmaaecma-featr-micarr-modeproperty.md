---
description: Gibt an, wie der Voice Capture-DSP die Verarbeitung von Mikrofonarrays durchführt.
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: MFPKEY_WMAAECMA_FEATR_MICARR_MODE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb948ff15655ccbdc0bf647194b2f6d3d7d1a40c36da32f6d65479152c76c3e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953520"
---
# <a name="mfpkey_wmaaecma_featr_micarr_mode-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ MODE-Eigenschaft

Gibt an, wie der Voice Capture-DSP die Verarbeitung von Mikrofonarrays durchführt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

MICARRAY \_ SINGLE \_ BALKEN

## <a name="applies-to"></a>Gilt für

-   [Voice Capture-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Der Wert dieser Eigenschaft ist ein Member der [MIC \_ ARRAY \_ MODE-Enumeration.](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) Der Standardwert ist MICARRAY \_ SINGLE \_ BALKEN. Vor dem Festlegen dieser Eigenschaft müssen Sie die [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE-Eigenschaft](mfpkey-wmaaecma-feature-modeproperty.md) auf VARIANT \_ TRUE festlegen.

Der DSP verwendet diese Eigenschaft nur, wenn die Mikrofonarrayverarbeitung aktiviert ist.

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

 

 
