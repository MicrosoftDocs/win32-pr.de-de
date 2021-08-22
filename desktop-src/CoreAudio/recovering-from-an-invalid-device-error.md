---
description: Wiederherstellen nach einem Invalid-Device Fehlers
ms.assetid: 1f5c3458-70ca-45ba-ac33-5c7b9f092320
title: Wiederherstellen nach einem Invalid-Device Fehlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9f56972aeeae5cfb370a656a621c6b6e206f8caa115bec33203cab7eded3e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318560"
---
# <a name="recovering-from-an-invalid-device-error"></a>Wiederherstellen nach einem Invalid-Device Fehlers

Viele der Methoden in WASAPI geben den Fehlercode AUDCLNT E DEVICE INVALIDATED zurück, wenn das Audioendpunktgerät, das die Clientanwendung verwendet, \_ \_ ungültig \_ wird. Dieser Fehlercode gibt an, dass das Endpunktgerät nicht angeschlossen wurde oder dass die Audiohardware oder die zugehörigen Hardwareressourcen neu konfiguriert, deaktiviert, entfernt oder anderweitig für die Verwendung nicht verfügbar gemacht wurden. Häufig kann die Anwendung nach diesem Fehler wiederhergestellt werden.

>[!NOTE]
> Informationen zur Wiederherstellung nach ungültigen Gerätefehlern bei Verwendung von RÄUMLICHEN Audio-APIs (ISAC) finden Sie unter Wiederherstellen nach einem Invalid-Device [(Räumlicher Sound)](recovering-from-an-invalid-device-error-spatial-sound.md)

Die Strategie, die eine Anwendung zur Wiederherstellung nach einem AUDCLNT E DEVICE INVALIDATED-Fehler verwenden sollte, hängt davon ab, welche der folgenden Verfahren die Anwendung zum Auswählen eines Audioendpunktgeräts \_ \_ \_ verwendet:

-   Wählen Sie immer das Standardgerät für Audiorendering oder -erfassung aus.
-   Wählen Sie ein bestimmtes Audioendpunktgerät aus.

Im letzteren Fall wählt die Anwendung entweder automatisch ein bestimmtes Gerät basierend auf internen Anforderungen aus, oder der Benutzer kann ein Gerät explizit aus einer Liste der verfügbaren Geräte auswählen.

Eine Anwendung, die das Standardgerät verwendet, kann versuchen, eine Wiederherstellung nach einem AUDCLNT \_ E \_ DEVICE \_ INVALIDATED-Fehler wie folgt zu versuchen:

1.  Geben Sie [**die IAudioClient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) und alle anderen WASAPI-Schnittstellen frei, die sie auf dem Gerät erworben hat.
2.  Rufen Sie die [**IMMDeviceEnumerator::GetDefaultAudioEndpoint-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) auf, um das aktuelle Standardaudiogerät zu erhalten.
3.  Versuchen Sie, [**IAudioClient auf**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) dem Standardaudiogerät zu aktivieren.

Wenn Sie die oben genannten Schritte ausführen, reagiert die Anwendung in der Regel entsprechend, unabhängig von der Ursache des Fehlers AUDCLNT \_ E \_ DEVICE \_ INVALIDATED. Wenn die Neukonfiguration des Standardgeräts den Fehler verursacht hat (z. B. wenn der Benutzer das vom Gerät verwendete Streamformat geändert hat), ermöglichen diese Schritte der Anwendung bei Erfolg, weiterhin dasselbe Gerät zu verwenden. Wenn der Benutzer das von der Anwendung verwendete Gerät deaktiviert oder entfernt hat und ein anderes Gerät verfügbar ist, um die Rolle des Standardgeräts zu übernehmen, kann die Anwendung mithilfe des neuen Standardgeräts fortgesetzt werden. In beiden Fällen wird die Anwendung automatisch angepasst, ohne dass der Benutzer eingreifen muss.

Eine Anwendung, die ein bestimmtes Gerät auswählt, kann versuchen, die Wiederherstellung nach dem Fehler AUDCLNT \_ E \_ DEVICE \_ INVALIDATED wie folgt zu versuchen:

1.  Geben Sie [**die IAudioClient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) und alle anderen WASAPI-Schnittstellen frei, die sie auf dem Gerät erworben hat.
2.  Versuchen Sie, eine [**IAudioClient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) auf demselben Gerät zu aktivieren.
3.  Wenn Schritt 2 fehlschlägt, kann die Anwendung den Benutzer optional auffordern, ein anderes Gerät auszuwählen.

Schritt 2 kann erfolgreich sein, wenn das von der Anwendung verwendete Gerät neu konfiguriert, aber nicht deaktiviert oder entfernt wurde. Wenn dies erfolgreich ist, ermöglicht Schritt 2 der Anwendung, dasselbe Gerät automatisch weiter zu verwenden, ohne dass der Benutzer eingreifen muss. Schritt 3 ist geeignet, wenn die Anwendung es dem Benutzer ermöglicht, explizit ein anderes Gerät auszuwählen, nachdem der Benutzer das zuvor verwendete Gerät deaktiviert oder entfernt hat.

Eine Anwendung kann die Ursache eines Gerätefehlers genauer bestimmen, indem sie sich registriert, um eine Benachrichtigung zu erhalten, wenn eine Sitzung ihre Verbindung mit einem Gerät verliert. Um diese Benachrichtigung zu aktivieren, implementiert die Anwendung eine [**IAudioSessionEvents-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) und ruft die [**IAudioSessionControl::RegisterAudioSessionNotification-Methode**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) auf, um die Schnittstelle zu registrieren. Wenn ein Fehler mit ungültigen Geräten dazu führt, dass die Sitzung getrennt wird, ruft WASAPI die [**IAudioSessionEvents::OnSessionDisconnected-Methode**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) in der registrierten Schnittstelle auf. Mit dieser Methode informiert WASAPI die Anwendung über den Grund für die Trennung der Verbindung. In Windows Vista identifiziert **der OnSessionDisconnected-Aufruf** die folgenden Gründe:

-   Der Benutzer hat das Audioendpunktgerät entfernt.
-   Der Windows Audiodienst wurde heruntergefahren.
-   Das bevorzugte Streamformat wurde für das Gerät geändert, mit dem die Audiositzung verbunden ist.
-   Der Benutzer hat die Windows-Terminal Services-Sitzung (WTS) abgemeldet, in der die Audiositzung ausgeführt wurde. Weitere Informationen zu WTS finden Sie in der Dokumentation Windows SDK.
-   Die WTS, in der die Audiositzung ausgeführt wurde, wurde getrennt.
-   Die Audiositzung (freigegebener Modus) wurde getrennt, um das Audioendpunktgerät für eine Verbindung im exklusiven Modus verfügbar zu machen.

Als Reaktion auf das Trennungsereignis schließt WASAPI alle Streams, die zur Sitzung gehören. Wenn eine Anwendung anschließend versucht, über eine WASAPI-Methode wie [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)auf einen geschlossenen Stream zuzugreifen, schlägt die Methode fehl und gibt den Fehlercode AUDCLNT \_ E DEVICE \_ \_ INVALIDATED zurück.

Ein weiterer Vorteil beim Empfangen von Benachrichtigungen über die [**IAudioSessionEvents-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) ist, dass die Benachrichtigungen asynchron eintreffen. Selbst wenn der Stream nicht ausgeführt wird, erhält die Anwendung daher weiterhin rechtzeitig eine Benachrichtigung über Fehler mit ungültigen Geräten, die die Ausführung des Streams verhindern können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streamverwaltung](stream-management.md)
</dt> </dl>

 

 



