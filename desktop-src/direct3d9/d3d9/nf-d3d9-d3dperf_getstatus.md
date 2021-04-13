---
title: D3DPERF_GetStatus-Funktion
description: Bestimmen Sie den aktuellen Status des Profilers aus dem Zielprogramm.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_GetStatus
targetos: Windows
ms.openlocfilehash: 626d56dd449b0a0aa92e85c82dabda119900680d
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "104314465"
---
# <a name="d3dperf_getstatus-function"></a><span data-ttu-id="c776d-103">D3DPERF_GetStatus-Funktion</span><span class="sxs-lookup"><span data-stu-id="c776d-103">D3DPERF_GetStatus function</span></span>

<span data-ttu-id="c776d-104">Bestimmen Sie den aktuellen Status des Profilers aus dem Zielprogramm.</span><span class="sxs-lookup"><span data-stu-id="c776d-104">Determine the current state of the profiler from the target program.</span></span>

## <a name="syntax"></a><span data-ttu-id="c776d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c776d-105">Syntax</span></span>

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a><span data-ttu-id="c776d-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c776d-106">Return value</span></span>

<span data-ttu-id="c776d-107">Ein Wert ungleich NULL, wenn pix die Profilerstellung für das Zielprogramm durchläuft. andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c776d-107">A non-zero value when PIX is profiling the target program; otherwise, zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c776d-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c776d-108">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c776d-109">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="c776d-109">**Target Platform**</span></span> | <span data-ttu-id="c776d-110">Windows</span><span class="sxs-lookup"><span data-stu-id="c776d-110">Windows</span></span> |
| <span data-ttu-id="c776d-111">**Header**</span><span class="sxs-lookup"><span data-stu-id="c776d-111">**Header**</span></span> | <span data-ttu-id="c776d-112">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="c776d-112">d3d9.h</span></span> |
| <span data-ttu-id="c776d-113">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="c776d-113">**Library**</span></span> | <span data-ttu-id="c776d-114">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="c776d-114">d3d9.lib</span></span> |
| <span data-ttu-id="c776d-115">**DLL**</span><span class="sxs-lookup"><span data-stu-id="c776d-115">**DLL**</span></span> | <span data-ttu-id="c776d-116">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="c776d-116">d3d9.dll</span></span> |