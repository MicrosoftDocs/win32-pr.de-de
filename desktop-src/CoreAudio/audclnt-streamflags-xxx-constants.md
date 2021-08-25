---
description: Gibt Merkmale an, die ein Client einem Audiostream während der Initialisierung des Streams zuweisen kann.
ms.assetid: 7b2267c3-79f5-4ada-a7ce-78dd514f8487
title: AUDCLNT_STREAMFLAGS_XXX Konstanten (Audiosessiontypes.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84817607092c179286f47eb35ef51f5e0f82d44211bcd2345ca3d27ee06b0e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407363"
---
# <a name="audclnt_streamflags_xxx-constants"></a>AUDCLNT \_ STREAMFLAGS \_ XXX-Konstanten

Gibt Merkmale an, die ein Client einem Audiostream während der Initialisierung des Streams zuweisen kann.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                | Beschreibung                                                                                                                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_STREAMFLAGS_CROSSPROCESS"></span><span id="audclnt_streamflags_crossprocess"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ CROSSPROCESS**</dt> <dt>0x00010000</dt> </dl>                                       | Der Audiostream ist Ein Mitglied einer prozessübergreifenden Audiositzung. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_LOOPBACK"></span><span id="audclnt_streamflags_loopback"></span><dl> <dt>**AUDCLNT \_ \_STREAMFLAGS-LOOPBACK 0x00020000**</dt> <dt></dt> </dl>                                                   | Der Audiostream wird im Loopbackmodus ausgeführt. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                                                                                                      |
| <span id="AUDCLNT_STREAMFLAGS_EVENTCALLBACK"></span><span id="audclnt_streamflags_eventcallback"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK-0x00040000**</dt> <dt></dt> </dl>                                    | Die Verarbeitung des Audiopuffers durch den Client erfolgt ereignisgesteuert. Weitere Informationen finden Sie in den Hinweisen. <br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_NOPERSIST"></span><span id="audclnt_streamflags_nopersist"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ NOPERSIST-0x00080000**</dt> <dt></dt> </dl>                                                | Die Einstellungen für Lautstärke und Stummschaltung für eine Audiositzung bleiben bei Anwendungsneustarts nicht erhalten. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                                                           |
| <span id="AUDCLNT_STREAMFLAGS_RATEADJUST"></span><span id="audclnt_streamflags_rateadjust"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ RATEADJUST**</dt> <dt>0x00100000</dt> </dl>                                             | Diese Konstante ist neu in Windows 7. Die Abtastrate des Streams wird an eine von einer Anwendung angegebene Rate angepasst. Weitere Informationen finden Sie in den Hinweisen. <br/>                                                                                                                                                                                 |
| <span id="AUDCLNT_STREAMFLAGS_AUTOCONVERTPCM"></span><span id="audclnt_streamflags_autoconvertpcm"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM-0x80000000**</dt> <dt></dt> </dl>                                 | Ein Kanalmatrixer und ein Abtastratenkonverter werden nach Bedarf eingefügt, um zwischen dem für [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) bereitgestellten unkomprimierten Format und dem Audio-Engine-Mischungsformat zu konvertieren.<br/>                                                                                                            |
| <span id="AUDCLNT_STREAMFLAGS_SRC_DEFAULT_QUALITY"></span><span id="audclnt_streamflags_src_default_quality"></span><dl> <dt>**AUDCLNT \_ \_STANDARDQUALITÄTSEINSTELLUNGEN \_ FÜR \_ STREAMFLAGS SRC**</dt> <dt>0x08000000</dt> </dl>                | Bei Verwendung mit **AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM** wird ein Abtastratenkonverter mit einer besseren Qualität als die Standardkonvertierung, aber mit höheren Leistungskosten verwendet. Dies sollte verwendet werden, wenn die Audiodaten letztendlich von Menschen gehört werden sollen, im Gegensatz zu anderen Szenarien wie dem Pumpen von Stille oder dem Aufsauen eines Verbrauchszählers.<br/> |



## <a name="remarks"></a>Hinweise

Die [**IAudioClient::Initialize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) und die [**DIRECTX \_ AUDIO ACTIVATION \_ \_ PARAMS-Struktur**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) verwenden die AUDCLNT \_ STREAMFLAGS \_ XXX-Konstanten.

Das AUDCLNT \_ STREAMFLAGS CROSSPROCESS-Flag gibt an, dass die Audiositzung für den Stream \_ eine prozessübergreifende Sitzung ist. Eine prozessübergreifende Sitzung kann Datenströme von mehr als einem Prozess akzeptieren. Wenn zwei Anwendungen in zwei separaten Prozessen **IAudioClient::Initialize** mit identischen Sitzungs-GUIDs aufrufen und beide Anwendungen das AUDCLNT \_ SHAREMODE CROSSPROCESS-Flag festlegen, weist die Audio-Engine ihre Streams derselben prozessübergreifenden Sitzung \_ zu. Dieses Flag überschreibt das Standardverhalten, bei dem der Stream einer prozessspezifischen Sitzung statt einer prozessübergreifenden Sitzung zugewiesen wird. Das AUDCLNT \_ STREAMFLAGS \_ CROSSPROCESS-Flagbit ist nicht mit dem exklusiven Modus kompatibel. Weitere Informationen zu prozessübergreifenden Sitzungen finden Sie unter [Audiositzungen](audio-sessions.md).

Das AUDCLNT \_ STREAMFLAGS \_ LOOPBACK-Flag ermöglicht die Loopbackaufzeichnung. In der Loopbackaufzeichnung kopiert die Audio-Engine den Audiodatenstrom, der von einem Renderingendpunktgerät abgespielt wird, in einen Audioendpunktpuffer, damit ein [WASAPI-Client](wasapi.md) den Stream erfassen kann. Wenn dieses Flag festgelegt ist, versucht die **IAudioClient::Initialize-Methode,** einen Erfassungspuffer auf dem Renderinggerät zu öffnen. Dieses Flag ist nur für ein Renderinggerät gültig und nur, wenn der **Initialize-Aufruf** den *ShareMode-Parameter* auf AUDCLNT \_ SHAREMODE \_ SHARED legt. Andernfalls **kann der Initialize-Aufruf** nicht verwendet werden. Wenn der Aufruf erfolgreich ist, kann der Client die [**IAudioClient::GetService-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) aufrufen, um eine [**IAudioCaptureClient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) auf dem Renderinggerät zu erhalten. Weitere Informationen finden Sie unter [Loopbackaufzeichnung.](loopback-recording.md)

Das AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK-Flag ermöglicht die ereignisgesteuerte Pufferung. Wenn ein Client dieses Flag im Aufruf von **IAudioClient::Initialize** fest legt, der einen Stream initialisiert, muss der Client anschließend die [**IAudioClient::SetEventHandle-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) aufrufen, um ein Ereignishandle für den Stream zu liefern. Nachdem der Stream gestartet wurde, signalisiert die Audio-Engine dem Ereignishand handle, den Client jedes Mal zu benachrichtigen, wenn ein Puffer für die Verarbeitung durch den Client bereit ist. WASAPI unterstützt die ereignisgesteuerte Pufferung für Rendering- und Erfassungspuffer. Streams im freigegebenen Modus und im exklusiven Modus können ereignisgesteuerte Pufferung verwenden. Ein Codebeispiel, in dem das AUDCLNT \_ STREAMFLAGS EVENTCALLBACK-Flag verwendet wird, finden Sie unter \_ [Exclusive-Mode Streams.](exclusive-mode-streams.md)

Das AUDCLNT STREAMFLAGS NOPERSIST-Flag deaktiviert die Persistenz des Volumes und stummgeschaltete Einstellungen für eine Sitzung, \_ \_ die Renderingstreams enthält. Standardmäßig sind die Volumeebene und der Veränderungszustand für eine Renderingsitzung bei Anwendungsneustarts persistent. Die Volumeebene und der Veränderungszustand für eine Erfassungssitzung sind nie persistent. Weitere Informationen zur Persistenz von Sitzungsvolumen und Stummschaltungseinstellungen finden Sie unter [Audiositzungen](audio-sessions.md).

Mit dem Flag AUDCLNT STREAMFLAGS RATEADJUST kann eine Anwendung einen Verweis auf die \_ \_ [**IAudioClockAdjustment-Schnittstelle**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment) erhalten, die zum Festlegen der Abtastrate für den Stream verwendet wird. Um einen Zeiger auf diese Interace zu erhalten, muss eine Anwendung den Audioclient mit diesem Flag initialisieren und dann [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) aufrufen, indem der **\_ IAudioClockAdjustment-Bezeichner** der IID angegeben wird. Rufen Sie zum Festlegen der neuen Abtastrate [**IAudioClockAdjustment::SetSampleRate auf.**](/windows/desktop/api/audioclient/nf-audioclient-iaudioclockadjustment-setsamplerate) Dieses Flag ist nur für ein Renderinggerät gültig. Andernfalls **schlägt der GetService-Aufruf** mit dem Fehlercode AUDCLNT \_ E WRONG ENDPOINT TYPE \_ \_ \_ fehl. Die Anwendung muss auch den *ShareMode-Parameter* während des Initialize-Aufrufs auf AUDCLNT \_ SHAREMODE \_ SHARED festlegen. [](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) **SetSampleRate schlägt** fehl, wenn sich der Audioclient nicht im freigegebenen Modus befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Audiosessiontypes.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Kernaudiokonstten](core-audio-constants.md)
</dt> <dt>

[**IAudioCaptureClient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)
</dt> <dt>

[**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
</dt> <dt>

[**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)
</dt> <dt>

[**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)
</dt> </dl>

 

 




