---
description: Wiederherstellen nach einem Invalid-Device Fehler
ms.assetid: 1f5c3458-70ca-45ba-ac33-5c7b9f092320
title: Wiederherstellen nach einem Invalid-Device Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca20c32be46367f53a14ce26c39f980e3649b652
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127421"
---
# <a name="recovering-from-an-invalid-device-error"></a>Wiederherstellen nach einem Invalid-Device Fehler

Viele der Methoden in der WASAPI geben Fehlercode "audclnt \_ E \_ Device" ungültig aus \_ , wenn das audioendpunktgerät, das von der Client Anwendung verwendet wird, ungültig wird. Dieser Fehlercode gibt an, dass das Endpunkt Gerät getrennt wurde oder dass die Audiohardware oder die zugehörigen Hardware Ressourcen neu konfiguriert, deaktiviert, entfernt oder anderweitig zur Verwendung nicht verfügbar gemacht wurden. Häufig kann die Anwendung nach diesem Fehler wieder hergestellt werden.

>[!NOTE]
> Informationen zum Wiederherstellen von Fehlern bei ungültigen Geräten bei Verwendung von Spatial Audio APIs (Isac) finden Sie unter wieder [herstellen nach einem Invalid-Device Fehlers (räumlicher Sound)](recovering-from-an-invalid-device-error-spatial-sound.md) .

Die Strategie, die eine Anwendung für die Wiederherstellung nach einem ungültigen Fehler vom Typ "audclnt E" verwendet, \_ \_ \_ hängt davon ab, welche der folgenden Techniken von der Anwendung zum Auswählen eines audioendpunktgeräts verwendet wird:

-   Wählen Sie immer das standardmäßige audiorendering oder das Erfassungsgerät aus.
-   Wählen Sie ein bestimmtes audioendpunktgerät aus.

Im letzteren Fall wählt die Anwendung automatisch ein bestimmtes Gerät basierend auf den internen Anforderungen aus oder ermöglicht dem Benutzer, ein Gerät explizit aus einer Liste der verfügbaren Geräte auszuwählen.

Eine Anwendung, die das Standardgerät verwendet, kann versuchen, einen Fehler mit ungültigen Fehlern von "audclnt \_ E \_ Device" \_ wie folgt wiederherzustellen:

1.  Geben Sie die [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle und alle anderen WASAPI-Schnittstellen frei, die Sie auf dem Gerät erworben haben.
2.  Aufrufen der [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) -Methode, um das aktuelle Standardaudiogerät zu erhalten.
3.  Versuchen Sie, [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) auf dem Standardaudiogerät zu aktivieren.

Wenn Sie die obigen Schritte ausführen, reagiert die Anwendung in der Regel entsprechend, unabhängig von der Ursache des \_ \_ \_ ungültigen Fehlers "audclnt E Device". Wenn die Neukonfiguration des Standard Geräts den Fehler verursacht hat (z. b. wenn der Benutzer das vom Gerät verwendete Streamformat geändert hat), können diese Schritte, wenn Sie erfolgreich ausgeführt werden, es der Anwendung ermöglichen, das gleiche Gerät weiterhin zu verwenden. Wenn der Benutzer das Gerät, das von der Anwendung verwendet wurde, deaktiviert oder entfernt hat und ein anderes Gerät zur Annahme der Rolle des Standard Geräts verfügbar ist, kann die Anwendung mit dem neuen Standardgerät fortgesetzt werden. In beiden Fällen wird die Anwendung automatisch angepasst, ohne dass ein Eingreifen des Benutzers erforderlich ist.

Eine Anwendung, die ein bestimmtes Gerät auswählt, kann versuchen, eine Wiederherstellung mit einem \_ \_ ungültigen Fehler des Typs "audclnt E" durchführen \_ :

1.  Geben Sie die [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle und alle anderen WASAPI-Schnittstellen frei, die Sie auf dem Gerät erworben haben.
2.  Versuchen Sie, eine [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle auf demselben Gerät zu aktivieren.
3.  Wenn Schritt 2 fehlschlägt, kann die Anwendung als Option den Benutzer auffordern, ein anderes Gerät auszuwählen.

Schritt 2 kann erfolgreich ausgeführt werden, wenn das Gerät, das von der Anwendung verwendet wird, neu konfiguriert, aber nicht deaktiviert oder entfernt wurde. Bei erfolgreicher Ausführung ermöglicht Schritt 2 der Anwendung, das gleiche Gerät automatisch weiter zu verwenden, ohne dass ein Eingreifen des Benutzers erforderlich ist. Schritt 3 ist geeignet, wenn die Anwendung es dem Benutzer ermöglicht, ein anderes Gerät explizit auszuwählen, nachdem der Benutzer das zuvor verwendete Gerät deaktiviert oder entfernt hat.

Eine Anwendung kann die Ursache eines ungültigen Geräte Fehlers genauer ermitteln, indem registriert wird, um eine Benachrichtigung zu erhalten, wenn eine Sitzung die Verbindung zu einem Gerät verliert. Um diese Benachrichtigung zu aktivieren, implementiert die Anwendung eine [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle und ruft die [**iaudiosessioncontrol:: registeraudiosessionnotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) -Methode auf, um die Schnittstelle zu registrieren. Wenn ein ungültiger Gerätefehler bewirkt, dass die Sitzung getrennt wird, ruft WASAPI die [**iaudiosessionevents:: onsessiongetrennte**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) -Methode in der registrierten Schnittstelle auf. Über diese Methode informiert WASAPI die Anwendung über den Grund für die Trennung der Verbindung. In Windows Vista identifiziert der **onsessiongetrennte** -Befehl die folgenden Gründe:

-   Der Benutzer hat das audioendpunktgerät entfernt.
-   Der Windows-Audiodienst wurde heruntergefahren.
-   Das bevorzugte Streamformat wurde für das Gerät geändert, mit dem die Audiositzung verbunden ist.
-   Der Benutzer hat die Sitzung der Windows-Terminal Dienste (WTS) protokolliert, in der die Audiositzung ausgeführt wurde. Weitere Informationen zu WTS-Sitzungen finden Sie in der Windows SDK-Dokumentation.
-   Die WTS-Sitzung, in der die Audiositzung ausgeführt wurde, wurde getrennt.
-   Die (Shared-Mode)-Audiositzung wurde getrennt, um das audioendpunktgerät für eine Verbindung im exklusiven Modus verfügbar zu machen.

Als Reaktion auf das Ereignis zum Trennen der Verbindung schließt WASAPI alle Streams, die zur Sitzung gehören. Wenn eine Anwendung anschließend versucht, über eine WASAPI-Methode wie [**iaudioclient:: getcurrentpadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)auf einen geschlossenen Datenstrom zuzugreifen, schlägt die Methode fehl und gibt den Fehlercode "audclnt \_ E \_ Device \_ invalidiert" zurück.

Ein zusätzlicher Vorteil beim Empfang von Benachrichtigungen über die [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle besteht darin, dass die Benachrichtigungen asynchron eintreffen. Folglich erhält die Anwendung auch dann, wenn der Stream nicht ausgeführt wird, eine rechtzeitige Benachrichtigung über Fehler aufgrund ungültiger Geräte, die die Ausführung des Streams verhindern können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenstrom Verwaltung](stream-management.md)
</dt> </dl>

 

 



