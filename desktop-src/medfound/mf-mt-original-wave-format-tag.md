---
description: Enthält das ursprüngliche WAVE-Formattag für einen Audiostream.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: MF_MT_ORIGINAL_WAVE_FORMAT_TAG -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89f05086858f54c619e3896f5978cf81005e9b1e80e858bc89c71e951ab48b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741665"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a>\_Tagattribut "MF MT \_ ORIGINAL \_ WAVE \_ \_ FORMAT"

Enthält das ursprüngliche WAVE-Formattag für einen Audiostream.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**BESCHRIFTUNGMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Hinweise

Je nach Quelldatei kann die AVI-Medienquelle dieses Attribut für die von ihr angebotenen Medientypen festlegen.

Eine AVI-Datei enthält einen Streamheader für jeden Stream in der Datei. Die AVI-Medienquelle übersetzt den Streamheader in einen Medientyp. Für Audiostreams enthält der Streamheader ein Formattag, das das Audioformat identifiziert. (Das Formattag ist im **wFormatTag-Member** der [**WAVEFORMATEX-Struktur**](/previous-versions/dd757713(v=vs.85)) enthalten.) In den meisten Fällen konvertiert die AVI-Medienquelle das Formattag direkt in eine Untertyp-GUID, wie im Thema [**Audio Subtype GUIDs beschrieben.**](audio-subtype-guids.md) In einigen Fällen ordnet sie jedoch das ursprüngliche Formattag einem anderen Formattag zu, das äquivalent ist. In diesem Zustand speichert die Medienquelle das ursprüngliche Formattag im Medientyp unter Verwendung des TAG-Attributs MF \_ MT \_ ORIGINAL WAVE \_ \_ \_ FORMAT.

Die Formatzuordnungen werden in der Registrierung unter dem folgenden Schlüssel gespeichert:

**HKEY \_ CLASSES \_ ROOT** \\ **MediaFoundation** \\ **MapAudioFormatTag**

Jeder Eintrag ist ein **DWORD-Wert.** Der Name des Eintrags ist die Dezimaldarstellung des Formattags. Der Wert des Eintrags ist das entsprechende Formattag.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 
