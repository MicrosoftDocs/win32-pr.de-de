---
title: Szenario 3-Leistungsindikatoren
description: Leistungsindikatoren messen die Menge an Informationen oder Daten entsprechend der Anzahl, Größe, Dauer und Geschwindigkeit der angeforderten oder empfangenen Daten.
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de90607cbda0542ee385b83f44bec878927d509f
ms.sourcegitcommit: fc3f2a28a55e590ac38846048f10b64ba527a98d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "106338508"
---
# <a name="scenario-3-performance-counters"></a><span data-ttu-id="6e37d-103">Szenario 3: Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="6e37d-103">Scenario 3: Performance Counters</span></span>

<span data-ttu-id="6e37d-104">Leistungsindikatoren messen die Menge an Informationen oder Daten entsprechend der Anzahl, Größe, Dauer und Geschwindigkeit der angeforderten oder empfangenen Daten.</span><span class="sxs-lookup"><span data-stu-id="6e37d-104">Performance counters measure quantities of information or data, according to the number, size, duration, and rate of data being requested or received.</span></span> <span data-ttu-id="6e37d-105">Es ist nicht zu erwarten, dass Sie eine Liste der Details eines Zählers erhalten, z. b. eine Liste der Fehlermeldungen.</span><span class="sxs-lookup"><span data-stu-id="6e37d-105">You should not expect to get a list of details from a counter, such as a list of error messages.</span></span> <span data-ttu-id="6e37d-106">Verwenden Sie stattdessen Leistungsindikatoren, um Mengen zu erhalten, z. b. die Anzahl der Fehlermeldungen seit dem Start oder die Rate, mit der Fehlermeldungen generiert werden.</span><span class="sxs-lookup"><span data-stu-id="6e37d-106">Instead, use performance counters to get quantities, such as the number of error message since startup or the rate at which error messages are being generated.</span></span>

## <a name="performance-counters-for-httpsys"></a><span data-ttu-id="6e37d-107">Leistungsindikatoren für HTTP.sys</span><span class="sxs-lookup"><span data-stu-id="6e37d-107">Performance Counters for HTTP.sys</span></span>

<span data-ttu-id="6e37d-108">Ab Windows Vista und Windows Server 2008 bietet HTTP.sys die folgenden Leistungsindikatoren, um Sie bei der Überwachung, Diagnose und Kapazitätsplanung für Webserver zu unterstützen: die HTTP-Server-API-Komponente verfügt über die folgenden Leistungsindikatoren, um Sie bei der Überwachung, Diagnose und Kapazitätsplanung für Webserver zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="6e37d-108">Starting with Windows Vista and Windows Server 2008, HTTP.sys has the following performance metric counters to help you with monitoring, diagnosing, and capacity planning for Web servers: The HTTP Server API component has the following performance counters to help you with monitoring, diagnosing, and capacity planning for Web servers:</span></span>

- <span data-ttu-id="6e37d-109">HTTP-Dienst Zähler:</span><span class="sxs-lookup"><span data-stu-id="6e37d-109">HTTP Service Counters:</span></span>
  - <span data-ttu-id="6e37d-110">Anzahl der URIs im Cache, die seit dem Start hinzugefügt, seit dem Start gelöscht wurden, sowie die Anzahl der Cache Leerungen</span><span class="sxs-lookup"><span data-stu-id="6e37d-110">Number of URIs in the cache, added since startup, deleted since startup, and number of cache flushes</span></span>
  - <span data-ttu-id="6e37d-111">Cache Treffer/Sekunde und Cache Fehler/Sekunde</span><span class="sxs-lookup"><span data-stu-id="6e37d-111">Cache hits/second and Cache misses/second</span></span>
- <span data-ttu-id="6e37d-112">HTTP-Dienst-URL-Gruppen:</span><span class="sxs-lookup"><span data-stu-id="6e37d-112">HTTP Service URL Groups:</span></span>
  - <span data-ttu-id="6e37d-113">Datensenderate, Daten Empfangs Rate, übertragene Bytes (gesendet und empfangen)</span><span class="sxs-lookup"><span data-stu-id="6e37d-113">Data send rate, data receive rate, bytes transferred (sent and received)</span></span>
  - <span data-ttu-id="6e37d-114">Maximale Anzahl von Verbindungen, Rate der Verbindungsversuche, Rate für Get-und Head-Anforderungen und Gesamtzahl der Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e37d-114">Maximum number of connections, connection attempts rate, rate for GET and HEAD requests, and total number of requests</span></span>
- <span data-ttu-id="6e37d-115">HTTP-Dienst Anforderungs Warteschlangen:</span><span class="sxs-lookup"><span data-stu-id="6e37d-115">HTTP Service Request Queues:</span></span>
  - <span data-ttu-id="6e37d-116">Anzahl der Anforderungen in der Warteschlange, Alter der ältesten Anforderungen in der Warteschlange (Alter der letzten Anforderung in der Warteschlange)</span><span class="sxs-lookup"><span data-stu-id="6e37d-116">Number of requests in queue, age of oldest requests in queue (age of the last request in the queue)</span></span>
  - <span data-ttu-id="6e37d-117">Rate der in die Warteschlange eingereiften Anforderungen, Rate der Ablehnung, Gesamtzahl der abgelehnten Anforderungen, Rate der Cache Treffer</span><span class="sxs-lookup"><span data-stu-id="6e37d-117">Rate of request arrivals into the queue, rate of rejection, total number of rejected requests, rate of cache hits</span></span>

<span data-ttu-id="6e37d-118">**Zugreifen auf Leistungsindikatoren**</span><span class="sxs-lookup"><span data-stu-id="6e37d-118">**Accessing Performance Counters**</span></span>

1.  <span data-ttu-id="6e37d-119">Geben Sie **Perfmon** an der Eingabeaufforderung ein, um die Leistungs Diagnose Konsole zu starten.</span><span class="sxs-lookup"><span data-stu-id="6e37d-119">Type **perfmon** at the command prompt to start the Performance Diagnostic Console.</span></span>
2.  <span data-ttu-id="6e37d-120">Wählen Sie im Struktur Steuerelement System **Monitor** aus, und öffnen Sie dann die **Zähler hinzufügen** , indem Sie **+** auf klicken</span><span class="sxs-lookup"><span data-stu-id="6e37d-120">Select **Performance Monitor** in the tree control and then open the **Add Counters** by clicking **+**.</span></span>
3.  <span data-ttu-id="6e37d-121">Wählen Sie unter **Zähler hinzufügen** aus den drei Leistungsindikator Sätzen aus: **http-Dienst**, **http-Dienst Anforderungs Warteschlangen** oder **http-Dienst-URL-Gruppen**.</span><span class="sxs-lookup"><span data-stu-id="6e37d-121">From **Add Counters** select from the three Performance Counters sets: **HTTP Service**, **HTTP Service Request Queues** , or **HTTP Service Url Groups**.</span></span>
4.  <span data-ttu-id="6e37d-122">Wählen Sie zum Anzeigen von Indikatoren aus den Indikatorensätzen **http-Dienst Anforderungs Warteschlangen** und **http-Dienst-URL-Gruppen** die Option **Instanz (e)** aus, **und klicken Sie** dann auf **Hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="6e37d-122">To view counters from the **HTTP Service Request Queues** and **HTTP Service Url Groups** counter sets, select **instance(s)** and click **Add**, and then click **OK**.</span></span> <span data-ttu-id="6e37d-123">Um die HTTP-Dienst Zähler anzuzeigen, wählen Sie den Indikatorensatz im linken Bereich aus, und klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="6e37d-123">To view the HTTP Service counters, select the counter set in the left pane and click **Add**.</span></span>

> [!Note]  
> <span data-ttu-id="6e37d-124">Pro Computer ist nur eine Instanz der HTTP-Server-API-Indikatoren vorhanden, da diese Leistungsindikatoren den Komponenten weiten Status darstellen.</span><span class="sxs-lookup"><span data-stu-id="6e37d-124">Only one instance of the HTTP Server API counters exists per machine, as these counters represent the component-wide state.</span></span> <span data-ttu-id="6e37d-125">Mit Instanzen von URL-Gruppen-Leistungsindikatoren entspricht die Instanz-ID (für den Leistungsindikator) der URL-Gruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="6e37d-125">With instances of Url Group performance counters, the instance ID (for the performance counter) will match the Url Group ID.</span></span> <span data-ttu-id="6e37d-126">Die URL-Gruppen-ID kann angezeigt werden, indem Sie **netsh http Show SERVICESTATE ausgeführt wird** ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e37d-126">The Url Group ID can be viewed by running **netsh http show servicestate**.</span></span> <span data-ttu-id="6e37d-127">Mit Instanzen von Leistungsindikatoren der Anforderungs Warteschlange entspricht der Instanzname dem Namen der Anforderungs Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="6e37d-127">With instances of Request Queues performance counters, the instance name corresponds to Request Queue Name.</span></span> <span data-ttu-id="6e37d-128">Der Name der Anforderungs Warteschlange (sofern vorhanden) kann vom gleichen **netsh http Show SERVICESTATE ausgeführt wird** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6e37d-128">The Request Queue Name (if one exists) can be shown by the same **netsh http show servicestate**.</span></span> <span data-ttu-id="6e37d-129">Einige Server Anwendungen haben jedoch möglicherweise unbenannte Anforderungs Warteschlangen, die nicht mit einer Instanz-ID des Leistungs Zählers übereinstimmen können.</span><span class="sxs-lookup"><span data-stu-id="6e37d-129">However, some server applications may have unnamed Request Queues that cannot be matched to a performance counter instance ID.</span></span>

 

 

 




