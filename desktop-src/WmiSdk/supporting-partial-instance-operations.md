---
description: Ein Anbieter muss keine partiellen instanzvorgänge unterstützen. Ein Anbieter muss jedoch entweder die gesamte Semantik eines partiellen instanzvorgangs unterstützen, eine vollständige Instanz verarbeiten oder den \_ nicht unterstützten WBEM E-Parameter zurückgeben \_ \_ .
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: Unterstützung Partial-Instance Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf656688ffbcc6981c6a3e55dc480570ad0f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347317"
---
# <a name="supporting-partial-instance-operations"></a><span data-ttu-id="0583e-104">Unterstützung Partial-Instance Vorgänge</span><span class="sxs-lookup"><span data-stu-id="0583e-104">Supporting Partial-Instance Operations</span></span>

<span data-ttu-id="0583e-105">Ein Anbieter muss keine partiellen instanzvorgänge unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0583e-105">A provider is not required to support any partial-instance operations.</span></span> <span data-ttu-id="0583e-106">Ein Anbieter muss jedoch entweder die gesamte Semantik eines partiellen instanzvorgangs unterstützen, eine vollständige Instanz verarbeiten oder den **\_ \_ nicht unterstützten \_ WBEM E-Parameter** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0583e-106">However, a provider must either support all the semantics of a partial-instance operation, process a complete instance, or return **WBEM\_E\_UNSUPPORTED\_PARAMETER**.</span></span>

<span data-ttu-id="0583e-107">Beim Erstellen eines Anbieters, der partielle instanzvorgänge unterstützt, müssen Sie die folgenden Regeln beachten:</span><span class="sxs-lookup"><span data-stu-id="0583e-107">When creating a provider that supports partial-instance operations, you must observe the following rules:</span></span>

-   <span data-ttu-id="0583e-108">Wieder verwenden des gleichen Kontext Objekts, das von WMI an den Anbieter gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0583e-108">Reuse the same context object that WMI sends to the provider.</span></span> <span data-ttu-id="0583e-109">WMI verwendet den \_ \_ \_ benannten Wert "Get Ext \_ Client \_ Request", um Deadlocks zu verhindern und den Client zu entfernen, bevor das Kontext Objekt an einen Anbieter weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="0583e-109">WMI uses the "\_\_GET\_EXT\_CLIENT\_REQUEST" named value to prevent deadlocks and removes this client before forwarding the context object to a provider.</span></span>
-   <span data-ttu-id="0583e-110">Für Wiedereintritts fähige Aufrufe an WMI, die keinen partiellen Instanzvorgang erfordern, müssen Sie sicherstellen, dass das gleiche Kontext Objekt ohne Änderungen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0583e-110">For reentrant calls back into WMI that do not require a partial-instance operation, ensure to pass back the same context object without any modifications.</span></span> <span data-ttu-id="0583e-111">WMI empfängt das Kontext Objekt ohne den \_ \_ \_ benannten Wert "Get Ext \_ Client \_ Request" und löscht alle benannten Werte, die partiellen instanzvorgängen zugeordnet sind, aus dem Kontext Objekt, bevor es an andere Anbieter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0583e-111">WMI receives the context object without the "\_\_GET\_EXT\_CLIENT\_REQUEST" named value set and deletes all named values associated with partial-instance operations from the context object before passing it to other providers.</span></span> <span data-ttu-id="0583e-112">Wenn Sie das Kontext Objekt nicht ändern, werden von anderen Anbietern keine partiellen Instanzen Abruf Vorgänge empfangen, die für ein anderes, nicht verwandtes Objekt vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="0583e-112">Not changing the context object blocks other providers from receiving partial-instance retrieval operations intended for a different, unrelated object.</span></span>
-   <span data-ttu-id="0583e-113">Zum Ausführen eines wieder eintretende partiellen instanzvorgangs bei der Ausführung einer Anforderung legen Sie den fehlenden " \_ \_ get \_ Ext \_ Client \_ Request"-Wert und die Eigenschaft "Clear" fest.</span><span class="sxs-lookup"><span data-stu-id="0583e-113">To perform a reentrant partial-instance operation while carrying out a request, set the missing "\_\_GET\_EXT\_CLIENT\_REQUEST" named value and property clear.</span></span> <span data-ttu-id="0583e-114">Optional können Sie die Eigenschaften im \_ \_ \_ benannten Wert "Get Ext \_ Properties" ändern, bevor Sie das Kontext Objekt mit dem Wiedereintritts fähige-Befehl zurück an WMI senden.</span><span class="sxs-lookup"><span data-stu-id="0583e-114">Optionally, you can modify the properties in the "\_\_GET\_EXT\_PROPERTIES" named value before sending the context object back into WMI with the reentrant call.</span></span>
-   <span data-ttu-id="0583e-115">Greifen Sie nicht auf das Kontext Objekt zu, nachdem Sie es während eines Wiedereinstiegs Aufrufes an WMI zurückgegeben haben. andere Anbieter können die Eigenschaften Listen oder andere Werte während des erneuten Eintritts ändern.</span><span class="sxs-lookup"><span data-stu-id="0583e-115">Do not access the context object after you return it to WMI during a reentrant call; other providers may modify the property lists or other values during reentrancy.</span></span> <span data-ttu-id="0583e-116">Sie können das Kontext Objekt nur für die Dauer des von Ihnen implementierten [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Aufrufes überprüfen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="0583e-116">You can examine or modify the context object only for the duration of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) call that you implement.</span></span>

 

 



