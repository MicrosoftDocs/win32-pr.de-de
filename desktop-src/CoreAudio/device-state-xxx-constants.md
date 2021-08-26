---
description: Die DEVICE \_ STATE \_ XXX-Konstanten geben den aktuellen Zustand eines Audioendpunktgeräts an.
ms.assetid: d03f2fbc-313a-42cf-902a-fd9f6dce2a35
title: DEVICE_STATE_XXX Konstanten (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d5632f14ff52fec2aa907dc2786f2a3ab893f921cd44433548510163f66a1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053870"
---
# <a name="device_state_xxx-constants"></a>DEVICE \_ STATE \_ XXX-Konstanten

Die DEVICE \_ STATE \_ XXX-Konstanten geben den aktuellen Zustand eines Audioendpunktgeräts an.



| Konstante/Wert                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DEVICE_STATE_ACTIVE"></span><span id="device_state_active"></span><dl> <dt>**GERÄT \_ STATE \_ ACTIVE**</dt> <dt>0x00000001</dt> </dl>             | Das Audioendpunktgerät ist aktiv. Das heißt, der Audioadapter, der eine Verbindung mit dem Endpunktgerät herstellt, ist vorhanden und aktiviert. Wenn das Endpunktgerät an eine Buchse des Adapters angeschlossen ist, wird das Endpunktgerät angeschlossen.<br/>                                                                                                                            |
| <span id="DEVICE_STATE_DISABLED"></span><span id="device_state_disabled"></span><dl> <dt>**GERÄT \_ STATE \_ DISABLED**</dt> <dt>0x00000002</dt> </dl>       | Das Audioendpunktgerät ist deaktiviert. Der Benutzer hat das Gerät in der Windows Multimedia-Systemsteuerung deaktiviert, Mmsys.cpl. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                                                        |
| <span id="DEVICE_STATE_NOTPRESENT"></span><span id="device_state_notpresent"></span><dl> <dt>**GERÄT \_ STATE \_ NOTPRESENT**</dt> <dt>0x00000004</dt> </dl> | Das Audioendpunktgerät ist nicht vorhanden, da der Audioadapter, der eine Verbindung mit dem Endpunktgerät herstellt, aus dem System entfernt wurde oder der Benutzer das Adaptergerät in Geräte-Manager deaktiviert hat.<br/>                                                                                                                                                              |
| <span id="DEVICE_STATE_UNPLUGGED"></span><span id="device_state_unplugged"></span><dl> <dt>**GERÄT \_ STATE \_ UNPLUGGED**</dt> <dt>0x00000008</dt> </dl>    | Das Audioendpunktgerät wird aus dem Netz. Der Audioadapter, der die Buchse für das Endpunktgerät enthält, ist vorhanden und aktiviert, aber das Endpunktgerät ist nicht an die Buchse angeschlossen. Nur ein Gerät mit Jack-Presence-Erkennung kann sich in diesem Zustand befinden. Weitere Informationen zur Erkennung von Jack-Presence finden Sie unter [Audioendpunktgeräte.](audio-endpoint-devices.md)<br/> |
| <span id="DEVICE_STATEMASK_ALL"></span><span id="device_statemask_all"></span><dl> <dt>**GERÄT \_ STATEMASK \_ ALL**</dt> <dt>0x0000000F</dt> </dl>          | Schließt Audioendpunktgeräte in allen Zuständen aktiv, deaktiviert, nicht vorhanden und unplugged ein.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Hinweise

Die Methoden [**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints), [**IMMDevice::GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)und [**IMMNotificationClient::OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged) verwenden die DEVICE \_ STATE \_ XXX-Konstanten. Mit diesen Methoden können Clients Informationen zu Endpunktgeräten abrufen, die sich in einem der Zustände befinden, die durch die DEVICE \_ STATE \_ XXX-Konstanten dargestellt werden.

Ein Client kann jedoch nur auf einem Gerät mit dem Status DEVICE STATE ACTIVE einen Stream öffnen (z. B. durch Abrufen einer [**IAudioClient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) für das \_ \_ Gerät).

Die Windows Multimedia-Systemsteuerung Mmsys.cpl zeigt die Audioendpunktgeräte im System an. Das Deaktivieren eines Geräts in Mmsys.cpl blendet das Gerät vor den Geräteermittlungsmechanismen in Audio-APIs auf höherer Ebene aus, macht jedoch keine Datenstromobjekte ungültig, die ein Client vor der Deaktivierung des Geräts instanziiert hat. Wenn beispielsweise ein Stream auf dem Gerät wiedergegeben wird, wenn der Benutzer ihn in Mmsys.cpl deaktiviert, wird der Stream weiterhin unterbrechungsfrei wiedergegeben.

Im Gegensatz dazu entfernt das Deaktivieren eines Geräts in Geräte-Manager das Gerät effektiv aus dem System.

Um Mmsys.cpl zum Anzeigen der Renderinggeräte zu verwenden, öffnen Sie ein Eingabeaufforderungsfenster, und geben Sie den folgenden Befehl ein:

**control mmsys.cpl,,0**

Geben Sie den folgenden Befehl ein, um die Erfassungsgeräte anzuzeigen:

**control mmsys.cpl,,1**

Alternativ können Sie die Renderinggeräte oder Erfassungsgeräte in Mmsys.cpl anzeigen, indem Sie mit der rechten Maustaste auf das Lautsprechersymbol im Infobereich klicken, der sich rechts auf der Taskleiste befindet, und **wiedergabegeräte** oder **Aufzeichnungsgeräte** auswählen.

Mmsys.cpl zeigt immer Endpunktgeräte an, die sich im Status DEVICE \_ STATE \_ ACTIVE befinden. Darüber hinaus kann es so konfiguriert werden, dass deaktivierte und getrennte Geräte angezeigt werden.

Um Endpunktgeräte anzuzeigen, die sich in den Zuständen DEVICE \_ STATE DISABLED und DEVICE STATE \_ \_ NOTPRESENT befinden, klicken Sie mit der rechten Maustaste in das Fenster \_ Mmsys.cpl, und wählen Sie die Option **Deaktivierte Geräte anzeigen** aus.

Klicken Sie mit der rechten Maustaste in das Fenster Mmsys.cpl, und wählen Sie die Option Getrennte Geräte anzeigen aus, um Endpunktgeräte anzuzeigen, die sich im Status DEVICE \_ STATE \_ UNPLUGGED **befinden.**

Um nur Endpunktgeräte anzuzeigen, die sich im Status DEVICE \_ STATE \_ ACTIVE befinden, deaktivieren Sie sowohl die Optionen **Deaktivierte Geräte anzeigen** als auch Getrennte Geräte **anzeigen.**

Um ein Endpunktgerät in Mmsys.cpl zu aktivieren oder zu deaktivieren, klicken Sie auf **Wiedergabe** oder **Aufzeichnung**, je nachdem, ob es sich bei dem Gerät um ein Wiedergabe- oder Aufzeichnungsgerät handelt. Wählen Sie als Nächstes das Gerät aus, und klicken Sie auf **Eigenschaften.** Wählen Sie im Fenster **Eigenschaften** neben **Geräteverwendung** entweder **Dieses Gerät verwenden (aktivieren)** oder **Dieses Gerät nicht verwenden (deaktivieren) aus.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kernaudiokonstanten](core-audio-constants.md)
</dt> <dt>

[**IMMDevice::GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)
</dt> <dt>

[**IMMDeviceEnumerator-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints)
</dt> <dt>

[**IMMNotificationClient::OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged)
</dt> </dl>

 

 




