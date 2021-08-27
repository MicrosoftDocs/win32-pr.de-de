---
description: XAudio2-Konstanten, die Standardparameter, Höchstwerte und Flags angeben.
ms.assetid: 074ac40e-a17e-7366-1954-6699407b82f7
title: XAudio2-Begrenzungswerte und -Flags (Xaudio2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11293b55a44b0aefdeacf95b9e36e90a626de2c1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470706"
---
# <a name="xaudio2-boundary-values-and-flags"></a>XAudio2-Begrenzungswerte und -Flags

XAudio2-Konstanten, die Standardparameter, Höchstwerte und Flags angeben.

**XAudio2-Begrenzungswerte**



| Konstante                                                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_MAX_BUFFER_BYTES"></span><span id="xaudio2_max_buffer_bytes"></span><dl> <dt>**XAUDIO2 \_ MAX \_ BUFFER \_ BYTES**</dt> </dl>             | Maximalwert, der für [**XAUDIO2 \_ BUFFER zulässig ist.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Audiobytes.<br/>                                                      |
| <span id="XAUDIO2_MAX_QUEUED_BUFFERS"></span><span id="xaudio2_max_queued_buffers"></span><dl> <dt>**XAUDIO2 \_ \_ MAX. PUFFER IN \_ WARTESCHLANGE**</dt> </dl>       | Maximal zulässige Puffer in einer Sprachwarteschlange.<br/>                                                                                            |
| <span id="XAUDIO2_MAX_BUFFERS_SYSTEM"></span><span id="xaudio2_max_buffers_system"></span><dl> <dt>**XAUDIO2 \_ MAX \_ BUFFERS \_ SYSTEM**</dt> </dl>       | Maximal zulässige Puffer für Systemthreads (nur Xbox 360).<br/>                                                                          |
| <span id="XAUDIO2_MAX_AUDIO_CHANNELS"></span><span id="xaudio2_max_audio_channels"></span><dl> <dt>**XAUDIO2 \_ MAX \_ AUDIO \_ CHANNELS**</dt> </dl>       | Maximalwert, der für **WAVEFORMATEX.nChannels zulässig ist.**<br/>                                                                                |
| <span id="XAUDIO2_MIN_SAMPLE_RATE"></span><span id="xaudio2_min_sample_rate"></span><dl> <dt>**XAUDIO2 \_ MIN \_ SAMPLE \_ RATE**</dt> </dl>                | Unterstützte Mindestrate für Audiostichproben.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_SAMPLE_RATE"></span><span id="xaudio2_max_sample_rate"></span><dl> <dt>**XAUDIO2 \_ MAX \_ SAMPLE \_ RATE**</dt> </dl>                | Maximale unterstützte Audio-Abtastrate.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_VOLUME_LEVEL"></span><span id="xaudio2_max_volume_level"></span><dl> <dt>**XAUDIO2 \_ MAX \_ VOLUME \_ LEVEL**</dt> </dl>             | Maximal zulässige Volumeebene.<br/>                                                                                                        |
| <span id="XAUDIO2_MIN_FREQ_RATIO"></span><span id="xaudio2_min_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ MIN \_ FREQ \_ RATIO**</dt> </dl>                   | Mindestfrequenzverhältnis, das in einer Quellstimme zulässig ist.<br/>                                                                                   |
| <span id="XAUDIO2_MAX_FREQ_RATIO"></span><span id="xaudio2_max_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ MAX \_ FREQ \_ RATIO**</dt> </dl>                   | Maximales Häufigkeitsverhältnis, das in einer Quellstimme zulässig ist.<br/>                                                                                   |
| <span id="XAUDIO2_DEFAULT_FREQ_RATIO"></span><span id="xaudio2_default_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ DEFAULT \_ FREQ \_ RATIO**</dt> </dl>       | Standardwert für das **MaxFrequencyRatio-Argument** [**von IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice).<br/> |
| <span id="XAUDIO2_MAX_FILTER_ONEOVERQ"></span><span id="xaudio2_max_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ MAX \_ FILTER \_ ONEOVERQ**</dt> </dl>    | Maximalwert für [**XAUDIO2-FILTERPARAMETER \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**OneOverQ**.<br/>                                     |
| <span id="XAUDIO2_MAX_FILTER_FREQUENCY"></span><span id="xaudio2_max_filter_frequency"></span><dl> <dt>**XAUDIO2 \_ MAX \_ FILTER \_ FREQUENCY**</dt> </dl> | Maximalwert für [**XAUDIO2-FILTERPARAMETER \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**Häufigkeit.**<br/>                                    |
| <span id="XAUDIO2_MAX_LOOP_COUNT"></span><span id="xaudio2_max_loop_count"></span><dl> <dt>**XAUDIO2 \_ MAX \_ LOOP \_ COUNT**</dt> </dl>                   | Maximalwert, der nicht als Endlosschleife für [**XAUDIO2 \_ BUFFER behandelt wird.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)**LoopCount**.<br/>              |
| <span id="XAUDIO2_MAX_INSTANCES"></span><span id="xaudio2_max_instances"></span><dl> <dt>**XAUDIO2 \_ MAX \_ INSTANCES**</dt> </dl>                       | Maximale Anzahl gleichzeitiger Instanzen von XAudio2, die für Xbox 360.<br/>                                                                       |



**XAudio2-Werte mit besonderer Bedeutung**



| Konstante                                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_COMMIT_NOW"></span><span id="xaudio2_commit_now"></span><dl> <dt>**XAUDIO2 \_ COMMIT \_ NOW**</dt> </dl>                         | Wird als Parameter für Methoden mit einem OperationSet-Argument verwendet. Weitere Informationen finden Sie unter [XAudio2-Vorgangssätze.](xaudio2-operation-sets.md)<br/>                  |
| <span id="XAUDIO2_COMMIT_ALL"></span><span id="xaudio2_commit_all"></span><dl> <dt>**XAUDIO2 \_ COMMIT \_ ALL**</dt> </dl>                         | Wird als Parameter in [**IXAudio2::CommitChanges verwendet.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges)<br/>                                                                   |
| <span id="XAUDIO2_INVALID_OPSET"></span><span id="xaudio2_invalid_opset"></span><dl> <dt>**XAUDIO2 \_ INVALID \_ OPSET**</dt> </dl>                | Gibt einen ungültigen Wert für OperationSet-Argumente an. Weitere Informationen finden Sie unter [XAudio2-Vorgangssätze.](xaudio2-operation-sets.md)<br/>                         |
| <span id="XAUDIO2_NO_LOOP_REGION"></span><span id="xaudio2_no_loop_region"></span><dl> <dt>**XAUDIO2– \_ KEIN \_ \_ SCHLEIFENBEREICH**</dt> </dl>            | Gibt keinen Schleifenbereich an, der in [**XAUDIO2 \_ BUFFER verwendet wird.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)**LoopCount**.<br/>                                                                    |
| <span id="XAUDIO2_LOOP_INFINITE"></span><span id="xaudio2_loop_infinite"></span><dl> <dt>**XAUDIO2-SCHLEIFE \_ \_ UNENDLICH**</dt> </dl>                | Gibt endlose Schleifen an, die in [**XAUDIO2 \_ BUFFER verwendet werden.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)**LoopCount**.<br/>                                                                  |
| <span id="XAUDIO2_DEFAULT_CHANNELS"></span><span id="xaudio2_default_channels"></span><dl> <dt>**\_XAUDIO2-STANDARDKANÄLE \_**</dt> </dl>       | Gibt die Standardanzahl von Kanälen für die aktuelle Plattform an, die in [**IXAudio2::CreateMasteringVoice verwendet wird.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)<br/> |
| <span id="XAUDIO2_DEFAULT_SAMPLERATE"></span><span id="xaudio2_default_samplerate"></span><dl> <dt>**XAUDIO2 \_ DEFAULT \_ SAMPLERATE**</dt> </dl> | Gibt die Standard-Abtastrate für die aktuelle Plattform an, die in [**IXAudio2::CreateMasteringVoice verwendet wird.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)<br/>        |



**XAudio2-Flags**




| Konstante | BESCHREIBUNG | 
|----------|-------------|
| <span id="XAUDIO2_DEBUG_ENGINE"></span><span id="xaudio2_debug_engine"></span><dl><dt><strong>XAUDIO2_DEBUG_ENGINE</strong></dt></dl> | Gibt an, dass die debug-/überprüfte Version der Audio-Engine anstelle der Releaseversion verwendet werden soll. Weitere Informationen <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>finden Sie unter XAudio2Erzeugen von</strong></a>.<br /><blockquote>[!Note]<br />Dieses Flag wird auf -Windows 8- Windows 10.</blockquote><br /> | 
| <span id="XAUDIO2_VOICE_NOPITCH"></span><span id="xaudio2_voice_nopitch"></span><dl><dt><strong>XAUDIO2_VOICE_NOPITCH</strong></dt></dl> | Gibt an, dass eine Quellstimme keine Tonhöhenverschiebung verwendet. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice</strong></a>.<br /> | 
| <span id="XAUDIO2_VOICE_NOSRC"></span><span id="xaudio2_voice_nosrc"></span><dl><dt><strong>XAUDIO2_VOICE_NOSRC</strong></dt></dl> | Gibt an, dass auf einer Quellstimme keine Stichprobenratenkonvertierung verfügbar ist. Die Ausgaben der Stimme müssen dieselbe Abtastrate haben. Siehe <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice</strong></a>.<br /> | 
| <span id="XAUDIO2_VOICE_USEFILTER"></span><span id="xaudio2_voice_usefilter"></span><dl><dt><strong>XAUDIO2_VOICE_USEFILTER</strong></dt></dl> | Gibt an, dass der Filtereffekt auf einer Stimme verfügbar sein soll. Siehe <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice</strong></a> und <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice"><strong>IXAudio2::CreateSubmixVoice</strong></a>.<br /> | 
| <span id="XAUDIO2_PLAY_TAILS"></span><span id="xaudio2_play_tails"></span><dl><dt><strong>XAUDIO2_PLAY_TAILS</strong></dt></dl> | Gibt an, dass eine Stimme weiterhin Eine Effektausgabe ausgibt, nachdem sie beendet wurde. Siehe <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop"><strong>IXAudio2SourceVoice::Stop</strong></a>.<br /> | 
| <span id="XAUDIO2_END_OF_STREAM"></span><span id="xaudio2_end_of_stream"></span><dl><dt><strong>XAUDIO2_END_OF_STREAM</strong></dt></dl> | Gibt den letzten Puffer in einem Stream an. Siehe <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer"><strong>XAUDIO2_BUFFER</strong></a>. <strong>Kennzeichnet</strong>.<br /> | 
| <span id="XAUDIO2_STOP_ENGINE_WHEN_IDLE"></span><span id="xaudio2_stop_engine_when_idle"></span><dl><dt><strong>XAUDIO2_STOP_ENGINE_WHEN_IDLE</strong></dt></dl> | Gibt an, dass die Audio-Engine anhalten soll, wenn keine Quellstimmen gestartet werden, und beim Starten einer Stimme starten soll. Weitere Informationen <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>finden Sie unter XAudio2Erzeugen von</strong></a>.<br /> | 
| <span id="XAUDIO2_SEND_USEFILTER"></span><span id="xaudio2_send_usefilter"></span><dl><dt><strong>XAUDIO2_SEND_USEFILTER</strong></dt></dl> | Gibt an, dass bei einer Sprachsendung ein Filter verwendet werden soll. Siehe <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor"><strong>XAUDIO2_SEND_DESCRIPTOR</strong></a>. <strong>Kennzeichnet</strong>.<br /> | 
| <span id="XAUDIO2_1024_QUANTUM"></span><span id="xaudio2_1024_quantum"></span><dl><dt><strong>XAUDIO2_1024_QUANTUM</strong></dt></dl> | Gibt ein nicht standardmäßiges Verarbeitungsquantum von 21,33 ms an (1.024 Samples bei 48KHz). Weitere Informationen <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>finden Sie unter XAudio2Erzeugen von</strong></a>.<br /> | 
| <span id="XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT"></span><span id="xaudio2_no_virtual_audio_client"></span><dl><dt><strong>XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT</strong></dt></dl> | Gibt an, dass kein virtueller Audioclient verwendet werden soll. Siehe <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice"><strong>IXAudio2::CreateMasteringVoice</strong></a>.<br /><blockquote>[!Note]<br />Auf Geräten der Familie Mobile Geräte wird immer ein virtueller Audioclient verwendet, unabhängig davon, ob dieses Flag verwendet wird.</blockquote><br /> | 




**XAudio2-Standardparameter für den integrierten Sprachfilter**



| Konstante                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_DEFAULT_FILTER_TYPE"></span><span id="xaudio2_default_filter_type"></span><dl> <dt>**\_ \_ XAUDIO2-STANDARDFILTERTYP \_**</dt> </dl>                | Gibt den Standardfiltertyp an, der mit Stimmen und Sprachnachrichten verwendet werden soll.<br/>          |
| <span id="XAUDIO2_DEFAULT_FILTER_FREQUENCY"></span><span id="xaudio2_default_filter_frequency"></span><dl> <dt>**\_ \_ XAUDIO2-STANDARDFILTERHÄUFIGKEIT \_**</dt> </dl> | Gibt die Standardfilterhäufigkeit an, die mit Stimmen und Sprachnachrichten verwendet werden soll.<br/>     |
| <span id="XAUDIO2_DEFAULT_FILTER_ONEOVERQ"></span><span id="xaudio2_default_filter_oneoverq"></span><dl> <dt>**\_XAUDIO2-STANDARDFILTER \_ \_ ONEOVERQ**</dt> </dl>    | Gibt die Standardfilterrate des Verfalls an, die mit Stimmen und Sprachnachrichten verwendet werden soll.<br/> |



## <a name="remarks"></a>Hinweise

### <a name="platform-requirements"></a>Plattformanforderungen

Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Xaudio2.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XAudio2::Constants](constants.md)
</dt> </dl>

 

 
