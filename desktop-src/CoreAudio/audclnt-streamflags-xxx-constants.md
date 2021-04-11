---
description: Gibt Merkmale an, die ein Client einem Audiostream während der Initialisierung des Streams zuweisen kann.
ms.assetid: 7b2267c3-79f5-4ada-a7ce-78dd514f8487
title: AUDCLNT_STREAMFLAGS_XXX Konstanten (audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65faf887c35b4ce1110cecb7d7509eb3dfda1d57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126908"
---
# <a name="audclnt_streamflags_xxx-constants"></a>Audclnt \_ StreamFlags \_ xxx-Konstanten

Gibt Merkmale an, die ein Client einem Audiostream während der Initialisierung des Streams zuweisen kann.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_STREAMFLAGS_CROSSPROCESS"></span><span id="audclnt_streamflags_crossprocess"></span><dl> " <dt>**Audclnt \_ " StreamFlags \_ CrossProcess**</dt> <dt>0x00010000 bis</dt> </dl>                                       | Der Audiodatenstrom ist ein Member einer prozessübergreifenden Audiositzung. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_LOOPBACK"></span><span id="audclnt_streamflags_loopback"></span><dl> " <dt>**Audclnt \_ " StreamFlags- \_ Loopback**</dt> <dt>0x00020000</dt> </dl>                                                   | Der Audiodatenstrom wird im Loopback Modus ausgeführt. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                                                                                                      |
| <span id="AUDCLNT_STREAMFLAGS_EVENTCALLBACK"></span><span id="audclnt_streamflags_eventcallback"></span><dl> " <dt>**Audclnt \_ " StreamFlags \_ EventCallback**</dt> <dt>0x00040000</dt> </dl>                                    | Die Verarbeitung des Audiopuffers durch den Client wird ereignisgesteuert. Weitere Informationen finden Sie in den Hinweisen. <br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_NOPERSIST"></span><span id="audclnt_streamflags_nopersist"></span><dl> " <dt>**Audclnt \_ " StreamFlags \_ nopersist**</dt> <dt>0x00080000</dt> </dl>                                                | Die Volume-und stumm Einstellungen für eine Audiositzung bleiben nicht über Anwendungs Neustarts hinweg erhalten. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                                                           |
| <span id="AUDCLNT_STREAMFLAGS_RATEADJUST"></span><span id="audclnt_streamflags_rateadjust"></span><dl> " <dt>**Audclnt \_ " StreamFlags- \_ rateanpassung**</dt> <dt>0x00100000</dt> </dl>                                             | Diese Konstante ist neu in Windows 7. Die Stichprobenrate des Streams wird an eine von einer Anwendung angegebene Rate angepasst. Weitere Informationen finden Sie in den Hinweisen. <br/>                                                                                                                                                                                 |
| <span id="AUDCLNT_STREAMFLAGS_AUTOCONVERTPCM"></span><span id="audclnt_streamflags_autoconvertpcm"></span><dl> " <dt>**Audclnt \_ " StreamFlags \_ autoconvertpcm**</dt> <dt>0x80000000</dt> </dl>                                 | Ein kanalmatrixer und ein Sample Rate Converter werden bei Bedarf eingefügt, um zwischen dem nicht komprimierten Format zu konvertieren, das für [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) und das Audio-Engine-Mischungs Format bereitgestellt wird.<br/>                                                                                                            |
| <span id="AUDCLNT_STREAMFLAGS_SRC_DEFAULT_QUALITY"></span><span id="audclnt_streamflags_src_default_quality"></span><dl> " <dt>**Audclnt \_ " StreamFlags \_ src \_ Standard \_ Qualität**</dt> <dt>0x08000000</dt> </dl>                | Bei Verwendung mit der Verwendung von **audclnt \_ StreamFlags \_ autoconvertpcm** wird ein Sample Rate Converter mit besserer Qualität als die Standard Konvertierung verwendet, aber mit einem höheren Leistungs Aufwand. Dieser Wert sollte verwendet werden, wenn die Audiodaten letztendlich von Menschen im Gegensatz zu anderen Szenarios, z. b. dem Übertragen von schweigen oder dem Auffüllen einer Verbrauchseinheit, gehört werden sollen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode und die [**DirectX \_ - \_ audioaktivierungs- \_**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) Parameterstruktur verwenden die "audclnt \_ StreamFlags xxx"- \_ Konstanten.

Das Kennzeichen "audclnt \_ StreamFlags \_ CrossProcess" gibt an, dass die Audiositzung für den Stream eine prozessübergreifende Sitzung ist. Eine prozessübergreifende Sitzung kann Streams von mehr als einem Prozess akzeptieren. Wenn zwei Anwendungen in zwei separaten Prozessen **iaudioclient:: Initialize** mit identischen Sitzungs-GUIDs aufzurufen, und beide Anwendungen das Symbol für das "audclnt \_ sharemode \_ CrossProcess" festlegen, weist die Audioengine ihre Streams der gleichen prozessübergreifenden Sitzung zu. Dieses Flag überschreibt das Standardverhalten, d. h., der Stream wird einer prozessspezifischen Sitzung anstatt einer prozessübergreifenden Sitzung zugewiesen. Das Flag für das "audclnt \_ StreamFlags \_ CrossProcess" ist mit dem exklusiven Modus nicht kompatibel. Weitere Informationen zu prozessübergreifenden Sitzungen finden Sie unter [audiositzungen](audio-sessions.md).

Das "audclnt \_ StreamFlags \_ Loopback"-Flag ermöglicht Loopback Aufzeichnung. Bei der Loopback Aufzeichnung kopiert die Audioengine den Audiostream, der von einem renderingendpunkt-Gerät abgespielt wird, in einen audioendpunktpuffer, sodass ein [WASAPI](wasapi.md) -Client den Datenstrom erfassen kann. Wenn dieses Flag festgelegt ist, versucht die **iaudioclient:: Initialize** -Methode, einen Aufzeichnungs Puffer auf dem renderinggerät zu öffnen. Dieses Flag ist nur für ein renderinggerät und nur dann gültig, wenn der **Initialize** -Befehl den *share Mode* -Parameter auf den freigegebenen Modus von audclnt \_ share Mode festlegt \_ . Andernfalls schlägt der **Initialize** -Befehl fehl. Wenn der-Befehl erfolgreich ausgeführt wird, kann der Client die [**iaudioclient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) -Methode aufrufen, um eine [**iaudiocaptureclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) -Schnittstelle auf dem renderinggerät zu erhalten. Weitere Informationen finden Sie unter [Loopback Aufzeichnung](loopback-recording.md).

Das "audclnt \_ StreamFlags \_ EventCallback"-Flag ermöglicht die ereignisgesteuerte Pufferung. Wenn ein Client dieses Flag im **iaudioclient:: Initialize** -Befehl festlegt, der einen Stream initialisiert, muss der Client anschließend die [**iaudioclient:: seteventhandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) -Methode zum Angeben eines Ereignis Handles für den Stream aufruft. Nachdem der Stream gestartet wurde, signalisiert das Audiomodul dem Ereignis handle, dass der Client jedes Mal benachrichtigt wird, wenn ein Puffer für die Verarbeitung durch den Client bereit ist. WASAPI unterstützt ereignisgesteuerte Pufferung für Rendering-und Aufzeichnungs Puffer. Sowohl Datenströme im gemeinsam genutzten Modus als auch im exklusiven Modus können ereignisgesteuerte Pufferung verwenden. Ein Codebeispiel, in dem das getclnt \_ StreamFlags \_ EventCallback-Flag verwendet wird, finden Sie unter Daten [Ströme im exklusiven Modus](exclusive-mode-streams.md).

Das Flag "audclnt \_ StreamFlags \_ nopersist" deaktiviert die Persistenz des Volumes und die stumm Einstellungen für eine Sitzung, die renderingdatenströme enthält. Standardmäßig sind die Volumeebene und der stumm Schaltung-Status für eine renderingsitzung über Anwendungs Neustarts hinweg persistent. Die Volumeebene und der stumm Schaltung-Status für eine Aufzeichnungs Sitzung werden niemals persistent sein. Weitere Informationen zur Persistenz von Sitzungs Volume und stumm Einstellungen finden Sie unter [audiositzungen](audio-sessions.md).

Das Flag "ltclnt \_ StreamFlags \_ rateanpassung" ermöglicht einer Anwendung, einen Verweis auf die [**iaudioclock-Anpassungs**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment) Schnittstelle zu erhalten, mit der die Stichprobenrate für den Stream festgelegt wird. Um einen Zeiger auf diesen Austausch zu erhalten, muss eine Anwendung den AudioClient mit diesem Flag initialisieren und dann [**iaudioclient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) aufrufen, indem Sie den **IID \_ iaudioclock-Anpassungs** Bezeichner angibt. Um die neue Samplingrate festzulegen, nennen Sie [**iaudioclockanpassung:: setsamplerate**](/windows/desktop/api/audioclient/nf-audioclient-iaudioclockadjustment-setsamplerate). Dieses Flag ist nur für ein renderinggerät gültig. Andernfalls schlägt der **GetService** -Befehl mit dem Fehlercode "audclnt \_ E \_ falscher \_ \_ Endpunkttyp" fehl. Die Anwendung muss auch den *share Mode* -Parameter auf den \_ \_ während des [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -aufrufys freigegebenen Funktions-und Debugmodus von "" **Setsamplerate** schlägt fehl, wenn sich der AudioClient nicht im Modus "freigegeben" befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Audiosessiontypes. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kernaudiokonstanten](core-audio-constants.md)
</dt> <dt>

[**Iaudiocaptureclient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)
</dt> <dt>

[**Iaudioclient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
</dt> <dt>

[**Iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)
</dt> <dt>

[**Iaudioclient:: Einstellungs Element**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)
</dt> </dl>

 

 




