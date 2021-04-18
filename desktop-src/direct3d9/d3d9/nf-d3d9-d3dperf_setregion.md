---
title: D3DPERF_SetRegion-Funktion
description: Markieren Sie in der Datei "pixrun" eine Reihe von Frames mit der angegebenen Farbe und dem angegebenen Namen. Diese Funktion wird zurzeit von Pix nicht unterstützt.
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
- D3DPERF_SetRegion
targetos: Windows
ms.openlocfilehash: 650cc6063865da5ce30b97ed1468c1718ace5da6
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "106340483"
---
# <a name="d3dperf_setregion-function"></a><span data-ttu-id="011fe-104">D3DPERF_SetRegion-Funktion</span><span class="sxs-lookup"><span data-stu-id="011fe-104">D3DPERF_SetRegion function</span></span>

<span data-ttu-id="011fe-105">Markieren Sie in der Datei "pixrun" eine Reihe von Frames mit der angegebenen Farbe und dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="011fe-105">Mark a series of frames with the specified color and name in the PIXRun file.</span></span> <span data-ttu-id="011fe-106">Diese Funktion wird zurzeit von Pix nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="011fe-106">This function is not currently supported by PIX.</span></span>

## <a name="syntax"></a><span data-ttu-id="011fe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="011fe-107">Syntax</span></span>

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="011fe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="011fe-108">Parameters</span></span>

`col`

<span data-ttu-id="011fe-109">Ereignis Farbe.</span><span class="sxs-lookup"><span data-stu-id="011fe-109">Event color.</span></span> <span data-ttu-id="011fe-110">Dies ist die Farbe, um das Ereignis in der Ereignisansicht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="011fe-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="011fe-111">Ereignisname.</span><span class="sxs-lookup"><span data-stu-id="011fe-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="011fe-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="011fe-112">Return value</span></span>

<span data-ttu-id="011fe-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="011fe-113">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="011fe-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="011fe-114">Remarks</span></span>

<span data-ttu-id="011fe-115">Um die Analyse zu vereinfachen, kann das Zielprogramm Farben verwenden, um jede Ebene eines Zielprogramms zu markieren.</span><span class="sxs-lookup"><span data-stu-id="011fe-115">To make analysis easier, the target program can use color to mark each level of a target program.</span></span>

## <a name="requirements"></a><span data-ttu-id="011fe-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="011fe-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="011fe-117">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="011fe-117">**Target Platform**</span></span> | <span data-ttu-id="011fe-118">Windows</span><span class="sxs-lookup"><span data-stu-id="011fe-118">Windows</span></span> |
| <span data-ttu-id="011fe-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="011fe-119">**Header**</span></span> | <span data-ttu-id="011fe-120">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="011fe-120">d3d9.h</span></span> |
| <span data-ttu-id="011fe-121">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="011fe-121">**Library**</span></span> | <span data-ttu-id="011fe-122">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="011fe-122">d3d9.lib</span></span> |
| <span data-ttu-id="011fe-123">**DLL**</span><span class="sxs-lookup"><span data-stu-id="011fe-123">**DLL**</span></span> | <span data-ttu-id="011fe-124">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="011fe-124">d3d9.dll</span></span> |