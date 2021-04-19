---
title: ID2D1HwndRenderTarget Resize-Methoden (D2d1. h)
description: Ändert die Größe des Renderziels in die angegebene Pixelgröße.
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- Größenänderung von Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f15af87c59c943bd7d5dc8ece708d3603bddce6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370209"
---
# <a name="id2d1hwndrendertargetresize-methods"></a><span data-ttu-id="9f2d7-104">ID2D1HwndRenderTarget:: Resize-Methoden</span><span class="sxs-lookup"><span data-stu-id="9f2d7-104">ID2D1HwndRenderTarget::Resize methods</span></span>

<span data-ttu-id="9f2d7-105">Ändert die Größe des Renderziels in die angegebene Pixelgröße.</span><span class="sxs-lookup"><span data-stu-id="9f2d7-105">Changes the size of the render target to the specified pixel size.</span></span>

### <a name="overload-list"></a><span data-ttu-id="9f2d7-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="9f2d7-106">Overload list</span></span>



| <span data-ttu-id="9f2d7-107">Methode</span><span class="sxs-lookup"><span data-stu-id="9f2d7-107">Method</span></span>                                                                         | <span data-ttu-id="9f2d7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f2d7-108">Description</span></span>                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="9f2d7-109">[**Resize (D2D1 \_ size \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))</span><span class="sxs-lookup"><span data-stu-id="9f2d7-109">[**Resize(D2D1\_SIZE\_U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))</span></span>  | <span data-ttu-id="9f2d7-110">Ändert die Größe des Renderziels in die angegebene Pixelgröße.</span><span class="sxs-lookup"><span data-stu-id="9f2d7-110">Changes the size of the render target to the specified pixel size.</span></span> <br/> |
| <span data-ttu-id="9f2d7-111">[**Größe ändern (D2D1 \_ size \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u))</span><span class="sxs-lookup"><span data-stu-id="9f2d7-111">[**Resize(D2D1\_SIZE\_U\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u))</span></span> | <span data-ttu-id="9f2d7-112">Ändert die Größe des Renderziels in die angegebene Pixelgröße.</span><span class="sxs-lookup"><span data-stu-id="9f2d7-112">Changes the size of the render target to the specified pixel size.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="9f2d7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f2d7-113">Remarks</span></span>

<span data-ttu-id="9f2d7-114">Nachdem diese Methode aufgerufen wurde, wird der Inhalt des Back Puffers des Renderziels nicht definiert, auch wenn beim Erstellen des Renderziels die [**D2D1 Present options-Option " \_ \_ \_ \_ Inhalt beibehalten**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) " angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9f2d7-114">After this method is called, the contents of the render target's back-buffer are not defined, even if the [**D2D1\_PRESENT\_OPTIONS\_RETAIN\_CONTENTS**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) option was specified when the render target was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f2d7-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f2d7-115">Requirements</span></span>



| <span data-ttu-id="9f2d7-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f2d7-116">Requirement</span></span> | <span data-ttu-id="9f2d7-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9f2d7-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9f2d7-118">Header</span><span class="sxs-lookup"><span data-stu-id="9f2d7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9f2d7-119"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f2d7-119"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f2d7-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9f2d7-120">Library</span></span><br/> | <dl> <span data-ttu-id="9f2d7-121"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f2d7-121"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="9f2d7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9f2d7-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="9f2d7-123"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f2d7-123"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f2d7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f2d7-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="9f2d7-125">[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9f2d7-125">[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span></span>
</dt> </dl>

<span data-ttu-id="9f2d7-126">�</span><span class="sxs-lookup"><span data-stu-id="9f2d7-126">�</span></span>

<span data-ttu-id="9f2d7-127">�</span><span class="sxs-lookup"><span data-stu-id="9f2d7-127">�</span></span>
