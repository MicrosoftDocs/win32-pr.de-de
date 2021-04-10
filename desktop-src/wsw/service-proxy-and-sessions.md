---
title: Dienst Proxy und-Sitzungen
description: Der Dienst Proxy weist ein spezielles Verhalten für Sitzungs basierte und nicht Sitzungs basierte Kanal Bindungen auf.
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Dienst Proxy-und Sitzungs-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8477a8cd03579e1d8cbfe4509f89890af8482
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039861"
---
# <a name="service-proxy-and-sessions"></a><span data-ttu-id="ab272-106">Dienst Proxy und-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="ab272-106">Service Proxy and Sessions</span></span>

<span data-ttu-id="ab272-107">Der [Dienst Proxy](service-proxy.md) weist ein spezielles Verhalten für Sitzungs basierte und nicht Sitzungs basierte Kanal Bindungen auf.</span><span class="sxs-lookup"><span data-stu-id="ab272-107">The [service proxy](service-proxy.md) has special behaviors for session and non-session-based channel bindings.</span></span> <span data-ttu-id="ab272-108">Der Dienst Proxy stellt eine Sitzungs basierte Semantik bereit, wenn die zugrunde liegende kanalbindung Sitzungs basiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab272-108">The service proxy provides session based semantics if the underlying channel binding is session based.</span></span> <span data-ttu-id="ab272-109">In diesem Fall wird ein einzelner Kanal für die Dienst Aufrufe verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab272-109">In this case a single channel is used to service calls.</span></span> <span data-ttu-id="ab272-110">Wenn die kanalbindung jedoch nicht Sitzungs basiert ist, erstellt der Dienst Proxy einen separaten Kanal für jeden-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="ab272-110">However, if the channel binding is not session based, the service proxy creates a separate channel for each call.</span></span> <span data-ttu-id="ab272-111">Beachten Sie jedoch, dass nicht Sitzungs basierte Kanäle in einem Pool zusammengefasst und möglicherweise wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab272-111">Note, though, that non-session-based channels are pooled and maybe reused.</span></span> <span data-ttu-id="ab272-112">Bei der Wiederverwendung eines Kanals hält der Dienst Proxy den Kanal geöffnet, wenn der zugrunde liegende Kanal nicht einen Fehler verursacht hat oder der-Vorgang für einen Kanal dazu geführt hat, dass der Kanal des Dienst Proxys fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="ab272-112">In reusing a channel, the service proxy keeps the channel open if the underlying channel has not faulted or the call on a channel has resulted in the service proxy's faulting the channel.</span></span> <span data-ttu-id="ab272-113">Beachten Sie, dass.</span><span class="sxs-lookup"><span data-stu-id="ab272-113">Note that.</span></span> <span data-ttu-id="ab272-114">Wenn ein Kanal geöffnet ist, wird er im Falle eines Fehlers geöffnet, solange der Dienst Proxy geöffnet ist und nur geschlossen wird, wenn der Dienst Proxy geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="ab272-114">except in the event of a fault, once a channel is opened it is kept open as long as the service proxy is open and is closed only when the service proxy is closed.</span></span>


<span data-ttu-id="ab272-115">Wenn die kanalbindung Sitzungs basiert ist und der zugrunde liegende Kanal fehlerhaft ist, wechselt der Dienst Proxy-Zustands Automat in den Status des [**WS- \_ Dienst Proxy \_ \_ Zustands \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .</span><span class="sxs-lookup"><span data-stu-id="ab272-115">If the channel binding is session based and if the underlying channel faults, the service proxy state machine will transition into the [**WS\_SERVICE\_PROXY\_STATE\_FAULTED**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) state.</span></span> <span data-ttu-id="ab272-116">Im Fall einer nicht Sitzungs basierten channelbindung bewirkt ein Fehler im zugrunde liegenden Kanal nicht, dass der Proxy in den Status des **WS- \_ Dienst \_ Proxy \_ Zustands \_** übergeht.</span><span class="sxs-lookup"><span data-stu-id="ab272-116">In the case of non-session based channel binding, a fault in the underlying channel does not cause the proxy to transition into **WS\_SERVICE\_PROXY\_STATE\_FAULTED** state.</span></span>

<span data-ttu-id="ab272-117">Weitere Informationen zum Dienst Proxy und dessen Beziehung zum Status finden Sie im Thema zu [Dienst Proxys](service-proxy.md) .</span><span class="sxs-lookup"><span data-stu-id="ab272-117">For more information on the service proxy and its relation to state, see the [Service Proxy](service-proxy.md) topic.</span></span> <span data-ttu-id="ab272-118">Beispiele für verschiedene Kanal Bindungen finden Sie in den folgenden Beispielen:</span><span class="sxs-lookup"><span data-stu-id="ab272-118">For examples of different channel bindings see the following examples:</span></span>

-   <span data-ttu-id="ab272-119">nicht-Sitzungs kanalbindung, [httpcalculatorclieintexample](httpcalculatorclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="ab272-119">non-session channel binding, [HttpCalculatorClientExample](httpcalculatorclientexample.md)</span></span>
-   <span data-ttu-id="ab272-120">Sitzungs basierte kanalbindung, [sessionfullcalculatorclieintexample](sessionfullcalculatorclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="ab272-120">session-based channel binding, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)</span></span>

 

 




