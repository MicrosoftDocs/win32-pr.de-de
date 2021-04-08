---
title: Problembehandlung bei Internet Verbindungen
description: In diesem Szenario versucht ein Benutzer, www.MSN.com über das HTTPS-Protokoll zu suchen, kann jedoch keine Verbindung herstellen. Mithilfe von Netsh und Netzwerkmonitor können Sie Ablauf Verfolgungen erfassen und anzeigen, um zu ermitteln, warum die Verbindung nicht hergestellt werden konnte.
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753636c1186243a96e3cef5a4ab73244556daec4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855912"
---
# <a name="troubleshooting-internet-connections"></a><span data-ttu-id="dcdc7-104">Problembehandlung bei Internet Verbindungen</span><span class="sxs-lookup"><span data-stu-id="dcdc7-104">Troubleshooting Internet Connections</span></span>

<span data-ttu-id="dcdc7-105">In diesem Szenario versucht ein Benutzer, www.MSN.com über das HTTPS-Protokoll zu suchen, kann jedoch keine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="dcdc7-105">In this scenario, a user is attempting to browse to www.msn.com using the https protocol, but is unable to connect.</span></span> <span data-ttu-id="dcdc7-106">Mithilfe von Netsh und Netzwerkmonitor können Sie Ablauf Verfolgungen erfassen und anzeigen, um zu ermitteln, warum die Verbindung nicht hergestellt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="dcdc7-106">You can use Netsh and Network Monitor to collect and view traces in order to help determine why the connection failed.</span></span>

<span data-ttu-id="dcdc7-107">Zuerst können Sie mit Netsh eine Ablauf Verfolgung starten.</span><span class="sxs-lookup"><span data-stu-id="dcdc7-107">First, you can use netsh to start a trace.</span></span> <span data-ttu-id="dcdc7-108">Wenn Sie **Netsh Trace Start Scenario = Internetclient Tracefile = MSN. ETL** eingeben, wird die Ablauf Verfolgung für alle unter dem Internet Client-Szenario aktivierten Anbieter gestartet, wobei die Ergebnisse in einer Datei namens MSN. ETL gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="dcdc7-108">Typing **netsh trace start scenario = InternetClient tracefile=msn.etl** starts tracing for all of the providers enabled under the InternetClient scenario, saving the results to a file named msn.etl.</span></span> <span data-ttu-id="dcdc7-109">Nachdem Sie mithilfe eines Webbrowsers versucht haben, www.MSN.com zu erreichen, wird die Eingabe von **Netsh Trace beenden** beendet und die Ablauf Verfolgungs Datei korreliert.</span><span class="sxs-lookup"><span data-stu-id="dcdc7-109">After using a web browser to attempt to reach www.msn.com, typing **netsh trace stop** terminates and correlates the trace file.</span></span>

<span data-ttu-id="dcdc7-110">Sie können dann die Datei msn. ETL in Netzwerkmonitor öffnen.</span><span class="sxs-lookup"><span data-stu-id="dcdc7-110">You can then open the msn.etl file in Network Monitor.</span></span> <span data-ttu-id="dcdc7-111">Die Ereignisse werden im linken Bereich nach der Aktivitäts-ID gruppiert.</span><span class="sxs-lookup"><span data-stu-id="dcdc7-111">The events are grouped by activity ID in the left pane.</span></span> <span data-ttu-id="dcdc7-112">Mithilfe der Filter **Beschreibung. enthält ("MSN")** zeigt nur die Ereignisse an, die die Zeichenfolge "MSN" in ihrer Protokoll Beschreibung enthalten.</span><span class="sxs-lookup"><span data-stu-id="dcdc7-112">Using the filter **description.contains("msn")** will show only those events which include the string "msn" in their protocol description.</span></span>

![Problembehandlung bei Internetverbindungen mithilfe des Netzwerk Monitors (1)](images/internetclient1.png)

<span data-ttu-id="dcdc7-114">Als nächstes können Sie die Ereignisse in der Frame Zusammenfassung überprüfen, um ein Ereignis zu identifizieren, das relevant aussieht.</span><span class="sxs-lookup"><span data-stu-id="dcdc7-114">Next, you can review the events in the frame summary to identify an event which looks relevant.</span></span> <span data-ttu-id="dcdc7-115">Nachdem Sie das Ereignis ausgewählt haben, klicken Sie mit der rechten Maustaste, und zeigen Sie auf Konversationen suchen, und klicken Sie dann auf utevent, um die Konversation auf der utevent</span><span class="sxs-lookup"><span data-stu-id="dcdc7-115">After you select the event, right-click and point to Find Conversations, then click UTEvent to select the conversation at the UTEvent level.</span></span>

![Problembehandlung bei Internetverbindungen mithilfe des Netzwerk Monitors (2)](images/internetclient2.png)

<span data-ttu-id="dcdc7-117">Die zugeordnete normalisierte Aktivität im linken Bereich wird dann hervorgehoben, in diesem Fall utevent ActivityId 397.</span><span class="sxs-lookup"><span data-stu-id="dcdc7-117">The associated normalized activity in the left pane is then highlighted, in this case UTEvent ActivityID 397.</span></span>

![Problembehandlung bei Internetverbindungen mithilfe des Netzwerk Monitors (3)](images/internetclient3.png)

<span data-ttu-id="dcdc7-119">Wenn Sie Netzwerkmonitor verwenden, um die Ablauf Verfolgungs Informationen anzuzeigen und zu filtern, wurde die Anzahl der zu überprüfenden Ereignisse von 1989 auf 96 reduziert.</span><span class="sxs-lookup"><span data-stu-id="dcdc7-119">By using Network Monitor to view and filter the trace information, the number of events to examine has been reduced from 1989 to 96.</span></span>

 

 




