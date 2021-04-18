---
title: ID2D1Geometry computelength-Methoden
description: Berechnet die Länge der Geometrie, als wäre jedes Segment in eine Zeile entrollt worden.
ms.assetid: 4659d880-0aa3-485d-ac71-044d9ace6759
keywords:
- Computelength-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: b49b1beb0525d95967ad903b0f0fb3c464edf4d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365412"
---
# <a name="id2d1geometrycomputelength-methods"></a><span data-ttu-id="0b051-104">ID2D1Geometry:: computelength-Methoden</span><span class="sxs-lookup"><span data-stu-id="0b051-104">ID2D1Geometry::ComputeLength methods</span></span>

<span data-ttu-id="0b051-105">Berechnet die Länge der Geometrie, als wäre jedes Segment in eine Zeile entrollt worden.</span><span class="sxs-lookup"><span data-stu-id="0b051-105">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span>

### <a name="overload-list"></a><span data-ttu-id="0b051-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="0b051-106">Overload list</span></span>



| <span data-ttu-id="0b051-107">Methode</span><span class="sxs-lookup"><span data-stu-id="0b051-107">Method</span></span>                                                                                                                          | <span data-ttu-id="0b051-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b051-108">Description</span></span>                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b051-109">[**Computelength (D2D1 \_ Matrix \_ 3x2 \_ F&, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="0b051-109">[**ComputeLength(D2D1\_MATRIX\_3X2\_F&,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span></span>              | <span data-ttu-id="0b051-110">Berechnet die Länge der Geometrie, als wäre jedes Segment in eine Zeile entrollt worden.</span><span class="sxs-lookup"><span data-stu-id="0b051-110">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span><br/>  |
| <span data-ttu-id="0b051-111">[**Computelength (D2D1 \_ Matrix \_ 3x2 \_ F \* , float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="0b051-111">[**ComputeLength(D2D1\_MATRIX\_3X2\_F\*,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span></span>             | <span data-ttu-id="0b051-112">Berechnet die Länge der Geometrie, als wäre jedes Segment in eine Zeile entrollt worden.</span><span class="sxs-lookup"><span data-stu-id="0b051-112">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span><br/>  |
| <span data-ttu-id="0b051-113">[**Computelength (D2D1 \_ Matrix \_ 3x2 \_ F&, float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f__float_float))</span><span class="sxs-lookup"><span data-stu-id="0b051-113">[**ComputeLength(D2D1\_MATRIX\_3X2\_F&,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f__float_float))</span></span>  | <span data-ttu-id="0b051-114">Berechnet die Länge der Geometrie, als wäre jedes Segment in eine Zeile entrollt worden.</span><span class="sxs-lookup"><span data-stu-id="0b051-114">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span><br/>  |
| <span data-ttu-id="0b051-115">[**Computelength (D2D1 \_ Matrix \_ 3x2 \_ F \* , float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="0b051-115">[**ComputeLength(D2D1\_MATRIX\_3X2\_F\*,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span></span> | <span data-ttu-id="0b051-116">Berechnet die Länge der Geometrie, als wäre jedes Segment in eine Zeile entrollt worden.</span><span class="sxs-lookup"><span data-stu-id="0b051-116">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="0b051-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b051-117">Examples</span></span>

<span data-ttu-id="0b051-118">Der folgende Code zeigt, wie Sie mit **computelength** die Länge einer angegebenen Pfad Geometrie berechnen können.</span><span class="sxs-lookup"><span data-stu-id="0b051-118">The following code shows how to use **ComputeLength** to compute the length of a specified path geometry.</span></span>


```C++
float length = 0;
hr = m_pPathGeometry->ComputeLength(
    NULL, //no transform
    &length
    );

if (SUCCEEDED(hr))
{
    m_Animation.SetStart(0);        //start at beginning of path
    m_Animation.SetEnd(length);     //length at end of path
    m_Animation.SetDuration(5.0f);  //seconds

    ZeroMemory(&m_DwmTimingInfo, sizeof(m_DwmTimingInfo));
    m_DwmTimingInfo.cbSize = sizeof(m_DwmTimingInfo);

    // Get the composition refresh rate. If the DWM isn't running,
    // get the refresh rate from GDI -- probably going to be 60Hz
    if (FAILED(DwmGetCompositionTimingInfo(NULL, &m_DwmTimingInfo)))
    {
        HDC hdc = GetDC(m_hwnd);
        m_DwmTimingInfo.rateCompose.uiDenominator = 1;
        m_DwmTimingInfo.rateCompose.uiNumerator = GetDeviceCaps(hdc, VREFRESH);
        ReleaseDC(m_hwnd, hdc);
    }

    ShowWindow(m_hwnd, SW_SHOWNORMAL);

    UpdateWindow(m_hwnd);
}
```



## <a name="requirements"></a><span data-ttu-id="0b051-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b051-119">Requirements</span></span>



| <span data-ttu-id="0b051-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b051-120">Requirement</span></span> | <span data-ttu-id="0b051-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0b051-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0b051-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0b051-122">Library</span></span><br/> | <dl> <span data-ttu-id="0b051-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b051-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="0b051-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0b051-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="0b051-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b051-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b051-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b051-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b051-127">**ID2D1Geometry**</span><span class="sxs-lookup"><span data-stu-id="0b051-127">**ID2D1Geometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

