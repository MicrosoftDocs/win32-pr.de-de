---
description: Enthält das ursprüngliche Wave-Formattag für einen Audiodatenstrom.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: MF_MT_ORIGINAL_WAVE_FORMAT_TAG-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba89171f9ae2bf3ab99df05bd3ae64b7d52be6d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357082"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a>Das MF \_ MT-Tag- \_ Attribut für ursprüngliches \_ Wellen \_ Format \_

Enthält das ursprüngliche Wave-Formattag für einen Audiodatenstrom.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Bemerkungen

Abhängig von der Quelldatei kann die AVI-Medienquelle dieses Attribut auf den Medientypen festlegen, die es anbietet.

Eine AVI-Datei enthält einen Streamheader für jeden Stream in der Datei. Die AVI-Medienquelle übersetzt den Datenstrom Header in einen Medientyp. Für Audiostreams enthält der Stream-Header ein Formattag, das das Audioformat identifiziert. (Das Formattag ist im **wformattag** -Member der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur enthalten.) In den meisten Fällen konvertiert die AVI-Medienquelle das Formattag direkt in eine Untertyp-GUID, wie im Thema [**audiountertyp-GUIDs**](audio-subtype-guids.md)beschrieben. In einigen Fällen wird das ursprüngliche Formattag jedoch einem anderen Format-Tag zugeordnet, das Äquivalent ist. Wenn dies der Fall ist, speichert die Medienquelle das ursprüngliche Formatierungstag im Medientyp unter Verwendung des "MF \_ MT \_ Original \_ Wave Format"- \_ \_ tagattributs.

Die Format Zuordnungen werden in der Registrierung unter dem folgenden Schlüssel gespeichert:

**HKEY \_ Klassen \_** Stamm \\ **mediafoundung** \\ **mapaudioformattag**

Jeder Eintrag ist ein **DWORD** -Wert. Der Name des Eintrags ist die Dezimal Darstellung des Formattags. Der Wert des Eintrags ist das entsprechende Formattag.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 
