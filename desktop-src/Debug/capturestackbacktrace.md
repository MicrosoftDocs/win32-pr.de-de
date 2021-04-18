---
UID: ''
title: Capturestackbacktrace-Funktion
description: Erfasst eine Stapel Rückverfolgung, indem der Stapel nach oben durchlaufen wird.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: RtlCaptureStackBackTrace
ms.topic: reference
req.header: WinBase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-rtlsupport-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-rtlsupport-l1-1-0.dll
api_name:
- CaptureStackBackTrace
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 3c9edc9184000d513b82ad4131e3ac05c2ed22d6
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "106341286"
---
# <a name="capturestackbacktrace-function"></a><span data-ttu-id="2daa0-103">Capturestackbacktrace-Funktion</span><span class="sxs-lookup"><span data-stu-id="2daa0-103">CaptureStackBackTrace function</span></span>

## <a name="description"></a><span data-ttu-id="2daa0-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2daa0-104">Description</span></span>

<span data-ttu-id="2daa0-105">Erfasst eine Stapel Rückverfolgung, indem der Stapel nach oben durchlaufen und die Informationen für die einzelnen Frames aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="2daa0-105">Captures a stack back trace by walking up the stack and recording the information for each frame.</span></span>

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a><span data-ttu-id="2daa0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2daa0-106">Parameters</span></span>

### <a name="framestoskip-in"></a><span data-ttu-id="2daa0-107">Framestoskip [in]</span><span class="sxs-lookup"><span data-stu-id="2daa0-107">FramesToSkip [in]</span></span>

<span data-ttu-id="2daa0-108">Die Anzahl der Rahmen, die vom Anfang der Rückverfolgung ausgelassen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2daa0-108">The number of frames to skip from the start of the back trace.</span></span>

### <a name="framestocapture-in"></a><span data-ttu-id="2daa0-109">Framestocapture [in]</span><span class="sxs-lookup"><span data-stu-id="2daa0-109">FramesToCapture [in]</span></span>

<span data-ttu-id="2daa0-110">Die Anzahl der zu erfassenden Frames.</span><span class="sxs-lookup"><span data-stu-id="2daa0-110">The number of frames to be captured.</span></span>
<span data-ttu-id="2daa0-111">Sie können bis zu **maxushort** -Frames erfassen.</span><span class="sxs-lookup"><span data-stu-id="2daa0-111">You can capture up to **MAXUSHORT** frames.</span></span>

<span data-ttu-id="2daa0-112">**Windows Server 2003 und Windows XP:**  Die Summe der Parameter " *framestoskip* " und " *framestocapture* " muss kleiner als 63 sein.</span><span class="sxs-lookup"><span data-stu-id="2daa0-112">**Windows Server 2003 and Windows XP:**  The sum of the *FramesToSkip* and *FramesToCapture* parameters must be less than 63.</span></span>

### <a name="backtrace-out"></a><span data-ttu-id="2daa0-113">Rückverfolgung [out]</span><span class="sxs-lookup"><span data-stu-id="2daa0-113">BackTrace [out]</span></span>

<span data-ttu-id="2daa0-114">Ein Array von Zeigern, die von der aktuellen Stapel Überwachung aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="2daa0-114">An array of pointers captured from the current stack trace.</span></span>

### <a name="backtracehash-out-optional"></a><span data-ttu-id="2daa0-115">Backtracehash [out, optional]</span><span class="sxs-lookup"><span data-stu-id="2daa0-115">BackTraceHash [out, optional]</span></span>

<span data-ttu-id="2daa0-116">Ein Wert, der zum Organisieren von Hash Tabellen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2daa0-116">A value that can be used to organize hash tables.</span></span>
<span data-ttu-id="2daa0-117">Wenn dieser Parameter **null** ist, wird kein Hashwert berechnet.</span><span class="sxs-lookup"><span data-stu-id="2daa0-117">If this parameter is **NULL**, then no hash value is computed.</span></span>

<span data-ttu-id="2daa0-118">Dieser Wert wird basierend auf den Werten der Zeiger berechnet, die im Backtrace-Array zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2daa0-118">This value is calculated based on the values of the pointers returned in the BackTrace array.</span></span>
<span data-ttu-id="2daa0-119">Zwei identische Stapel Überwachungen generieren identische Hashwerte.</span><span class="sxs-lookup"><span data-stu-id="2daa0-119">Two identical stack traces will generate identical hash values.</span></span>

## <a name="returns"></a><span data-ttu-id="2daa0-120">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="2daa0-120">Returns</span></span>

<span data-ttu-id="2daa0-121">Die Anzahl der aufgezeichneten Frames.</span><span class="sxs-lookup"><span data-stu-id="2daa0-121">The number of captured frames.</span></span>

## <a name="remarks"></a><span data-ttu-id="2daa0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2daa0-122">Remarks</span></span>

<span data-ttu-id="2daa0-123">Die **capturestackbacktrace** -Funktion ist als **rtlcapturestackbacktrace** -Funktion definiert (die Definition ist in der Windows SDK ab Windows Vista enthalten).</span><span class="sxs-lookup"><span data-stu-id="2daa0-123">The **CaptureStackBackTrace** function is defined as the **RtlCaptureStackBackTrace** function (the definition is included in the Windows SDK beginning with Windows Vista).</span></span>
<span data-ttu-id="2daa0-124">Weitere Informationen finden Sie unter Winbase. h und WinNT. h.</span><span class="sxs-lookup"><span data-stu-id="2daa0-124">For more information, see WinBase.h and WinNT.h.</span></span>

## <a name="see-also"></a><span data-ttu-id="2daa0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2daa0-125">See also</span></span>
