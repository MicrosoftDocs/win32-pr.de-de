---
description: Konfigurieren von COM+-Diensten mit cserviceconfig
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: Konfigurieren von COM+-Diensten mit cserviceconfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8bbc6c3131347f450340863db70fd9b3999730
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748049"
---
# <a name="configuring-com-services-with-cserviceconfig"></a><span data-ttu-id="cf343-103">Konfigurieren von COM+-Diensten mit cserviceconfig</span><span class="sxs-lookup"><span data-stu-id="cf343-103">Configuring COM+ Services with CServiceConfig</span></span>

<span data-ttu-id="cf343-104">Die [**cserviceconfig**](cserviceconfig.md) -Klasse wird verwendet, um die com+-Dienste zu konfigurieren, die ohne Komponenten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="cf343-104">The [**CServiceConfig**](cserviceconfig.md) class is used to configure the COM+ services that can be used without components.</span></span> <span data-ttu-id="cf343-105">Er aggregiert den frei Thread-Mars Haller und kann daher in verschiedenen Apartments verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf343-105">It aggregates the free-threaded marshaler, so it can be used in different apartments.</span></span> <span data-ttu-id="cf343-106">Um einen einzelnen Dienst zu konfigurieren, müssen Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die dem Dienst zugeordnete-Schnittstelle aufzurufen und dann Methoden für diese Schnittstelle aufzurufen, um die entsprechende Konfiguration einzurichten.</span><span class="sxs-lookup"><span data-stu-id="cf343-106">To configure an individual service, you must call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.</span></span> <span data-ttu-id="cf343-107">In der folgenden Tabelle werden die Schnittstellen beschrieben, die durch die **cserviceconfig** -Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="cf343-107">The following table describes the interfaces that are implemented through the **CServiceConfig** class.</span></span>



| <span data-ttu-id="cf343-108">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cf343-108">Interface</span></span>                                                                         | <span data-ttu-id="cf343-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf343-109">Description</span></span>                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf343-110">**Iserviceingeerbanceconfig**</span><span class="sxs-lookup"><span data-stu-id="cf343-110">**IServiceInheritanceConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/>         | <span data-ttu-id="cf343-111">Die Standardschnittstelle für die-Klasse.</span><span class="sxs-lookup"><span data-stu-id="cf343-111">The default interface for the class.</span></span> <span data-ttu-id="cf343-112">Es wird verwendet, um viele der com+-Dienste schnell zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="cf343-112">It is used to quickly initialize many of the COM+ services.</span></span><br/>                                                                                              |
| [<span data-ttu-id="cf343-113">**Iservicecomtiintrinsicsconfig**</span><span class="sxs-lookup"><span data-stu-id="cf343-113">**IServiceComTIIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> | <span data-ttu-id="cf343-114">Wird verwendet, um die systeminternen Informationen zu COM Transaction Integrator (COMTI) zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cf343-114">Used to configure the COM Transaction Integrator (COMTI) intrinsics information.</span></span> <span data-ttu-id="cf343-115">Mit COMTI können Entwickler Mainframe-basierte Transaktions Programme in komponentenbasierte Anwendungen integrieren.</span><span class="sxs-lookup"><span data-stu-id="cf343-115">COMTI allows developers to integrate mainframe-based transaction programs with component-based applications.</span></span><br/> |
| [<span data-ttu-id="cf343-116">**Iserviceiisintrinsicsconfig**</span><span class="sxs-lookup"><span data-stu-id="cf343-116">**IServiceIISIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/>     | <span data-ttu-id="cf343-117">Wird verwendet, um die systeminternen Informationen zu Internetinformationsdienste (IIS) zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cf343-117">Used to configure the Internet Information Services (IIS) intrinsics information.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="cf343-118">**Iservicepartitionconfig**</span><span class="sxs-lookup"><span data-stu-id="cf343-118">**IServicePartitionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/>             | <span data-ttu-id="cf343-119">Wird verwendet, um zu konfigurieren, wie COM+-Partitionen mit den Diensten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf343-119">Used to configure how COM+ partitions are used with the services.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="cf343-120">**Iservicesxsconfig**</span><span class="sxs-lookup"><span data-stu-id="cf343-120">**IServiceSxSConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/>                         | <span data-ttu-id="cf343-121">Wird verwendet, um parallele Assemblys zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cf343-121">Used to configure side-by-side assemblies.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="cf343-122">**Iservicesynchronizationconfig**</span><span class="sxs-lookup"><span data-stu-id="cf343-122">**IServiceSynchronizationConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> | <span data-ttu-id="cf343-123">Wird zum Konfigurieren der com+-Synchronisierungs Dienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf343-123">Used to configure COM+ synchronization services.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="cf343-124">**Iservicethreadpoolconfig**</span><span class="sxs-lookup"><span data-stu-id="cf343-124">**IServiceThreadPoolConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/>           | <span data-ttu-id="cf343-125">Wird verwendet, um den Thread Pool für den com+-Dienst zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cf343-125">Used to configure the thread pool for the COM+ service.</span></span> <span data-ttu-id="cf343-126">Der Thread Pool kann nur konfiguriert werden, wenn die [**cokreateactivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf343-126">The thread pool can be configured only when using the [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function.</span></span><br/>                          |
| [<span data-ttu-id="cf343-127">**Iservicetrackerconfig**</span><span class="sxs-lookup"><span data-stu-id="cf343-127">**IServiceTrackerConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/>                 | <span data-ttu-id="cf343-128">Wird zum Konfigurieren der Tracker-Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf343-128">Used to configure the Tracker property.</span></span> <span data-ttu-id="cf343-129">Tracker ist ein Berichtsmechanismus, der von der Überwachung des Codes verwendet wird, um zu beobachten, welcher Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf343-129">Tracker is a reporting mechanism used by monitoring code to watch which code is running when.</span></span><br/>                                                         |
| [<span data-ttu-id="cf343-130">**Iservicetransaktionconfig**</span><span class="sxs-lookup"><span data-stu-id="cf343-130">**IServiceTransactionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/>         | <span data-ttu-id="cf343-131">Wird verwendet, um den com+-Transaktions Dienst zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cf343-131">Used to configure the COM+ transaction service.</span></span><br/>                                                                                                                                               |



 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="cf343-132">Verwaltungs Tool für Komponenten Dienste</span><span class="sxs-lookup"><span data-stu-id="cf343-132">Component Services Administrative Tool</span></span>

<span data-ttu-id="cf343-133">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="cf343-133">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="cf343-134">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cf343-134">Visual Basic</span></span>

<span data-ttu-id="cf343-135">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="cf343-135">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="cf343-136">C/C++</span><span class="sxs-lookup"><span data-stu-id="cf343-136">C/C++</span></span>

<span data-ttu-id="cf343-137">Das folgende Code Fragment veranschaulicht, wie ein [**cserviceconfig**](cserviceconfig.md) -Objekt erstellt und konfiguriert wird, um com+-Transaktionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cf343-137">The following code fragment illustrates how to create and configure a [**CServiceConfig**](cserviceconfig.md) object to use COM+ transactions.</span></span>


```C++
// Create a CServiceConfig object.
HRESULT hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
  IID_IUnknown, (void**)&pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Query for the IServiceInheritanceConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceInheritanceConfig, 
  (void**)&pInheritanceConfig);
if (FAILED(hr)) throw(hr);

// Inherit the current context before using transactions.
hr = pInheritanceConfig->ContainingContextTreatment(CSC_Inherit);
if (FAILED(hr)) throw(hr);

// Query for the IServiceTransactionConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceTransactionConfig, 
  (void**)&pTransactionConfig);
if (FAILED(hr)) throw(hr);

// Configure transactions to always create a new one.
hr = pTransactionConfig->ConfigureTransaction(CSC_NewTransaction);
if (FAILED(hr)) throw(hr);

// Set the isolation level of the transactions to ReadCommitted.
hr = pTransactionConfig->IsolationLevel( 
  COMAdminTxIsolationLevelReadCommitted);
if (FAILED(hr)) throw(hr);

// Set the transaction time-out to 1 minute.
hr = pTransactionConfig->TransactionTimeout(60);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a><span data-ttu-id="cf343-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cf343-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf343-139">**Cserviceconfig**</span><span class="sxs-lookup"><span data-stu-id="cf343-139">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="cf343-140">Verwenden von COM+-Diensten über cokreateactivity</span><span class="sxs-lookup"><span data-stu-id="cf343-140">Using COM+ Services Through CoCreateActivity</span></span>](using-com--services-through-cocreateactivity.md)
</dt> <dt>

[<span data-ttu-id="cf343-141">Verwenden von COM+-Diensten über coenterservicedomain und coleaveservicedomain</span><span class="sxs-lookup"><span data-stu-id="cf343-141">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

