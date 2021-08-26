---
description: Gibt an, ob der Codec beim Codieren den Rauschfilter verwendet.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: MFPKEY_DENOISEOPTION-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0483edbda1c2eb3ec929fb662fe4544cb09e7d43dfd1b30421d14eb06d2a365b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954070"
---
# <a name="mfpkey_denoiseoption-property"></a>MFPKEY \_ DENOISEOPTION-Eigenschaft

Gibt an, ob der Codec beim Codieren den Rauschfilter verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCDenoiseOption

## <a name="data-type"></a>Datentyp

VT \_ BOOL

## <a name="default-value"></a>Standardwert

FALSE

## <a name="remarks"></a>Hinweise

Der Rauschfilter kann die Qualität von lauten Videoquellen verbessern, z. B. Film mit viel Grain oder Videoaufnahmen bei geringem Licht. Dieser Filter kann in Livecodierungsszenarien verwendet werden, in denen die externe Vorverarbeitung keine Option ist.

Dieser Filter sollte für bereinigte Videoquellen deaktiviert werden, da er die Imagequalität reduzieren kann, wenn die Qualität gut ist.

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

 

 




