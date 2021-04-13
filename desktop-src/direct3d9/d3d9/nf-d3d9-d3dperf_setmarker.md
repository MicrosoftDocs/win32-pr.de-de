---
title: D3DPERF_SetMarker-Funktion
description: Markieren Sie ein sofortiges Ereignis. Pix kann dieses Ereignis verwenden, um eine Aktion zu initiieren.
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
- D3DPERF_SetMarker
targetos: Windows
ms.openlocfilehash: 8eef59b9914ce30b95751641c16becf1963b19e0
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2020
ms.locfileid: "104390005"
---
# <a name="d3dperf_setmarker-function"></a><span data-ttu-id="c1b84-104">D3DPERF_SetMarker-Funktion</span><span class="sxs-lookup"><span data-stu-id="c1b84-104">D3DPERF_SetMarker function</span></span>

<span data-ttu-id="c1b84-105">Markieren Sie ein sofortiges Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c1b84-105">Mark an instantaneous event.</span></span> <span data-ttu-id="c1b84-106">Pix kann dieses Ereignis verwenden, um eine Aktion zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="c1b84-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1b84-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1b84-107">Syntax</span></span>

```cpp
void WINAPI D3DPERF_SetMarker(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="c1b84-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1b84-108">Parameters</span></span>

`col`

<span data-ttu-id="c1b84-109">Ereignis Farbe.</span><span class="sxs-lookup"><span data-stu-id="c1b84-109">Event color.</span></span> <span data-ttu-id="c1b84-110">Dies ist die Farbe, um das Ereignis in der Ereignisansicht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c1b84-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="c1b84-111">Ereignisname.</span><span class="sxs-lookup"><span data-stu-id="c1b84-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1b84-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1b84-112">Return value</span></span>

<span data-ttu-id="c1b84-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c1b84-113">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1b84-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1b84-114">Remarks</span></span>

<span data-ttu-id="c1b84-115">Bei sofortigen Benutzer Ereignissen werden andere Ereignisse nicht in eckige Klammern oder gruppiert.</span><span class="sxs-lookup"><span data-stu-id="c1b84-115">Instantaneous user events do not bracket or group other events.</span></span> <span data-ttu-id="c1b84-116">Wenn der Benutzer z. b. eine Waffe in einem Spiel auslöst, könnte ein Ereignis vom Typ " *shot* " ausgelöst werden, indem ein **D3DPERF_SetMarker** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c1b84-116">For example, when the user fires a weapon in a game, a *Shot Fired* event could be created by a **D3DPERF_SetMarker** call.</span></span> <span data-ttu-id="c1b84-117">Wenn Sie mehrere Ereignisse unter einem einzelnen benutzerdefinierten Namen gruppieren möchten, verwenden Sie **D3DPERF_BeginEvent** und **D3DPERF_EndEvent** anstelle von **D3DPERF_SetMarker**.</span><span class="sxs-lookup"><span data-stu-id="c1b84-117">To group together multiple events under a single, user-defined name, use **D3DPERF_BeginEvent** and **D3DPERF_EndEvent** rather than **D3DPERF_SetMarker**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1b84-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1b84-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c1b84-119">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="c1b84-119">**Target Platform**</span></span> | <span data-ttu-id="c1b84-120">Windows</span><span class="sxs-lookup"><span data-stu-id="c1b84-120">Windows</span></span> |
| <span data-ttu-id="c1b84-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="c1b84-121">**Header**</span></span> | <span data-ttu-id="c1b84-122">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="c1b84-122">d3d9.h</span></span> |
| <span data-ttu-id="c1b84-123">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="c1b84-123">**Library**</span></span> | <span data-ttu-id="c1b84-124">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="c1b84-124">d3d9.lib</span></span> |
| <span data-ttu-id="c1b84-125">**DLL**</span><span class="sxs-lookup"><span data-stu-id="c1b84-125">**DLL**</span></span> | <span data-ttu-id="c1b84-126">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="c1b84-126">d3d9.dll</span></span> |