---
description: Gibt das Komplexitäts Profil des codierten Inhalts an.
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: MFPKEY_DECODERCOMPLEXITYPROFILE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39544830a0a05e21779a637da61d3bcb310fcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864175"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a>Mfpkey- \_ decodercomplexityprofile-Eigenschaft

Gibt das Komplexitäts Profil des codierten Inhalts an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcdecodercomplexityprofile

## <a name="data-type"></a>Datentyp

**VT \_ BSTR**

## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert erst lesen, nachdem die Codierung abgeschlossen wurde.

Für Audiodaten verfügt diese Eigenschaft über einen der folgenden Werte.



| Wert | BESCHREIBUNG                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| L1  | Standard Codierung mit einer Samplingrate von 44,1 kHz und einer maximalen Bitrate von 161 Kbit/s.         |
| L2  | Standard Codierung mit Samplingrate von bis zu 48 kHz und einer maximalen Bitrate von 161 Kbit/s.         |
| L3  | Standard Codierung mit Samplingrate von bis zu 48 kHz und einer maximalen Bitrate von 385 kbit/s.         |
| "M0a" | Professionelle Codierung mit Stichproben Raten von bis zu 48 kHz und Bitraten zwischen 48 und 192 Kbit/s.  |
| "M0b" | Professionelle Codierung mit Stichproben Raten von bis zu 48 kHz und einer maximalen Bitrate von 192 Kbit/s.      |
| M1  | Professionelle Codierung mit Stichproben Raten von bis zu 48 kHz und einer maximalen Bitrate von 384 Kbit/s.      |
| Groß  | Professionelle Codierung mit Stichproben Raten von bis zu 96 kHz und einer maximalen Bitrate von 768 Kbit/s.      |
| Kubikmeter  | Professionelle Codierung mit Stichproben Raten von bis zu 96 kHz und einer maximalen Bitrate von 1,5 MBit/s.      |
| N1  | Verlust lose Codierung mit Stichproben Raten von bis zu 48 kHz und maximal 2 Kanälen.                |
| N2  | Verlust lose Codierung mit Stichproben Raten von bis zu 96 kHz und maximal 6 Kanälen (5,1-umschließende). |
| N3  | Verlust lose Codierung mit Stichproben Raten von bis zu 96 kHz und maximal 8 Kanälen (7,1-umschließende). |



 

Für das Video weist diese Eigenschaft einen der folgenden Werte auf:



| Wert | BESCHREIBUNG                                                                       |
|-------|-----------------------------------------------------------------------------------|
| Unglücks  | Erweitertes Profil (nur auf Windows Media Video 9 Advanced Profile Codec verfügbar) |
| Erfolgen  | nicht mehr unterstützt                                                               |
| Schlanken  | Hauptprofil                                                                      |
| El  | einfaches Profil                                                                    |



 

Für Videoinhalte können Sie eine Profil Ebene anfordern, indem Sie [mfpkey \_ decodercomplexityangeforderten](mfpkey-decodercomplexityrequestedproperty.md) festlegen, bevor Sie mit der Codierung beginnen. Der Codec versucht, in den Parametern der angeforderten Komplexitäts Stufe zu codieren, aber die anderen Einstellungen, die Sie konfigurieren, haben Vorrang. Sie sollten den tatsächlichen Komplexitäts Profil-Wert nach der Codierung immer überprüfen, falls Ihre Anforderung nicht berücksichtigt werden konnte.

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

 

 




