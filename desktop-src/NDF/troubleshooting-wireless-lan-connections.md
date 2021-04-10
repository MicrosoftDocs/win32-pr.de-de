---
title: Problembehandlung für drahtlose LAN-Verbindungen
description: In diesem Szenario versucht ein Benutzer, eine Verbindung mit einem drahtlosen LAN herzustellen, kann jedoch keine Verbindung herstellen. Mithilfe von Netsh und Netzwerkmonitor können Sie Ablauf Verfolgungen erfassen und anzeigen, um zu ermitteln, warum die Verbindung nicht hergestellt werden konnte.
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55878afcee0091634415d4dbc465d1b143f46057
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037435"
---
# <a name="troubleshooting-wireless-lan-connections"></a><span data-ttu-id="51980-104">Problembehandlung für drahtlose LAN-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="51980-104">Troubleshooting Wireless LAN Connections</span></span>

<span data-ttu-id="51980-105">In diesem Szenario versucht ein Benutzer, eine Verbindung mit einem drahtlosen LAN herzustellen, kann jedoch keine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="51980-105">In this scenario, a user is attempting to connect to a wireless LAN, but is unable to connect.</span></span> <span data-ttu-id="51980-106">Mithilfe von Netsh und Netzwerkmonitor können Sie Ablauf Verfolgungen erfassen und anzeigen, um zu ermitteln, warum die Verbindung nicht hergestellt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="51980-106">You can use Netsh and Network Monitor to collect and view traces in order to help determine why the connection failed.</span></span>

<span data-ttu-id="51980-107">Zuerst können Sie mit Netsh eine Ablauf Verfolgung starten.</span><span class="sxs-lookup"><span data-stu-id="51980-107">First, you can use netsh to start a trace.</span></span> <span data-ttu-id="51980-108">Wenn Sie **Netsh Trace Start Scenario = WLAN Tracefile = wlanwpp. ETL** eingeben, wird die Ablauf Verfolgung für alle Anbieter gestartet, die im WLAN-Szenario aktiviert sind, und die Ergebnisse werden in einer Datei namens wlanwpp. ETL gespeichert.</span><span class="sxs-lookup"><span data-stu-id="51980-108">Typing **netsh trace start scenario = wlan tracefile=wlanwpp.etl** starts tracing for all of the providers enabled under the WLAN scenario, saving the results to a file named wlanwpp.etl.</span></span> <span data-ttu-id="51980-109">Wenn Sie versuchen, eine Verbindung mit dem drahtlosen LAN herzustellen, wird die Eingabe von **Netsh Trace beenden** beendet und die Ablauf Verfolgungs Datei korreliert.</span><span class="sxs-lookup"><span data-stu-id="51980-109">After attempting to connect to the wireless LAN, typing **netsh trace stop** terminates and correlates the trace file.</span></span>

<span data-ttu-id="51980-110">Anschließend können Sie die Datei wlanwpp. ETL in Netzwerkmonitor öffnen.</span><span class="sxs-lookup"><span data-stu-id="51980-110">You can then open the wlanwpp.etl file in Network Monitor.</span></span> <span data-ttu-id="51980-111">Die Ereignisse werden im linken Bereich nach der Aktivitäts-ID gruppiert.</span><span class="sxs-lookup"><span data-stu-id="51980-111">The events are grouped by activity ID in the left pane.</span></span>

![Problembehandlung bei drahtlosen LAN-Verbindungen mithilfe des Netzwerk Monitors (1)](images/1wlan.png)

<span data-ttu-id="51980-113">Die ETL enthält viele Ablauf Verfolgungen von anderen aktivierten Netzwerkanbietern.</span><span class="sxs-lookup"><span data-stu-id="51980-113">The ETL contains lot of traces from other network providers that are enabled.</span></span> <span data-ttu-id="51980-114">Sie können einen Filter anwenden, um nur die Ereignisse anzuzeigen, die für den **WLAN- \_ microsoftwindowtauautoconfig** -Anbieter relevant sind.</span><span class="sxs-lookup"><span data-stu-id="51980-114">You can apply a filter to display only those events which are relevant to the **WLAN\_MicrosoftWindowsWlanAutoConfig** provider.</span></span>

![Problembehandlung bei drahtlosen LAN-Verbindungen mithilfe des Netzwerk Monitors (2)](images/2wlan.png)

<span data-ttu-id="51980-116">Nachdem der Filter angewendet wurde, können Sie die Ereignisse in der Frame Zusammenfassung überprüfen, um ein Ereignis zu identifizieren, das relevant ist.</span><span class="sxs-lookup"><span data-stu-id="51980-116">After the filter has been applied, you can review the events in the frame summary to identify an event which looks relevant.</span></span> <span data-ttu-id="51980-117">Nachdem Sie das Ereignis ausgewählt haben, klicken Sie mit der rechten Maustaste, zeigen Sie auf Konversationen suchen, und klicken Sie auf netevent</span><span class="sxs-lookup"><span data-stu-id="51980-117">After you select the event, right-click and point to Find Conversations, then click NetEvent.</span></span>

![Problembehandlung bei drahtlosen LAN-Verbindungen mithilfe des Netzwerk Monitors (3)](images/3wlan.png)

<span data-ttu-id="51980-119">Wenn Sie die Elemente unter einer Aktivitäts-ID im linken Bereich erweitern, können Sie alle anderen relevanten Anbieter für den Verbindungsversuch anzeigen.</span><span class="sxs-lookup"><span data-stu-id="51980-119">Expanding the items under an activity ID in the left pane will allow you to view all of the other relevant providers for the connection attempt.</span></span> <span data-ttu-id="51980-120">Um die Ereignisse von anderen Anbietern anzuzeigen, werden alle Filter entfernt, indem Sie im **Anzeige Filter** Bereich auf **Entfernen** klicken.</span><span class="sxs-lookup"><span data-stu-id="51980-120">To view the events from other providers, all filters are removed by clicking **Remove** in the **Display Filter** pane.</span></span> <span data-ttu-id="51980-121">Die Ablauf Verfolgungen können analysiert werden, indem Sie durch die Frame Zusammenfassung scrollen und nach Bedarf weitere Ereignisse auswählen, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="51980-121">The traces can be analyzed by scrolling through the frame summary, selecting additional events as needed to gather more information.</span></span> <span data-ttu-id="51980-122">In diesem Fall enthält der Bereich "Frame Details" Informationen, dass der Fehler aufgrund eines Schlüsselaustausch Fehlers verursacht wird. Dies liegt wahrscheinlich daran, dass der Benutzer die falsche Pass-Taste eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="51980-122">In this case, the Frame Details pane provides information that the failure is due to key exchange failure, most likely due to the user entering the wrong pass key.</span></span>

 

 




