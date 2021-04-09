---
title: Änderungs Benachrichtigungen
description: Die Änderungs Benachrichtigungen für die Basis Filter-Engine (BFE) folgen dem Veröffentlichen/Abonnieren-Muster.
ms.assetid: 443f1767-5694-4584-ba0f-229275900774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7a3a2069525cc44823ed975fade3b5f100efd8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103948453"
---
# <a name="change-notifications"></a><span data-ttu-id="2441f-103">Änderungs Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="2441f-103">Change Notifications</span></span>

<span data-ttu-id="2441f-104">Die Änderungs Benachrichtigungen für die Basis Filter-Engine (BFE) folgen dem Veröffentlichen/Abonnieren-Muster: um eine der veröffentlichten Änderungs Benachrichtigungen zu empfangen, muss Sie von einer Anwendung abonniert werden.</span><span class="sxs-lookup"><span data-stu-id="2441f-104">The Base Filtering Engine (BFE) change notifications follow the publish/subscribe pattern: in order to receive one of the published change notifications, an application has to subscribe to it.</span></span>

<span data-ttu-id="2441f-105">Die veröffentlichten BFE-Änderungs Benachrichtigungen sind "Add" und "Remove [**" für Legenden**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**Filter**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**Anbieter**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**Anbieter Kontexte**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)und [**untergeordnete Ebenen**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).</span><span class="sxs-lookup"><span data-stu-id="2441f-105">The published BFE change notifications are Add and Remove for [**callouts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**filters**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**providers**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**provider contexts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0), and [**sub-layers**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).</span></span>

<span data-ttu-id="2441f-106">Um eine der obigen Benachrichtigungen zu abonnieren, ruft eine Anwendung die entsprechende [**fwpm- \* SubscribeChanges0**](fwp-mgmt-functions.md) Verwaltungsfunktion auf (z. b. [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)).</span><span class="sxs-lookup"><span data-stu-id="2441f-106">To subscribe to one of the above notifications, an application calls the corresponding [**Fwpm\*SubscribeChanges0**](fwp-mgmt-functions.md) management function (for example, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)).</span></span> <span data-ttu-id="2441f-107">Die Rückruffunktion, die als Argument an **fwpm \* SubscribeChanges0** übermittelt wird, wird von BFE aufgerufen, wenn die Änderung, die Sie abonniert hat, erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2441f-107">The callback function passed as an argument to **Fwpm\*SubscribeChanges0** is invoked by BFE when the change to which it subscribed occurs.</span></span>

<span data-ttu-id="2441f-108">Um eine der obigen Benachrichtigungen abzubestellen, ruft eine Anwendung die entsprechende **fwpm- \* UnsubscribeChanges0** Verwaltungsfunktion auf (z. b. [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).</span><span class="sxs-lookup"><span data-stu-id="2441f-108">To unsubscribe to one of the above notifications, an application calls the corresponding **Fwpm\*UnsubscribeChanges0** management function (for example, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).</span></span>

<span data-ttu-id="2441f-109">Um die aktuellen Abonnements für eine der obigen Benachrichtigungen anzuzeigen, ruft eine Anwendung die entsprechende [**fwpm- \* SubscriptionsGet0**](fwp-mgmt-functions.md) Verwaltungsfunktion auf (z. b. [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).</span><span class="sxs-lookup"><span data-stu-id="2441f-109">To see the current subscriptions for one of the above notifications, an application calls the corresponding [**Fwpm\*SubscriptionsGet0**](fwp-mgmt-functions.md) management function (for example [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).</span></span>

<span data-ttu-id="2441f-110">Die von den BFE angebotenen Änderungs Benachrichtigungen lauten:</span><span class="sxs-lookup"><span data-stu-id="2441f-110">The change notifications offered by the BFE are:</span></span>

-   <span data-ttu-id="2441f-111">Asynchronous – der Funktions Aufrufwert, der eine Benachrichtigung ausgelöst hat, kann zurückgeben, bevor die Benachrichtigung an alle Abonnenten gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2441f-111">Asynchronous — The function call that triggered a notification may return before the notification has been dispatched to all subscribers.</span></span>
-   <span data-ttu-id="2441f-112">Unzuverlässig – es wird keine Garantie gegeben, dass Benachrichtigungen erfolgreich zugestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2441f-112">Unreliable — No guarantee is made that notifications will be successfully delivered.</span></span>

<span data-ttu-id="2441f-113">Abonnenten erhalten keine Benachrichtigungen zu Änderungen, die mit dem Sitzungs handle vorgenommen wurden, das Sie zum Abonnieren verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="2441f-113">Subscribers do not receive notifications for changes made with the session handle they used to subscribe.</span></span> <span data-ttu-id="2441f-114">Im Allgemeinen müssen Abonnenten nur über die von anderen vorgenommenen Änderungen informiert werden. Sie wissen bereits, welche Änderungen von sich selbst vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="2441f-114">Generally, subscribers only need to be informed of the changes made by others; they already know which changes were made by themselves.</span></span>

 

 




