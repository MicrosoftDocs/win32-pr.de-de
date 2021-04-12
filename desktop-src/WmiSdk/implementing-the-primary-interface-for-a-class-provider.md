---
description: 'Es gibt zwei Möglichkeiten zum Implementieren eines Klassen Anbieters: Implementieren Sie die-Schnittstelle als pushanbieter oder als Pull-Anbieter.'
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: Implementieren der primären Schnittstelle für einen Klassen Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f760dba053cadf56d37445c997fc52a99b242a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346728"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a><span data-ttu-id="2182c-103">Implementieren der primären Schnittstelle für einen Klassen Anbieter</span><span class="sxs-lookup"><span data-stu-id="2182c-103">Implementing the Primary Interface for a Class Provider</span></span>

<span data-ttu-id="2182c-104">Es gibt zwei Möglichkeiten zum Implementieren eines Klassen Anbieters: Implementieren Sie die-Schnittstelle als pushanbieter oder als Pull-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="2182c-104">There are two ways to implement a class provider: implement the interface as a push provider, or as a pull provider.</span></span>

<span data-ttu-id="2182c-105">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="2182c-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="2182c-106">Implementieren der primären Schnittstelle für einen Push-Klassen Anbieter</span><span class="sxs-lookup"><span data-stu-id="2182c-106">Implementing the Primary Interface for a Push Class Provider</span></span>](#implementing-the-primary-interface-for-a-push-class-provider)
-   [<span data-ttu-id="2182c-107">Implementieren der primären Schnittstelle für einen Pull-Klassen Anbieter</span><span class="sxs-lookup"><span data-stu-id="2182c-107">Implementing the Primary Interface for a Pull Class Provider</span></span>](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a><span data-ttu-id="2182c-108">Implementieren der primären Schnittstelle für einen Push-Klassen Anbieter</span><span class="sxs-lookup"><span data-stu-id="2182c-108">Implementing the Primary Interface for a Push Class Provider</span></span>

<span data-ttu-id="2182c-109">Während alle Anbieter [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) für die Initialisierung und mindestens eine andere Schnittstelle als primäre Schnittstelle implementieren, implementiert ein Push-Anbieter nur **iwbemproviderinit**.</span><span class="sxs-lookup"><span data-stu-id="2182c-109">Whereas all providers implement [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) for initialization and at least one other interface as their primary interface, a push provider implements only **IWbemProviderInit**.</span></span>

<span data-ttu-id="2182c-110">Stellen Sie sicher, dass Ihre-Implementierung die folgenden Aufgaben ausführt:</span><span class="sxs-lookup"><span data-stu-id="2182c-110">Ensure that your implementation performs the following tasks:</span></span>

-   <span data-ttu-id="2182c-111">Ruft die entsprechenden Klassen Daten ab.</span><span class="sxs-lookup"><span data-stu-id="2182c-111">Retrieves the appropriate class data.</span></span>
-   <span data-ttu-id="2182c-112">Platziert die Daten im WMI-Repository.</span><span class="sxs-lookup"><span data-stu-id="2182c-112">Places the data in the WMI repository.</span></span>
-   <span data-ttu-id="2182c-113">Löscht veraltete Daten.</span><span class="sxs-lookup"><span data-stu-id="2182c-113">Deletes obsolete data.</span></span>

<span data-ttu-id="2182c-114">Nach Abschluss des Initialisierungs Vorgangs verarbeitet WMI alle Anwendungsanforderungen für Klassen, die zum Push-Anbieter gehören, ohne dass weitere Anbieter Interaktionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="2182c-114">After completing the initialization process, WMI handles all application requests for classes belonging to the push provider without any further provider interaction.</span></span> <span data-ttu-id="2182c-115">Danach fungiert der Push-Anbieter effektiv als Client von WMI anstelle eines Anbieters.</span><span class="sxs-lookup"><span data-stu-id="2182c-115">Afterward, the push provider effectively acts as a client of WMI rather than a provider.</span></span> <span data-ttu-id="2182c-116">Weitere Informationen zum Implementieren von [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)finden Sie unter [Initialisieren eines Anbieters](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2182c-116">For more information about implementing [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), see [Initializing a Provider](initializing-a-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="2182c-117">Wenn Sie WMI aufrufen, um Daten in einem Push-Anbieter zu erstellen, zu aktualisieren oder zu entfernen, legen Sie den *lFlags* -Parameter so fest, dass in allen Aufrufen von [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Methoden das kennflag für das **\_ \_ Besitzer \_ Update von WBEM**</span><span class="sxs-lookup"><span data-stu-id="2182c-117">When calling WMI to create, update, or remove data in a push provider, set the *lFlags* parameter to include the **WBEM\_FLAG\_OWNER\_UPDATE** flag in all calls to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods.</span></span>

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a><span data-ttu-id="2182c-118">Implementieren der primären Schnittstelle für einen Pull-Klassen Anbieter</span><span class="sxs-lookup"><span data-stu-id="2182c-118">Implementing the Primary Interface for a Pull Class Provider</span></span>

<span data-ttu-id="2182c-119">Ein Pull-Anbieter für die Klasse sollte [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) als primäre Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="2182c-119">A class pull provider should implement [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface.</span></span> <span data-ttu-id="2182c-120">Die **IWbemServices** -Schnittstelle unterstützt Datenabruf, Datenaktualisierung, Entfernen von Daten, Enumeration und Abfrage Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="2182c-120">The **IWbemServices** interface supports data retrieval, data update, data removal, enumeration, and query processing.</span></span> <span data-ttu-id="2182c-121">Da **IWbemServices** jedoch auch von Anwendungen und Anbietern verwendet wird, um Dienste von WMI anzufordern, enthält **IWbemServices** viele Methoden, die für einen Klassen Anbieter irrelevant sind.</span><span class="sxs-lookup"><span data-stu-id="2182c-121">However, because **IWbemServices** is also used by applications and providers to request services of WMI, **IWbemServices** contains many methods that are irrelevant to a class provider.</span></span> <span data-ttu-id="2182c-122">Ihre-Implementierung muss den Abruf und die Enumeration der Klasse über die [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) [**-Methode und**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) die-Methode der Methode "die Methode" ".</span><span class="sxs-lookup"><span data-stu-id="2182c-122">Your implementation must support class retrieval and enumeration, through the [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) and [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) methods respectively.</span></span> <span data-ttu-id="2182c-123">In der folgenden Tabelle sind die zusätzlichen asynchronen **IWbemServices** -Methoden aufgelistet, die Sie für einen Klassen Anbieter implementieren können.</span><span class="sxs-lookup"><span data-stu-id="2182c-123">The following table lists the additional asynchronous **IWbemServices** methods that you can implement for a class provider.</span></span>



| <span data-ttu-id="2182c-124">Methode</span><span class="sxs-lookup"><span data-stu-id="2182c-124">Method</span></span>                                                     | <span data-ttu-id="2182c-125">Funktion</span><span class="sxs-lookup"><span data-stu-id="2182c-125">Feature</span></span>      |
|------------------------------------------------------------|--------------|
| [<span data-ttu-id="2182c-126">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="2182c-126">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | <span data-ttu-id="2182c-127">Modifikation (Modification)</span><span class="sxs-lookup"><span data-stu-id="2182c-127">Modification</span></span> |
| [<span data-ttu-id="2182c-128">**DeleteClassAsync**</span><span class="sxs-lookup"><span data-stu-id="2182c-128">**DeleteClassAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | <span data-ttu-id="2182c-129">Löschen</span><span class="sxs-lookup"><span data-stu-id="2182c-129">Deletion</span></span>     |



 

> [!Note]  
> <span data-ttu-id="2182c-130">Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2182c-130">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="2182c-131">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2182c-131">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="2182c-132">Der Klassen Anbieter sollte eine Stub-Implementierung bereitstellen, die den WBEM E-Anbieter zurückgibt, der nicht für alle anderen [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Methoden **\_ \_ \_ \_ geeignet ist** , die die Funktionsgruppe nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2182c-132">Your class provider should supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** for all of other [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods that do not support your feature set.</span></span> <span data-ttu-id="2182c-133">WMI unterstützt insbesondere keine Abfrage Verarbeitung für Klassen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="2182c-133">Specifically, WMI does not support query processing for class providers.</span></span> <span data-ttu-id="2182c-134">Daher muss ein Klassen Anbieter den **WBEM E- \_ \_ Anbieter \_ \_** zurückgeben, der aus der Implementierung [**von IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)nicht kompatibel ist, seine **querysupportlevels** -Registrierungs Eigenschaft auf **null** oder beides festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="2182c-134">As such, a class provider must return **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from their implementation of [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), set their **QuerySupportLevels** registration property to **NULL**, or both.</span></span>

<span data-ttu-id="2182c-135">Die Schnittstellen, die von einem Klassen Anbieter implementiert werden, ähneln den Schnittstellen für einen Instanzanbieter und einen Methoden Anbieter.</span><span class="sxs-lookup"><span data-stu-id="2182c-135">The interfaces that a class provider implements are very similar to the interfaces for an instance provider and a method provider.</span></span> <span data-ttu-id="2182c-136">Tatsächlich kann ein einzelner Anbieter als alle drei Typen von Anbietern fungieren, indem er alle Methoden implementiert und ordnungsgemäß registriert wird.</span><span class="sxs-lookup"><span data-stu-id="2182c-136">In fact, a single provider can act as all three types of provider by implementing all the methods and registering properly.</span></span>

 

 



