---
description: Verwenden von COM+-Diensten über coenterservicedomain und coleaveservicedomain
ms.assetid: 763fb01e-5daf-4e9b-8ef1-9ae79c0a84cc
title: Verwenden von COM+-Diensten über coenterservicedomain und coleaveservicedomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d87931628e177374dd07b40e9917a56c168a81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127133"
---
# <a name="using-com-services-through-coenterservicedomain-and-coleaveservicedomain"></a><span data-ttu-id="18994-103">Verwenden von COM+-Diensten über coenterservicedomain und coleaveservicedomain</span><span class="sxs-lookup"><span data-stu-id="18994-103">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>

<span data-ttu-id="18994-104">[**Coenterservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) und [**coleaveservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) werden zusammen verwendet, um einen Code Bereich zu umschließen, der in einem eigenen Kontext ausgeführt wird und com+-Dienste verwenden kann, ohne dass COM+-Komponenten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="18994-104">[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) are used together to surround an area of code that runs in its own context and can use COM+ services without the need for COM+ components.</span></span> <span data-ttu-id="18994-105">Die com+-Dienste, die in diesem Kontext verwendet werden, werden über das [**cserviceconfig**](cserviceconfig.md) -Objekt konfiguriert, das an **coenterservicedomain** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="18994-105">The COM+ services that are used in this context are configured through the [**CServiceConfig**](cserviceconfig.md) object that is passed in to **CoEnterServiceDomain**.</span></span> <span data-ttu-id="18994-106">Der Code, der von **coenterservicedomain** und **coleaveservicedomain** umgeben ist, verhält sich so, als ob es sich um eine Methode handelt, die für ein in diesem Kontext erstelltes Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="18994-106">The code that is surrounded by **CoEnterServiceDomain** and **CoLeaveServiceDomain** behaves as though it were a method that is called on an object created within this context.</span></span>

<span data-ttu-id="18994-107">Eine Skript Anwendung kann dieses Funktions paar verwenden, um Laufzeitunterstützung für COM+-Dienste ohne Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="18994-107">A scripting application can use this pair of functions to provide run-time support of COM+ services without components.</span></span> <span data-ttu-id="18994-108">Beispielsweise kann eine Skript Anwendung so entwickelt werden, dass Sie Tags bereitstellt, mit denen die Skript Schreiber eine Dienst Domäne innerhalb des Skripts eingeben und verlassen können.</span><span class="sxs-lookup"><span data-stu-id="18994-108">For example, a scripting application can be developed to provide tags that allow the script writers to enter and leave a service domain within the script.</span></span> <span data-ttu-id="18994-109">Wenn die Skript-Engine das Skript verarbeitet und auf die Tags stößt, kann es [**coenterservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) mit einem vorkonfigurierten [**cserviceconfig**](cserviceconfig.md) -Objekt anrufen, den erforderlichen Code ausführen und dann [**coleaveservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="18994-109">When the scripting engine processes the script and encounters the tags, it can call [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) with a preconfigured [**CServiceConfig**](cserviceconfig.md) object, run the necessary code, and then call [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="18994-110">Verwaltungs Tool für Komponenten Dienste</span><span class="sxs-lookup"><span data-stu-id="18994-110">Component Services Administrative Tool</span></span>

<span data-ttu-id="18994-111">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="18994-111">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="18994-112">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="18994-112">Visual Basic</span></span>

<span data-ttu-id="18994-113">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="18994-113">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="18994-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="18994-114">C/C++</span></span>

<span data-ttu-id="18994-115">Das folgende Code Fragment veranschaulicht, wie COM+-Dienste zwischen Aufrufen von [**coenterservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) und [**coleaveservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18994-115">The following code fragment illustrates how to use COM+ services between calls to [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span></span> <span data-ttu-id="18994-116">Die Fehlerbehandlung wurde weggelassen, um die Komplexität gering zu halten.</span><span class="sxs-lookup"><span data-stu-id="18994-116">Error handling is omitted for brevity.</span></span> <span data-ttu-id="18994-117">Dieses Code Fragment verwendet das [**cserviceconfig**](cserviceconfig.md) -Objekt, das in [Konfigurieren von COM+-Diensten mit cserviceconfig](configuring-com--services-with-cserviceconfig.md)erstellt und konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="18994-117">This code fragment uses the [**CServiceConfig**](cserviceconfig.md) object that was created and configured in [Configuring COM+ Services with CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span></span>


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
//   IID_IUnknown, (void**)&pUnknownCSC);

// Enter the Service Domain.
HRESULT hr = CoEnterServiceDomain(pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Do the work that uses COM+ services here.
//DoMyWork();

// Leave the Service Domain.
CoLeaveServiceDomain(NULL);
```



## <a name="related-topics"></a><span data-ttu-id="18994-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="18994-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18994-119">**Coenterservicedomain**</span><span class="sxs-lookup"><span data-stu-id="18994-119">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[<span data-ttu-id="18994-120">**Coleaveservicedomain**</span><span class="sxs-lookup"><span data-stu-id="18994-120">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[<span data-ttu-id="18994-121">Konfigurieren von COM+-Diensten mit cserviceconfig</span><span class="sxs-lookup"><span data-stu-id="18994-121">Configuring COM+ Services with CServiceConfig</span></span>](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="18994-122">**Cserviceconfig**</span><span class="sxs-lookup"><span data-stu-id="18994-122">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="18994-123">Verwenden von COM+-Diensten über cokreateactivity</span><span class="sxs-lookup"><span data-stu-id="18994-123">Using COM+ Services Through CoCreateActivity</span></span>](using-com--services-through-cocreateactivity.md)
</dt> </dl>

 

 



