---
title: Plug-In für Typ 2-Onlineshops
description: Plug-In für Typ 2-Onlineshops
ms.assetid: 16e90a01-20be-49a6-96df-de81a7283f42
keywords:
- Windows Media Player Online Stores, Plug-ins
- Online Stores, Plug-ins
- Typ 2 Online Stores, Plug-ins
- Windows Media Player Online Stores, iwmpabonneptionservice-Schnittstelle
- Online Stores, iwmpabonneptionservice-Schnittstelle
- Type 2 Online Stores, iwmpabonneptionservice Interface
- Plug-ins, Windows Media Player Online Stores
- Plug-ins, Online Stores
- Plug-ins, Typ 2 Online Stores
- Plug-ins, iwmpabonneptionservice-Schnittstelle
- Windows Media Player-Plug-ins, Typ 2 Online Stores
- Windows Media Player-Plug-ins, Online Stores
- Windows Media Player-Plug-ins, Windows Media Player Online Stores
- Windows Media Player-Plug-ins, iwmpabonneptionservice-Schnittstelle
- Iwmpabonptionservice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d2f3aeeaa7456c3452b498a1a728e24c96783c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101355"
---
# <a name="type-2-online-store-plug-in"></a>Plug-In für Typ 2-Onlineshops

Ein Typ 2-Onlinespeicher-Plug-in ist eine COM-Komponente, die die [iwmpabonneptionservice](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) -Schnittstelle und optional die [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2) -Schnittstelle implementiert. Windows Media Player 9 Ruft die Methoden der **iwmpabonneptionservice** -Schnittstelle auf. Windows Media Player 10 oder höher Ruft die Methoden der **iwmpabonneptionservice** -und **IWMPSubscriptionService2** -Schnittstellen auf.

Ein Online-Speicher-Plug-in für den Typ 2 wird als Prozess interner com-Server verpackt. Das heißt, das Plug-in wird in einer DLL-Datei implementiert, die dem Windows-Media Player Prozess zugeordnet ist.

Windows Media Player aktiviert bei Bedarf Type 2 Online Store-Plug-ins. Nehmen wir beispielsweise an, der Benutzer versucht, ein geschütztes Lied wiederzugeben, und es ist keine aktuelle Lizenz vorhanden. In diesem Fall überprüft Windows Media Player das **contentdistributor** -Attribut entweder im File-Header oder im DRM-Header. Wenn ein Wert vorhanden ist, der mit dem Schlüsselnamen eines Online Stores übereinstimmt, wird die Registrierung von Windows Media Player überprüft, um festzustellen, ob der Online Shop ein Plug-in vom Typ 2 bereitgestellt hat. Wenn das Plug-in vorhanden ist, lädt Windows Media Player das Plug-in und ruft seine Methoden auf, um zu bestimmen, ob der Benutzer über die Berechtigung zum Abspielen des Titels verfügt.

In der folgenden Liste werden einige Szenarien beschrieben, in denen Windows Media Player ein Online Store-Plug-in vom Typ 2 aufruft.

-   **Der Benutzer versucht, Online Store-Inhalte wiederzugeben.** In diesem Fall ruft Windows Media Player die [iwmpabonneptionservice:: allowplay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) -Methode des Plug-Ins auf und übergibt einen Zeiger auf das digitale Medien Element, das vom Benutzer wiedergegeben werden soll. Der Online Shop kann diese Option verwenden, um die Lizenz des Benutzers zu aktualisieren, um den Inhalt wiederzugeben oder wiederzugeben. Wenn das Plug-in im *pfallowplay* -Parameter **true** zurückgibt, versucht Windows Media Player, den Inhalt wiederzugeben. Die Wiedergabe schlägt weiterhin fehl, wenn keine gültige Lizenz vorhanden ist. bei diesem Prozess werden Digital Rights Management (DRM) nicht umgangen.
-   **Der Benutzer fordert die Berechtigung zum Brennen von Inhalten auf eine CD oder DVD an.** In diesem Fall ruft Windows Media Player die [iwmpabonneptionservice:: allowcdburn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn) -Methode des Plug-Ins auf.
-   **Der Benutzer versucht, Online Store-Inhalte mit einem Gerät zu synchronisieren, oder Windows Media Player bereit für die automatische Synchronisierung von Online Store-Inhalten mit einem Gerät.** In diesem Fall ruft Windows Media Player die [IWMPSubscriptionService2::p](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync) -Methode des Plug-Ins auf, um den Online Store zu warnen, dass ein Medien Element mit einem bestimmten Gerät synchronisiert werden soll, das durch den kanonischen Namen identifiziert wird. Dies ist eine Möglichkeit für den Online Shop, zu bestimmen, ob der Benutzer das Medien Element mit dem Gerät synchronisieren darf. Es ist auch eine Möglichkeit für den Online Shop, das Gerät auf die Synchronisierung vorzubereiten und Datensätze zu aktualisieren, wie z. b. Synchronisierungs Anzahlen, die mit dem Gerät oder dem Medien Element verknüpft sind. Das Plug-in sollte die Berechtigungen für Berechtigungen, Vorbereitung und Daten Satz Aufbewahrung an einen separaten Thread übergeben und direkt von **prepareforsync** zurückgeben. Wenn der separate Thread seine Arbeit beendet hat, muss er den Windows-Media Player Benachrichtigen, indem er " [iwmpabonneptionservicecallback:: OnComplete](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservicecallback-oncomplete)" anruft.
-   **Ein Gerät wird für die Hintergrundverarbeitung verfügbar.** Wenn ein Gerät verbunden ist, benachrichtigt Windows Media Player den Online Store, dass das Gerät verfügbar ist, und befindet sich im Leerlauf, indem [IWMPSubscriptionService2::d eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable)aufgerufen wird.
-   **Der Benutzer klickt auf eine Schaltfläche, um einen Online Shop in Windows Media Player zu aktivieren.** Wenn dies auftritt, ruft Windows Media Player die [IWMPSubscriptionService2:: serviceevent](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-serviceevent) -Methode des Plug-Ins auf. Außerdem ruft Windows Media Player diese Methode auf, wenn der Benutzer zu einem anderen Dienst wechselt.
-   **Windows Media Player wechselt in den Zustand "geringe Aktivität".** In diesem Fall ruft der Player die [iwmpabonneptionservice:: startbackgroundprocessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing) -Methode des Plug-Ins auf. Der Online Shop kann diese Gelegenheit nutzen, um Threads zu starten oder zu reaktivieren, die Hintergrundaufgaben ausführen, z. b. das erneuern abgelaufener Lizenzen oder das Kompilieren von Wiedergabe Daten.
-   **Windows Media Player wechselt in den Status "hohe Aktivität".** In diesem Fall ruft Windows Media Player die [IWMPSubscriptionService2:: stopbackgroundprocessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-stopbackgroundprocessing) -Methode des Plug-Ins auf. Dadurch wird dem Plug-in mitgeteilt, dass es alle Threads aussetzen muss, die Hintergrundaufgaben ausführen.

Windows Media Player gibt die Online Store-Komponente frei, wenn die Spieler Sitzung beendet wird. Bei der Freigabe muss die Komponente alle im laufenden Hintergrund verarbeiteten Vorgänge unterbrechen und dann Herunterfahren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmpabonneptionservice-Schnittstelle**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**IWMPSubscriptionService2-Schnittstelle**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> <dt>

[**Iwmpabonneptionservicecallback-Schnittstelle**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)
</dt> <dt>

[**Type 2 Online Store-Beispiele**](type-2-online-store-samples.md)
</dt> </dl>

 

 




