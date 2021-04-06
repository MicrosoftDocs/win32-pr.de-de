---
title: Idcompositionvisual SetClip-Methoden (Dcomp. h)
description: Legt die Clip-Eigenschaft dieses visuellen Elements auf den angegebenen rechteckigen Bereich oder das angegebene Clip Objekt fest.
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
keywords:
- SetClip-Methoden directcomposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e421c916d305b95029bb6ffd8328346b4ea36918
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743409"
---
# <a name="idcompositionvisualsetclip-methods"></a><span data-ttu-id="de717-104">Idcompositionvisual:: SetClip-Methoden</span><span class="sxs-lookup"><span data-stu-id="de717-104">IDCompositionVisual::SetClip methods</span></span>

<span data-ttu-id="de717-105">Legt die Clip-Eigenschaft dieses visuellen Elements auf den angegebenen rechteckigen Bereich oder das angegebene Clip Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="de717-105">Sets the Clip property of this visual to the specified rectangular region or clip object.</span></span> <span data-ttu-id="de717-106">Die Clip-Eigenschaft schränkt das Rendering der visuellen Teilstruktur, die an diesem visuellen Element liegt, auf einen rechteckigen Bereich ein.</span><span class="sxs-lookup"><span data-stu-id="de717-106">The Clip property restricts the rendering of the visual subtree that is rooted at this visual to a rectangular region.</span></span>

### <a name="overload-list"></a><span data-ttu-id="de717-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="de717-107">Overload list</span></span>



| <span data-ttu-id="de717-108">Methode</span><span class="sxs-lookup"><span data-stu-id="de717-108">Method</span></span>                                                                                | <span data-ttu-id="de717-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de717-109">Description</span></span>                                                            |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span data-ttu-id="de717-110">[**SetClip (konstant D2D \_ Rect \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="de717-110">[**SetClip(const D2D\_RECT\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))</span></span> | <span data-ttu-id="de717-111">Legt die Clip-Eigenschaft auf den angegebenen rechteckigen Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="de717-111">Sets the Clip property to the specified rectangular region.</span></span><br/> |
| <span data-ttu-id="de717-112">[**SetClip (idcompositionclip \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip))</span><span class="sxs-lookup"><span data-stu-id="de717-112">[**SetClip(IDCompositionClip\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip))</span></span> | <span data-ttu-id="de717-113">Legt die Clip-Eigenschaft auf das angegebene Clip Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="de717-113">Sets the Clip property to the specified clip object.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="de717-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de717-114">Requirements</span></span>



| <span data-ttu-id="de717-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de717-115">Requirement</span></span> | <span data-ttu-id="de717-116">Wert</span><span class="sxs-lookup"><span data-stu-id="de717-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="de717-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de717-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de717-118">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de717-118">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="de717-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de717-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de717-120">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de717-120">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="de717-121">Header</span><span class="sxs-lookup"><span data-stu-id="de717-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="de717-122"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="de717-122"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="de717-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de717-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="de717-124"><dt>Dcomp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de717-124"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="de717-125">DLL</span><span class="sxs-lookup"><span data-stu-id="de717-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de717-126"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de717-126"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de717-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de717-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de717-128">Freistellen</span><span class="sxs-lookup"><span data-stu-id="de717-128">Clipping</span></span>](clipping.md)
</dt> <dt>

[<span data-ttu-id="de717-129">**Idcompositionvisual**</span><span class="sxs-lookup"><span data-stu-id="de717-129">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> </dl>

<span data-ttu-id="de717-130">�</span><span class="sxs-lookup"><span data-stu-id="de717-130">�</span></span>

<span data-ttu-id="de717-131">�</span><span class="sxs-lookup"><span data-stu-id="de717-131">�</span></span>
