---
description: Gibt an, ob der Codec beim Codieren den Rauschfilter verwendet.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: MFPKEY_DENOISEOPTION-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f318e294f69095758fe300fce19043c23cf376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347927"
---
# <a name="mfpkey_denoiseoption-property"></a>Mfpkey \_ denoiseoption (Eigenschaft)

Gibt an, ob der Codec beim Codieren den Rauschfilter verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcdenoise-Option

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="default-value"></a>Standardwert

false

## <a name="remarks"></a>Bemerkungen

Der Rauschfilter kann die Qualität von lärmenden Videoquellen verbessern, wie z. b. Film, der große Mengen an Granularität oder Videoaufnahmen enthält. Dieser Filter kann in Live Codierungs Szenarios verwendet werden, in denen die externe Vorverarbeitung keine Option ist.

Dieser Filter sollte für saubere Videoquellen deaktiviert werden, da er die Bildqualität reduzieren kann, wenn die Qualität für den Einstieg geeignet ist.

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

 

 




