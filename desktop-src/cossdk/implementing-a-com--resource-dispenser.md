---
description: Implementieren eines com+-Ressourcen Verteilers
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Implementieren eines com+-Ressourcen Verteilers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81e189f3bfc5025bc949ef6e5bc82bf9408c339
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127549"
---
# <a name="implementing-a-com-resource-dispenser"></a><span data-ttu-id="c5cb1-103">Implementieren eines com+-Ressourcen Verteilers</span><span class="sxs-lookup"><span data-stu-id="c5cb1-103">Implementing a COM+ Resource Dispenser</span></span>

<span data-ttu-id="c5cb1-104">Die folgenden Schritte beschreiben ein allgemeines Verfahren zum Implementieren eines com+-Ressourcen Verteilers:</span><span class="sxs-lookup"><span data-stu-id="c5cb1-104">The following steps outline a general procedure for implementing a COM+ resource dispenser:</span></span>

1.  <span data-ttu-id="c5cb1-105">Entscheiden Sie sich für das **restypid** -Format, in dem die Unterschiede zwischen den Ressourcen voneinander kategorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c5cb1-105">Decide on **RESTYPID** format that categorizes how your resources differ from each other.</span></span>

2.  <span data-ttu-id="c5cb1-106">Verwenden Sie die Header Datei bzw. die Bibliothek "mtxdm. h" und "mtxdm. lib".</span><span class="sxs-lookup"><span data-stu-id="c5cb1-106">Use the Mtxdm.h and Mtxdm.lib header file and library, respectively.</span></span>

3.  <span data-ttu-id="c5cb1-107">Erstellen Sie eine DLL, die die [**idispenser Server Driver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) -Schnittstelle und die API implementiert, die Sie für Anwendungen verfügbar machen möchten.</span><span class="sxs-lookup"><span data-stu-id="c5cb1-107">Build a DLL that implements the [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) interface and the API you want to expose to applications.</span></span>

4.  <span data-ttu-id="c5cb1-108">Aufrufen der [**getdispenser-Manager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) -Funktion beim Start ([*DllMain*](/windows/desktop/Dlls/dllmain) oder ersten Aufrufen der Dispenser-API).</span><span class="sxs-lookup"><span data-stu-id="c5cb1-108">In the startup ([*DllMain*](/windows/desktop/Dlls/dllmain) or first call to the dispenser API), call the [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) function.</span></span> <span data-ttu-id="c5cb1-109">Dies gibt einen Zeiger auf die [**idispenser Manager Manager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) -Schnittstelle des Dispenser-Managers zurück.</span><span class="sxs-lookup"><span data-stu-id="c5cb1-109">This returns a pointer to the dispenser manager's [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) interface.</span></span>

5.  <span data-ttu-id="c5cb1-110">Wenden Sie [**idispenser Server Manager:: registerdispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser)an, und übergeben Sie einen Zeiger auf Ihre Implementierung von [**idispenser Server Driver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver).</span><span class="sxs-lookup"><span data-stu-id="c5cb1-110">Call [**IDispenserManager::RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), passing a pointer to your implementation of [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver).</span></span> <span data-ttu-id="c5cb1-111">Dies bewirkt, dass der Dispenser-Manager einen Halter (Pooling-Manager) für den Ressourcen Verteiler erstellt und dann den Zeiger auf Ihre [**ihälter**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) -Schnittstelle zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c5cb1-111">This causes the dispenser manager to create a holder (pooling manager) for your resource dispenser and then return the pointer to your [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) interface.</span></span>

6.  <span data-ttu-id="c5cb1-112">Speichern Sie diesen Zeiger, damit Sie [**ihälter:: Zuweisung**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) und [**ihälter:: freeresource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource)aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="c5cb1-112">Store this pointer so that you can call [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) and [**IHolder::FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span></span>

7.  <span data-ttu-id="c5cb1-113">Sie können jetzt (als Reaktion auf Aufrufe ihrer API) Aufrufe an " [**zugriffsource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) " und " [**freeresource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource)" tätigen.</span><span class="sxs-lookup"><span data-stu-id="c5cb1-113">You can now (in response to calls to your API) make calls to [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) and [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span></span> <span data-ttu-id="c5cb1-114">" **Zuweisung** " ist zunächst eine Antwort auf die [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) -Methode, **die später jedoch** aus dem wachsenden Ressourcenpool bedient wird.</span><span class="sxs-lookup"><span data-stu-id="c5cb1-114">**AllocResource** initially responds by calling back to your [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) method, but later **AllocResource** calls are serviced from the growing pool of resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5cb1-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5cb1-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5cb1-116">Konzepte des com+-Ressourcen Verteilers</span><span class="sxs-lookup"><span data-stu-id="c5cb1-116">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="c5cb1-117">Com+-Ressourcen Verteiler Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c5cb1-117">COM+ Resource Dispenser Interfaces</span></span>](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
