---
title: Start Sequenz
description: Schritte zum Starten des benutzerdefinierten Protokolls.
ms.assetid: 34c6eb08-668b-43b7-b49b-9ab7536ab658
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af0716e39d1df96bbdf29f4a3abbb14e32bc752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206349"
---
# <a name="start-sequence"></a>Start Sequenz

Um den Protokoll Anbieter zu starten, wird der Remotedesktopdienste-Dienst:

-   Ruft den Namen des Listener und die CLSID des Protokoll-Manager-Objekts ([**iwrdsprotocolmanager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) aus der Registrierung ab. Weitere Informationen finden Sie unter [Registrieren des Protokoll-Managers](registering-the-custom-protocol.md).
-   Ruft [**initialisieren**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) auf, um den Protokoll-Manager zu initialisieren.
-   Erstellt ein Protokoll-Manager-Objekt mit der CLSID. Auch wenn mehrere Listener für denselben Protokoll Anbieter registriert sind, erstellt der Dienst nur ein Protokoll-Manager-Objekt.
-   Ruft [**"**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) up" auf, um das Protokoll-Manager-Objekt anzuweisen, ein [**iwrdsprotocollistener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) -Listenerobjekt zu erstellen und an den Dienst zurückzugeben. Das Protokoll-Manager-Objekt muss einen Verweis auf das Listenerobjekt hinzufügen, bevor es an den Dienst zurückgegeben wird. Der Dienst gibt das Objekt frei, wenn der Dienst beendet wird oder der Listener gelöscht wird.
-   Ruft [**StartListening**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) für das Listener-Objekt auf, sodass der Listener mit dem lauschen auf eingehende Verbindungen beginnen kann.
-   Ruft [**Stop**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) -Abhör Vorgang auf, um das lauschen des listenerobjekts anzuhalten.
-   Ruft die [**uninitialisierung**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) auf, um den Protokoll-Manager zu initialisieren.

Der Listener erstellt ein [**iwrdsprodecolconnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) -Objekt, wenn ein Client versucht, eine Verbindung herzustellen. Das Listener-Objekt ruft [**onconnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) auf, um den Remotedesktopdienste-Dienst zu benachrichtigen, dass ein neuer Client versucht, eine Verbindung herzustellen oder die Verbindung wiederherzustellen, und übergibt das **iwrdsprodecolconnection** -Objekt in diesem Aufruf. Der Remotedesktopdienste-Dienst gibt wiederum ein [**iwrdsprotocolconnectioncallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) -Objekt in diesem-Befehl zurück, damit das Protokoll bei Bedarf mit dem Remotedesktopdienste Dienst kommunizieren kann. Der Dienst fügt vor der Rückgabe einen Verweis auf das Rückruf Objekt hinzu, und das Protokoll muss diesen Verweis freigeben, wenn die Verbindung geschlossen wird.

Die folgende Abbildung zeigt die Interaktion zwischen den verschiedenen Objekten während des Starts.

![RCM-Startsequenz](images/protocol-startsequence.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Methoden aufrufssequenz](method-call-sequence.md)
</dt> <dt>

[Verbindungs Sequenz](connection-sequence.md)
</dt> </dl>

 

 




