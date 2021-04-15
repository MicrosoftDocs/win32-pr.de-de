---
title: gladdtauaphintrectwin-Funktion (GL. h)
description: Die Funktion "gladdswap aphintrectwin" gibt einen Satz von Rechtecke an, die von "Swap" kopiert werden sollen.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- gladdtauaphintrectwin-Funktion OpenGL
topic_type:
- apiref
api_name:
- glAddSwapHintRectWIN
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3e10c2f51ff8d7c9763ff1dad7d09d800cd60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391999"
---
# <a name="gladdswaphintrectwin-function"></a><span data-ttu-id="61d52-104">gladdtauaphintrectwin-Funktion</span><span class="sxs-lookup"><span data-stu-id="61d52-104">glAddSwapHintRectWIN function</span></span>

<span data-ttu-id="61d52-105">Die Funktion " **gladdswap aphintrectwin** " gibt einen Satz von Rechtecke an, die von " [**Swap**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)" kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61d52-105">The **glAddSwapHintRectWIN** callback function specifies a set of rectangles that are to be copied by [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span>

## <a name="syntax"></a><span data-ttu-id="61d52-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="61d52-106">Syntax</span></span>


```C++
void WINAPI glAddSwapHintRectWIN(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="61d52-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="61d52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61d52-108">*x*</span><span class="sxs-lookup"><span data-stu-id="61d52-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="61d52-109">Die *x*-Koordinate (in Fenster Koordinaten) der unteren linken Ecke des Hint-Bereichs Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="61d52-109">The *x*-coordinate (in window coordinates) of the lower-left corner of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="61d52-110">*y*</span><span class="sxs-lookup"><span data-stu-id="61d52-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="61d52-111">Die *y*-Koordinate (in Fenster Koordinaten) der unteren linken Ecke des Hint-Bereichs Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="61d52-111">The *y*-coordinate (in window coordinates) of the lower-left corner of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="61d52-112">*width*</span><span class="sxs-lookup"><span data-stu-id="61d52-112">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="61d52-113">Die Breite des Hint-Bereichs Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="61d52-113">The width of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="61d52-114">*height*</span><span class="sxs-lookup"><span data-stu-id="61d52-114">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="61d52-115">Die Höhe des Hint-Bereichs Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="61d52-115">The height of the hint region rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61d52-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61d52-116">Return value</span></span>

<span data-ttu-id="61d52-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="61d52-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61d52-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61d52-118">Remarks</span></span>

<span data-ttu-id="61d52-119">Die Funktion " **gladdtauaphintrectwin** " beschleunigt die Animation, indem die Menge an Umzeichnung zwischen Frames reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="61d52-119">The **glAddSwapHintRectWIN** function speeds up animation by reducing the amount of repainting between frames.</span></span> <span data-ttu-id="61d52-120">Mit " **gladdtauaphintrectwin**" geben Sie einen Satz von rechteckigen Bereichen an, die beim Abrufen von " [**Austausch Puffern**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)" kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61d52-120">With **glAddSwapHintRectWIN**, you specify a set of rectangular areas that you want copied when you call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span> <span data-ttu-id="61d52-121">Wenn Sie vor dem Aufrufen von " **Austausch Puffer**" keine Rechtecke mit " **gladdtauaphintrectwin** " angeben, wird der gesamte Frame Puffer ausgetauscht.</span><span class="sxs-lookup"><span data-stu-id="61d52-121">When you do not specify any rectangles with **glAddSwapHintRectWIN** before calling **SwapBuffers**, the entire framebuffer is swapped.</span></span> <span data-ttu-id="61d52-122">Die Verwendung von " **gladdtauaphintrectwin** ", um nur geänderte Teile des Puffers zu kopieren, kann die Leistung von "Swap"- **Puffer** erheblich erhöhen, insbesondere dann, wenn " **Swap Buffers** " in Software implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="61d52-122">Using **glAddSwapHintRectWIN** to copy only changed parts of the buffer can significantly increase the performance of **SwapBuffers**, especially when **SwapBuffers** is implemented in software.</span></span>

<span data-ttu-id="61d52-123">Die Funktion " **gladdtauaphintrectwin** " fügt dem Hinweis Bereich ein Rechteck hinzu.</span><span class="sxs-lookup"><span data-stu-id="61d52-123">The **glAddSwapHintRectWIN** function adds a rectangle to the hint region.</span></span> <span data-ttu-id="61d52-124">Wenn das PFD \_ - \_ auslagerungskopierflag der [**pixelformatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) -Pixel Format Struktur festgelegt ist, verwendet **swapbuffers** diesen Bereich, um das Kopieren des Hintergrund Puffers auf den Frontpuffer abzuschneiden.</span><span class="sxs-lookup"><span data-stu-id="61d52-124">When the PFD\_SWAP\_COPY flag of the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) pixel format structure is set, **SwapBuffers** uses this region to clip the copying of the back buffer to the front buffer.</span></span> <span data-ttu-id="61d52-125">Sie geben die PFD \_ - \_ swapkopie nicht an. Sie wird durch die leistungsfähige Hardware festgelegt.</span><span class="sxs-lookup"><span data-stu-id="61d52-125">You don't specify PFD\_SWAP\_COPY; it is set by capable hardware.</span></span> <span data-ttu-id="61d52-126">Der Hinweis Bereich wird nach jedem Rückruf von " **Austausch Puffer**" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="61d52-126">The hint region is cleared after each call to **SwapBuffers**.</span></span> <span data-ttu-id="61d52-127">Bei manchen Hardware Konfigurationen können **Austausch Puffer** den Hinweis Bereich ignorieren und den gesamten Puffer austauschen.</span><span class="sxs-lookup"><span data-stu-id="61d52-127">With some hardware configurations, **SwapBuffers** can ignore the hint region and exchange the entire buffer.</span></span> <span data-ttu-id="61d52-128">**Swap-Puffer** werden vom System implementiert, nicht von der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="61d52-128">**SwapBuffers** is implemented by the system, not by the application.</span></span>

<span data-ttu-id="61d52-129">OpenGL verwaltet für jedes Fenster einen separaten Hinweis Bereich.</span><span class="sxs-lookup"><span data-stu-id="61d52-129">OpenGL maintains a separate hint region for each window.</span></span> <span data-ttu-id="61d52-130">Wenn Sie " **gladdtauaphintrectwin** " für alle einem Fenster zugeordneten renderingkontexte aufzurufen, werden die Hinweis Rechtecke in einer einzelnen Region kombiniert.</span><span class="sxs-lookup"><span data-stu-id="61d52-130">When you call **glAddSwapHintRectWIN** on any rendering contexts associated with a window, the hint rectangles are combined into a single region.</span></span>

<span data-ttu-id="61d52-131">Wenden Sie " **gladdtauaphintrectwin** " mit einem umschließenden Rechteck für jedes für einen Frame gezeichnete Objekt an, und für jedes Rechteck, das zum Löschen Vorheriger Frame Objekte gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="61d52-131">Call **glAddSwapHintRectWIN** with a bounding rectangle for each object drawn for a frame and for each rectangle cleared to erase previous frame objects.</span></span>

> [!Note]  
> <span data-ttu-id="61d52-132">Die Funktion " **gladdswaphintrectwin** " ist eine Erweiterungs Funktion, die nicht Teil der OpenGL-Standardbibliothek ist, aber Teil der GL- \_ Win-Swap- \_ \_ Hinweis Erweiterung ist.</span><span class="sxs-lookup"><span data-stu-id="61d52-132">The **glAddSwapHintRectWIN** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_WIN\_swap\_hint extension.</span></span> <span data-ttu-id="61d52-133">Um zu überprüfen, ob die Implementierung von OpenGL " **gladdtauaphintrectwin**" unterstützt, nennen Sie " **glgetstring**(GL \_ Extensions)".</span><span class="sxs-lookup"><span data-stu-id="61d52-133">To check whether your implementation of OpenGL supports **glAddSwapHintRectWIN**, call **glGetString**(GL\_EXTENSIONS).</span></span> <span data-ttu-id="61d52-134">Wenn der GL. Win-Swap-Hinweis zurückgegeben wird \_ \_ \_ , wird " **gladdswaphintrectwin** " unterstützt.</span><span class="sxs-lookup"><span data-stu-id="61d52-134">If it returns GL\_WIN\_swap\_hint, **glAddSwapHintRectWIN** is supported.</span></span> <span data-ttu-id="61d52-135">Rufen Sie zum Abrufen der Adresse einer Erweiterungs Funktion **wglgetprocaddress** auf.</span><span class="sxs-lookup"><span data-stu-id="61d52-135">To obtain the address of an extension function, call **wglGetProcAddress**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="61d52-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61d52-136">Requirements</span></span>



| <span data-ttu-id="61d52-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61d52-137">Requirement</span></span> | <span data-ttu-id="61d52-138">Wert</span><span class="sxs-lookup"><span data-stu-id="61d52-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="61d52-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61d52-139">Minimum supported client</span></span><br/> | <span data-ttu-id="61d52-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61d52-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="61d52-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61d52-141">Minimum supported server</span></span><br/> | <span data-ttu-id="61d52-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61d52-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="61d52-143">Header</span><span class="sxs-lookup"><span data-stu-id="61d52-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="61d52-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="61d52-144"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61d52-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61d52-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61d52-146">**glgetstring**</span><span class="sxs-lookup"><span data-stu-id="61d52-146">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="61d52-147">**Pixelformatdescriptor**</span><span class="sxs-lookup"><span data-stu-id="61d52-147">**PIXELFORMATDESCRIPTOR**</span></span>](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
</dt> <dt>

[<span data-ttu-id="61d52-148">**Austausch Puffer**</span><span class="sxs-lookup"><span data-stu-id="61d52-148">**SwapBuffers**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)
</dt> <dt>

[<span data-ttu-id="61d52-149">**wglgetprocaddress**</span><span class="sxs-lookup"><span data-stu-id="61d52-149">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





