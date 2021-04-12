---
title: D3DPERF_BeginEvent-Funktion
description: Markiert den Anfang eines benutzerdefinierten Ereignisses. Pix kann dieses Ereignis verwenden, um eine Aktion zu initiieren.
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
- D3DPERF_BeginEvent
targetos: Windows
ms.openlocfilehash: f6732d4ce969cbd26cdb32f4750654c7baacd324
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "104390004"
---
# <a name="d3dperf_beginevent-function"></a><span data-ttu-id="ba664-104">D3DPERF_BeginEvent-Funktion</span><span class="sxs-lookup"><span data-stu-id="ba664-104">D3DPERF_BeginEvent function</span></span>

<span data-ttu-id="ba664-105">Markiert den Anfang eines benutzerdefinierten Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="ba664-105">Marks the beginning of a user-defined event.</span></span> <span data-ttu-id="ba664-106">Pix kann dieses Ereignis verwenden, um eine Aktion zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="ba664-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba664-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba664-107">Syntax</span></span>

```cpp
int WINAPI D3DPERF_BeginEvent(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="ba664-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba664-108">Parameters</span></span>

`col`

<span data-ttu-id="ba664-109">Ereignis Farbe.</span><span class="sxs-lookup"><span data-stu-id="ba664-109">Event color.</span></span> <span data-ttu-id="ba664-110">Dies ist die Farbe, um das Ereignis in der Ereignisansicht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ba664-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="ba664-111">Ereignisname.</span><span class="sxs-lookup"><span data-stu-id="ba664-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba664-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba664-112">Return value</span></span>

<span data-ttu-id="ba664-113">Die null basierte Ebene der Hierarchie, in der dieses Ereignis beginnt.</span><span class="sxs-lookup"><span data-stu-id="ba664-113">The zero-based level of the hierarchy that this event is starting in.</span></span> <span data-ttu-id="ba664-114">Wenn ein Fehler auftritt, wird der Rückgabewert negativ sein.</span><span class="sxs-lookup"><span data-stu-id="ba664-114">If an error occurs, the return value will be negative.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba664-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba664-115">Remarks</span></span>

<span data-ttu-id="ba664-116">Benutzerdefinierte Ereignisse gruppieren andere Ereignisse auf eine Weise, die für das Zielprogramm sinnvoll ist, damit Sie in Leistungsprofil Erstellungs Tools besser dargestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="ba664-116">User-defined events group together other events in a way that is meaningful to the target program so that they can be better represented in performance profiling tools.</span></span> <span data-ttu-id="ba664-117">Beispielsweise kann ein *Draw-Spaceship* -Ereignis eine Reihe von Direct3D-aufrufen Klammern, die das Zeichnen eines-Spaceship in einem Spiel verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ba664-117">For example, a *Draw Spaceship* event might bracket a number of Direct3D calls that handle drawing a spaceship in a game.</span></span> <span data-ttu-id="ba664-118">Ereignisse können eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="ba664-118">Events can be nested.</span></span>

<span data-ttu-id="ba664-119">Jeder **D3DPERF_BeginEvent** -aufrufsbefehl sollte über einen passenden **D3DPERF_EndEvent** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ba664-119">Each **D3DPERF_BeginEvent** call should have a matching **D3DPERF_EndEvent** call.</span></span> <span data-ttu-id="ba664-120">Sofortige Ereignisse (bei denen andere Ereignisse nicht eckige Klammern sind) sollten mithilfe von **D3DPERF_SetMarker** und nicht durch **D3DPERF_BeginEvent** und **D3DPERF_EndEvent** gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="ba664-120">Instantaneous events (which do not bracket other events) should be labeled by using **D3DPERF_SetMarker** rather than by **D3DPERF_BeginEvent** and **D3DPERF_EndEvent**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba664-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba664-121">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ba664-122">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="ba664-122">**Target Platform**</span></span> | <span data-ttu-id="ba664-123">Windows</span><span class="sxs-lookup"><span data-stu-id="ba664-123">Windows</span></span> |
| <span data-ttu-id="ba664-124">**Header**</span><span class="sxs-lookup"><span data-stu-id="ba664-124">**Header**</span></span> | <span data-ttu-id="ba664-125">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="ba664-125">d3d9.h</span></span> |
| <span data-ttu-id="ba664-126">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="ba664-126">**Library**</span></span> | <span data-ttu-id="ba664-127">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="ba664-127">d3d9.lib</span></span> |
| <span data-ttu-id="ba664-128">**DLL**</span><span class="sxs-lookup"><span data-stu-id="ba664-128">**DLL**</span></span> | <span data-ttu-id="ba664-129">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="ba664-129">d3d9.dll</span></span> |