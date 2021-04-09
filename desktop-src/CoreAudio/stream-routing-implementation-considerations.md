---
description: In Windows 7 implementieren allgemeine Plattform-APIs, die kernaudio-APIs verwenden, wie Media Foundation-, DirectSound-und Wave-APIs, das Streaming-Routing Feature, indem Sie den Datenstrom Wechsel von einem vorhandenen Gerät zu einem neuen standardaudioendpunkt verarbeiten.
ms.assetid: ecda0b5b-6583-43b4-a9b4-f12a95f09452
title: Überlegungen zur Implementierung von streamrouting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27dc1f7e3fe56d6b421ca59f528ab1a65d2261a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958423"
---
# <a name="stream-routing-implementation-considerations"></a>Überlegungen zur Implementierung von streamrouting

In Windows 7 implementieren allgemeine Plattform-APIs, die kernaudio-APIs verwenden, wie Media Foundation-, DirectSound-und Wave-APIs, das Streaming-Routing Feature, indem Sie den Datenstrom Wechsel von einem vorhandenen Gerät zu einem neuen standardaudioendpunkt verarbeiten. Medienanwendungen, die diese APIs verwenden, verwenden das Datenstrom-Routing Verhalten ohne Änderungen an der Quelle. Direkte WASAPI-Clients können die Benachrichtigungen verwenden, die von den kernaudiokomponenten gesendet werden, und die streamweiterleitungs Funktion implementieren.

Direkte WASAPI-Clients (Medienanwendungen, die WASAPI direkt verwenden) erhalten neue Geräte-und audiositzungsbenachrichtigungen, die von kernaudiokomponenten gesendet werden. Das Verhalten der streamweiterleitungs Funktion wird durch die Behandlung dieser Benachrichtigungen durch die Anwendung definiert.

Die mmdevice-API und die Audiositzung senden Benachrichtigungen zu Änderungen am Gerätestatus und Sitzungs Änderungen an WASAPI-Clients in Form von Rückrufe. Um diese Benachrichtigungen zu erhalten, muss der Client seine Implementierung von [**immnotificationclient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) und [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)registrieren. Weitere Informationen finden Sie unter [relevante Benachrichtigungen für das Datenstrom Routing](relevant-device-notifications-for-stream-routing.md).

In dem im [Stream-Routing](stream-routing.md)beschriebenen USB-Headset-Szenario gibt eine Anwendung einen Audiostream wieder und verwendet mmdeviceapi und WASAPI, um den Stream auf dem Standard renderinggerät ( **Sprecher**) zu rendern. Wenn das Standardgerät geändert wird, empfängt die Anwendung eine [**immnotificationclient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) -Benachrichtigung. Die Anwendung empfängt außerdem [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Benachrichtigungen, die angeben, dass der Benutzer das audioendpunktgerät entfernt hat oder dass sich das Streamformat für das Gerät geändert hat, mit dem die Audiositzung verbunden ist. Beim Empfang der Benachrichtigungen beendet die Anwendung das Streaming an den Sprecher Endpunkt und öffnet den Stream für das Rendering auf dem aktuellen Standard Endpunkt, dem Headset, erneut.

![Diagramm des Datenflusses für Geräte Benachrichtigungen.](images/stream-routing.gif)

Als Reaktion auf solche Benachrichtigungen kann der Client den Datenstrom auf dem neuen Standardgerät in dem vom Benutzer ausgewählten Format erneut öffnen.

## <a name="stream-managment"></a>Stream-Verwaltung

In der folgenden Liste sind die Schritte zusammengefasst, die ein WASAPI-Client ausführen muss, um die Datenstrom Wechselfunktion bereitzustellen.

1.  Warten Sie auf die relevante [**immnotificationclient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) -Benachrichtigung. Wenn es sich bei dem Gerät um das Standardgerät handelt, wird die Meldung " [**immnotificationclient:: ondefaultdevicechanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) " empfangen.
2.  Wenn ein neues Gerät verfügbar ist, erhalten Sie einen Verweis auf den Endpunkt des neuen Geräts. " [**Immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) " für das neue Standardgerät aufrufen. Wenn das neue Gerät nicht das Standardgerät ist, können Sie das Gerät durch Aufrufen von [**immdeviceenumerator:: getdevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)abrufen. Weitere Informationen finden Sie unter [Getting the Device Endpoint for Stream Routing](getting-the-default-device-endpoint-for-stream-routing.md).
3.  Warten Sie auf [**iaudiosessionevents:: onsessiontrennt**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) mit dem Wert "Reason".
    > [!Note]  
    > Da alle diese Vorgänge asynchron sind, wird die Reihenfolge, in der die Anwendung die Benachrichtigungen über Geräte Änderung und Sitzungs Trennung empfängt, nicht vorhergesagt. Die Anwendung muss die Benachrichtigungs Behandlung implementieren, um diese Benachrichtigungen in beliebiger Reihenfolge zu empfangen. In der Regel erhält die Anwendung jedoch den Wert **audiosessiondisconnect** vor der Standard Benachrichtigung für Geräteänderungen.

     

4.  Werten Sie den Grund Wert aus, und bestimmen Sie, ob der Stream an einen anderen audioendpunkt übertragen werden muss oder ob der Stream mit einem neuen Format erneut initialisiert werden muss.
5.  Beendet das Streaming auf das alte Standardgerät, wenn der Grund darauf hinweist, dass der Datenstrom an das neue Standardgerät weitergeleitet werden soll.
6.  Führt Berechnungen zur Positions Zuordnung aus.
7.  Öffnen Sie den Stream auf dem neuen Gerät, und übertragen Sie alle Zustandsinformationen.
8.  Setzen Sie das Streaming auf dem neuen Standardgerät fort.
9.  Behandeln Sie die Abfahrt des alten Standard Geräts.

Damit der streamwechselvorgang nahtlos angezeigt wird, muss er so schnell wie möglich ausgeführt werden. Dies hängt von der Leistung der Komponenten ab, die an der erneuten Initiierung des Streams auf dem neuen Gerät beteiligt sind.

## <a name="position-mapping-considerations"></a>Überlegungen zur Positions Zuordnung

Wenn die Anwendung die Benachrichtigungen " [**immnotificationclient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) " und " [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) " erhält, kann Sie die vorhandenen Streams an das neue Standardgerät weiterleiten. Wenn ein vorhandener Audiostream unterbrochen und auf dem neuen Gerät geöffnet wird, muss das Rendering auf dem neuen Gerät an der Position beginnen, an der der Stream auf dem alten Gerät angehalten wurde. Zu diesem Zweck muss die Anwendung die letzte bekannte Geräte Position aufweisen, um die Startposition auf dem neuen Gerät zu berechnen. Diese Position kann z. b. als Delta Offset für die nachfolgende Positions Zuordnung verwendet werden. Wenn der Stream das Rendering startet, kann die neue Geräte Position der zwischengespeicherten Geräte Position neu zugeordnet werden.

In den folgenden Schritten wird der Prozess der nahtlosen Datenstrom Umstellung zusammengefasst.

1.  Zwischenspeichern der letzten Geräte Position des Streams auf dem alten Gerät.
2.  Beendet den Stream auf dem alten Gerät.
3.  Führen Sie Neuzuordnung von Berechnungen durch, um die neue Position zu erhalten.
4.  Startet das Rendern des Streams auf dem neuen Gerät.
5.  Geben Sie den alten Stream frei.

Während des Übergangs muss die Anwendung sicherstellen, dass die Uhr nicht synchron ist, was zu nicht Synchronisierungs-Audiodaten und Videostreams führt. Dies kann vorkommen, wenn die Videobeispiele weiterhin gerouteten werden, während der Audiodatenstrom an das neue Gerät weitergeleitet wird. Die Anwendung muss die Uhrzeit Position für die Neuzuordnung Zwischenspeichern und sicherstellen, dass die Videobeispiele erst gerendert werden, wenn der Audiodatenstrom auf dem neuen Gerät wieder geöffnet wird, sodass die Audiodaten und die Videostreams synchronisiert werden, wenn der Clip das Rendering wieder aufnimmt. In einigen Fällen, in denen die Präsentationszeit zum Rendern der Videorahmen auf der audiouhr basiert, reicht es aus, den Audiostream zu beenden, bis der Streamwechsel beendet ist und keine weitere Implementierung der Positions Zuordnung für den Videostream für die audiovideosynchronisierung erforderlich ist.

Wenn beim Rendern [**iaudiorenderclient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) einen Fehler zurückgibt, weil das alte Gerät verloren gegangen ist, muss die Anwendung den alten Stream nicht beenden, da der Streamingvorgang bereits beendet wurde. Informationen zur Behandlung dieses Fehlers finden Sie unter wieder [herstellen nach einem Invalid-Device Fehler](recovering-from-an-invalid-device-error.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über die mmdevice-API](mmdevice-api.md)
</dt> <dt>

[Informationen zu WASAPI](wasapi.md)
</dt> <dt>

[Streamrouting](stream-routing.md)
</dt> </dl>

 

 



