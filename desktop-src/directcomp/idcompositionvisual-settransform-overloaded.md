---
title: Idcompositionvisual setTransform-Methoden (Dcomp. h)
description: Legt die Transform-Eigenschaft dieses visuellen Elements fest. Die Transform-Eigenschaft gibt eine 2D-Transformation an, mit der das Koordinatensystem dieses visuellen Elements geändert wird. Die-Eigenschaft kann entweder eine 3-bis-2-Transformationsmatrix oder ein Transform-Objekt angeben.
ms.assetid: DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D
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
ms.openlocfilehash: 00f5da890cd22c5c827a36062a0b0c3f9bc19cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341167"
---
# <a name="idcompositionvisualsettransform-methods"></a><span data-ttu-id="17af8-106">Idcompositionvisual:: setTransform-Methoden</span><span class="sxs-lookup"><span data-stu-id="17af8-106">IDCompositionVisual::SetTransform methods</span></span>

<span data-ttu-id="17af8-107">Legt die Transform-Eigenschaft dieses visuellen Elements fest.</span><span class="sxs-lookup"><span data-stu-id="17af8-107">Sets the Transform property of this visual.</span></span> <span data-ttu-id="17af8-108">Die Transform-Eigenschaft gibt eine 2D-Transformation an, mit der das Koordinatensystem dieses visuellen Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="17af8-108">The Transform property specifies a 2D transform used to modify the coordinate system of this visual.</span></span> <span data-ttu-id="17af8-109">Die-Eigenschaft kann entweder eine 3-bis-2-Transformationsmatrix oder ein Transform-Objekt angeben.</span><span class="sxs-lookup"><span data-stu-id="17af8-109">The property can specify either a 3-by-2 transform matrix or a transform object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="17af8-110">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="17af8-110">Overload list</span></span>



| <span data-ttu-id="17af8-111">Methode</span><span class="sxs-lookup"><span data-stu-id="17af8-111">Method</span></span>                                                                                                    | <span data-ttu-id="17af8-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17af8-112">Description</span></span>                                                                    |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="17af8-113">[**SetTransform (D2D \_ Matrix \_ 3x2 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="17af8-113">[**SetTransform(D2D\_MATRIX\_3X2\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))</span></span>          | <span data-ttu-id="17af8-114">Legt die Transform-Eigenschaft auf die angegebene Transformationsmatrix fest.</span><span class="sxs-lookup"><span data-stu-id="17af8-114">Sets the Transform property to the specified transform matrix.</span></span><br/>      |
| <span data-ttu-id="17af8-115">[**SetTransform (idcompositiontransform \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform))</span><span class="sxs-lookup"><span data-stu-id="17af8-115">[**SetTransform(IDCompositionTransform\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform))</span></span> | <span data-ttu-id="17af8-116">Legt die Transform-Eigenschaft auf das angegebene Transformations Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="17af8-116">Sets the Transform property to the specified transformation object.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="17af8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17af8-117">Requirements</span></span>



| <span data-ttu-id="17af8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17af8-118">Requirement</span></span> | <span data-ttu-id="17af8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="17af8-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="17af8-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17af8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="17af8-121">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17af8-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="17af8-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17af8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="17af8-123">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17af8-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="17af8-124">Header</span><span class="sxs-lookup"><span data-stu-id="17af8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="17af8-125"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="17af8-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="17af8-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="17af8-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="17af8-127"><dt>Dcomp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17af8-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="17af8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="17af8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17af8-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17af8-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17af8-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17af8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17af8-131">**Idcompositionmatrixtransform**</span><span class="sxs-lookup"><span data-stu-id="17af8-131">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[<span data-ttu-id="17af8-132">**Idcompositionrotatetransform**</span><span class="sxs-lookup"><span data-stu-id="17af8-132">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[<span data-ttu-id="17af8-133">**Idcompositionscaletransform**</span><span class="sxs-lookup"><span data-stu-id="17af8-133">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="17af8-134">**Idcompositionschräwtransform**</span><span class="sxs-lookup"><span data-stu-id="17af8-134">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[<span data-ttu-id="17af8-135">**Idcompositiontransform**</span><span class="sxs-lookup"><span data-stu-id="17af8-135">**IDCompositionTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[<span data-ttu-id="17af8-136">**Idcompositiontranslatetransform**</span><span class="sxs-lookup"><span data-stu-id="17af8-136">**IDCompositionTranslateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[<span data-ttu-id="17af8-137">**Idcompositionvisual**</span><span class="sxs-lookup"><span data-stu-id="17af8-137">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[<span data-ttu-id="17af8-138">**Idcompositionvisual:: Seto ffsetx**</span><span class="sxs-lookup"><span data-stu-id="17af8-138">**IDCompositionVisual::SetOffsetX**</span></span>](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="17af8-139">**Idcompositionvisual:: Seto ffsety**</span><span class="sxs-lookup"><span data-stu-id="17af8-139">**IDCompositionVisual::SetOffsetY**</span></span>](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

<span data-ttu-id="17af8-140">�</span><span class="sxs-lookup"><span data-stu-id="17af8-140">�</span></span>

<span data-ttu-id="17af8-141">�</span><span class="sxs-lookup"><span data-stu-id="17af8-141">�</span></span>
