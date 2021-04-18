---
title: ADSI-Dienstanbieter
description: Dieses Thema enthält eine Übersicht über die ADSI-Dienstanbieter, die auf dem Server bereitgestellt werden.
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Dienstanbieter
- Dienstanbieter ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44ba4ebc63338bfb38d2b9d5da1f46e51b31aa8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106340532"
---
# <a name="adsi-service-providers"></a><span data-ttu-id="02912-105">ADSI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="02912-105">ADSI Service Providers</span></span>

<span data-ttu-id="02912-106">ADSI schließt die in der folgenden Tabelle aufgeführten Dienstanbieter ein.</span><span class="sxs-lookup"><span data-stu-id="02912-106">ADSI includes the service providers listed in the following table.</span></span>



| <span data-ttu-id="02912-107">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="02912-107">Service provider</span></span> | <span data-ttu-id="02912-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02912-108">Description</span></span>                                                                                | <span data-ttu-id="02912-109">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="02912-109">For more information</span></span>                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="02912-110">LDAP</span><span class="sxs-lookup"><span data-stu-id="02912-110">LDAP</span></span><br/>  | <span data-ttu-id="02912-111">Die Namespace Implementierung ist kompatibel mit dem Lightweight Directory Access Protocol.</span><span class="sxs-lookup"><span data-stu-id="02912-111">Namespace implementation compatible with Lightweight Directory Access Protocol.</span></span><br/> | [<span data-ttu-id="02912-112">ADSI-LDAP-Anbieter</span><span class="sxs-lookup"><span data-stu-id="02912-112">ADSI LDAP Provider</span></span>](adsi-ldap-provider.md)<br/>   |
| <span data-ttu-id="02912-113">WinNT</span><span class="sxs-lookup"><span data-stu-id="02912-113">WinNT</span></span><br/> | <span data-ttu-id="02912-114">Die mit Windows kompatible Namespace Implementierung.</span><span class="sxs-lookup"><span data-stu-id="02912-114">Namespace implementation compatible with Windows.</span></span><br/>                               | [<span data-ttu-id="02912-115">ADSI WinNT-Anbieter</span><span class="sxs-lookup"><span data-stu-id="02912-115">ADSI WinNT Provider</span></span>](adsi-winnt-provider.md)<br/> |



 

<span data-ttu-id="02912-116">Andere Dienstanbieter sind als Teil von anderen Produkten als ADSI enthalten.</span><span class="sxs-lookup"><span data-stu-id="02912-116">Other service providers are included as part of products other than ADSI.</span></span> <span data-ttu-id="02912-117">Im folgenden finden Sie die von Microsoft implementierten ADSI-Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="02912-117">The following are the ADSI service providers implemented by Microsoft.</span></span>



| <span data-ttu-id="02912-118">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="02912-118">Service provider</span></span> | <span data-ttu-id="02912-119">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="02912-119">For more information</span></span>                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="02912-120">IIS</span><span class="sxs-lookup"><span data-stu-id="02912-120">IIS</span></span><br/>   | <span data-ttu-id="02912-121">[IIS ADSI-Anbieter Architektur](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="02912-121">[IIS ADSI Provider Architecture](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))</span></span><br/> |



 

<span data-ttu-id="02912-122">Die von ADSI-Schnittstellen verfügbar gemachten Methoden und Eigenschaften Methoden werden von keinem Dienstanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="02912-122">The methods and property methods exposed by ADSI interfaces are not supported by every service provider.</span></span> <span data-ttu-id="02912-123">Da unterschiedliche Verzeichnisdienste in den Typen der gespeicherten Objekte und Eigenschaften variieren, verwenden Sie unterschiedliche Protokolle und die Authentifizierung, ADSI ist für die nahtlose Zusammenarbeit mit unterstützten Dienstanbietern konzipiert.</span><span class="sxs-lookup"><span data-stu-id="02912-123">Because different directory services vary in the types of objects and properties stored, use different protocols, and authentication, ADSI is designed to work seamlessly with supported service providers.</span></span> <span data-ttu-id="02912-124">Folglich gibt es Schnittstellen, Methoden und Eigenschaften Methoden, die mit einem Dienstanbieter (z. b. LDAP) funktionieren, der möglicherweise nicht auf einem anderen, z. b. WinNT, funktioniert.</span><span class="sxs-lookup"><span data-stu-id="02912-124">Thus, there are interfaces, methods, and property methods that work with one service provider, such as LDAP, that may not work on another, such as WinNT.</span></span>

<span data-ttu-id="02912-125">Dieser Abschnitt enthält anbieterspezifische Informationen, z. b. das ADsPath-Format, eine Auflistung von ADSI-Objekten, die für diesen Dienstanbieter verwendet werden, sowie Datentyp-und Syntax Informationen für die in ADSI enthaltenen Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="02912-125">This section contains provider-specific information, such as the ADsPath format, a listing of ADSI objects used for that service provider, and data type and syntax information for the service providers included with ADSI.</span></span> <span data-ttu-id="02912-126">Es gibt auch eine zusammenfassende Beschreibung der ADSI-Schnittstellen, die von jedem in ADSI enthaltenen Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="02912-126">There is also a summary description of ADSI interfaces supported by each provider included with ADSI.</span></span>

<span data-ttu-id="02912-127">In ADSI sind unterschiedliche Anbieter verschiedenen DLLs zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="02912-127">In ADSI, different providers are associated with different DLLs.</span></span> <span data-ttu-id="02912-128">Der LDAP-Anbieter ist Adsldp.dll, Adsldpc.dll und Adsmsext.dll verknüpft.</span><span class="sxs-lookup"><span data-stu-id="02912-128">The LDAP provider is associated with Adsldp.dll, Adsldpc.dll, and Adsmsext.dll.</span></span> <span data-ttu-id="02912-129">Der WinNT-Anbieter ist Adsnt.dll zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="02912-129">The WinNT provider is associated with Adsnt.dll.</span></span> <span data-ttu-id="02912-130">Der routeranbieter ist Activeds.dll zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="02912-130">The ROUTER provider is associated with Activeds.dll.</span></span>

> [!Note]  
> <span data-ttu-id="02912-131">Gehen Sie nicht davon aus, dass die standardmäßigen ADSI-Anbieter Thread sicher sind.</span><span class="sxs-lookup"><span data-stu-id="02912-131">Do not assume that default ADSI providers are thread-safe.</span></span> <span data-ttu-id="02912-132">Entwickler von Multithreadanwendungen sollten den Zugriff zwischen Threads durch die ordnungsgemäße Verwendung von Synchronisierungs Objekten wie Semaphore, Mutexen, kritischen Abschnitten usw. koordinieren.</span><span class="sxs-lookup"><span data-stu-id="02912-132">Multithreaded application developers should coordinate access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

<span data-ttu-id="02912-133">Weitere Informationen zu ADSI-Dienstanbietern finden Sie unter Unterstützung von ADSI- [Routern](adsi-router.md) und [Anbietern von ADSI-Schnittstellen](provider-support-of-adsi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="02912-133">For more information about ADSI service providers, see [ADSI Router](adsi-router.md) and [Provider Support of ADSI interfaces](provider-support-of-adsi-interfaces.md).</span></span>

 

