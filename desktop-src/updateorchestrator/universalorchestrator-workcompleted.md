---
title: IUniversalOrchestrator::WorkCompleted
description: Ruft Universal Orchestrator auf, um anzugeben, dass die Arbeit fertig ist
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 8d4a08e7f021811e59a182a8b726397476b78433
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "106369910"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a><span data-ttu-id="489f4-103">Iuniversalorchestrator:: workabgeschlossene-Methode</span><span class="sxs-lookup"><span data-stu-id="489f4-103">IUniversalOrchestrator::WorkCompleted method</span></span>

> [!NOTE] 
> <span data-ttu-id="489f4-104">Diese API gehört der universellen Orchestrator-API an.</span><span class="sxs-lookup"><span data-stu-id="489f4-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="489f4-105">Ermöglicht Clients, den universellen Orchestrator mitzuteilen, dass die zuvor geplante Arbeit abgeschlossen wurde, und beendet die Rückrufe, um die Arbeit bis zum nächsten erfolgreichen schedulework-Aufruf auszuführen.</span><span class="sxs-lookup"><span data-stu-id="489f4-105">Allows clients to inform Universal Orchestrator that the previously scheduled work has been completed and stop callbacks to perform work until the next successful ScheduleWork call.</span></span>

## <a name="syntax"></a><span data-ttu-id="489f4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="489f4-106">Syntax</span></span>

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a><span data-ttu-id="489f4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="489f4-107">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="489f4-108">Eine eindeutige Zeichenfolge, die alle Aufrufe von diesem bestimmten Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="489f4-108">A unique string that identifies all calls from this specific client.</span></span>

`workCompleted`

<span data-ttu-id="489f4-109">**True** , wenn die Arbeit erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="489f4-109">**TRUE** if the work successfully completed.</span></span> <span data-ttu-id="489f4-110">Andernfalls **false** , wenn der arbeitsversuch fehlgeschlagen ist und in der Zukunft erneut versucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="489f4-110">Otherwise, **FALSE** if the work attempt failed and should be retried in the future.</span></span> 

## <a name="return-value"></a><span data-ttu-id="489f4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="489f4-111">Return value</span></span>
<span data-ttu-id="489f4-112">Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="489f4-112">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="489f4-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="489f4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="489f4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="489f4-114">Requirements</span></span>

| <span data-ttu-id="489f4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="489f4-115">Requirement</span></span> | <span data-ttu-id="489f4-116">Version</span><span class="sxs-lookup"><span data-stu-id="489f4-116">Version</span></span> |
|---|---|
| <span data-ttu-id="489f4-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="489f4-117">Minimum supported client</span></span> | <span data-ttu-id="489f4-118">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="489f4-118">Windows 10 1903</span></span> |
|   |   |



 

 



