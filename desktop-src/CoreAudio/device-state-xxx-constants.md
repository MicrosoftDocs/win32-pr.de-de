---
description: Die \_ Konstanten Gerätestatus \_ xxx geben den aktuellen Status eines audioendpunktgeräts an.
ms.assetid: d03f2fbc-313a-42cf-902a-fd9f6dce2a35
title: DEVICE_STATE_XXX Konstanten (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65fc09a547ad702d27e96e968915f9d70e3313e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747760"
---
# <a name="device_state_xxx-constants"></a>Geräte \_ Status \_ xxx-Konstanten

Die \_ Konstanten Gerätestatus \_ xxx geben den aktuellen Status eines audioendpunktgeräts an.



| Konstante/Wert                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DEVICE_STATE_ACTIVE"></span><span id="device_state_active"></span><dl> <dt>**Gerät \_ Status \_ aktiv**</dt> <dt>0x00000001</dt> </dl>             | Das audioendpunktgerät ist aktiv. Das heißt, dass der Audioadapter, der eine Verbindung mit dem Endpunkt Gerät herstellt, vorhanden und aktiviert ist. Außerdem wird das Endpunkt Gerät angeschlossen, wenn das Endpunkt Gerät an einen Jack auf dem Adapter angeschlossen ist.<br/>                                                                                                                            |
| <span id="DEVICE_STATE_DISABLED"></span><span id="device_state_disabled"></span><dl> <dt>**Gerät \_ Status \_ deaktiviert**</dt> <dt>0x00000002</dt> </dl>       | Das audioendpunktgerät ist deaktiviert. Der Benutzer hat das Gerät in der Windows-Multimedia-Systemsteuerung (Mmsys.cpl) deaktiviert. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                                                        |
| <span id="DEVICE_STATE_NOTPRESENT"></span><span id="device_state_notpresent"></span><dl> <dt>**Gerät \_ State \_ notpresent**</dt> <dt>0x00000004</dt> </dl> | Das audioendpunktgerät ist nicht vorhanden, weil der Audioadapter, der eine Verbindung mit dem Endpunkt Gerät herstellt, aus dem System entfernt wurde oder der Benutzer das Adapter Gerät in Device Manager deaktiviert hat.<br/>                                                                                                                                                              |
| <span id="DEVICE_STATE_UNPLUGGED"></span><span id="device_state_unplugged"></span><dl> <dt>**Gerät \_ Status \_**</dt> nicht getrennt <dt>0x00000008</dt> </dl>    | Das audioendpunktgerät ist nicht getrennt. Der Audioadapter, der den Jack für das Endpunkt Gerät enthält, ist vorhanden und aktiviert, aber das Endpunkt Gerät ist nicht an den Jack angeschlossen. In diesem Zustand kann nur ein Gerät mit der Erkennung von Jack-Presence vorhanden sein. Weitere Informationen zur Erkennung von Jack-Presence finden Sie unter [audioendpunktgeräte](audio-endpoint-devices.md).<br/> |
| <span id="DEVICE_STATEMASK_ALL"></span><span id="device_statemask_all"></span><dl> <dt>**Gerät \_ Statusfrage \_ alle**</dt> <dt>0x0000000f</dt> </dl>          | Schließt audioendpunktgeräte in allen Zuständen ein, die aktiv, deaktiviert, nicht vorhanden und getrennt sind.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Bemerkungen

Die Methoden " [**immdeviceenumerator:: enumaudioendpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints)", " [**immdevice:: GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)" und " [**immnotificationclient:: ondevicestatechanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged) " verwenden die Geräte \_ Status-xxx- \_ Konstanten. Mit diesen Methoden können Clients Informationen zu Endpunkt Geräten abrufen, die sich in einem der Zustände befinden, die durch die Geräte \_ Status xxx-Konstanten dargestellt werden \_ .

Ein Client kann jedoch einen Stream (z. b. durch Abrufen einer [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle für das Gerät) nur auf einem Gerät öffnen, das sich im Zustand "aktiver Gerätestatus" befindet \_ \_ .

In der Windows-Multimedia-Systemsteuerung (Mmsys.cpl) werden die audioendpunktgeräte im System angezeigt. Wenn Sie ein Gerät in Mmsys.cpl deaktivieren, wird das Gerät vor den Geräte Ermittlungs Mechanismen in übergeordneten audioapis ausgeblendet, aber es werden keine Streamobjekte ungültig, die möglicherweise von einem Client vor der Deaktivierung des Geräts instanziiert wurden. Wenn z. b. ein Stream auf dem Gerät abgespielt wird, wenn der Benutzer ihn in Mmsys.cpl deaktiviert, wird der Stream weiterhin ununterbrochen abgespielt.

Im Gegensatz dazu wird durch das Deaktivieren eines Geräts in Device Manager das Gerät effektiv aus dem System entfernt.

Um Mmsys.cpl zum Anzeigen der renderinggeräte zu verwenden, öffnen Sie ein Eingabe Aufforderungs Fenster, und geben Sie den folgenden Befehl ein:

**Steuerelement mmsys.cpl,, 0**

Geben Sie den folgenden Befehl ein, um die Erfassungsgeräte anzuzeigen:

**Steuerelement mmsys.cpl,, 1**

Alternativ dazu können Sie die renderinggeräte oder die Erfassungsgeräte in Mmsys.cpl anzeigen, indem Sie mit der rechten Maustaste auf das Redner Symbol im Infobereich klicken, der sich auf der rechten Seite der Taskleiste befindet, und **Geräte wieder** geben oder **Geräte aufzeichnen** auswählen.

Mmsys.cpl zeigt immer Endpunkt Geräte an, die den Zustand "aktiver Gerätestatus" aufweisen \_ \_ . Außerdem kann Sie so konfiguriert werden, dass Sie deaktivierte und getrennte Geräte anzeigt.

\_ \_ Klicken Sie mit der \_ \_ rechten Maustaste in das Mmsys.cpl Fenster, und wählen Sie die Option **deaktivierte Geräte anzeigen** aus, um Endpunkt Geräte anzuzeigen, die den Status "deaktiviert" aufweisen

\_ \_ Klicken Sie mit der rechten Maustaste in das Mmsys.cpl Fenster, und wählen Sie die Option **getrennte Geräte anzeigen** aus, um Endpunkt Geräte anzuzeigen, die sich im Zustand Gerätezustand befinden befinden.

Wenn Sie nur Endpunkt Geräte anzeigen möchten, die den \_ \_ Status "aktiv" aufweisen, deaktivieren Sie die Optionen " **deaktivierte Geräte anzeigen** " und " **getrennte Geräte anzeigen** ".

Zum Aktivieren oder Deaktivieren eines Endpunkt Geräts in Mmsys.cpl klicken Sie auf **Wiedergabe** oder **Aufzeichnung**, je nachdem, ob es sich beim Gerät um ein Wiedergabe-oder Aufzeichnungsgerät handelt. Wählen Sie dann das Gerät aus, und klicken Sie auf **Eigenschaften**. Wählen Sie im **Eigenschaften** Fenster neben **Geräte Verwendung** entweder **dieses Gerät verwenden (aktivieren)** oder **dieses Gerät nicht verwenden (deaktivieren)** aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kernaudiokonstanten](core-audio-constants.md)
</dt> <dt>

[**Immdevice:: GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)
</dt> <dt>

[**Immdeviceenumerator-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**Immdeviceenumerator:: enumaudioendpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints)
</dt> <dt>

[**Immnotificationclient:: ondevicestatechanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged)
</dt> </dl>

 

 




