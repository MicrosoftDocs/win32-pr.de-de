---
description: Das com+-Anwendungs Pooling ermöglicht das Skalieren von Single Thread-Prozessen, ähnlich wie beim Thread Pooling das Skalieren von Single Thread-Objekten ermöglicht wird.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: Konzepte für das com+-Anwendungs Pooling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a72f5681896e8ac0e6a50b3bddfc16cf4303f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860875"
---
# <a name="com-application-pooling-concepts"></a><span data-ttu-id="ecf93-103">Konzepte für das com+-Anwendungs Pooling</span><span class="sxs-lookup"><span data-stu-id="ecf93-103">COM+ Application Pooling Concepts</span></span>

<span data-ttu-id="ecf93-104">Das com+-Anwendungs Pooling ermöglicht das Skalieren von Single Thread-Prozessen, ähnlich wie beim Thread Pooling das Skalieren von Single Thread-Objekten ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="ecf93-104">COM+ application pooling allows single-threaded processes to scale, similar to the way that thread pooling allows single-threaded objects to scale.</span></span> <span data-ttu-id="ecf93-105">Das Anwendungs Pooling kann auch zur Wiederherstellung nach Fehlern in einzelnen Prozessen beitragen, indem andere laufende Prozesse bereitgestellt werden, die Aktivierungen verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="ecf93-105">Application pooling can also help recover from failures in single processes by providing other running processes able to handle activations.</span></span>

> [!Note]  
> <span data-ttu-id="ecf93-106">Bibliotheksanwendungen verfügen über die Eigenschaften zum wieder verwenden und zum Pooling Ihres Host Prozesses.</span><span class="sxs-lookup"><span data-stu-id="ecf93-106">Library applications have the recycling and pooling properties of their host process.</span></span>

 

<span data-ttu-id="ecf93-107">Alle Methoden der [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) -Schnittstelle unterstützen das Anwendungs Pooling.</span><span class="sxs-lookup"><span data-stu-id="ecf93-107">All methods of the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface support application pooling.</span></span>

<span data-ttu-id="ecf93-108">Das com+-Anwendungs Pooling kann pro Anwendung mithilfe der concurrentapps-Eigenschaft des [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekts in der [**Anwendungs**](applications.md) Auflistung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ecf93-108">COM+ application pooling is configurable per application by using the ConcurrentApps property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="ecf93-109">Concurrentapps ist ein ganzzahliger Wert, der die maximale Anzahl gleichzeitiger dllhost-Prozesse angibt, die gestartet werden sollten, um Aktivierungen für eine Anwendung zu warten.</span><span class="sxs-lookup"><span data-stu-id="ecf93-109">ConcurrentApps is an integer value that specifies the maximum number of simultaneous Dllhost processes that should be started to service activations for an application.</span></span> <span data-ttu-id="ecf93-110">Diese Eigenschaft kann mithilfe des Verwaltungs Tools für Komponenten Dienste oder Programm gesteuert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ecf93-110">This property can be set by using the Component Services administration tool or programmatically.</span></span>

<span data-ttu-id="ecf93-111">Wenn die concurrentapps-Eigenschaft auf 1 festgelegt ist, was der Standardwert ist, wird der com+-anwendungspoolingdienst deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ecf93-111">If the ConcurrentApps property is set to 1, which is the default value, the COM+ Application Pooling service is disabled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ecf93-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ecf93-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecf93-113">Com+-anwendungspoolingaufgaben</span><span class="sxs-lookup"><span data-stu-id="ecf93-113">COM+ Application Pooling Tasks</span></span>](com--application-pooling-tasks.md)
</dt> <dt>

[<span data-ttu-id="ecf93-114">Konzepte der com+-Anwendungs Wiederverwendung</span><span class="sxs-lookup"><span data-stu-id="ecf93-114">COM+ Application Recycling Concepts</span></span>](com--application-recycling-concepts.md)
</dt> </dl>

 

 



