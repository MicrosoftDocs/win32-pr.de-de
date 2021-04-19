---
description: Mithilfe des System Ereignis Benachrichtigungs Diensts können Anwendungen, die von der System Ereignis Benachrichtigung überwachen, Benachrichtigungen von System Ereignissen empfangen. Wenn das angeforderte Ereignis auftritt, benachrichtigt Sens die Anwendung.
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: Benachrichtigungen (System Ereignis Benachrichtigungsdienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272f0ea60369015328e34d3a83231ab0b254253a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359464"
---
# <a name="notifications-system-event-notification-service"></a><span data-ttu-id="f1004-104">Benachrichtigungen (System Ereignis Benachrichtigungsdienst)</span><span class="sxs-lookup"><span data-stu-id="f1004-104">Notifications (System Event Notification Service)</span></span>

<span data-ttu-id="f1004-105">Mithilfe des System Ereignis Benachrichtigungs Diensts können Anwendungen, die von der System Ereignis Benachrichtigung überwachen, Benachrichtigungen von System Ereignissen empfangen.</span><span class="sxs-lookup"><span data-stu-id="f1004-105">The System Event Notification Service enables mobile-aware applications to receive notifications from system events that SENS monitors.</span></span> <span data-ttu-id="f1004-106">Wenn das angeforderte Ereignis auftritt, benachrichtigt Sens die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f1004-106">When the requested event occurs, SENS notifies the application.</span></span>

<span data-ttu-id="f1004-107">Sens kann Anwendungen über drei Klassen von System Ereignissen Benachrichtigen:</span><span class="sxs-lookup"><span data-stu-id="f1004-107">SENS can notify applications about three classes of system events:</span></span>

-   <span data-ttu-id="f1004-108">TCP/IP-Netzwerkereignisse, z. b. der Status einer TCP/IP-Netzwerkverbindung oder die Qualität der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="f1004-108">TCP/IP network events, such as the status of a TCP/IP network connection or the quality of the connection.</span></span>
-   <span data-ttu-id="f1004-109">Benutzer Anmelde Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="f1004-109">User logon events.</span></span>
-   <span data-ttu-id="f1004-110">Akku-und Strom Leistungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="f1004-110">Battery and AC power events.</span></span>

<span data-ttu-id="f1004-111">Beispielsweise kann eine Anwendung eines der folgenden Systemereignisse abonnieren:</span><span class="sxs-lookup"><span data-stu-id="f1004-111">For example, an application can subscribe to any of the following system events:</span></span>

-   <span data-ttu-id="f1004-112">Einrichtung der Netzwerk Konnektivität</span><span class="sxs-lookup"><span data-stu-id="f1004-112">Establishment of network connectivity</span></span>
-   <span data-ttu-id="f1004-113">Benachrichtigung, wenn ein angegebenes Ziel innerhalb der angegebenen qoc (Quality of Connection)-Parameter erreicht werden kann</span><span class="sxs-lookup"><span data-stu-id="f1004-113">Notification when a specified destination can be reached within specified Quality of Connection (QOC) parameters</span></span>
-   <span data-ttu-id="f1004-114">Der Computer wurde in den Akku Betrieb gewechselt.</span><span class="sxs-lookup"><span data-stu-id="f1004-114">The computer has switched to battery power</span></span>
-   <span data-ttu-id="f1004-115">Der Prozentsatz der verbleibenden Akkuleistung liegt innerhalb eines angegebenen Parameters.</span><span class="sxs-lookup"><span data-stu-id="f1004-115">The percentage of remaining battery power is within a specified parameter</span></span>
-   <span data-ttu-id="f1004-116">Geplante Ereignisse mithilfe des Synchronisierungs-Managers</span><span class="sxs-lookup"><span data-stu-id="f1004-116">Scheduled events using Synchronization Manager occur</span></span>

<span data-ttu-id="f1004-117">**Windows Server 2008 R2 und Windows 7:** Der Abonnent hat maximal 3 Minuten Zeit, um auf eine Benachrichtigung über die [**isenslogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) -und [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) -Schnittstellen zu antworten.</span><span class="sxs-lookup"><span data-stu-id="f1004-117">**Windows Server 2008 R2 and Windows 7:** The subscriber has a maximum of 3 minutes to respond to a notification on the [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) and [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) interfaces.</span></span> <span data-ttu-id="f1004-118">Nach drei Minuten bricht er den Rückruf von Abonnenten ab und hebt die Blockierung des Benachrichtigungs Threads auf.</span><span class="sxs-lookup"><span data-stu-id="f1004-118">After 3 minutes, SENS cancels the call to subscribers and unblocks the notification thread.</span></span> <span data-ttu-id="f1004-119">Wenn ein längerer Vorgang erforderlich ist, um auf die Benachrichtigung zu antworten, kehren Sie von **isenslogon** oder **ISensLogon2** so schnell wie möglich zurück, und öffnen Sie einen anderen Thread für die Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="f1004-119">If a lengthy operation is required to respond to the notification, return from **ISensLogon** or **ISensLogon2** as quickly as possible and open another thread for processing.</span></span>

 

 



