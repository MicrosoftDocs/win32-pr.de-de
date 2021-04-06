---
title: Starten und Beenden von Microsoft Locator
description: Die RPC-Laufzeitbibliotheken starten Microsoft Locator bei Bedarf automatisch. Sie können den Locator manuell beenden und starten, wenn Sie z. b. die Datenbank beim Debuggen einer verteilten Anwendung löschen müssen.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ffdb11e86b06ee53d9b01f7f7755758538f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036247"
---
# <a name="starting-and-stopping-microsoft-locator"></a><span data-ttu-id="5e12b-104">Starten und Beenden von Microsoft Locator</span><span class="sxs-lookup"><span data-stu-id="5e12b-104">Starting and Stopping Microsoft Locator</span></span>

<span data-ttu-id="5e12b-105">Die RPC-Laufzeitbibliotheken starten Microsoft Locator bei Bedarf automatisch.</span><span class="sxs-lookup"><span data-stu-id="5e12b-105">The RPC run-time libraries automatically start Microsoft Locator when necessary.</span></span> <span data-ttu-id="5e12b-106">Sie können den Locator manuell beenden und starten, wenn Sie z. b. die Datenbank beim Debuggen einer verteilten Anwendung löschen müssen.</span><span class="sxs-lookup"><span data-stu-id="5e12b-106">You can manually stop and start the Locator if, for example, you need to clear the database while debugging a distributed application.</span></span>

<span data-ttu-id="5e12b-107">**So starten Sie den Microsoft-Locator und starten ihn**</span><span class="sxs-lookup"><span data-stu-id="5e12b-107">**To stop and start Microsoft Locator**</span></span>

1.  <span data-ttu-id="5e12b-108">Klicken Sie in der Systemsteuerung auf das Symbol "Dienste".</span><span class="sxs-lookup"><span data-stu-id="5e12b-108">From Control Panel, click the Services icon.</span></span>

    <span data-ttu-id="5e12b-109">Das Dialogfeld **Dienste** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e12b-109">The **Services** dialog box appears.</span></span>

2.  <span data-ttu-id="5e12b-110">Wählen Sie im Dialogfeld **Dienst** die Option **Microsoft Locator** aus, und klicken Sie dann auf **starten oder starten** .</span><span class="sxs-lookup"><span data-stu-id="5e12b-110">In the **Service** dialog box, select **Microsoft Locator** and then click **Start** or **Stop**.</span></span>

<span data-ttu-id="5e12b-111">Sie können den Microsoft-Locator auch über die Befehlszeile starten und Abbrechen, indem Sie Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="5e12b-111">You can also start and stop Microsoft Locator from the command line by typing:</span></span>

<span data-ttu-id="5e12b-112">**NET \[ Start/-Vorgang zum Abbrechen von \] RpcLocator**</span><span class="sxs-lookup"><span data-stu-id="5e12b-112">**net \[start/stop\] rpclocator**</span></span>

<span data-ttu-id="5e12b-113">Nur ein Administrator kann den Microsoft-Locator starten, nachdem er beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5e12b-113">Only an administrator can start Microsoft Locator once it is stopped.</span></span> <span data-ttu-id="5e12b-114">Wenn Sie beendet ist, wird Sie nach Bedarf von den RPC-Laufzeitbibliotheken neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="5e12b-114">If stopped, it will be restarted as necessary by the RPC run-time libraries.</span></span>

 

 




