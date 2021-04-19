---
description: Gibt die Dienste an, die in der Dienst Domäne aktiv sein sollen, die beim Aufrufen von cocreateactivity oder coenterservicedomain eingegeben werden soll, und konfiguriert diese.
ms.assetid: f546ded4-255e-4565-b588-f36175902778
title: Cserviceconfig-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CServiceConfig
api_type:
- COM
ms.openlocfilehash: e0b48b05be4afa1d42dbc8a16c4b596a08aba859
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346433"
---
# <a name="cserviceconfig-class"></a><span data-ttu-id="0b02c-103">Cserviceconfig-Klasse</span><span class="sxs-lookup"><span data-stu-id="0b02c-103">CServiceConfig class</span></span>

<span data-ttu-id="0b02c-104">Gibt die Dienste an, die in der Dienst Domäne aktiv sein sollen, die beim Aufrufen von [**cocreateactivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) oder [**coenterservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)eingegeben werden soll, und konfiguriert diese.</span><span class="sxs-lookup"><span data-stu-id="0b02c-104">Specifies and configures the services that are to be active in the service domain entered when calling either [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) or [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="0b02c-105">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="0b02c-105">When to implement</span></span>

<span data-ttu-id="0b02c-106">Diese Klasse wird von com+ implementiert.</span><span class="sxs-lookup"><span data-stu-id="0b02c-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="0b02c-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b02c-107">Requirement</span></span> | <span data-ttu-id="0b02c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0b02c-108">Value</span></span> |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b02c-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="0b02c-109">CLSID</span></span>      | <span data-ttu-id="0b02c-110">CLSID \_ cserviceconfig</span><span class="sxs-lookup"><span data-stu-id="0b02c-110">CLSID\_CServiceConfig</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="0b02c-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="0b02c-111">ProgID</span></span>     | <span data-ttu-id="0b02c-112">L "Comsvcs. Cserviceconfig "</span><span class="sxs-lookup"><span data-stu-id="0b02c-112">L"COMSVCS.CServiceConfig"</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="0b02c-113">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0b02c-113">Interfaces</span></span> | [<span data-ttu-id="0b02c-114">**Iservicecomtiintrinsicsconfig**</span><span class="sxs-lookup"><span data-stu-id="0b02c-114">**IServiceComTIIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> [<span data-ttu-id="0b02c-115">**Iserviceiisintrinsicsconfig**</span><span class="sxs-lookup"><span data-stu-id="0b02c-115">**IServiceIISIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/> [<span data-ttu-id="0b02c-116">**Iserviceingeerbanceconfig**</span><span class="sxs-lookup"><span data-stu-id="0b02c-116">**IServiceInheritanceConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/> [<span data-ttu-id="0b02c-117">**Iservicepartitionconfig**</span><span class="sxs-lookup"><span data-stu-id="0b02c-117">**IServicePartitionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/> [<span data-ttu-id="0b02c-118">**Iservicesxsconfig**</span><span class="sxs-lookup"><span data-stu-id="0b02c-118">**IServiceSxSConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/> [<span data-ttu-id="0b02c-119">**Iservicesynchronizationconfig**</span><span class="sxs-lookup"><span data-stu-id="0b02c-119">**IServiceSynchronizationConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> [<span data-ttu-id="0b02c-120">**Iservicethreadpoolconfig**</span><span class="sxs-lookup"><span data-stu-id="0b02c-120">**IServiceThreadPoolConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/> [<span data-ttu-id="0b02c-121">**Iservicetrackerconfig**</span><span class="sxs-lookup"><span data-stu-id="0b02c-121">**IServiceTrackerConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/> [<span data-ttu-id="0b02c-122">**Iservicetransaktionconfig**</span><span class="sxs-lookup"><span data-stu-id="0b02c-122">**IServiceTransactionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/> |



 

## <a name="when-to-use"></a><span data-ttu-id="0b02c-123">Verwendung</span><span class="sxs-lookup"><span data-stu-id="0b02c-123">When to use</span></span>

<span data-ttu-id="0b02c-124">Verwenden Sie diese Klasse, um die Dienste zu konfigurieren, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="0b02c-124">Use this class to configure the services that you want to use.</span></span> <span data-ttu-id="0b02c-125">Mit [**cokreateactivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) und [**coenterservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) können Sie die von dieser Klasse konfigurierten Dienste verwenden, ohne diese Dienste vor der Verwendung an eine Komponente binden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="0b02c-125">[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) and [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) enable you to use the services configured by this class without needing to tie those services to a component before using them.</span></span>

<span data-ttu-id="0b02c-126">Diese Klasse wurde nicht für die Verwendung in Visual Basic konzipiert.</span><span class="sxs-lookup"><span data-stu-id="0b02c-126">This class was not designed to be used in Visual Basic.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b02c-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b02c-127">Remarks</span></span>

<span data-ttu-id="0b02c-128">Um dieses Objekt zu erstellen, rufen Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)auf.</span><span class="sxs-lookup"><span data-stu-id="0b02c-128">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="0b02c-129">Objekte, die von der **cserviceconfig** -Klasse instanziiert werden, Aggregieren den Freethread-Mars Haller, sodass Sie von System Laufzeiten gespeichert und in unterschiedlichen Apartments wieder verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0b02c-129">Objects instantiated from the **CServiceConfig** class aggregate the free-threaded marshaler so that they can be stored by system runtimes and reused in different apartments.</span></span>

<span data-ttu-id="0b02c-130">Um einen einzelnen Dienst zu konfigurieren, wird [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die dem Dienst zugeordnete-Schnittstelle aufgerufen und dann Methoden für diese Schnittstelle aufgerufen, um die entsprechende Konfiguration einzurichten.</span><span class="sxs-lookup"><span data-stu-id="0b02c-130">To configure an individual service, call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b02c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b02c-131">Requirements</span></span>



| <span data-ttu-id="0b02c-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b02c-132">Requirement</span></span> | <span data-ttu-id="0b02c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0b02c-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0b02c-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b02c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0b02c-135">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b02c-135">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0b02c-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b02c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0b02c-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b02c-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0b02c-138">Header</span><span class="sxs-lookup"><span data-stu-id="0b02c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b02c-139"><dt>"Comsvcs. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0b02c-139"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b02c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b02c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b02c-141">**Cokreateactivity**</span><span class="sxs-lookup"><span data-stu-id="0b02c-141">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[<span data-ttu-id="0b02c-142">**Cokreatefreethreadedmarshaler**</span><span class="sxs-lookup"><span data-stu-id="0b02c-142">**CoCreateFreeThreadedMarshaler**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)
</dt> <dt>

[<span data-ttu-id="0b02c-143">**Coenterservicedomain**</span><span class="sxs-lookup"><span data-stu-id="0b02c-143">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[<span data-ttu-id="0b02c-144">**Coleaveservicedomain**</span><span class="sxs-lookup"><span data-stu-id="0b02c-144">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[<span data-ttu-id="0b02c-145">Com+-Dienste ohne Komponenten</span><span class="sxs-lookup"><span data-stu-id="0b02c-145">COM+ Services Without Components</span></span>](com--services-without-components.md)
</dt> </dl>

 

