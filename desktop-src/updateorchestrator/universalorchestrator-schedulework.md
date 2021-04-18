---
title: IUniversalOrchestrator::ScheduleWork
description: Ruft Universal Orchestrator auf, um Arbeit zu planen.
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 456df8f975114f7bdf750a0449f3bd98efcc3b2e
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "106361095"
---
# <a name="iuniversalorchestratorschedulework-method"></a><span data-ttu-id="c8374-103">Iuniversalorchestrator:: schedulework-Methode</span><span class="sxs-lookup"><span data-stu-id="c8374-103">IUniversalOrchestrator::ScheduleWork method</span></span>

> [!NOTE] 
> <span data-ttu-id="c8374-104">Diese API gehört der universellen Orchestrator-API an.</span><span class="sxs-lookup"><span data-stu-id="c8374-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="c8374-105">Ermöglicht Clients, den universellen Orchestrator zu informieren, dass die Arbeit aussteht, und eine Binärdatei bereitzustellen, die von Universal Orchestrator aufgerufen wird, um die Update Arbeit zu einem späteren Zeitpunkt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c8374-105">Allows clients to inform Universal Orchestrator that work is pending and provide a binary that will be called by Universal Orchestrator to perform the update work at a later time.</span></span>

<span data-ttu-id="c8374-106">Die Rückruf Binärdatei muss mit einem gültigen Microsoft-Zertifikat signiert werden, und der Aufrufer muss den schedulework-Aufruf aus dem System Kontext aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c8374-106">The callback binary must be signed with a valid Microsoft certificate, and the caller must be invoking the ScheduleWork call from SYSTEM context.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8374-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8374-107">Syntax</span></span>

```C++
HRESULT ScheduleWork(
  LPCWSTR callerIdentifier,
  LPCWSTR cmdLine
  LPCWSTR startArg,
  LPCWSTR pauseArg);
```

## <a name="parameters"></a><span data-ttu-id="c8374-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8374-108">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="c8374-109">Eine eindeutige Zeichenfolge, die alle Aufrufe von diesem bestimmten Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c8374-109">A unique string that identifies all calls from this specific client.</span></span>

`cmdLine`

<span data-ttu-id="c8374-110">Der vollständige Pfad zur Rückruf Binärdatei, die von Universal Orchestrator aufgerufen wird, um Arbeit auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c8374-110">The full path to the callback binary that will be invoked by Universal Orchestrator to perform work.</span></span>

`startArg`

<span data-ttu-id="c8374-111">Parameter, die an die Rückruf Binärdatei übergeben werden, um anzugeben, dass der Start angefordert wird</span><span class="sxs-lookup"><span data-stu-id="c8374-111">Parameters to pass to the callback binary to indicate Start is requested.</span></span>

`pauseArg`

<span data-ttu-id="c8374-112">*(optional)* Parameter, die an die Rückruf Binärdatei übergeben werden, um anzugeben, dass die Pause angefordert wird</span><span class="sxs-lookup"><span data-stu-id="c8374-112">*(optional)* Parameters to pass to the callback binary to indicate Pause is requested.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8374-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8374-113">Return value</span></span>
<span data-ttu-id="c8374-114">Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c8374-114">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="c8374-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c8374-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8374-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8374-116">Requirements</span></span>

| <span data-ttu-id="c8374-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8374-117">Requirement</span></span> | <span data-ttu-id="c8374-118">Version</span><span class="sxs-lookup"><span data-stu-id="c8374-118">Version</span></span> |
|---|---|
| <span data-ttu-id="c8374-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8374-119">Minimum supported client</span></span> | <span data-ttu-id="c8374-120">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="c8374-120">Windows 10 1903</span></span> |
|   |   |



 

 



