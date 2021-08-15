---
description: Legt den Verarbeitungsmodus für den Spracherfassungs-DSP fest.
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
# <a name="mfpkey_wmaaecma_system_mode-property"></a>MFPKEY \_ WMAAECMA \_ \_ -Systemmoduseigenschaft

Legt den Verarbeitungsmodus für den Spracherfassungs-DSP fest.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="applies-to"></a>Gilt für

-   [Spracherfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Der Wert dieser Eigenschaft ist ein Member der [AEC \_ SYSTEM \_ MODE-Enumeration.](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode)

Die -Eigenschaft muss einer der folgenden Werte sein.



| Wert | BESCHREIBUNG                                 |
|-------|---------------------------------------------|
| 0     | Nur AEC-Modus (Audio Echo Cancellation)     |
| 2     | Nur MAP-Modus (Microphone Array Processing, Mikrofonarrayverarbeitung) |
| 4     | AEC- und MAP-Modus                            |
| 5     | Weder AEC noch MAP-Modus                    |



 

Sie müssen diese Eigenschaft festlegen, bevor Sie den Spracherfassungs-DSP verwenden. Nachdem Sie diese Eigenschaft festgelegt haben, können Sie den DSP mit den Standardeinstellungen verwenden oder zusätzliche Eigenschaften festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Spracherfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
