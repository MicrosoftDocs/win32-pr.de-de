---
description: Gibt die Konformitäts Vorlage für Geräte an, die Sie für die Videocodierung verwenden möchten.
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: MFPKEY_DECODERCOMPLEXITYREQUESTED-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e017361d7e8267d33ecb2cfdbce2a6e79758fac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348319"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a>Mfpkey- \_ decodercomplexityangeforderten-Eigenschaft

Gibt die Konformitäts Vorlage für Geräte an, die Sie für die Videocodierung verwenden möchten.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

1

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcdecodercomplexityangefordert

## <a name="data-type-for-ipropertybag"></a>Datentyp für IPropertyBag

VT \_ BSTR

## <a name="default-value-for-ipropertybag"></a>Standardwert für IPropertyBag

Schlanken

## <a name="remarks"></a>Bemerkungen

Der Codec versucht, den Inhalt mithilfe der Geräte Konformitäts Vorlage zu codieren, die durch diesen Wert angegeben wird. Die tatsächliche Vorlage, der der codierte Inhalt entspricht, kann nach der Codierung von der [mfpkey- \_ decodercomplexityprofile](mfpkey-decodercomplexityprofileproperty.md) -Eigenschaft abgerufen werden.

Diese Eigenschaft muss einen der folgenden Werte aufweisen.



| Wert für IPropertyStore | Wert für IPropertyBag | BESCHREIBUNG         |
|--------------------------|------------------------|---------------------|
| 0                        | El                   | einfaches Profil      |
| 1                        | Schlanken                   | Hauptprofil        |
| 2                        | Erfolgen                   | nicht mehr unterstützt |



 

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

 

 




