---
title: IUniversalOrchestrator-Schnittstelle
description: Eine COM-Schnittstelle, die Methoden bereitstellt, mit denen ein Client mit dem universellen Orchestrator kommunizieren kann.
ms.date: 01/14/2021
ms.topic: interface
ms.openlocfilehash: 6fa5dfd9f7853159645fbe3b543c228450f4e1c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "106355690"
---
# <a name="iuniversalorchestrator-interface"></a><span data-ttu-id="5e253-103">IUniversalOrchestrator-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5e253-103">IUniversalOrchestrator interface</span></span>

> [!NOTE] 
> <span data-ttu-id="5e253-104">Diese API gehört der universellen Orchestrator-API an.</span><span class="sxs-lookup"><span data-stu-id="5e253-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="5e253-105">**Iuniversalorchestrator** ist eine COM-Schnittstelle, die die folgenden Methoden bereitstellt, um einem Client die Kommunikation mit dem universellen Orchestrator zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5e253-105">**IUniversalOrchestrator** is a COM interface that provides the following methods to allow a client to communicate with the Universal Orchestrator.</span></span>

## <a name="methods"></a><span data-ttu-id="5e253-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="5e253-106">Methods</span></span>

|<span data-ttu-id="5e253-107">Methode</span><span class="sxs-lookup"><span data-stu-id="5e253-107">Method</span></span> | <span data-ttu-id="5e253-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e253-108">Description</span></span> |
|---|---|
|[<span data-ttu-id="5e253-109">:: Schedulework</span><span class="sxs-lookup"><span data-stu-id="5e253-109">::ScheduleWork</span></span>](universalorchestrator-schedulework.md) | <span data-ttu-id="5e253-110">Registriert ausstehende Arbeit beim universellen Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="5e253-110">Registers pending work with the Universal Orchestrator.</span></span> |
|[<span data-ttu-id="5e253-111">:: Workabgeschlossene</span><span class="sxs-lookup"><span data-stu-id="5e253-111">::WorkCompleted</span></span>](universalorchestrator-workcompleted.md) | <span data-ttu-id="5e253-112">Informiert den universellen Orchestrator, dass die gesamte Arbeit vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="5e253-112">Informs the Universal Orchestrator that all work is complete.</span></span> |
|[<span data-ttu-id="5e253-113">:: Hasmoratoriumbestandene</span><span class="sxs-lookup"><span data-stu-id="5e253-113">::HasMoratoriumPassed</span></span>](universalorchestrator-hasmoratoriumpassed.md) | <span data-ttu-id="5e253-114">Fragt den universellen Orchestrator ab, um zu bestimmen, ob er unmittelbar nach dem neuen Gerät außerhalb des Felds funktioniert.</span><span class="sxs-lookup"><span data-stu-id="5e253-114">Queries Universal Orchestrator to determine if it is operating immediately after the new device Out of Box Experience.</span></span> |


## <a name="requirements"></a><span data-ttu-id="5e253-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e253-115">Requirements</span></span>

| <span data-ttu-id="5e253-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e253-116">Requirement</span></span> | <span data-ttu-id="5e253-117">Version</span><span class="sxs-lookup"><span data-stu-id="5e253-117">Version</span></span> |
|---|---|
| <span data-ttu-id="5e253-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e253-118">Minimum supported client</span></span> | <span data-ttu-id="5e253-119">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="5e253-119">Windows 10 1903</span></span> |
|   |   |