---
description: Gibt das Ausgabeformat für den Decoder an.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: AVDecCommonOutputFormat-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 129f9a1171c5870eab243108fc0ed6992be4993b886cbd36d72fe91988f321b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586750"
---
# <a name="avdeccommonoutputformat-property"></a>AVDecCommonOutputFormat (Eigenschaft)

Gibt das Ausgabeformat für den Decoder an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecCommonOutputFormat**

## <a name="property-value"></a>Eigenschaftswert



| GUID                                                               | Beschreibung                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM                        | PCM-Audio mit einer beliebigen Anzahl von Kanälen                                                                                                                                                                             |
| \_CODECAPI-GUID \_ AVDecAudioOutputFormat \_ \_ PCM-Benutzeroberflächen            | Stereo-PCM-Audio mit Downmix von links/rechts (Lo/Ro)                                                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ Stereo \_ Auto          | Stereo-PCM-Audio mit automatischer Auswahl des Stereo-Downmixmodus (Lo/Ro oder Lt/Rt). Sie können diesen Wert für Audioformate verwenden, in denen der Eingabestream den bevorzugten Downmixmodus definiert, z. B. Dolby AC-3. |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ Stereo \_ MatrixEncoded | Stereo-PCM-Audio mit matrixcodiertem Stereo-Downmix (Lt/Rt)                                                                                                                                                       |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ CODIF \_ Bitstream           | S/PDIF (Format der digitalen Schnittstelle/Desa) komprimierter Bitstream gemäß IEC-60958                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ CODIF \_ PCM                 | S/PDIF PCM Stereo gemäß IEC-60958                                                                                                                                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




