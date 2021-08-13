---
description: Gibt an, ob der Voice Capture-DSP die automatische Verstärkungssteuerung ausführt.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: MFPKEY_WMAAECMA_FEATR_AGC-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f038b18657363677e0953f8fe973c2e3029130ffc2183a08344e1b0cd6905747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343810"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ AGC-Eigenschaft

Gibt an, ob der Voice Capture-DSP die automatische Verstärkungssteuerung ausführt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mithilfe von [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

VT \_ BOOL

## <a name="default-value"></a>Standardwert

VARIANT \_ FALSE

## <a name="applies-to"></a>Gilt für

-   [Voice Capture-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Die automatische Verstärkungssteuerung ist eine DSP-Komponente (Digital Signal Processing), mit der der Gewinn so angepasst wird, dass die Ausgabeebene des Signals innerhalb des gleichen ungefähren Bereichs bleibt.

Diese Eigenschaft kann die folgenden Werte haben.



| Wert          | BESCHREIBUNG                     |
|----------------|---------------------------------|
| VARIANT \_ FALSE | Deaktivieren Sie die automatische Verstärkungssteuerung. |
| VARIANT \_ TRUE  | Aktivieren Sie die automatische Verstärkungssteuerung.  |



 

Der Standardwert dieser Eigenschaft ist VARIANT \_ FALSE (deaktiviert). Bevor Sie diese Eigenschaft festlegen, müssen Sie die [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE-Eigenschaft](mfpkey-wmaaecma-feature-modeproperty.md) auf VARIANT \_ TRUE festlegen.

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

 

 
