---
description: In der folgenden Tabelle werden die wichtigsten Medientypen beschrieben.
ms.assetid: 718a07f6-e2e4-4670-b9cf-982b53abffd2
title: Haupttypen (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5722cbad713f2fb9ae876e58941bde44c2e110
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358058"
---
# <a name="major-types"></a>Haupttypen

In der folgenden Tabelle werden die wichtigsten Medientypen beschrieben.



| GUID                                                                                                                                                                                                                                  | Beschreibung                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="MEDIATYPE_AnalogAudio"></span><span id="mediatype_analogaudio"></span><span id="MEDIATYPE_ANALOGAUDIO"></span><dl> <dt>**"MediaType" \_ -Analog**</dt> </dl>         | Analoge Audiodaten.<br/>                                                                                  |
| <span id="MEDIATYPE_AnalogVideo"></span><span id="mediatype_analogvideo"></span><span id="MEDIATYPE_ANALOGVIDEO"></span><dl> <dt>**MediaType \_ Analog gvideo**</dt> </dl>         | Analoges Video.<br/>                                                                                  |
| <span id="MEDIATYPE_Audio"></span><span id="mediatype_audio"></span><span id="MEDIATYPE_AUDIO"></span><dl> <dt>**MediaType \_ -Audiodatei**</dt> </dl>                                 | Audio. Siehe [audiountertypen](audio-subtypes.md).<br/>                                               |
| <span id="MEDIATYPE_AUXLine21Data"></span><span id="mediatype_auxline21data"></span><span id="MEDIATYPE_AUXLINE21DATA"></span><dl> <dt>**MediaType \_ AUXLine21Data**</dt> </dl> | Zeile 21-Daten. Wird von Untertiteln verwendet. Siehe [**Zeile 21-Medientypen**](line-21-media-types.md).<br/> |
| <span id="MEDIATYPE_File"></span><span id="mediatype_file"></span><span id="MEDIATYPE_FILE"></span><dl> <dt>**MediaType- \_ Datei**</dt> </dl>                                     | Datei. (Veraltet)<br/>                                                                               |
| <span id="MEDIATYPE_Interleaved"></span><span id="mediatype_interleaved"></span><span id="MEDIATYPE_INTERLEAVED"></span><dl> <dt>**Überlappende \_ mediaType**</dt> </dl>         | Verschachtelte Audiodaten und Videos. Wird für digitales Video (DV) verwendet.<br/>                                      |
| <span id="MEDIATYPE_LMRT"></span><span id="mediatype_lmrt"></span><dl> <dt>**MediaType \_ lmrt**</dt> </dl>                                                                      | Veraltet. Darf nicht verwendet werden.<br/>                                                                          |
| <span id="MEDIATYPE_Midi"></span><span id="mediatype_midi"></span><span id="MEDIATYPE_MIDI"></span><dl> <dt>**MediaType ( \_ MIDI)**</dt> </dl>                                     | Das MIDI-Format.<br/>                                                                                   |
| <span id="MEDIATYPE_MPEG2_PES"></span><span id="mediatype_mpeg2_pes"></span><dl> <dt>**MediaType \_ MPEG2 \_**</dt> </dl>                                                      | MPEG-2-PE-Pakete. Weitere Informationen finden Sie unter [MPEG-2-Medientypen](mpeg-2-media-types.md).<br/>                          |
| <span id="MEDIATYPE_MPEG2_SECTIONS"></span><span id="mediatype_mpeg2_sections"></span><dl> <dt>**Abschnitte zu "MediaType" \_ \_**</dt> </dl>                                       | MPEG-2-Abschnitts Daten. Weitere Informationen finden Sie unter [MPEG-2-Medientypen](mpeg-2-media-types.md).<br/>                         |
| <span id="MEDIATYPE_ScriptCommand"></span><span id="mediatype_scriptcommand"></span><span id="MEDIATYPE_SCRIPTCOMMAND"></span><dl> <dt>**MediaType \_ ScriptCommand**</dt> </dl> | Bei den Daten handelt es sich um einen Skript Befehl, der von Untertiteln verwendet wird.<br/>                                             |
| <span id="MEDIATYPE_Stream"></span><span id="mediatype_stream"></span><span id="MEDIATYPE_STREAM"></span><dl> <dt>**MediaType- \_ Stream**</dt> </dl>                             | Byte Datenstrom ohne Zeitstempel. Siehe Daten [**Strom-Untertypen**](stream-subtypes.md).<br/>               |
| <span id="MEDIATYPE_Text"></span><span id="mediatype_text"></span><span id="MEDIATYPE_TEXT"></span><dl> <dt>**MediaType- \_ Text**</dt> </dl>                                     | Text.<br/>                                                                                          |
| <span id="MEDIATYPE_Timecode"></span><span id="mediatype_timecode"></span><span id="MEDIATYPE_TIMECODE"></span><dl> <dt>**MediaType- \_ Timecode**</dt> </dl>                     | Timecode-Daten. Hinweis: DirectShow stellt keine Filter bereit, die diesen Medientyp unterstützen.<br/>     |
| <span id="MEDIATYPE_URL_STREAM"></span><span id="mediatype_url_stream"></span><dl> <dt>**MediaType- \_ URL- \_ Stream**</dt> </dl>                                                   | Veraltet. Darf nicht verwendet werden.<br/>                                                                          |
| <span id="MEDIATYPE_VBI"></span><span id="mediatype_vbi"></span><dl> <dt>**MediaType \_ VBI**</dt> </dl>                                                                         | Daten des vertikalen Auslassungs Intervalls (VBI) (für das Fernsehen). Identisch mit dem ksdataformat- \_ Typ \_ VBI.<br/>       |
| <span id="MEDIATYPE_Video"></span><span id="mediatype_video"></span><span id="MEDIATYPE_VIDEO"></span><dl> <dt>**MediaType- \_ Video**</dt> </dl>                                 | Video. Siehe [Video-Untertypen](video-subtypes.md).<br/>                                               |



## <a name="remarks"></a>Bemerkungen

Der Untertyp-GUID definiert das Format weiter. Bei manchen Formaten kann der Untertyp "GUID" mediasubtype \_ None lauten, was bedeutet, dass das Format keinen Untertyp erfordert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 




