---
title: Supplicant-API-Rückruf Sequenz
description: Erfahren Sie mehr über die Supplicant-API-Rückruf Sequenz. Hier finden Sie eine Übersicht über die Rückruf Sequenz und weitere verfügbare Ressourcen.
ms.assetid: 83276783-aee5-43ac-982d-1144df982a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c93afea6dbf4c3220bbeaec4f6278eb3d0b756
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949131"
---
# <a name="supplicant-api-call-sequence"></a>Supplicant-API-Rückruf Sequenz

In diesem Thema wird die spezifische Rückruf Sequenz für die Supplicant-API bereitstellt.

## <a name="supplicant-api-call-sequence-overview"></a>Übersicht über die Supplicant-API-Rückruf Sequenz

Wenn der Supplicant ein EAP-Paket von einem Anbieter empfängt (z. b. einen Zugriffspunkt), erfolgt in der Regel der folgende Supplicant API-Aufruffluss.

-   Die Anwendung ruft " [**eaphostpeer erbeginsession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) " mit EAPHost-Konfigurationsdaten und Benutzerdaten auf. Bei einem erfolgreichen-Rückruf wird ein Sitzungs Handle des **EAP- \_ Sitzungs \_ Handles** zurückgegeben.
-   Jedes vom Supplicant empfangene Paket wird durch einen [**eaphostpeer-processreceivedpacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket)-Code verarbeitet. Der Supplicant ruft dann die Funktion auf, die dem von der Funktion zurückgegebenen Aktions Code entspricht.
-   Wenn der Aktions Code **eaphosteterresponsesend** ist, ruft der Supplicant [**eaphostpeer-getsendpacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) auf, um die an den Authentifikator zu sendende Antwort zu erhalten.
-   Wenn während der Sitzung der an den Supplicant zurückgegebene Aktions Code **eaphostpeerresponserespond** ist, weist dies darauf hin, dass EAP-Attribute verfügbar sind. Der Supplicant ruft dann [**eaphostpeer Attribute**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) auf, um Sie abzurufen. Diese Attribute enthalten ergänzende Daten, die während des Authentifizierungs Vorgangs verwendet werden. Nachdem der Supplicant die Verarbeitung der Attribute abgeschlossen hat, ruft er [**eaphostpeer Attribute**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) auf, die die Daten aktualisieren. Diese Funktion gibt einen Aktions Code zurück, der die nächste Aktion des Supplicant bestimmt.
-   Wenn der Aktions Code **eaphosteterresponseinvokeui** lautet, löst der Supplicant ein Dialogfeld für die Benutzeroberfläche aus, um interaktive Daten vom Benutzer zu erhalten, z. b. Anmelde Informationen oder Identitätsinformationen. Weitere Informationen finden Sie unten unter Benutzerinteraktion mit dem Supplicant-API-Aufrufe.
-   Wenn der Aktions Code **eaphosteterresponseresult** ist, weist dies darauf hin, dass die Ergebnisse der Authentifizierungs Sitzung für den Supplicant verfügbar sind. Der Supplicant ruft dann [**eaphostpeer ergetresult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult) auf, um die Ergebnisse zu erhalten. Unabhängig davon, ob die Ergebnisse Erfolg oder Fehler anzeigen, ruft der Supplicant [**eaphostpeer-EndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession)auf. Bei einem Fehler kann die erneute Authentifizierung versucht werden, indem eine andere Sitzung mit EAPHost geöffnet und eine neue Identität bereitgestellt wird oder die Authentifizierung mit der ursprünglichen Identität erneut versucht wird.

## <a name="user-interaction-with-the-supplicant-api-call-flow"></a>Benutzerinteraktion mit dem Supplicant API-Aufruffluss

In bestimmten Fällen muss der Supplicant Informationen vom Benutzer abrufen, um den Authentifizierungsprozess fortzusetzen.

In der folgenden Liste wird die Abfolge der Aufrufe für den Supplicant-und den EAPHost-UI-Prozess veranschaulicht, die zum Aktivieren interaktiver Eingaben erforderlich sind.

1.  Der Supplicant erhält den aktuellen Benutzeroberflächen Kontext durch Aufrufen von [**eaphostpeer ergetuicontext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext).
2.  Der Supplicant sendet dann die Benutzeroberflächen-Kontext Daten an den Supplicant-UI-Prozess.
    > [!Note]  
    > Der UI-Prozess, der in der Regel eine Benutzeroberfläche sammelt oder interaktive Benutzeroberfläche verarbeitet, ist vom Supplicant-Prozess getrennt. Das Trennen der beiden Prozesse ist keine Voraussetzung für EAPHost, aber dies hat den Vorteil, dass der UI-Prozess mit dem Desktop interagieren kann.

     

3.  Wenn das Supplicant-Element die Benutzeroberfläche selbst Rendering will, ruft es die [**eaphostpeer-queryinteractiveuiinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) -Funktion auf, um die Eingabefelder für interaktive UI-Komponenten zu erhalten, die ausgelöst werden sollen. Andernfalls folgt es dem herkömmlichen Modell des Aufrufs der interaktiven UI-Methode durch Aufrufen von [ **eaphostpeer-invokeinteractiveui** .](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)
    > [!Note]  
    > Wenn der [**Vorgang "EAP \_ E \_ EAPHost- \_ Methode \_ \_ nicht \_ unterstützt**](eap-related-error-and-information-constants.md) " zurückgegeben wird, muss der Supplicant dem herkömmlichen Modell des Aufrufs der interaktiven UI der Methode folgen, indem er [**eaphostpeerinvokeinteractiveui**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)aufruft. Wenn ein Fehler auftritt, gibt [**eaphostpeer-queryinteractiveuiinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) einen anderen Rückgabecode als **null** zurück.

     

4.  Unabhängig davon, ob die Supplicant [**eaphostpeer-queryinteractiveuiinputfields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) oder [**eaphostpeer activeui**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) aufruft, übergibt der UI-Prozess die vorhandenen Kontext Daten und lädt Eappcfg.dll. Die entsprechende Benutzeroberfläche wird zum Erfassen der neuen Daten ausgelöst. Die neuen Benutzeroberflächen-Kontext Daten, die jetzt möglicherweise Benutzereingaben enthalten, werden kopiert, und die alten Kontext Daten werden mit einem [**eappeerfrememory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory)-aufrufungs Vorgang freigegeben.
5.  Der UI-Prozess gibt die neuen Kontext Daten an den Supplicant zurück, der " [**eaphostetersetuicontext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) " aufruft, um ihn festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Peer Method API-Rückruf Sequenz](peer-method-api-call-sequence.md)
</dt> <dt>

[Authentifizierungsmethode-API-Rückruf Sequenz](authenticator-method-api-call-sequence.md)
</dt> <dt>

[EAPHost-Rückruf Sequenz](about-eaphost-call-sequences.md)
</dt> <dt>

[EAPHost-Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 




