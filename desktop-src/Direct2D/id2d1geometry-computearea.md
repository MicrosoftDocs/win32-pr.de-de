---
title: ID2D1Geometry computearea-Methoden
description: Berechnet den Bereich der Geometrie.
ms.assetid: 655f11bc-7435-4d23-b4b1-3d7c2110aa48
keywords:
- Computearea-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: f6b79e8434a2174bcb05659f6656a46cc2d43cbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358801"
---
# <a name="id2d1geometrycomputearea-methods"></a><span data-ttu-id="ea10b-104">ID2D1Geometry:: computearea-Methoden</span><span class="sxs-lookup"><span data-stu-id="ea10b-104">ID2D1Geometry::ComputeArea methods</span></span>

<span data-ttu-id="ea10b-105">Berechnet den Bereich der Geometrie.</span><span class="sxs-lookup"><span data-stu-id="ea10b-105">Computes the area of the geometry.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ea10b-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="ea10b-106">Overload list</span></span>



| <span data-ttu-id="ea10b-107">Methode</span><span class="sxs-lookup"><span data-stu-id="ea10b-107">Method</span></span>                                                                                                                      | <span data-ttu-id="ea10b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea10b-108">Description</span></span>                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea10b-109">[**Computearea (D2D1 \_ Matrix \_ 3x2 \_ F&, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))</span><span class="sxs-lookup"><span data-stu-id="ea10b-109">[**ComputeArea(D2D1\_MATRIX\_3X2\_F&,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))</span></span>              | <span data-ttu-id="ea10b-110">Berechnet den Bereich der Geometrie, nachdem er durch die angegebene Matrix transformiert und mit der Standardtoleranz vereinfacht wurde.</span><span class="sxs-lookup"><span data-stu-id="ea10b-110">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the default tolerance.</span></span><br/>    |
| <span data-ttu-id="ea10b-111">[**Computearea (D2D1 \_ Matrix \_ 3x2 \_ F \* , float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="ea10b-111">[**ComputeArea(D2D1\_MATRIX\_3X2\_F\*,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span></span>             | <span data-ttu-id="ea10b-112">Berechnet den Bereich der Geometrie, nachdem er durch die angegebene Matrix transformiert und mithilfe der Standardtoleranz vereinfacht wurde.</span><span class="sxs-lookup"><span data-stu-id="ea10b-112">Computes the area of the geometry after it has been transformed by the specified matrix and flattened by using the default tolerance.</span></span><br/> |
| <span data-ttu-id="ea10b-113">[**Computearea (D2D1 \_ Matrix \_ 3x2 \_ F&, float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))</span><span class="sxs-lookup"><span data-stu-id="ea10b-113">[**ComputeArea(D2D1\_MATRIX\_3X2\_F&,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))</span></span>  | <span data-ttu-id="ea10b-114">Berechnet den Bereich der Geometrie, nachdem er durch die angegebene Matrix transformiert und mithilfe der angegebenen Toleranz vereinfacht wurde.</span><span class="sxs-lookup"><span data-stu-id="ea10b-114">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/>  |
| <span data-ttu-id="ea10b-115">[**Computearea (D2D1 \_ Matrix \_ 3x2 \_ F \* , float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="ea10b-115">[**ComputeArea(D2D1\_MATRIX\_3X2\_F\*,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span></span> | <span data-ttu-id="ea10b-116">Berechnet den Bereich der Geometrie, nachdem er durch die angegebene Matrix transformiert und mithilfe der angegebenen Toleranz vereinfacht wurde.</span><span class="sxs-lookup"><span data-stu-id="ea10b-116">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="ea10b-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea10b-117">Examples</span></span>

<span data-ttu-id="ea10b-118">Im folgenden Codebeispiel wird **computearea** verwendet, um den Bereich eines angegebenen Kreises (**m \_ pCircleGeometry1**) zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="ea10b-118">The following code example uses **ComputeArea** to compute the area of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



## <a name="requirements"></a><span data-ttu-id="ea10b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea10b-119">Requirements</span></span>



| <span data-ttu-id="ea10b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea10b-120">Requirement</span></span> | <span data-ttu-id="ea10b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ea10b-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ea10b-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ea10b-122">Library</span></span><br/> | <dl> <span data-ttu-id="ea10b-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea10b-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="ea10b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ea10b-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="ea10b-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea10b-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea10b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea10b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea10b-127">**ID2D1Geometry**</span><span class="sxs-lookup"><span data-stu-id="ea10b-127">**ID2D1Geometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

