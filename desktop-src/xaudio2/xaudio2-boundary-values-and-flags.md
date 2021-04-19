---
description: XAudio2-Konstanten, die Standardparameter, maximale Werte und Flags angeben.
ms.assetid: 074ac40e-a17e-7366-1954-6699407b82f7
title: XAudio2 Begrenzungs Werte und Flags (XAudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe59f229ea406eb5bf6c6b3f5c124d6d0d19c047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369229"
---
# <a name="xaudio2-boundary-values-and-flags"></a>XAudio2 Begrenzungs Werte und Flags

XAudio2-Konstanten, die Standardparameter, maximale Werte und Flags angeben.

**XAudio2-Begrenzungs Werte**



| Konstante                                                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_MAX_BUFFER_BYTES"></span><span id="xaudio2_max_buffer_bytes"></span><dl> <dt>**XAUDIO2 \_ Max. \_ Puffer \_ Bytes**</dt> </dl>             | Der maximal zulässige Wert für den [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer). AudioBytes.<br/>                                                      |
| <span id="XAUDIO2_MAX_QUEUED_BUFFERS"></span><span id="xaudio2_max_queued_buffers"></span><dl> <dt>**XAUDIO2 \_ Max. \_ Puffer in Warteschlange \_**</dt> </dl>       | Maximal zulässige Puffer in einer sprach Warteschlange.<br/>                                                                                            |
| <span id="XAUDIO2_MAX_BUFFERS_SYSTEM"></span><span id="xaudio2_max_buffers_system"></span><dl> <dt>**XAUDIO2 \_ Max. \_ Puffer \_ System**</dt> </dl>       | Maximal zulässige Puffer für Systemthreads (nur Xbox 360).<br/>                                                                          |
| <span id="XAUDIO2_MAX_AUDIO_CHANNELS"></span><span id="xaudio2_max_audio_channels"></span><dl> <dt>**XAUDIO2 \_ Maximale \_ \_ Audiokanäle**</dt> </dl>       | Maximal zulässiger Wert für **WaveFormatEx. nchannels**.<br/>                                                                                |
| <span id="XAUDIO2_MIN_SAMPLE_RATE"></span><span id="xaudio2_min_sample_rate"></span><dl> <dt>**XAUDIO2 \_ Min. \_ Stichproben \_ Rate**</dt> </dl>                | Minimale audiobeispielrate unterstützt.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_SAMPLE_RATE"></span><span id="xaudio2_max_sample_rate"></span><dl> <dt>**XAUDIO2 \_ Max. \_ Stichproben \_ Rate**</dt> </dl>                | Maximal unterstützte audiosamplingrate.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_VOLUME_LEVEL"></span><span id="xaudio2_max_volume_level"></span><dl> <dt>**XAUDIO2 \_ Maximale \_ \_ Volumeebene**</dt> </dl>             | Maximal zulässige Volumeebene.<br/>                                                                                                        |
| <span id="XAUDIO2_MIN_FREQ_RATIO"></span><span id="xaudio2_min_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ Min. \_ freq- \_ Verhältnis**</dt> </dl>                   | Das minimale Häufigkeits Verhältnis, das in einer Quell Stimme zulässig ist.<br/>                                                                                   |
| <span id="XAUDIO2_MAX_FREQ_RATIO"></span><span id="xaudio2_max_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ Maximales \_ freq- \_ Verhältnis**</dt> </dl>                   | Maximales Häufigkeits Verhältnis, das in einer Quell Stimme zulässig ist.<br/>                                                                                   |
| <span id="XAUDIO2_DEFAULT_FREQ_RATIO"></span><span id="xaudio2_default_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ standardmäßiges \_ freq- \_ Verhältnis**</dt> </dl>       | Standardwert für das **maxfrequencyratio** -Argument von [**IXAudio2:: kreatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice).<br/> |
| <span id="XAUDIO2_MAX_FILTER_ONEOVERQ"></span><span id="xaudio2_max_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ Max. \_ Filter \_ oneoverq**</dt> </dl>    | Maximalwert für [**XAUDIO2 \_ Filter- \_ Parameter**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**Oneoverq**.<br/>                                     |
| <span id="XAUDIO2_MAX_FILTER_FREQUENCY"></span><span id="xaudio2_max_filter_frequency"></span><dl> <dt>**XAUDIO2 \_ Maximale \_ Filter \_ Häufigkeit**</dt> </dl> | Maximalwert für [**XAUDIO2 \_ Filter- \_ Parameter**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**Häufigkeit**.<br/>                                    |
| <span id="XAUDIO2_MAX_LOOP_COUNT"></span><span id="xaudio2_max_loop_count"></span><dl> <dt>**XAUDIO2 \_ Maximale \_ Schleifen \_ Anzahl**</dt> </dl>                   | Maximalwert, der nicht als Endlosschleife für den XAUDIO2- [**\_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)behandelt wird.**LoopCount**.<br/>              |
| <span id="XAUDIO2_MAX_INSTANCES"></span><span id="xaudio2_max_instances"></span><dl> <dt>**XAUDIO2 \_ Max. \_ Instanzen**</dt> </dl>                       | Maximale Anzahl gleichzeitiger Instanzen von XAudio2 auf Xbox 360 zulässig.<br/>                                                                       |



**XAudio2-Werte mit spezieller Bedeutung**



| Konstante                                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_COMMIT_NOW"></span><span id="xaudio2_commit_now"></span><dl> <dt>**XAUDIO2 \_ \_ jetzt Commit**</dt> </dl>                         | Wird als Parameter für Methoden mit einem operationset-Argument verwendet. Weitere Informationen finden Sie unter [XAudio2 Operation Sets](xaudio2-operation-sets.md) .<br/>                  |
| <span id="XAUDIO2_COMMIT_ALL"></span><span id="xaudio2_commit_all"></span><dl> <dt>**XAUDIO2 \_ Commit für \_ alle**</dt> </dl>                         | Wird als Parameter in [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges)verwendet.<br/>                                                                   |
| <span id="XAUDIO2_INVALID_OPSET"></span><span id="xaudio2_invalid_opset"></span><dl> <dt>**XAUDIO2 \_ ungültiges \_ opset**</dt> </dl>                | Gibt einen ungültigen Wert für operationset-Argumente an. Weitere Informationen finden Sie unter [XAudio2 Operation Sets](xaudio2-operation-sets.md) .<br/>                         |
| <span id="XAUDIO2_NO_LOOP_REGION"></span><span id="xaudio2_no_loop_region"></span><dl> <dt>**XAUDIO2 \_ kein \_ Schleifen \_ Bereich**</dt> </dl>            | Gibt keinen Schleifen Bereich an, der im [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)verwendet wird.**LoopCount**.<br/>                                                                    |
| <span id="XAUDIO2_LOOP_INFINITE"></span><span id="xaudio2_loop_infinite"></span><dl> <dt>**XAUDIO2- \_ Schleife \_ unendlich**</dt> </dl>                | Gibt unendliche Schleifen an, die im [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)verwendet werden.**LoopCount**.<br/>                                                                  |
| <span id="XAUDIO2_DEFAULT_CHANNELS"></span><span id="xaudio2_default_channels"></span><dl> <dt>**XAUDIO2- \_ Standard \_ Kanäle**</dt> </dl>       | Gibt die Standard Anzahl von Kanälen für die aktuelle Plattform an, die in [**IXAudio2:: kreatemasteringvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)verwendet werden.<br/> |
| <span id="XAUDIO2_DEFAULT_SAMPLERATE"></span><span id="xaudio2_default_samplerate"></span><dl> <dt>**XAUDIO2 \_ Standard \_ Samplerate**</dt> </dl> | Gibt die Standard Samplingrate für die aktuelle Plattform an, die in [**IXAudio2:: kreatemasteringvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)verwendet wird.<br/>        |



**XAudio2-Flags**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_DEBUG_ENGINE"></span><span id="xaudio2_debug_engine"></span><dl> <dt><strong>XAUDIO2_DEBUG_ENGINE</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, dass die Debug/aktivierte Version der Audioengine anstelle der Releaseversion verwendet werden soll. Siehe <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird unter Windows 8 oder Windows 10 nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOPITCH"></span><span id="xaudio2_voice_nopitch"></span><dl> <dt><strong>XAUDIO2_VOICE_NOPITCH</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, dass für eine Quell Stimme keine Platz Verschiebungen verwendet werden. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: kreatesourcevoice</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOSRC"></span><span id="xaudio2_voice_nosrc"></span><dl> <dt><strong>XAUDIO2_VOICE_NOSRC</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, dass keine Stichproben Raten Konvertierung in einer Quellsprache verfügbar ist. die Ausgaben der Stimme müssen die gleiche Stichprobenrate aufweisen. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: kreatesourcevoice</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_USEFILTER"></span><span id="xaudio2_voice_usefilter"></span><dl> <dt><strong>XAUDIO2_VOICE_USEFILTER</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, dass der Filtereffekt auf einer Stimme verfügbar sein soll. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: kreatesourcevoice</strong></a> und <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice"><strong>IXAudio2:: kreatesubmixvoice</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_PLAY_TAILS"></span><span id="xaudio2_play_tails"></span><dl> <dt><strong>XAUDIO2_PLAY_TAILS</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, dass eine Stimme nach dem Beenden weiterhin die Effekt Ausgabe ausgeben soll. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop"><strong>IXAudio2SourceVoice:: Beendigung</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_END_OF_STREAM"></span><span id="xaudio2_end_of_stream"></span><dl> <dt><strong>XAUDIO2_END_OF_STREAM</strong></dt> </dl></td>
<td style="text-align: left;">Gibt den letzten Puffer in einem Stream an. Siehe <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer"><strong>XAUDIO2_BUFFER</strong></a>. <strong>Flags</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_STOP_ENGINE_WHEN_IDLE"></span><span id="xaudio2_stop_engine_when_idle"></span><dl> <dt><strong>XAUDIO2_STOP_ENGINE_WHEN_IDLE</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, dass die Audioengine beendet werden soll, wenn keine Quell Stimmen gestartet und gestartet werden, wenn eine Stimme gestartet wird. Siehe <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_SEND_USEFILTER"></span><span id="xaudio2_send_usefilter"></span><dl> <dt><strong>XAUDIO2_SEND_USEFILTER</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, dass ein Filter für einen sprachsendevorgang verwendet werden soll. Siehe <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor"><strong>XAUDIO2_SEND_DESCRIPTOR</strong></a>. <strong>Flags</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_1024_QUANTUM"></span><span id="xaudio2_1024_quantum"></span><dl> <dt><strong>XAUDIO2_1024_QUANTUM</strong></dt> </dl></td>
<td style="text-align: left;">Gibt ein nicht standardmäßiges Verarbeitungs Quantum von 21,33 MS an (1024 Stichproben bei 48 kHz). Siehe <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT"></span><span id="xaudio2_no_virtual_audio_client"></span><dl> <dt><strong>XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, dass ein virtueller AudioClient nicht verwendet werden soll. Weitere Informationen finden Sie unter <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice"><strong>IXAudio2:: kreatemasteringvoice</strong></a>.<br/>
<blockquote>
[!Note]<br />
Auf Geräten der mobilen Gerätefamilie wird immer ein virtueller AudioClient verwendet, unabhängig davon, ob dieses Flag verwendet wird.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



**XAudio2 Standardparameter für den integrierten Sprach Filter**



| Konstante                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_DEFAULT_FILTER_TYPE"></span><span id="xaudio2_default_filter_type"></span><dl> <dt>**XAUDIO2 \_ Standard \_ \_ Filtertyp**</dt> </dl>                | Gibt den Standard Filtertyp an, der für Stimmen und sprach Sendungen verwendet werden soll.<br/>          |
| <span id="XAUDIO2_DEFAULT_FILTER_FREQUENCY"></span><span id="xaudio2_default_filter_frequency"></span><dl> <dt>**XAUDIO2 \_ Standard \_ Filter \_ Häufigkeit**</dt> </dl> | Gibt die standardmäßige Filter Häufigkeit an, die für Stimmen und sprach Sendungen verwendet werden soll.<br/>     |
| <span id="XAUDIO2_DEFAULT_FILTER_ONEOVERQ"></span><span id="xaudio2_default_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ Standard \_ Filter \_ oneoverq**</dt> </dl>    | Gibt die Standardfilter Rate des Versatzes an, der für Stimmen und sprach Sendungen verwendet werden soll.<br/> |



## <a name="remarks"></a>Bemerkungen

### <a name="platform-requirements"></a>Plattformanforderungen

Windows 10 (xaudio2.9); Windows 8, Windows Phone 8 (xaudio2,8); DirectX SDK (xaudio2,7)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Xaudio2. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XAudio2:: Konstanten](constants.md)
</dt> </dl>

 

 
