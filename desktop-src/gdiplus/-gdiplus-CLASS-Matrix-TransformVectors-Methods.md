---
description: In diesem Thema werden die TransformVectors-Methoden der Matrix Klasse aufgelistet. Eine umfassende Liste der Methoden für die Matrix Klasse finden Sie unter Matrix Methoden.
ms.assetid: 6a2ed6a7-825a-422b-b035-b88746f3ab5d
title: Matrix. TransformVectors-Methoden (gdiplus Matrix. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3bdb67d839163ffe2d26623a01fc186f8e885ca2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982900"
---
# <a name="matrixtransformvectors-methods"></a><span data-ttu-id="1b937-104">Matrix. TransformVectors-Methoden</span><span class="sxs-lookup"><span data-stu-id="1b937-104">Matrix.TransformVectors methods</span></span>

<span data-ttu-id="1b937-105">In diesem Thema werden die TransformVectors-Methoden der [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Klasse aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1b937-105">This topic lists the TransformVectors methods of the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="1b937-106">Eine umfassende Liste der Methoden für die **Matrix** Klasse finden Sie unter [Matrix Methoden](-gdiplus-class-matrix-methods.md).</span><span class="sxs-lookup"><span data-stu-id="1b937-106">For a complete list of methods for the **Matrix** class, see [Matrix Methods](-gdiplus-class-matrix-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="1b937-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="1b937-107">Overload list</span></span>



| <span data-ttu-id="1b937-108">Methode</span><span class="sxs-lookup"><span data-stu-id="1b937-108">Method</span></span>                                                                                                 | <span data-ttu-id="1b937-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b937-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b937-110">[**TransformVectors (Punkt \* , int)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="1b937-110">[**TransformVectors(Point\*,INT)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))</span></span>   | <span data-ttu-id="1b937-111">Die [**Matrix:: TransformVectors**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)) -Methode multipliziert jeden Vektor in einem Array mit dieser Matrix.</span><span class="sxs-lookup"><span data-stu-id="1b937-111">The [**Matrix::TransformVectors**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)) method multiplies each vector in an array by this matrix.</span></span> <span data-ttu-id="1b937-112">Die zu verschiebenden Elemente dieser Matrix (dritte Zeile) werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1b937-112">The translation elements of this matrix (third row) are ignored.</span></span> <span data-ttu-id="1b937-113">Jeder Vektor wird als Zeilen Matrix behandelt.</span><span class="sxs-lookup"><span data-stu-id="1b937-113">Each vector is treated as a row matrix.</span></span> <span data-ttu-id="1b937-114">Die Multiplikation wird mit der Zeilen Matrix auf der linken Seite und dieser Matrix auf der rechten Seite ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b937-114">The multiplication is performed with the row matrix on the left and this matrix on the right.</span></span><br/>  |
| <span data-ttu-id="1b937-115">[**TransformVectors (PointF \* , int)**](/previous-versions//ms535319(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1b937-115">[**TransformVectors(PointF\*,INT)**](/previous-versions//ms535319(v=vs.85))</span></span> | <span data-ttu-id="1b937-116">Die [**Matrix:: TransformVectors**](/previous-versions//ms535319(v=vs.85)) -Methode multipliziert jeden Vektor in einem Array mit dieser Matrix.</span><span class="sxs-lookup"><span data-stu-id="1b937-116">The [**Matrix::TransformVectors**](/previous-versions//ms535319(v=vs.85)) method multiplies each vector in an array by this matrix.</span></span> <span data-ttu-id="1b937-117">Die zu verschiebenden Elemente dieser Matrix (dritte Zeile) werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1b937-117">The translation elements of this matrix (third row) are ignored.</span></span> <span data-ttu-id="1b937-118">Jeder Vektor wird als Zeilen Matrix behandelt.</span><span class="sxs-lookup"><span data-stu-id="1b937-118">Each vector is treated as a row matrix.</span></span> <span data-ttu-id="1b937-119">Die Multiplikation wird mit der Zeilen Matrix auf der linken Seite und dieser Matrix auf der rechten Seite ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b937-119">The multiplication is performed with the row matrix on the left and this matrix on the right.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1b937-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1b937-120">Requirements</span></span>



| <span data-ttu-id="1b937-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b937-121">Requirement</span></span> | <span data-ttu-id="1b937-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1b937-122">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b937-123">Header</span><span class="sxs-lookup"><span data-stu-id="1b937-123">Header</span></span><br/> | <dl> <span data-ttu-id="1b937-124"><dt>Gdiplus Matrix. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b937-124"><dt>Gdiplusmatrix.h</dt></span></span> </dl> |



 

 
