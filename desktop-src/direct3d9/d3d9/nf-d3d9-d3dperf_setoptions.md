---
title: D3DPERF_SetOptions-Funktion
description: Festlegen der vom Zielprogramm angegebenen Profiler-Optionen.
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
- D3DPERF_SetOptions
targetos: Windows
ms.openlocfilehash: 8bd877469864ccdaa833ce80d00eb06ae5fc18de
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "104472333"
---
# <a name="d3dperf_setoptions-function"></a><span data-ttu-id="b372e-103">D3DPERF_SetOptions-Funktion</span><span class="sxs-lookup"><span data-stu-id="b372e-103">D3DPERF_SetOptions function</span></span>

<span data-ttu-id="b372e-104">Festlegen der vom Zielprogramm angegebenen Profiler-Optionen.</span><span class="sxs-lookup"><span data-stu-id="b372e-104">Set profiler options specified by the target program.</span></span>

## <a name="syntax"></a><span data-ttu-id="b372e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b372e-105">Syntax</span></span>

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a><span data-ttu-id="b372e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b372e-106">Parameters</span></span>

`dwOptions`

<span data-ttu-id="b372e-107">Benutzeroptionen, die von Pix erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="b372e-107">User options recognizable by PIX.</span></span> <span data-ttu-id="b372e-108">Legen Sie diese Einstellung auf 1 fest, um pix zu benachrichtigen, dass das Zielprogramm keine Berechtigung für die Profilerstellung erteilt.</span><span class="sxs-lookup"><span data-stu-id="b372e-108">Set this to 1 to notify PIX that the target program does not give permission to be profiled.</span></span>

## <a name="return-value"></a><span data-ttu-id="b372e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b372e-109">Return value</span></span>

<span data-ttu-id="b372e-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b372e-110">This function doesn't return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b372e-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b372e-111">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b372e-112">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="b372e-112">**Target Platform**</span></span> | <span data-ttu-id="b372e-113">Windows</span><span class="sxs-lookup"><span data-stu-id="b372e-113">Windows</span></span> |
| <span data-ttu-id="b372e-114">**Header**</span><span class="sxs-lookup"><span data-stu-id="b372e-114">**Header**</span></span> | <span data-ttu-id="b372e-115">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="b372e-115">d3d9.h</span></span> |
| <span data-ttu-id="b372e-116">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="b372e-116">**Library**</span></span> | <span data-ttu-id="b372e-117">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="b372e-117">d3d9.lib</span></span> |
| <span data-ttu-id="b372e-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="b372e-118">**DLL**</span></span> | <span data-ttu-id="b372e-119">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="b372e-119">d3d9.dll</span></span> |