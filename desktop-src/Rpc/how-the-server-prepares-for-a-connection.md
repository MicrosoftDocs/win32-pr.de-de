---
title: Wie der Server eine Verbindung vorbereitet
description: Wenn ein Serverprogramm mit der Ausführung beginnt, muss es zuerst die Schnittstelle oder die darin enthaltenen Schnittstellen mit der RPC-Lauf Zeit Bibliothek registrieren.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9787cc0f4a10da99f1401843450a6e00073e135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310352"
---
# <a name="how-the-server-prepares-for-a-connection"></a><span data-ttu-id="bd76e-103">Wie der Server eine Verbindung vorbereitet</span><span class="sxs-lookup"><span data-stu-id="bd76e-103">How the Server Prepares for a Connection</span></span>

<span data-ttu-id="bd76e-104">Wenn ein Serverprogramm mit der Ausführung beginnt, muss es zuerst die Schnittstelle oder die darin enthaltenen Schnittstellen mit der RPC-Lauf Zeit Bibliothek registrieren.</span><span class="sxs-lookup"><span data-stu-id="bd76e-104">When a server program begins execution, it must first register the interface or interfaces it contains with the RPC run-time library.</span></span> <span data-ttu-id="bd76e-105">Anschließend werden die erforderlichen Bindungs Informationen erstellt.</span><span class="sxs-lookup"><span data-stu-id="bd76e-105">It then creates the necessary binding information.</span></span> <span data-ttu-id="bd76e-106">Das Serverprogramm muss auch den Endpunkt oder die Endpunkte registrieren, an dem er lauscht.</span><span class="sxs-lookup"><span data-stu-id="bd76e-106">The server program must also register the endpoint or endpoints it listens to.</span></span> <span data-ttu-id="bd76e-107">Er kann dann mit dem lauschen auf Client Aufrufe beginnen.</span><span class="sxs-lookup"><span data-stu-id="bd76e-107">It can then begin listening for client calls.</span></span> <span data-ttu-id="bd76e-108">Dieser Vorgang wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="bd76e-108">This process is illustrated in the following diagram.</span></span>

![eine RPC-Serveranwendung bereitet Clientverbindungen vor](images/srvrcon.png)

<span data-ttu-id="bd76e-110">Je nach ausgewähltem Entwurf kann eine Serveranwendung eine andere Gruppe von Schritten auswählen. im vorherigen Beispiel und in der Abbildung ist ein Ansatz enthalten.</span><span class="sxs-lookup"><span data-stu-id="bd76e-110">Depending on the design chosen, a server application may choose a different set of steps; the previous example and illustration provides one approach.</span></span>

<span data-ttu-id="bd76e-111">Dieser Abschnitt enthält Informationen zu den Schritten, die ein Server Prozess ausführen muss, um eine Verbindung vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="bd76e-111">This section presents information on the steps that a server process must take to prepare for a connection.</span></span> <span data-ttu-id="bd76e-112">Die Diskussion ist in die folgenden Abschnitte unterteilt:</span><span class="sxs-lookup"><span data-stu-id="bd76e-112">The discussion is divided into the following sections:</span></span>

-   [<span data-ttu-id="bd76e-113">Registrieren der-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="bd76e-113">Registering the Interface</span></span>](registering-the-interface.md)
-   [<span data-ttu-id="bd76e-114">Verfügbar machung des Servers im Netzwerk</span><span class="sxs-lookup"><span data-stu-id="bd76e-114">Making the Server Available on the Network</span></span>](making-the-server-available-on-the-network.md)
-   [<span data-ttu-id="bd76e-115">Registrieren von Endpunkten</span><span class="sxs-lookup"><span data-stu-id="bd76e-115">Registering Endpoints</span></span>](registering-endpoints.md)
-   [<span data-ttu-id="bd76e-116">Lauschen auf Client Anrufe</span><span class="sxs-lookup"><span data-stu-id="bd76e-116">Listening for Client Calls</span></span>](listening-for-client-calls.md)

 

 




