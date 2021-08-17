---
description: Legt den Verarbeitungsmodus für den Voice Capture-DSP fest.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: MFPKEY_WMAAECMA_SYSTEM_MODE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722b3e502b783f98ef4871cfc6dd184389dfce7f7f942bde1827468e96f5fa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973269"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a>MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE-Eigenschaft

Legt den Verarbeitungsmodus für den Voice Capture-DSP fest.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="applies-to"></a>Gilt für

-   [Voice Capture-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Der Wert dieser Eigenschaft ist ein Member der [AEC \_ SYSTEM \_ MODE-Enumeration.](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode)

Die -Eigenschaft muss einer der folgenden Werte sein.



| Wert | Beschreibung                                 |
|-------|---------------------------------------------|
| 0     | AEC-Modus (Audio Echo Cancellation)     |
| 2     | Nur-Mikrofon-Arrayverarbeitungsmodus (MAP) |
| 4     | AEC- und MAP-Modus                            |
| 5     | Weder AEC noch MAP-Modus                    |



 

Sie müssen diese Eigenschaft festlegen, bevor Sie den Voice Capture-DSP verwenden. Nachdem Sie diese Eigenschaft festgelegt haben, können Sie den DSP mit seinen Standardeinstellungen verwenden oder zusätzliche Eigenschaften festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Voice Capture-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
