---
title: Data-Pull Modell und Data-Push Modell
description: Data-Pull Modell und Data-Push Modell
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f6607e9b466c439859a99b857e7ce3fe6d8acd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391092"
---
# <a name="data-pull-model-and-data-push-model"></a><span data-ttu-id="66d5e-103">Data-Pull Modell und Data-Push Modell</span><span class="sxs-lookup"><span data-stu-id="66d5e-103">Data-Pull Model and Data-Push Model</span></span>

<span data-ttu-id="66d5e-104">Ein Client mit einem asynchronen Moniker kann zwischen einem datenpull-und einem datenpushmodell wählen, um einen asynchronen [**IMoniker:: bindesstorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) -Vorgang zu tätigen und asynchrone Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="66d5e-104">A client of an asynchronous moniker can choose between a data-pull and data-push model for driving an asynchronous [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) operation and receiving asynchronous notifications.</span></span> <span data-ttu-id="66d5e-105">Im Data-Pull-Modell steuert der Client den Bindungs Vorgang, und der Moniker stellt dem Client nur beim Lesen Daten bereit.</span><span class="sxs-lookup"><span data-stu-id="66d5e-105">In the data-pull model, the client drives the bind operation and the moniker provides data to the client only as it is read.</span></span> <span data-ttu-id="66d5e-106">Das heißt, dass der Moniker nach dem ersten Aufruf von [**ibindstatus-Callback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))keine Daten für den Client bereitstellt, es sei denn, der Client hat alle bereits verfügbaren Daten verbraucht.</span><span class="sxs-lookup"><span data-stu-id="66d5e-106">In other words, after the first call to [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), the moniker does not provide any data to the client unless the client has consumed all of the data that is already available.</span></span>

<span data-ttu-id="66d5e-107">Da Daten nur nach Anforderung heruntergeladen werden, müssen die Clients, die das datenpull-Modell auswählen, sicherstellen, dass diese Daten rechtzeitig gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="66d5e-107">Because data is downloaded only as it is requested, clients that choose the data-pull model must make sure to read this data in a timely manner.</span></span> <span data-ttu-id="66d5e-108">Im Fall von Internet Downloads mit [URL-Monikern](url-monikers.md)schlägt der Bindungs Vorgang möglicherweise fehl, wenn ein Client zu lange wartet, bevor mehr Daten angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="66d5e-108">In the case of Internet downloads with [URL monikers](url-monikers.md), the bind operation may fail if a client waits too long before requesting more data.</span></span>

<span data-ttu-id="66d5e-109">Im Daten Push-Modell steuert der Moniker den asynchronen Bindungs Vorgang und benachrichtigt den Client kontinuierlich, wenn neue Daten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="66d5e-109">In the data-push model, the moniker drives the asynchronous bind operation and continuously notifies the client whenever new data is available.</span></span> <span data-ttu-id="66d5e-110">Der Client kann entscheiden, ob die Daten zu einem beliebigen Zeitpunkt während des Bindungs Vorgangs gelesen werden sollen. der Moniker führt den Bindungs Vorgang jedoch unabhängig von der Beendigung durch.</span><span class="sxs-lookup"><span data-stu-id="66d5e-110">The client may choose whether to read the data at any point during the bind operation, but the moniker will drive the bind operation to completion regardless.</span></span>

<span data-ttu-id="66d5e-111">Beachten Sie auch, dass Sie bei der Verwendung asynchroner Moniker daran denken müssen, die com-Regeln für die Speicher Belegung zu befolgen, insbesondere die folgenden:</span><span class="sxs-lookup"><span data-stu-id="66d5e-111">Also, you need to remember to follow the COM rules for memory allocation when using asynchronous monikers, specifically the following:</span></span>

-   <span data-ttu-id="66d5e-112">Wenn eine COM-Schnittstelle oder ein Funktionsaufruf einen Puffer (Zeichenfolge oder einen anderen) an den Client zurückgibt, ist der Client für die Freigabe des Arbeitsspeichers durch Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="66d5e-112">Whenever a COM interface or function call returns a buffer (string or other) to its client, the client is responsible for freeing the memory by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>
-   <span data-ttu-id="66d5e-113">Wenn eine COM-Schnittstelle oder-Funktion einen Puffer von Ihrem Client erfordert, muss der Client diesen Puffer mithilfe von [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) zuordnen, und der aufgerufene muss ihn freigeben.</span><span class="sxs-lookup"><span data-stu-id="66d5e-113">Whenever a COM interface or function requires a buffer from its client, the client must allocate that buffer using [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) and the callee must free it.</span></span>

<span data-ttu-id="66d5e-114">Achten Sie darauf, dass Sie diese Regeln befolgen, wenn Sie Zeichen folgen oder Puffer zuordnen, die an asynchrone Moniker übermittelt werden, und denken Sie daran, den von asynchronen Monikern zurückgegebenen Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="66d5e-114">Be sure to follow these rules when allocating strings or buffers that are passed to asynchronous monikers, and remember to free memory returned by asynchronous monikers.</span></span> <span data-ttu-id="66d5e-115">Ausführliche Informationen finden Sie unter [Verwalten der Speicher Belegung](the-com-library.md) und verwandter Themen.</span><span class="sxs-lookup"><span data-stu-id="66d5e-115">See [Managing Memory Allocation](the-com-library.md) and related topics for complete details.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66d5e-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="66d5e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66d5e-117">Asynchrone Moniker</span><span class="sxs-lookup"><span data-stu-id="66d5e-117">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 