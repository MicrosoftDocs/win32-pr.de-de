---
description: Erfahren Sie mehr über Implementierungsüberlegungen für das Streamrouting. APIs implementieren Streamrouting, indem sie den Datenstromwechsel zu einem neuen Standardaudioendpunkt behandeln.
ms.assetid: ecda0b5b-6583-43b4-a9b4-f12a95f09452
title: Überlegungen zur Implementierung des Streamroutings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bd753fe027c92ffac9f5a41cea589b600d7f26
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068036"
---
# <a name="stream-routing-implementation-considerations"></a>Überlegungen zur Implementierung des Streamroutings

In Windows 7 implementieren plattformübergreifende APIs, die Core Audio-APIs wie Media Foundation-, DirectSound- und Wave-APIs verwenden, das Streamroutingfeature, indem sie den Streamwechsel von einem vorhandenen Gerät zu einem neuen Standardaudioendpunkt behandeln. Medienanwendungen, die diese APIs verwenden, verwenden das Streamroutingverhalten ohne Änderungen an der Quelle. Direkte WASAPI-Clients können die von Core Audio-Komponenten gesendeten Benachrichtigungen verwenden und das Streamroutingfeature implementieren.

Direkte WASAPI-Clients (Medienanwendungen, die WASAPI direkt verwenden) erhalten neue Geräte- und Audiositzungsbenachrichtigungen, die von Core Audio-Komponenten gesendet werden. Das Verhalten der Streamroutingfunktion wird durch die Art und Weise definiert, wie die Anwendung diese Benachrichtigungen behandelt.

Die MMDevice-API und die Audiositzung senden Benachrichtigungen über Gerätestatusänderungen und Sitzungsänderungen an WASAPI-Clients in Form von Rückrufen. Um diese Benachrichtigungen zu erhalten, muss der Client seine Implementierung von [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) und [**IAudioSessionEvents registrieren.**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) Weitere Informationen finden Sie unter [Relevante Benachrichtigungen für das Streamrouting.](relevant-device-notifications-for-stream-routing.md)

In dem unter Streamrouting beschriebenen USB-Headsetszenario gibt eine Anwendung einen Audiostream wieder und verwendet MMDeviceAPI und WASAPI, um den Stream auf dem Standardrenderinggerät Zu **rendern: Speaker.** [](stream-routing.md) Wenn das Standardgerät geändert wird, erhält die Anwendung eine [**IMMNotificationClient-Benachrichtigung.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) Die Anwendung empfängt außerdem [**IAudioSessionEvents-Benachrichtigungen,**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) die darauf hinweisen, dass der Benutzer das Audioendpunktgerät entfernt hat oder dass sich das Streamformat für das Gerät geändert hat, mit dem die Audiositzung verbunden ist. Nach dem Empfang der Benachrichtigungen beendet die Anwendung das Streaming an den Sprecherendpunkt und öffnet den Stream erneut für das Rendering auf dem aktuellen Standardendpunkt, dem Headset.

![Diagramm des Datenflusses für Gerätebenachrichtigungen.](images/stream-routing.gif)

Als Reaktion auf solche Benachrichtigungen kann der Client den Stream auf dem neuen Standardgerät in dem vom Benutzer ausgewählten neuen Format erneut öffnen.

## <a name="stream-managment"></a>Stream-Managment

In der folgenden Liste sind die Schritte zusammengefasst, die ein WASAPI-Client ausführen muss, um die Funktion zum Wechseln des Streams zu bieten.

1.  Warten Sie auf die relevante [**IMMNotificationClient-Benachrichtigung.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) Wenn das Gerät das Standardgerät ist, wird die [**Benachrichtigung IMMNotificationClient::OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) empfangen.
2.  Wenn ein neues Gerät verfügbar ist, erhalten Sie einen Verweis auf den Endpunkt des neuen Geräts. Rufen [**Sie IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) für das neue Standardgerät auf. Wenn das neue Gerät nicht das Standardgerät ist, können Sie es abrufen, indem Sie [**IMMDeviceEnumerator::GetDevice aufrufen.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) Weitere Informationen finden Sie unter [Abrufen des Geräteendpunkts für das Streamrouting.](getting-the-default-device-endpoint-for-stream-routing.md)
3.  Warten Sie, bis [**IAudioSessionEvents::OnSessionDisconnected mit**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) dem Grundwert verbunden ist.
    > [!Note]  
    > Da alle diese Vorgänge achron sind, kann die Reihenfolge, in der die Anwendung Benachrichtigungen zu Geräteänderung und Sitzungstrennung empfängt, nicht vorhergesagt werden. Die Anwendung muss die Benachrichtigungsverarbeitung implementieren, um diese Benachrichtigungen in beliebiger Reihenfolge zu empfangen. In der Regel empfängt die Anwendung jedoch den **Wert AudioSessionDisconnect,** bevor die Standardbenachrichtigung zur Geräteänderung angezeigt wird.

     

4.  Werten Sie den Grundwert aus, und bestimmen Sie, ob der Stream an einen anderen Audioendpunkt übertragen oder mit einem neuen Format erneut initialisiert werden muss.
5.  Beenden Sie das Streaming auf das alte Standardgerät, wenn der Grund darauf hinweist, dass der Stream an das neue Standardgerät umgeroutet werden soll.
6.  Führen Sie Positionszuordnungsberechnungen durch.
7.  Öffnen Sie den Stream auf dem neuen Gerät, und übertragen Sie alle Zustandsinformationen.
8.  Setzen Sie das Streaming auf dem neuen Standardgerät wieder auf.
9.  Behandeln Sie den Abbruch des alten Standardgeräts.

Damit der Datenstromwechsel nahtlos angezeigt wird, muss er so schnell wie möglich erfolgen. Dies hängt von der Leistung der Komponenten ab, die an der erneuten Initiierung des Streams auf dem neuen Gerät beteiligt sind.

## <a name="position-mapping-considerations"></a>Überlegungen zur Positionszuordnung

Wenn die Anwendung [**IMMNotificationClient-**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) und [**IAudioSessionEvents-Benachrichtigungen**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) erhält, kann sie die vorhandenen Streams an das neue Standardgerät routen. Wenn ein vorhandener Audiostream unterbrochen und auf dem neuen Gerät geöffnet wird, muss das Rendering auf dem neuen Gerät an der Position beginnen, an der der Stream auf dem alten Gerät beendet wurde. Hierzu muss die Anwendung über die letzte bekannte Geräteposition verfügen, um die Startposition auf dem neuen Gerät zu berechnen. Diese Position kann beispielsweise als Deltaoffset für die nachfolgende Positionszuordnung verwendet werden. Wenn das Rendern des Streams beginnt, kann die neue Geräteposition der zwischengespeicherten Geräteposition neu zugeordnet werden.

In den folgenden Schritten wird der Prozess eines nahtlosen Datenstromübergangs zusammengefasst.

1.  Speichern Sie die letzte Geräteposition des Streams auf dem alten Gerät zwischen.
2.  Beenden Sie den Stream auf dem alten Gerät.
3.  Führen Sie Neuberechnungen durch, um die neue Position zu erhalten.
4.  Beginnen Sie mit dem Rendern des Streams auf dem neuen Gerät.
5.  Geben Sie den alten Stream frei.

Während des Übergangs muss die Anwendung sicherstellen, dass die Uhr nicht aus der Synchronisierung herauskommt, was zu nicht synchronisierten Audio- und Videostreams führt. Dies kann auftreten, wenn die Videobeispiele weiterhin gerendert werden, während der Audiostream an das neue Gerät geroutet wird. Die Anwendung muss die Uhrposition für die Neuberechnung zwischenspeichern und sicherstellen, dass die Videobeispiele erst gerendert werden, wenn der Audiostream auf dem neuen Gerät erneut geöffnet wird, sodass die Audio- und Videostreams synchronisiert werden, wenn der Clip wieder gerendert wird. In einigen Fällen, in denen die Präsentationszeit für das Rendern der Videoframes auf der Audiouhr basiert, ist es ausreichend, den Audiostream zu beenden, bis der Streamwechsel abgeschlossen ist und keine andere Implementierung der Positionszuordnung für den Videostream für die Audiovideosynchronisierung erforderlich ist.

Wenn [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) während des Renderings einen Fehler zurückgibt, weil das alte Gerät verloren geht, muss die Anwendung den alten Stream nicht beenden, da der Streamingvorgang bereits beendet wurde. Informationen zur Behandlung dieses Fehlers finden Sie unter [Wiederherstellen nach einem Invalid-Device Fehlers.](recovering-from-an-invalid-device-error.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur MMDevice-API](mmdevice-api.md)
</dt> <dt>

[Informationen zu WASAPI](wasapi.md)
</dt> <dt>

[Streamrouting](stream-routing.md)
</dt> </dl>

 

 



