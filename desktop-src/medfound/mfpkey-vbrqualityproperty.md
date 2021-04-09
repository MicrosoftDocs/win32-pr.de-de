---
description: Gibt die tatsächliche Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (Variable-Bitrate) an.
ms.assetid: e45d583a-323b-4394-9df3-949a3f713708
title: MFPKEY_VBRQUALITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dff57fc27b952780737d63fa8f04faf722ed8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959410"
---
# <a name="mfpkey_vbrquality-property"></a>Mfpkey \_ vbrquality (Eigenschaft)

Gibt die tatsächliche Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (Variable-Bitrate) an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcvbrquality, g \_ wszwmcpaudiovbrquality

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Bemerkungen

Nicht alle Werte im Bereich haben eine eindeutige Bedeutung. Die Werte, die einen Schritt in der Qualität der vorherigen Ebene darstellen, sind: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97 und 100.

Für audioencoderobjekte werden die Qualitäts Modi in der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur der Ausgabetypen bereitgestellt, die Sie mithilfe von [**imediaobject:: getoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Auflisten von Audiotypen für bestimmte Codierungs Modi](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
