---
title: Startsequenz
description: Schritte zum Starten des benutzerdefinierten Protokolls.
ms.assetid: 34c6eb08-668b-43b7-b49b-9ab7536ab658
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29dbb899905dd96e806ffe17a0eafd0091ad97b547ba9f172527ab0acc1b2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000544"
---
# <a name="start-sequence"></a>Startsequenz

Um Ihren Protokollanbieter zu starten, verwenden Sie den Remotedesktopdienste-Dienst:

-   Ruft den Namen des Listeners und die CLSID Ihres Protokoll-Manager-Objekts [**(IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) aus der Registrierung ab. Weitere Informationen finden Sie unter [Registrieren des Protokoll-Managers.](registering-the-custom-protocol.md)
-   Ruft Initialize auf, um den Protokoll-Manager zu [**initialisieren.**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize)
-   Erstellt ein Protokoll-Manager-Objekt mithilfe der CLSID. Selbst wenn mehrere Listener für denselben Protokollanbieter registriert sind, erstellt der Dienst nur ein Protokoll-Manager-Objekt.
-   Ruft [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) auf, um das Protokoll-Manager-Objekt anzuweisen, ein [**IWRdsProtocolListener-Listenerobjekt**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) zu erstellen und es an den Dienst zurückzugeben. Das Protokoll-Manager-Objekt muss einen Verweis auf das Listenerobjekt hinzufügen, bevor es an den Dienst zurückgegeben wird. Der Dienst gibt das Objekt frei, wenn der Dienst beendet oder der Listener gelöscht wird.
-   Ruft [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) für das Listenerobjekt auf, damit der Listener mit dem Lauschen auf eingehende Verbindungen beginnen kann.
-   Ruft [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) auf, um zu verhindern, dass das Listenerobjekt lauscht.
-   Ruft [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) auf, um die Initialisierung des Protokoll-Managers zu aufheben.

Der Listener erstellt ein [**IWRdsProtocolConnection-Objekt,**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) wenn ein Client versucht, eine Verbindung herzustellen. Das Listenerobjekt ruft [**OnConnected auf,**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) um den Remotedesktopdienste Dienst zu benachrichtigen, dass ein neuer Client versucht, eine Verbindung herzustellen oder erneut eine Verbindung herzustellen, und übergibt das **IWRdsProtocolConnection-Objekt** in diesem Aufruf. Der Remotedesktopdienste Dienst gibt wiederum ein [**IWRdsProtocolConnectionCallback-Objekt**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) in diesem Aufruf zurück, damit das Protokoll bei Bedarf mit dem Remotedesktopdienste Dienst kommunizieren kann. Der Dienst fügt vor der Rückgabe einen Verweis auf das Rückrufobjekt hinzu, und das Protokoll muss diesen Verweis freigeben, wenn die Verbindung geschlossen wird.

Die folgende Abbildung zeigt die Interaktion zwischen den verschiedenen Objekten während des Starts.

![rcm-Startsequenz](images/protocol-startsequence.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Methodenaufrufsequenz](method-call-sequence.md)
</dt> <dt>

[Verbindungssequenz](connection-sequence.md)
</dt> </dl>

 

 




