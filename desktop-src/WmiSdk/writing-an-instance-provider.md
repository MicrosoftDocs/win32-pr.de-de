---
description: Ein Instanzanbieter stellt Instanzen von einer oder mehreren angegebenen Klassen bereit.
ms.assetid: d53c3399-cba8-4b5d-8da0-b5a23f94c0ae
ms.tgt_platform: multiple
title: Schreiben eines Instanzanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bddfaa867624bd84cc975d32a8e7b747064d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358536"
---
# <a name="writing-an-instance-provider"></a><span data-ttu-id="7c759-103">Schreiben eines Instanzanbieters</span><span class="sxs-lookup"><span data-stu-id="7c759-103">Writing an Instance Provider</span></span>

<span data-ttu-id="7c759-104">Ein Instanzanbieter stellt Instanzen von einer oder mehreren angegebenen Klassen bereit.</span><span class="sxs-lookup"><span data-stu-id="7c759-104">An instance provider supplies instances of one or more given classes.</span></span> <span data-ttu-id="7c759-105">Ein Instanzanbieter kann z. b. Informationen zu einer CPU oder einer anderen Art von Hardware bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7c759-105">For example, an instance provider can supply information regarding a CPU or other type of hardware.</span></span> <span data-ttu-id="7c759-106">Da sich die von einem Instanzanbieter verwalteten Objekte regelmäßig ändern, werden alle Instanzanbieter als Pull-Anbieter betrachtet. Das heißt, ein Anbieter, der Informationen zu einem verwalteten Objekt dynamisch abruft, wenn WMI eine Anforderung an die Informationen sendet.</span><span class="sxs-lookup"><span data-stu-id="7c759-106">Because the objects managed by an instance provider tend to change on a regular basis, all instance providers are considered pull providers; that is, a provider that dynamically retrieves information regarding a managed object whenever WMI makes a request for the information.</span></span> <span data-ttu-id="7c759-107">Der Name stammt aus der Idee, dass WMI die Informationen vom Anbieter im Auftrag einer Client Anforderung abruft.</span><span class="sxs-lookup"><span data-stu-id="7c759-107">The name comes from the idea that WMI "pulls" the information from the provider on behalf of a client request.</span></span> <span data-ttu-id="7c759-108">Mithilfe von pulltechnologien kann ein Instanzanbieter Abruf-, Enumerations-, Änderungs-, Lösch-und Abfrage Verarbeitung einer bestimmten-Instanz unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7c759-108">Using pull technology, an instance provider can support retrieval, enumeration, modification, deletion, and query processing of a specific instance.</span></span>

<span data-ttu-id="7c759-109">Hochleistungs Anbieter können die Effizienz eines Instanzanbieters erhöhen oder Programm gesteuert auf die Daten zugreifen, die im System Monitor angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7c759-109">High-performance providers can increase the efficiency of an instance provider or programmatically access the data that appears in System Monitor.</span></span> <span data-ttu-id="7c759-110">Weitere Informationen finden Sie unter [Erstellen eines Instanzanbieters in einen High-Performance-Anbieter](making-an-instance-provider-into-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7c759-110">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md).</span></span>

<span data-ttu-id="7c759-111">Im folgenden Verfahren wird beschrieben, wie ein Instanzanbieter geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7c759-111">The following procedure describes how to write an instance provider.</span></span>

<span data-ttu-id="7c759-112">**So schreiben Sie einen Instanzanbieter**</span><span class="sxs-lookup"><span data-stu-id="7c759-112">**To write an instance provider**</span></span>

1.  <span data-ttu-id="7c759-113">[Registrieren Sie Ihren Anbieter bei WMI](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7c759-113">[Register your provider with WMI](registering-an-instance-provider.md).</span></span>

    <span data-ttu-id="7c759-114">Instanzanbieter registrieren sich bei WMI, indem Sie eine [**\_ \_ Win32Provider**](--win32provider.md) -Instanz und eine [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Klasse erstellen.</span><span class="sxs-lookup"><span data-stu-id="7c759-114">Instance providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class.</span></span>

2.  <span data-ttu-id="7c759-115">[Initialisieren Sie den Anbieter](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7c759-115">[Initialize your provider](initializing-a-provider.md).</span></span>

    <span data-ttu-id="7c759-116">WMI verwendet [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) , um einen Anbieter zu laden und zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="7c759-116">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="7c759-117">Dies ist eine Aufgabe, die allen Anbietern gemeinsam ist.</span><span class="sxs-lookup"><span data-stu-id="7c759-117">This is a task common to all providers.</span></span>

    > [!Note]  
    > <span data-ttu-id="7c759-118">Instanzanbietern wird dringend empfohlen, das Multithreading-Modell "beide" zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c759-118">Instance providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="7c759-119">[Implementieren Sie die IWbemServices-Schnittstelle für Ihren Anbieter](implementing-the-primary-interface-for-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7c759-119">[Implement the IWbemServices interface for your provider](implementing-the-primary-interface-for-an-instance-provider.md).</span></span>

    <span data-ttu-id="7c759-120">Die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle ist die primäre Schnittstelle für einen Instanzanbieter.</span><span class="sxs-lookup"><span data-stu-id="7c759-120">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for an instance provider.</span></span>

4.  <span data-ttu-id="7c759-121">Fügen Sie zusätzlichen Code hinzu, der für Ihren Anbieter erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7c759-121">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="7c759-122">Wenn Sie Ihren Anbieter entwerfen, müssen Sie wahrscheinlich WMI-Schnittstellen abrufen.</span><span class="sxs-lookup"><span data-stu-id="7c759-122">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="7c759-123">Weitere Informationen finden Sie unter [Aufrufen von WMI-aufrufen](making-calls-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="7c759-123">For more information, see [Making Calls to WMI](making-calls-to-wmi.md).</span></span>

    <span data-ttu-id="7c759-124">Beim Abrufen von Informationen für einen Client müssen Sie möglicherweise auf die Sicherheitsebenen für diesen Client zugreifen.</span><span class="sxs-lookup"><span data-stu-id="7c759-124">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="7c759-125">Weitere Informationen finden Sie unter Annehmen der Identität [eines Clients](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="7c759-125">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="7c759-126">Implementieren Sie ggf. [die Hochleistungs Schnittstelle](improving-the-efficiency-of-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7c759-126">If necessary, [implement the high-performance interface](improving-the-efficiency-of-an-instance-provider.md).</span></span>

    <span data-ttu-id="7c759-127">Die Hochleistungs Schnittstelle erhöht die Geschwindigkeit, mit der der Anbieter auf WMI-Anforderungen reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="7c759-127">The high-performance interface increases the speed at which the provider can react to requests from WMI.</span></span>

6.  <span data-ttu-id="7c759-128">Implementieren Sie ggf. die [Unterstützung für Teil Instanzupdates](supporting-partial-instance-operations.md).</span><span class="sxs-lookup"><span data-stu-id="7c759-128">If necessary, [implement support for partial-instance updates](supporting-partial-instance-operations.md).</span></span>

    <span data-ttu-id="7c759-129">Wie der Name schon sagt, ist eine partielle Instanzaktualisierung eine Technik, mit der nur ein Teil einer Instanz aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7c759-129">As the name implies, a partial-instance update is a technique use to update only part of an instance.</span></span> <span data-ttu-id="7c759-130">Weitere Informationen zum Aufrufen einer partiellen Instanz von einem Client finden Sie unter [Aktualisieren eines Teils einer Instanz](updating-part-of-an-instance.md) und Abrufen eines Teils einer [WMI-Instanz](retrieving-part-of-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="7c759-130">For more information about calling a partial instance from a client, see [Updating Part of an Instance](updating-part-of-an-instance.md) and [Retrieving Part of a WMI Instance](retrieving-part-of-an-instance.md).</span></span>

7.  <span data-ttu-id="7c759-131">Ersetzen Sie den bereits vorhandenen Anbieter durch den neuen Code.</span><span class="sxs-lookup"><span data-stu-id="7c759-131">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="7c759-132">Sie müssen diesen Schritt nicht ausführen, wenn Sie nicht über einen vorhandenen Anbieter verfügen, der kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c759-132">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="7c759-133">Weitere Informationen finden Sie unter [Aktualisieren eines Anbieters](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7c759-133">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



