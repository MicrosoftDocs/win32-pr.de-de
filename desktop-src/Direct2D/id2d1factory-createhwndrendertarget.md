---
title: ID2D1Factory-Methode für die Methode "anatehwndrendertarget" (D2d1. h)
description: Erstellt ein ID2D1HwndRenderTarget-Renderziel, das in einem Fenster gerendert wird.
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
keywords:
- Methoden von "anatehwndrendertarget" Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 984de8aea923c5b90d05fb79bc0c9edc319fb4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369138"
---
# <a name="id2d1factorycreatehwndrendertarget-methods"></a><span data-ttu-id="8c066-104">ID2D1Factory:: kreatehwndrendertarget-Methoden</span><span class="sxs-lookup"><span data-stu-id="8c066-104">ID2D1Factory::CreateHwndRenderTarget methods</span></span>

<span data-ttu-id="8c066-105">Erstellt ein [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))-Renderziel, das in einem Fenster gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="8c066-105">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span>

### <a name="overload-list"></a><span data-ttu-id="8c066-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="8c066-106">Overload list</span></span>



| <span data-ttu-id="8c066-107">Methode</span><span class="sxs-lookup"><span data-stu-id="8c066-107">Method</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="8c066-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c066-108">Description</span></span>                                                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c066-109">[**"Kreatehwndrendertarget" (D2D1- \_ \_ Renderziel \_ Eigenschaften \* , D2D1 \_ HWND- \_ \_ renderzieleigenschaften \_ \* , ID2D1HwndRenderTarget \* \* )**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c066-109">[**CreateHwndRenderTarget(D2D1\_RENDER\_TARGET\_PROPERTIES\*,D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES\*,ID2D1HwndRenderTarget\*\*)**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span></span> | <span data-ttu-id="8c066-110">Erstellt ein [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))-Renderziel, das in einem Fenster gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="8c066-110">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span><br/> |
| <span data-ttu-id="8c066-111">[**"Kreatehwndrendertarget" (D2D1 \_ \_ Renderziel \_ Eigenschaften&, D2D1 \_ HWND \_ \_ Renderziel \_ Eigenschaften&, ID2D1HwndRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))</span><span class="sxs-lookup"><span data-stu-id="8c066-111">[**CreateHwndRenderTarget(D2D1\_RENDER\_TARGET\_PROPERTIES&,D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES&,ID2D1HwndRenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))</span></span>   | <span data-ttu-id="8c066-112">Erstellt ein [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))-Renderziel, das in einem Fenster gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="8c066-112">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8c066-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c066-113">Remarks</span></span>

<span data-ttu-id="8c066-114">Wenn Sie ein Renderziel erstellen und die Hardwarebeschleunigung verfügbar ist, weisen Sie der GPU des Computers Ressourcen zu.</span><span class="sxs-lookup"><span data-stu-id="8c066-114">When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU.</span></span> <span data-ttu-id="8c066-115">Wenn Sie ein Renderziel einmal erstellen und so lange wie möglich aufbewahren, profitieren Sie von Leistungsvorteilen.</span><span class="sxs-lookup"><span data-stu-id="8c066-115">By creating a render target once and retaining it as long as possible, you gain performance benefits.</span></span> <span data-ttu-id="8c066-116">Die Anwendung sollte einmal Renderziele erstellen und Sie für die Lebensdauer der Anwendung oder bis zum D2DERR-Erstellungs [**\_ \_ Ziel**](direct2d-error-codes.md) Fehler erhalten.</span><span class="sxs-lookup"><span data-stu-id="8c066-116">Your application should create render targets once and hold onto them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="8c066-117">Wenn Sie diesen Fehler erhalten, müssen Sie das Renderziel (und alle erstellten Ressourcen) neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8c066-117">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

## <a name="examples"></a><span data-ttu-id="8c066-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c066-118">Examples</span></span>

<span data-ttu-id="8c066-119">Im folgenden Beispiel wird ein [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))erstellt.</span><span class="sxs-lookup"><span data-stu-id="8c066-119">The following example creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).</span></span>


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



## <a name="requirements"></a><span data-ttu-id="8c066-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c066-120">Requirements</span></span>



| <span data-ttu-id="8c066-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c066-121">Requirement</span></span> | <span data-ttu-id="8c066-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8c066-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8c066-123">Header</span><span class="sxs-lookup"><span data-stu-id="8c066-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8c066-124"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c066-124"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c066-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8c066-125">Library</span></span><br/> | <dl> <span data-ttu-id="8c066-126"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c066-126"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="8c066-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8c066-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c066-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c066-128"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c066-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c066-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c066-130">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="8c066-130">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
