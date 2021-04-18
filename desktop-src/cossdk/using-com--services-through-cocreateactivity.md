---
description: Die cokreateactivity-Funktion wird verwendet, um Batch Arbeit an das com+-System zu übermitteln. Dadurch können skriptbasierte Anwendungen eine Anwendungs weite com+-Dienst Konfiguration unterstützen.
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: Verwenden von COM+-Diensten über cokreateactivity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b3296756b91d0f8ea29b1d67c11c78c431cfcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341156"
---
# <a name="using-com-services-through-cocreateactivity"></a><span data-ttu-id="2f7da-104">Verwenden von COM+-Diensten über cokreateactivity</span><span class="sxs-lookup"><span data-stu-id="2f7da-104">Using COM+ Services Through CoCreateActivity</span></span>

<span data-ttu-id="2f7da-105">Die [**cokreateactivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) -Funktion wird verwendet, um Batch Arbeit an das com+-System zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="2f7da-105">The [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function is used to submit batch work to the COM+ system.</span></span> <span data-ttu-id="2f7da-106">Dadurch können skriptbasierte Anwendungen eine Anwendungs weite com+-Dienst Konfiguration unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2f7da-106">It allows script-based applications to support an application-wide COM+ service configuration.</span></span>

<span data-ttu-id="2f7da-107">Die gewünschten com+-Dienste werden über ein [**cserviceconfig**](cserviceconfig.md) -Objekt konfiguriert, das an die Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2f7da-107">The desired COM+ services are configured through a [**CServiceConfig**](cserviceconfig.md) object that is passed in to the function.</span></span> <span data-ttu-id="2f7da-108">Die-Funktion erstellt ein Aktivitäts Objekt und gibt die [**iserviceactivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) -Schnittstelle des Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="2f7da-108">The function creates an activity object and returns the [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) interface of that object.</span></span> <span data-ttu-id="2f7da-109">Die Batch Verarbeitung kann entweder synchron oder asynchron übermittelt werden, indem die [**synchouscall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) -Methode oder die [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) -Methode von **iserviceactivity** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f7da-109">The batch work can be submitted either synchronously or asynchronously, by using the [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) or [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) methods of **IServiceActivity**, respectively.</span></span> <span data-ttu-id="2f7da-110">Ein Zeiger auf eine [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) -Schnittstelle wird an jede dieser Methoden übergeben, und die Batch Arbeit wird vom Entwickler in der [**OnCall-**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) Methode der **IServiceCall** -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="2f7da-110">A pointer to an [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) interface is passed in to each of these methods, and the batch work is implemented by the developer in the [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) method of the **IServiceCall** interface.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="2f7da-111">Verwaltungs Tool für Komponenten Dienste</span><span class="sxs-lookup"><span data-stu-id="2f7da-111">Component Services Administrative Tool</span></span>

<span data-ttu-id="2f7da-112">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="2f7da-112">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="2f7da-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2f7da-113">Visual Basic</span></span>

<span data-ttu-id="2f7da-114">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="2f7da-114">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="2f7da-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="2f7da-115">C/C++</span></span>

<span data-ttu-id="2f7da-116">Das folgende Code Fragment veranschaulicht, wie COM+-Dienste über [**cokreateactivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f7da-116">The following code fragment illustrates how to use COM+ services through [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity).</span></span> <span data-ttu-id="2f7da-117">Die Fehlerbehandlung wurde weggelassen, um die Komplexität gering zu halten.</span><span class="sxs-lookup"><span data-stu-id="2f7da-117">Error handling is omitted for brevity.</span></span> <span data-ttu-id="2f7da-118">Dieses Code Fragment verwendet das [**cserviceconfig**](cserviceconfig.md) -Objekt, das in [Konfigurieren von COM+-Diensten mit cserviceconfig](configuring-com--services-with-cserviceconfig.md)erstellt und konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="2f7da-118">This code fragment uses the [**CServiceConfig**](cserviceconfig.md) object that was created and configured in [Configuring COM+ Services with CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span></span>


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER,
//   IID_IUnknown, (void**)&pUnknownCSC);

// Create the activity for our services.
HRESULT hr = CoCreateActivity(pUnknownCSC, IID_IServiceActivity, (void**)&pActivity);
if (FAILED(hr)) throw(hr);

// Do the batch work synchronously.
// The batch work is implemented in pServiceCall->OnCall().
hr = pActivity->SynchronousCall(pServiceCall);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a><span data-ttu-id="2f7da-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2f7da-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f7da-120">**Cokreateactivity**</span><span class="sxs-lookup"><span data-stu-id="2f7da-120">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[<span data-ttu-id="2f7da-121">Konfigurieren von COM+-Diensten mit cserviceconfig</span><span class="sxs-lookup"><span data-stu-id="2f7da-121">Configuring COM+ Services with CServiceConfig</span></span>](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="2f7da-122">**Cserviceconfig**</span><span class="sxs-lookup"><span data-stu-id="2f7da-122">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="2f7da-123">Verwenden von COM+-Diensten über coenterservicedomain und coleaveservicedomain</span><span class="sxs-lookup"><span data-stu-id="2f7da-123">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



