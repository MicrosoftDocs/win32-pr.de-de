---
description: Gibt an, ob der Voice Capture-DSP den Mikrofongewinn umgibt.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d00e906ec953e2fd00d9c288336c322c2d0dc07ea1c2d74a014ab78ae21acd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113150"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a>MFPKEY \_ WMAAECMA \_ MIC GAIN \_ \_ BOUNDER-Eigenschaft

Gibt an, ob der Voice Capture-DSP den Mikrofongewinn umgibt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

VT \_ BOOL

## <a name="default-value"></a>Standardwert

VARIANT \_ TRUE

## <a name="applies-to"></a>Gilt für

-   [Voice Capture-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Durch die Mikrofongewinngrenze wird sichergestellt, dass das Mikrofon den richtigen Gewinn hat. Wenn der Gewinn zu hoch ist, ist das erfasste Signal möglicherweise übersättigt und wird abgeschnitten. Clipping ist ein nicht linearer Effekt, der dazu führen wird, dass der AEC-Algorithmus (Acoustic Echo Cancellation) fehlschlägt. Wenn der Gewinn zu niedrig ist, ist das Signal-Rausch-Verhältnis niedrig, was auch dazu führen kann, dass der AEC-Algorithmus fehlschlägt oder nicht gut funktioniert.

Diese Eigenschaft kann die folgenden Werte haben.



| Wert          | Beschreibung                       |
|----------------|-----------------------------------|
| VARIANT \_ TRUE  | Aktivieren Sie die Mikrofon-Verstärkungsgrenze.  |
| VARIANT \_ FALSE | Deaktivieren Sie die Mikrofongewinngrenze. |



 

Der Standardwert dieser Eigenschaft ist VARIANT \_ TRUE (aktiviert).

Die Mikrofongewinngrenze gilt nur, wenn der DSP im Quellmodus arbeitet. Im Filtermodus muss die Anwendung sicherstellen, dass das Mikrofon über die richtige Verstärkungsebene verfügt.

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

 

 
