---
description: Ereignis Abfragen werden von temporären Ereignisverbrauchern, permanenten Ereignisconsumern und Ereignis Anbietern verwendet. Ereignisconsumer verwenden Ereignis Abfragen, um relevante Ereignisse anzugeben, und Ereignis Anbieter verwenden die Abfragen, um die von Ihnen bereitgestellten Ereignisse anzugeben.
ms.assetid: 851ad9bd-2604-4988-8de0-8d29b5300b21
ms.tgt_platform: multiple
title: Empfangen von Ereignis Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43873c03155f2186f9d3a9a3daff9b8e322e511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347070"
---
# <a name="receiving-event-notifications"></a><span data-ttu-id="a386d-104">Empfangen von Ereignis Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="a386d-104">Receiving Event Notifications</span></span>

<span data-ttu-id="a386d-105">Ereignis Abfragen werden von temporären Ereignisverbrauchern, permanenten Ereignisconsumern und Ereignis Anbietern verwendet.</span><span class="sxs-lookup"><span data-stu-id="a386d-105">Event queries are used by temporary event consumers, permanent event consumers, and event providers.</span></span> <span data-ttu-id="a386d-106">Ereignisconsumer verwenden Ereignis Abfragen, um relevante Ereignisse anzugeben, und Ereignis Anbieter verwenden die Abfragen, um die von Ihnen bereitgestellten Ereignisse anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a386d-106">Event consumers use event queries to specify events of interest, and event providers use the queries to specify the events that they provide.</span></span>

<span data-ttu-id="a386d-107">[Temporäre](receiving-events-for-the-duration-of-your-application.md) Consumer platzieren Abfragen in Aufrufen der Methode [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) oder [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="a386d-107">[Temporary consumers](receiving-events-for-the-duration-of-your-application.md) place queries in calls to the [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) or [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method.</span></span> <span data-ttu-id="a386d-108">[Permanente](receiving-events-at-all-times.md) [**\_ \_ Ereignisconsumer**](--eventfilter.md) platzieren Abfragen in der **Query** -Eigenschaft einer Instanz der EventFilter-System Klasse.</span><span class="sxs-lookup"><span data-stu-id="a386d-108">[Permanent event consumers](receiving-events-at-all-times.md) place queries in the **Query** property of an instance of the [**\_\_EventFilter**](--eventfilter.md) system class.</span></span>

<span data-ttu-id="a386d-109">[Ereignis Anbieter](writing-an-event-provider.md) verwenden Ereignis Abfragen, um sich zu registrieren, um einen oder mehrere Ereignis Typen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a386d-109">[Event providers](writing-an-event-provider.md) use event queries to register to support one or more types of events.</span></span> <span data-ttu-id="a386d-110">Sie platzieren Abfragen in der **EventQueryList** -Eigenschaft einer Instanz der [**\_ \_ eventproviderregistration**](--eventproviderregistration.md) -System Klasse.</span><span class="sxs-lookup"><span data-stu-id="a386d-110">They place queries in the **EventQueryList** property of an instance of the [**\_\_EventProviderRegistration**](--eventproviderregistration.md) system class.</span></span> <span data-ttu-id="a386d-111">Alle Ereignis Anbieter erstellen eine **\_ \_ eventproviderregistration** -Instanz, um sich bei Windows-Verwaltungsinstrumentation (WMI) zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="a386d-111">All event providers create an **\_\_EventProviderRegistration** instance to register with Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="a386d-112">Weitere Informationen finden Sie unter [Registrieren eines Ereignis Anbieters](registering-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a386d-112">For more information, see [Registering an Event Provider](registering-an-event-provider.md).</span></span>

<span data-ttu-id="a386d-113">Ereignisconsumer und-Anbieter verwenden die [SELECT-Anweisung](select-statement-for-event-queries.md) und eine verwandte WHERE-Klausel für Ereignis Abfragen sowie eine Vielzahl von Erweiterungen, die für die WMI Query Language (WQL) spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="a386d-113">Event consumers and providers use the [SELECT statement](select-statement-for-event-queries.md) and a related WHERE clause for event queries, plus a variety of extensions specific to the WMI Query Language (WQL).</span></span> <span data-ttu-id="a386d-114">Die Erweiterungen werden verwendet, um zu verhindern, dass Consumer mit Benachrichtigungen überflutet werden, die zu häufig vorkommen, damit Sie hilfreich sind.</span><span class="sxs-lookup"><span data-stu-id="a386d-114">The extensions are used to protect consumers from being flooded with notifications that occur too frequently to be useful.</span></span>

<span data-ttu-id="a386d-115">Consumer, die bei Auftreten eines Ereignisses keine Benachrichtigung benötigen, können in Ihren Abfragen die folgenden Klauseln angeben:</span><span class="sxs-lookup"><span data-stu-id="a386d-115">Consumers that do not require notification each time an event occurs can specify the following clauses in their queries:</span></span>

-   <span data-ttu-id="a386d-116">[Within](within-clause.md) -Klausel</span><span class="sxs-lookup"><span data-stu-id="a386d-116">[WITHIN](within-clause.md) clause</span></span>
-   <span data-ttu-id="a386d-117">[Group](group-clause.md) -Klausel</span><span class="sxs-lookup"><span data-stu-id="a386d-117">[GROUP](group-clause.md) clause</span></span>
-   <span data-ttu-id="a386d-118">[Hat](having-clause.md) -Klausel</span><span class="sxs-lookup"><span data-stu-id="a386d-118">[HAVING](having-clause.md) clause</span></span>

<span data-ttu-id="a386d-119">Die in-und-Klauseln beeinflussen die zeitliche Steuerung von Ereignissen, und die Group-Klausel bewirkt, dass ein repräsentatives Ereignis anstelle eines häufig auftretenden Ereignisses gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a386d-119">The WITHIN and HAVING clauses affect the timing of events, and the GROUP clause causes a representative event to be sent in place of a frequently occurring event.</span></span>

 

 



