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
# <a name="start-sequence"></a><span data-ttu-id="c1ef8-103">Start Sequenz</span><span class="sxs-lookup"><span data-stu-id="c1ef8-103">Start Sequence</span></span>

<span data-ttu-id="c1ef8-104">Um den Protokoll Anbieter zu starten, wird der Remotedesktopdienste-Dienst:</span><span class="sxs-lookup"><span data-stu-id="c1ef8-104">To start your protocol provider, the Remote Desktop Services service:</span></span>

-   <span data-ttu-id="c1ef8-105">Ruft den Namen des Listener und die CLSID des Protokoll-Manager-Objekts ([**iwrdsprotocolmanager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-105">Retrieves the name of the listener and the CLSID of your protocol manager object ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) from the registry.</span></span> <span data-ttu-id="c1ef8-106">Weitere Informationen finden Sie unter [Registrieren des Protokoll-Managers](registering-the-custom-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="c1ef8-106">For more information, see [Registering the Protocol Manager](registering-the-custom-protocol.md).</span></span>
-   <span data-ttu-id="c1ef8-107">Ruft [**initialisieren**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) auf, um den Protokoll-Manager zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-107">Calls [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) to initialize the protocol manager.</span></span>
-   <span data-ttu-id="c1ef8-108">Erstellt ein Protokoll-Manager-Objekt mit der CLSID.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-108">Creates a protocol manager object using the CLSID.</span></span> <span data-ttu-id="c1ef8-109">Auch wenn mehrere Listener für denselben Protokoll Anbieter registriert sind, erstellt der Dienst nur ein Protokoll-Manager-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-109">Even if there are multiple listeners registered for the same protocol provider, the service only creates one protocol manager object.</span></span>
-   <span data-ttu-id="c1ef8-110">Ruft [**"**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) up" auf, um das Protokoll-Manager-Objekt anzuweisen, ein [**iwrdsprotocollistener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) -Listenerobjekt zu erstellen und an den Dienst zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-110">Calls [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) to instruct the protocol manager object to create an [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) listener object and return it to the service.</span></span> <span data-ttu-id="c1ef8-111">Das Protokoll-Manager-Objekt muss einen Verweis auf das Listenerobjekt hinzufügen, bevor es an den Dienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-111">The protocol manager object must add a reference to the listener object before returning it to the service.</span></span> <span data-ttu-id="c1ef8-112">Der Dienst gibt das Objekt frei, wenn der Dienst beendet wird oder der Listener gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-112">The service will release the object when the service stops or the listener is deleted.</span></span>
-   <span data-ttu-id="c1ef8-113">Ruft [**StartListening**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) für das Listener-Objekt auf, sodass der Listener mit dem lauschen auf eingehende Verbindungen beginnen kann.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-113">Calls [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) on the listener object so that the listener can start listening for incoming connections.</span></span>
-   <span data-ttu-id="c1ef8-114">Ruft [**Stop**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) -Abhör Vorgang auf, um das lauschen des listenerobjekts anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-114">Calls [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) to stop the listener object from listening.</span></span>
-   <span data-ttu-id="c1ef8-115">Ruft die [**uninitialisierung**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) auf, um den Protokoll-Manager zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-115">Calls [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) to uninitialize the protocol manager.</span></span>

<span data-ttu-id="c1ef8-116">Der Listener erstellt ein [**iwrdsprodecolconnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) -Objekt, wenn ein Client versucht, eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-116">The listener creates an [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) object when a client tries to connect.</span></span> <span data-ttu-id="c1ef8-117">Das Listener-Objekt ruft [**onconnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) auf, um den Remotedesktopdienste-Dienst zu benachrichtigen, dass ein neuer Client versucht, eine Verbindung herzustellen oder die Verbindung wiederherzustellen, und übergibt das **iwrdsprodecolconnection** -Objekt in diesem Aufruf.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-117">The listener object calls [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) to notify the Remote Desktop Services service that a new client is trying to connect or reconnect, and passes the **IWRdsProtocolConnection** object in that call.</span></span> <span data-ttu-id="c1ef8-118">Der Remotedesktopdienste-Dienst gibt wiederum ein [**iwrdsprotocolconnectioncallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) -Objekt in diesem-Befehl zurück, damit das Protokoll bei Bedarf mit dem Remotedesktopdienste Dienst kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-118">The Remote Desktop Services service will in turn return an [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) object in that call so that the protocol can communicate with the Remote Desktop Services service as needed.</span></span> <span data-ttu-id="c1ef8-119">Der Dienst fügt vor der Rückgabe einen Verweis auf das Rückruf Objekt hinzu, und das Protokoll muss diesen Verweis freigeben, wenn die Verbindung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-119">The service adds a reference to the callback object before returning, and the protocol must release that reference when the connection closes.</span></span>

<span data-ttu-id="c1ef8-120">Die folgende Abbildung zeigt die Interaktion zwischen den verschiedenen Objekten während des Starts.</span><span class="sxs-lookup"><span data-stu-id="c1ef8-120">The following illustration shows the interaction between the various objects during startup.</span></span>

![RCM-Startsequenz](images/protocol-startsequence.png)

## <a name="related-topics"></a><span data-ttu-id="c1ef8-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1ef8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1ef8-123">Methoden aufrufssequenz</span><span class="sxs-lookup"><span data-stu-id="c1ef8-123">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="c1ef8-124">Verbindungs Sequenz</span><span class="sxs-lookup"><span data-stu-id="c1ef8-124">Connection Sequence</span></span>](connection-sequence.md)
</dt> </dl>

 

 




