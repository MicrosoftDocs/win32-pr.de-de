---
title: D2D1_SIZE_U (D2DBaseTypes. h)
description: Speichert ein geordnetes Paar von ganzen Zahlen, i. d. R. die Breite und Höhe eines Rechtecks.
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b5c317a98169957402dd125c054b8f6e0bc69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103206"
---
# <a name="d2d1_size_u"></a><span data-ttu-id="4c098-104">D2D1 \_ Größe \_ U</span><span class="sxs-lookup"><span data-stu-id="4c098-104">D2D1\_SIZE\_U</span></span>

<span data-ttu-id="4c098-105">Speichert ein geordnetes Paar von ganzen Zahlen, i. d. R. die Breite und Höhe eines Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="4c098-105">Stores an ordered pair of integers, typically the width and height of a rectangle.</span></span>


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a><span data-ttu-id="4c098-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c098-106">Remarks</span></span>

<span data-ttu-id="4c098-107">Ebenso wie Punkte sind Größen ein weiteres wichtiges Grafikkonzept.</span><span class="sxs-lookup"><span data-stu-id="4c098-107">Like points, sizes are another important graphics concept.</span></span> <span data-ttu-id="4c098-108">In Direct2D werden Größen durch die Strukturen **D2D1 \_ size \_ U** oder [**D2D1 \_ size \_ F**](d2d1-size-f.md) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4c098-108">In Direct2D, sizes are represented by the **D2D1\_SIZE\_U** or [**D2D1\_SIZE\_F**](d2d1-size-f.md) structures.</span></span> <span data-ttu-id="4c098-109">Beide enthalten ein geordnetes Zahlenpaar.</span><span class="sxs-lookup"><span data-stu-id="4c098-109">They both contain an ordered pair of numbers.</span></span> <span data-ttu-id="4c098-110">Die **Struktur D2D1 \_ size \_ U** enthält ein geordnetes Paar von **UInt32** -Werten, und die Struktur **D2D1 \_ size \_ F** enthält ein geordnetes Paar von **float** -Werten.</span><span class="sxs-lookup"><span data-stu-id="4c098-110">The **D2D1\_SIZE\_U** structure contains an ordered pair of **UINT32** values, and the **D2D1\_SIZE\_F** structure contains an ordered pair of **FLOAT** values.</span></span>

<span data-ttu-id="4c098-111">Die Struktur " **D2D1 \_ size \_ U** " ist eine bequeme Möglichkeit, ein geordnetes Paar von Zahlen zu speichern, z. b. die Breite und Höhe eines Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="4c098-111">The **D2D1\_SIZE\_U** structure provides a convenient way for you to store an ordered pair of numbers, such as the width and height of a rectangle.</span></span>

<span data-ttu-id="4c098-112">**D2D1 \_ Größe \_ u** ist ein neuer Name für einen bereits definierten Typ **D2D \_ Größe \_ u**.</span><span class="sxs-lookup"><span data-stu-id="4c098-112">**D2D1\_SIZE\_U** is a new name for an already defined type **D2D\_SIZE\_U**.</span></span> <span data-ttu-id="4c098-113">Sie können die **D2D1:: sizeu-** Funktion verwenden, um eine **D2D1 \_ size \_ U** -Struktur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4c098-113">You can use the **D2D1::SizeU** function to create a **D2D1\_SIZE\_U** structure.</span></span> <span data-ttu-id="4c098-114">Diese Struktur wird häufig verwendet, um die Pixelgröße einer [**D2D1- \_ HWND- \_ \_ Renderziel- \_ Eigenschaften**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) Struktur anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4c098-114">A common use for this structure is to specify the pixel size of a [**D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) structure.</span></span> <span data-ttu-id="4c098-115">Im folgenden finden Sie ein Beispiel für die Verwendung dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="4c098-115">The following provides an example of using this structure.</span></span>


```C++
    if (!m_pRenderTarget)
    {
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



## <a name="requirements"></a><span data-ttu-id="4c098-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c098-116">Requirements</span></span>



| <span data-ttu-id="4c098-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c098-117">Requirement</span></span> | <span data-ttu-id="4c098-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4c098-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c098-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c098-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4c098-120">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4c098-120">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="4c098-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c098-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4c098-122">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4c098-122">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="4c098-123">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="4c098-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="4c098-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="4c098-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="4c098-125">Header</span><span class="sxs-lookup"><span data-stu-id="4c098-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c098-126"><dt>D2DBaseTypes. h (Include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c098-126"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4c098-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c098-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c098-128">**D2D \_ Größe \_ U**</span><span class="sxs-lookup"><span data-stu-id="4c098-128">**D2D\_SIZE\_U**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[<span data-ttu-id="4c098-129">**D2D1 \_ size \_ F**</span><span class="sxs-lookup"><span data-stu-id="4c098-129">**D2D1\_SIZE\_F**</span></span>](d2d1-size-f.md)
</dt> <dt>

[<span data-ttu-id="4c098-130">**D2D1:: hwndrendertargetproperties**</span><span class="sxs-lookup"><span data-stu-id="4c098-130">**D2D1::HwndRenderTargetProperties**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 

