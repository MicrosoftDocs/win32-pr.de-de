---
title: D3DPERF_QueryRepeatFrame-Funktion
description: Bestimmen Sie, ob ein leistungsprofiler anfordert, dass der aktuelle Frame zur Leistungsanalyse erneut an Direct3D übermittelt wird. Diese Funktion wird zurzeit von Pix nicht unterstützt.
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
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: c4054a0704fd0258483ee0d3d3d555cb5eabe7f9
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "103723877"
---
# <a name="d3dperf_queryrepeatframe-function"></a><span data-ttu-id="d9a56-104">D3DPERF_QueryRepeatFrame-Funktion</span><span class="sxs-lookup"><span data-stu-id="d9a56-104">D3DPERF_QueryRepeatFrame function</span></span>

<span data-ttu-id="d9a56-105">Bestimmen Sie, ob ein leistungsprofiler anfordert, dass der aktuelle Frame zur Leistungsanalyse erneut an Direct3D übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="d9a56-105">Determine whether a performance profiler is requesting that the current frame be resubmitted to Direct3D for performance analysis.</span></span> <span data-ttu-id="d9a56-106">Diese Funktion wird zurzeit von Pix nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d9a56-106">This function is not currently supported by PIX.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a56-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9a56-107">Syntax</span></span>

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a><span data-ttu-id="d9a56-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9a56-108">Return value</span></span>

<span data-ttu-id="d9a56-109">Wenn der Rückgabewert true ist, sollte der Aufrufer dieselbe Aufruf Sequenz wiederholen.</span><span class="sxs-lookup"><span data-stu-id="d9a56-109">If the return value is TRUE, the caller should repeat the same sequence of calls.</span></span> <span data-ttu-id="d9a56-110">Wenn false, sollte der Aufrufer fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="d9a56-110">If FALSE, the caller should continue.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9a56-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9a56-111">Remarks</span></span>

<span data-ttu-id="d9a56-112">Die-Funktion sollte unmittelbar nach IDirect3DDevice9 aufgerufen werden **::P Resent** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d9a56-112">The function should be called immediately after **IDirect3DDevice9::Present** is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9a56-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9a56-113">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d9a56-114">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="d9a56-114">**Target Platform**</span></span> | <span data-ttu-id="d9a56-115">Windows</span><span class="sxs-lookup"><span data-stu-id="d9a56-115">Windows</span></span> |
| <span data-ttu-id="d9a56-116">**Header**</span><span class="sxs-lookup"><span data-stu-id="d9a56-116">**Header**</span></span> | <span data-ttu-id="d9a56-117">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="d9a56-117">d3d9.h</span></span> |
| <span data-ttu-id="d9a56-118">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="d9a56-118">**Library**</span></span> | <span data-ttu-id="d9a56-119">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="d9a56-119">d3d9.lib</span></span> |
| <span data-ttu-id="d9a56-120">**DLL**</span><span class="sxs-lookup"><span data-stu-id="d9a56-120">**DLL**</span></span> | <span data-ttu-id="d9a56-121">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="d9a56-121">d3d9.dll</span></span> |