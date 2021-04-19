---
title: IDCompositionVisual3 setTransform-Methoden (Dcomp. h)
description: Legt die Transform-Eigenschaft dieses visuellen Elements fest. Die Transform-Eigenschaft gibt eine 3D-Transformation an, mit der das Koordinatensystem dieses visuellen Elements geändert wird. Die-Eigenschaft kann entweder eine 4 x 4-Transformationsmatrix oder ein Transform-Objekt angeben.
ms.assetid: a59498c2-8659-dd35-8dc2-87457f493965
keywords:
- SetTransform-Methoden directcomposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 50237d4bbc8504a6bdcc9650f6c02dbdc30d093c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339985"
---
# <a name="idcompositionvisual3settransform-methods"></a><span data-ttu-id="d3c24-106">IDCompositionVisual3:: setTransform-Methoden</span><span class="sxs-lookup"><span data-stu-id="d3c24-106">IDCompositionVisual3::SetTransform methods</span></span>

<span data-ttu-id="d3c24-107">Legt die Transform-Eigenschaft dieses visuellen Elements fest.</span><span class="sxs-lookup"><span data-stu-id="d3c24-107">Sets the Transform property of this visual.</span></span> <span data-ttu-id="d3c24-108">Die Transform-Eigenschaft gibt eine 3D-Transformation an, mit der das Koordinatensystem dieses visuellen Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d3c24-108">The Transform property specifies a 3D transform used to modify the coordinate system of this visual.</span></span> <span data-ttu-id="d3c24-109">Die-Eigenschaft kann entweder eine 4 x 4-Transformationsmatrix oder ein Transform-Objekt angeben.</span><span class="sxs-lookup"><span data-stu-id="d3c24-109">The property can specify either a 4-by-4 transform matrix or a transform object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d3c24-110">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="d3c24-110">Overload list</span></span>



| <span data-ttu-id="d3c24-111">Methode</span><span class="sxs-lookup"><span data-stu-id="d3c24-111">Method</span></span>                                                                                  | <span data-ttu-id="d3c24-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3c24-112">Description</span></span>                                                                    |
|:----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="d3c24-113">[**SetTransform (D2D \_ Matrix \_ 4X4 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))</span><span class="sxs-lookup"><span data-stu-id="d3c24-113">[**SetTransform(D2D\_MATRIX\_4X4\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))</span></span>       | <span data-ttu-id="d3c24-114">Legt die Transform-Eigenschaft auf die angegebene Transformationsmatrix fest.</span><span class="sxs-lookup"><span data-stu-id="d3c24-114">Sets the Transform property to the specified transform matrix.</span></span><br/>      |
| <span data-ttu-id="d3c24-115">[**SetTransform (IDCompositionTransform3D \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d))</span><span class="sxs-lookup"><span data-stu-id="d3c24-115">[**SetTransform(IDCompositionTransform3D\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d))</span></span> | <span data-ttu-id="d3c24-116">Legt die Transform-Eigenschaft auf das angegebene Transformations Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="d3c24-116">Sets the Transform property to the specified transformation object.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d3c24-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3c24-117">Requirements</span></span>



| <span data-ttu-id="d3c24-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3c24-118">Requirement</span></span> | <span data-ttu-id="d3c24-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d3c24-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c24-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3c24-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c24-121">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3c24-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d3c24-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3c24-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c24-123">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3c24-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d3c24-124">Header</span><span class="sxs-lookup"><span data-stu-id="d3c24-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3c24-125"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3c24-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3c24-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d3c24-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="d3c24-127"><dt>Dcomp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3c24-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="d3c24-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d3c24-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3c24-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3c24-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3c24-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3c24-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c24-131">**IDCompositionVisual3**</span><span class="sxs-lookup"><span data-stu-id="d3c24-131">**IDCompositionVisual3**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual3)
</dt> <dt>

[<span data-ttu-id="d3c24-132">**Idcompositionmatrixtransform**</span><span class="sxs-lookup"><span data-stu-id="d3c24-132">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[<span data-ttu-id="d3c24-133">**Idcompositionrotatetransform**</span><span class="sxs-lookup"><span data-stu-id="d3c24-133">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[<span data-ttu-id="d3c24-134">**Idcompositionscaletransform**</span><span class="sxs-lookup"><span data-stu-id="d3c24-134">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="d3c24-135">**Idcompositionschräwtransform**</span><span class="sxs-lookup"><span data-stu-id="d3c24-135">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[<span data-ttu-id="d3c24-136">**Idcompositiontransform**</span><span class="sxs-lookup"><span data-stu-id="d3c24-136">**IDCompositionTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[<span data-ttu-id="d3c24-137">**Idcompositiontranslatetransform**</span><span class="sxs-lookup"><span data-stu-id="d3c24-137">**IDCompositionTranslateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[<span data-ttu-id="d3c24-138">**Idcompositionvisual**</span><span class="sxs-lookup"><span data-stu-id="d3c24-138">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[<span data-ttu-id="d3c24-139">**Idcompositionvisual:: Seto ffsetx**</span><span class="sxs-lookup"><span data-stu-id="d3c24-139">**IDCompositionVisual::SetOffsetX**</span></span>](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="d3c24-140">**Idcompositionvisual:: Seto ffsety**</span><span class="sxs-lookup"><span data-stu-id="d3c24-140">**IDCompositionVisual::SetOffsetY**</span></span>](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

<span data-ttu-id="d3c24-141">�</span><span class="sxs-lookup"><span data-stu-id="d3c24-141">�</span></span>

<span data-ttu-id="d3c24-142">�</span><span class="sxs-lookup"><span data-stu-id="d3c24-142">�</span></span>
