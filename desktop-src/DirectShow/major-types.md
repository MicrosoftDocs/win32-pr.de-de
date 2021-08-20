---
description: In der folgenden Tabelle werden die wichtigsten Medientypen beschrieben.
ms.assetid: 718a07f6-e2e4-4670-b9cf-982b53abffd2
title: Haupttypen (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3764bffabb85b3b054fc7589d4eae9677adbc8835d0e4aa3029d31834eb887c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153242"
---
# <a name="major-types"></a>Haupttypen

In der folgenden Tabelle werden die wichtigsten Medientypen beschrieben.



| GUID                                                                                                                                                                                                                                  | Beschreibung                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="MEDIATYPE_AnalogAudio"></span><span id="mediatype_analogaudio"></span><span id="MEDIATYPE_ANALOGAUDIO"></span><dl> <dt>**MEDIATYPE \_ AnalogAudio**</dt> </dl>         | Analoge Audiodaten.<br/>                                                                                  |
| <span id="MEDIATYPE_AnalogVideo"></span><span id="mediatype_analogvideo"></span><span id="MEDIATYPE_ANALOGVIDEO"></span><dl> <dt>**MEDIATYPE \_ AnalogVideo**</dt> </dl>         | Analoges Video.<br/>                                                                                  |
| <span id="MEDIATYPE_Audio"></span><span id="mediatype_audio"></span><span id="MEDIATYPE_AUDIO"></span><dl> <dt>**MEDIATYPE \_ Audio**</dt> </dl>                                 | Audio. Weitere Informationen finden Sie unter [Audiountertypen.](audio-subtypes.md)<br/>                                               |
| <span id="MEDIATYPE_AUXLine21Data"></span><span id="mediatype_auxline21data"></span><span id="MEDIATYPE_AUXLINE21DATA"></span><dl> <dt>**MEDIATYPE \_ AUXLine21Data**</dt> </dl> | Daten der Zeile 21. Wird von Untertiteln verwendet. Weitere Informationen finden Sie unter [**Medientypen in Zeile 21.**](line-21-media-types.md)<br/> |
| <span id="MEDIATYPE_File"></span><span id="mediatype_file"></span><span id="MEDIATYPE_FILE"></span><dl> <dt>**\_MEDIATYPE-Datei**</dt> </dl>                                     | Datei. (Veraltet)<br/>                                                                               |
| <span id="MEDIATYPE_Interleaved"></span><span id="mediatype_interleaved"></span><span id="MEDIATYPE_INTERLEAVED"></span><dl> <dt>**MEDIATYPE \_ Interleaved**</dt> </dl>         | Verschachtelte Audio- und Videodaten. Wird für digitale Videos (DV) verwendet.<br/>                                      |
| <span id="MEDIATYPE_LMRT"></span><span id="mediatype_lmrt"></span><dl> <dt>**MEDIATYPE \_ LMRT**</dt> </dl>                                                                      | Veraltet. Darf nicht verwendet werden.<br/>                                                                          |
| <span id="MEDIATYPE_Midi"></span><span id="mediatype_midi"></span><span id="MEDIATYPE_MIDI"></span><dl> <dt>**\_MEDIATYPE- Und -Medientyp**</dt> </dl>                                     | FORMAT DER FORMAT-.<br/>                                                                                   |
| <span id="MEDIATYPE_MPEG2_PES"></span><span id="mediatype_mpeg2_pes"></span><dl> <dt>**MEDIATYPE \_ MPEG2 \_ PES**</dt> </dl>                                                      | MPEG-2 PES-Pakete. Weitere Informationen finden Sie unter [MPEG-2-Medientypen.](mpeg-2-media-types.md)<br/>                          |
| <span id="MEDIATYPE_MPEG2_SECTIONS"></span><span id="mediatype_mpeg2_sections"></span><dl> <dt>**MEDIATYPE \_ \_ MPEG2-ABSCHNITTE**</dt> </dl>                                       | MPEG-2-Abschnittsdaten. Weitere Informationen finden Sie unter [MPEG-2-Medientypen.](mpeg-2-media-types.md)<br/>                         |
| <span id="MEDIATYPE_ScriptCommand"></span><span id="mediatype_scriptcommand"></span><span id="MEDIATYPE_SCRIPTCOMMAND"></span><dl> <dt>**MEDIATYPE \_ ScriptCommand**</dt> </dl> | Daten sind ein Skriptbefehl, der von Untertiteln verwendet wird.<br/>                                             |
| <span id="MEDIATYPE_Stream"></span><span id="mediatype_stream"></span><span id="MEDIATYPE_STREAM"></span><dl> <dt>**\_MEDIATYPE-Stream**</dt> </dl>                             | Bytestream ohne Zeitstempel. Weitere Informationen finden Sie unter [**Stream-Untertypen.**](stream-subtypes.md)<br/>               |
| <span id="MEDIATYPE_Text"></span><span id="mediatype_text"></span><span id="MEDIATYPE_TEXT"></span><dl> <dt>**\_MEDIATYPE-Text**</dt> </dl>                                     | Text.<br/>                                                                                          |
| <span id="MEDIATYPE_Timecode"></span><span id="mediatype_timecode"></span><span id="MEDIATYPE_TIMECODE"></span><dl> <dt>**\_MEDIATYPE-Zeitcode**</dt> </dl>                     | Zeitcodedaten. Hinweis: DirectShow stellt keine Filter bereit, die diesen Medientyp unterstützen.<br/>     |
| <span id="MEDIATYPE_URL_STREAM"></span><span id="mediatype_url_stream"></span><dl> <dt>**MEDIATYPE \_ URL \_ STREAM**</dt> </dl>                                                   | Veraltet. Darf nicht verwendet werden.<br/>                                                                          |
| <span id="MEDIATYPE_VBI"></span><span id="mediatype_vbi"></span><dl> <dt>**\_MEDIATYPE-VBI**</dt> </dl>                                                                         | Daten zum vertikalen Leerraumintervall (Vertical Blanking Interval, VBI) (für Fernsehgerät). Identisch mit KSDATAFORMAT \_ TYPE \_ VBI.<br/>       |
| <span id="MEDIATYPE_Video"></span><span id="mediatype_video"></span><span id="MEDIATYPE_VIDEO"></span><dl> <dt>**\_MEDIATYPE-Video**</dt> </dl>                                 | Video. Weitere Informationen finden Sie unter [Videountertypen.](video-subtypes.md)<br/>                                               |



## <a name="remarks"></a>Hinweise

Die Untertyp-GUID definiert das Format weiter. Bei einigen Formaten kann die Untertyp-GUID MEDIASUBTYPE \_ None sein, was bedeutet, dass das Format keinen Untertyp erfordert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 




