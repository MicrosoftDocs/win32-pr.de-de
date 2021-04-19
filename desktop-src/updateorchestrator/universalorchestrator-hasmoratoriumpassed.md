---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Fragt den universellen Orchestrator ab, um zu bestimmen, ob der Post-OOBE-Zeitraum überschritten wurde.
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 2ed354d365b795a0c959396e6b26d6bc73baad97
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "106349744"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a><span data-ttu-id="1714f-103">Iuniversalorchestrator:: hasmoratoriumbestandene-Methode</span><span class="sxs-lookup"><span data-stu-id="1714f-103">IUniversalOrchestrator::HasMoratoriumPassed method</span></span>

> [!NOTE] 
> <span data-ttu-id="1714f-104">Diese API gehört der universellen Orchestrator-API an.</span><span class="sxs-lookup"><span data-stu-id="1714f-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="1714f-105">Ermöglicht Clients festzustellen, ob universelle Orchestrator unmittelbar nach der Out-of-Box-Obergrenze des neuen Geräts betrieben wird, was die Arbeit bei der Minimierung von Benutzer Unterbrechungen einschränkt.</span><span class="sxs-lookup"><span data-stu-id="1714f-105">Allows clients to determine if Universal Orchestrator is operating immediately after the new device Out of Box Experience, which limits work attempts to minimize user interruption.</span></span> 

## <a name="syntax"></a><span data-ttu-id="1714f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1714f-106">Syntax</span></span>

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a><span data-ttu-id="1714f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1714f-107">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="1714f-108">Eine eindeutige Zeichenfolge, die alle Aufrufe von diesem bestimmten Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1714f-108">A unique string that identifies all calls from this specific client.</span></span>

`hasMoratoriumPassed`

<span data-ttu-id="1714f-109">Ausgabeparameter, der das Ergebnis der Abfrage speichert.</span><span class="sxs-lookup"><span data-stu-id="1714f-109">Output parameter that stores the result of the query.</span></span>

## <a name="return-value"></a><span data-ttu-id="1714f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1714f-110">Return value</span></span>
<span data-ttu-id="1714f-111">Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1714f-111">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="1714f-112">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1714f-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1714f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1714f-113">Requirements</span></span>

| <span data-ttu-id="1714f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1714f-114">Requirement</span></span> | <span data-ttu-id="1714f-115">Version</span><span class="sxs-lookup"><span data-stu-id="1714f-115">Version</span></span> |
|---|---|
| <span data-ttu-id="1714f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1714f-116">Minimum supported client</span></span> | <span data-ttu-id="1714f-117">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="1714f-117">Windows 10 1903</span></span> |
|   |   |



 

 



