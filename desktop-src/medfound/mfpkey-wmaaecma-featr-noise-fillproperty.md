---
description: Gibt an, ob der sprach Erfassungs-DSP Füllvorgänge durchführt.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: MFPKEY_WMAAECMA_FEATR_NOISE_FILL-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c0af2b47767a7798d9b583ac55ad5112ddf1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349091"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a>Mfpkey \_ wmaaecma \_ featr- \_ Rausch \_ Füll Eigenschaft

Gibt an, ob der sprach Erfassungs-DSP Füllvorgänge durchführt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="default-value"></a>Standardwert

Variant \_ true

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Das Füll Füllungs Zeichen fügt eine kleine Menge an Geräuschen zu den Teilen des Signals hinzu, bei denen das Mittel Clipping die restlichen Echo Punkte entfernt hat. Dies führt zu einer besseren Benutzererfahrung als bei der Verwendung von stillen Lücken im Signal.

Diese Eigenschaft kann die folgenden Werte aufweisen.



| Wert          | BESCHREIBUNG            |
|----------------|------------------------|
| Variant \_ true  | Aktivieren Sie Füll Füllung.  |
| Variant \_ false | Deaktivieren Sie die Füll Füllung. |



 

Der Standardwert dieser Eigenschaft ist Variant \_ true (aktiviert). Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.

Der DSP verwendet diese Eigenschaft nur, wenn die AEC-Verarbeitung aktiviert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Sprach Erfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
