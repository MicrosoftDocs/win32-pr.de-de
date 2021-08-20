---
title: Plug-In für Typ 2-Onlineshops
description: Plug-In für Typ 2-Onlineshops
ms.assetid: 16e90a01-20be-49a6-96df-de81a7283f42
keywords:
- Windows Media Player,Plug-Ins
- Onlineshops, Plug-Ins
- 'Typ 2: Onlineshops,Plug-Ins'
- Windows Media Player,IWMPSubscriptionService-Schnittstelle
- Onlineshops,IWMPSubscriptionService-Schnittstelle
- Typ 2 Onlineshops,IWMPSubscriptionService-Schnittstelle
- Plug-Ins, Windows Media Player Onlineshops
- Plug-Ins, Onlineshops
- Plug-Ins, Geben Sie 2 Onlineshops ein.
- Plug-Ins, IWMPSubscriptionService-Schnittstelle
- Windows Media Player-Plug-Ins geben Sie zwei Onlineshops ein.
- Windows Media Player-Plug-Ins, Onlineshops
- Windows Media Player-Plug-Ins, Windows Media Player Onlineshops
- Windows Media Player Plug-Ins, IWMPSubscriptionService-Schnittstelle
- IWMPSubscriptionService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a254fe0aeed0d03f4437c408f4c00c181fdeb07cf75df8ff9d7a1139ea284150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117477"
---
# <a name="type-2-online-store-plug-in"></a>Plug-In für Typ 2-Onlineshops

Ein Typ 2-Onlineshop-Plug-In ist eine COM-Komponente, die die [IWMPSubscriptionService-Schnittstelle](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) und optional die [IWMPSubscriptionService2-Schnittstelle](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2) implementiert. Windows Media Player 9 ruft die Methoden der **IWMPSubscriptionService-Schnittstelle** auf. Windows Media Player 10 oder höher ruft die Methoden der **Schnittstellen IWMPSubscriptionService** und **IWMPSubscriptionService2** auf.

Ein Plug-In vom Typ 2 für den Onlineshop wird als In-Process-COM-Server gepackt. Das heißt, das Plug-In wird in einer .dll implementiert, die dem Windows Media Player zugeordnet ist.

Windows Media Player aktiviert plug-ins des Typs 2 nach Bedarf. Angenommen, der Benutzer versucht, einen geschützten Titel zu spielen, und es gibt keine aktuelle Lizenz für die Wiedergabe. In diesem Fall überprüft Windows Media Player **ContentDistributor-Attribut** entweder im Dateiheader oder im DRM-Header. Wenn ein Wert vorhanden ist, der dem Schlüsselnamen eines Onlineshops entspricht, überprüft Windows Media Player die Registrierung, um festzustellen, ob dieser Onlineshop ein Plug-In vom Typ 2 bereitgestellt hat. Wenn das Plug-In vorhanden ist, lädt Windows Media Player das Plug-In und ruft dessen Methoden auf, um zu bestimmen, ob der Benutzer über die Rechte zum Spielen des Titels verfügt.

In der folgenden Liste werden einige Szenarien beschrieben, in denen Windows Media Player ein Plug-In vom Typ 2 des Onlineshops aufruft.

-   **Der Benutzer versucht, Inhalte des Onlineshops wieder zu spielen.** In diesem Fall ruft Windows Media Player die [IWMPSubscriptionService::allowPlay-Methode](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) des Plug-Ins auf und überspringt dabei einen Zeiger auf das digitale Medienelement, das der Benutzer wiederzuspielen versucht. Der Onlineshop kann dies als Gelegenheit nutzen, die Lizenz des Benutzers zu aktualisieren, um den Inhalt wiedergeben oder die Wiedergabe zu veralten. Wenn das Plug-In **TRUE im** *parameter pfAllowPlay* zurückgibt, versucht Windows Media Player, den Inhalt wiederzuspielen. Die Wiedergabe wird weiterhin fehlschlagen, wenn keine gültige Lizenz vorhanden ist. Durch diesen Prozess wird die Verwaltung digitaler Rechte (Digital Rights Management, DRM) nicht umgangen.
-   **Der Benutzer fordert die Berechtigung an, Inhalte auf eine CD oder DVD zu speichern.** In diesem Fall ruft Windows Media Player die [IWMPSubscriptionService::allowCD Skript-Methode des Plug-Ins](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn) auf.
-   **Der Benutzer versucht, Inhalte des Onlineshops mit einem Gerät zu synchronisieren, oder Windows Media Player ist bereit, Inhalte des Onlineshops automatisch mit einem Gerät zu synchronisieren.** In diesem Fall ruft Windows Media Player die [IWMPSubscriptionService2::p repareForSync-Methode](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync) des Plug-Ins auf, um den Onlineshop zu warnen, dass ein Medienelement mit einem bestimmten Gerät synchronisiert werden soll, das durch seinen kanonischen Namen identifiziert wird. Dies ist eine Möglichkeit für den Onlineshop zu bestimmen, ob der Benutzer das Medienelement mit dem Gerät synchronisieren darf. Es ist auch eine Möglichkeit für den Onlineshop, das Gerät für die Synchronisierung vorzubereiten und Datensätze zu aktualisieren, z. B. die Synchronisierungsanzahl, die dem Gerät oder dem Medienelement zugeordnet sind. Das Plug-In sollte die Berechtigungs-, Vorbereitungs- und Datensatz-Aufbewahrungsaufgaben an einen separaten Thread übergeben und sofort von **prepareForSync zurückgeben.** Wenn der separate Thread seine Arbeit abgeschlossen hat, muss er Windows Media Player durch Aufrufen [von IWMPSubscriptionServiceCallback::onComplete benachrichtigen.](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservicecallback-oncomplete)
-   **Ein Gerät steht für die Hintergrundverarbeitung zur Verfügung.** Wenn ein Gerät verbunden ist, Windows Media Player den Onlineshop durch Aufrufen von [IWMPSubscriptionService2::d eviceAvailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable)darauf hin, dass das Gerät verfügbar ist und sich im Leerlauf befindet.
-   **Der Benutzer klickt auf eine Schaltfläche, um einen Onlineshop in der Windows Media Player.** In diesem Fall ruft Windows Media Player die [IWMPSubscriptionService2::serviceEvent-Methode](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-serviceevent) des Plug-Ins auf. Windows Media Player ruft diese Methode auch auf, wenn der Benutzer zu einem anderen Dienst wechselt.
-   **Windows Media Player in einen Zustand mit geringer Aktivität.** In diesem Fall ruft der Player die [IWMPSubscriptionService::startBackgroundProcessing-Methode](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing) des Plug-Ins auf. Der Onlineshop kann diese Gelegenheit nutzen, um Threads zu starten oder zu reaktivieren, die Hintergrundaufgaben ausführen, z. B. das Erneuern abgelaufener Lizenzen oder das Kompilieren von Play count-Daten.
-   **Windows Media Player in einen Zustand mit hoher Aktivität.** In diesem Fall ruft Windows Media Player die [IWMPSubscriptionService2::stopBackgroundProcessing-Methode](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-stopbackgroundprocessing) des Plug-Ins auf. Dadurch wird das Plug-In darüber informiert, dass alle Threads angehalten werden müssen, die Hintergrundaufgaben ausführen.

Windows Media Player die Komponente des Onlineshops frei, wenn die Player-Sitzung beendet wird. Nach der Veröffentlichung muss die Komponente die laufende Hintergrundverarbeitung unterbrechen und dann herunterfahren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMPSubscriptionService-Schnittstelle**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**IWMPSubscriptionService2-Schnittstelle**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> <dt>

[**IWMPSubscriptionServiceCallback-Schnittstelle**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)
</dt> <dt>

[**Geben Sie 2 Online Store beispiele ein.**](type-2-online-store-samples.md)
</dt> </dl>

 

 




