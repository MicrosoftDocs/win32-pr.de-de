---
title: gluTessEndContour-Funktion (glu. h)
description: Die Funktionen "glutess begincontour" und "gluTessEndContour" begrenzen eine Kontur Beschreibung. | gluTessEndContour-Funktion (glu. h)
ms.assetid: 115db079-cbcb-48e1-8bab-0eb4814afb82
keywords:
- gluTessEndContour-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluTessEndContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac53f3920476489a1453bb6b5dc1e01d650d4fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352539"
---
# <a name="glutessendcontour-function"></a><span data-ttu-id="caba0-105">gluTessEndContour-Funktion</span><span class="sxs-lookup"><span data-stu-id="caba0-105">gluTessEndContour function</span></span>

<span data-ttu-id="caba0-106">Die Funktionen " [**glutess begincontour**](glutessbegincontour.md) " und " **gluTessEndContour** " begrenzen eine Kontur Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="caba0-106">The [**gluTessBeginContour**](glutessbegincontour.md) and **gluTessEndContour** functions delimit a contour description.</span></span>

## <a name="syntax"></a><span data-ttu-id="caba0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="caba0-107">Syntax</span></span>


```C++
void WINAPI gluTessEndContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="caba0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="caba0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caba0-109">*ATI*</span><span class="sxs-lookup"><span data-stu-id="caba0-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="caba0-110">Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="caba0-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caba0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="caba0-111">Return value</span></span>

<span data-ttu-id="caba0-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="caba0-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="caba0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="caba0-113">Remarks</span></span>

<span data-ttu-id="caba0-114">Die Funktionen " [**glutess begincontour**](glutessbegincontour.md) " und " **gluTessEndContour** " begrenzen die Definition einer Polygon-Kontur.</span><span class="sxs-lookup"><span data-stu-id="caba0-114">The [**gluTessBeginContour**](glutessbegincontour.md) and **gluTessEndContour** functions delimit the definition of a polygon contour.</span></span> <span data-ttu-id="caba0-115">Innerhalb jedes **glutessenbegincontour**-Paars " / **gluTessEndContour** " können NULL oder mehr Aufrufe an " [**glutess Vertex**](glutessvertex.md)" vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="caba0-115">Within each **gluTessBeginContour**/**gluTessEndContour** pair, there can be zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="caba0-116">Die Eckpunkte geben eine geschlossene Kontur an (der letzte Scheitelpunkt jeder Kontur wird automatisch mit dem ersten-Element verknüpft).</span><span class="sxs-lookup"><span data-stu-id="caba0-116">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span> <span data-ttu-id="caba0-117">Sie können " **glutess begincontour** " nur zwischen " [**glutess beginpolygon**](glutessbeginpolygon.md) " und " [**glutessendpolygon**](glutessendpolygon.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="caba0-117">You can call **gluTessBeginContour** only between [**gluTessBeginPolygon**](glutessbeginpolygon.md) and [**gluTessEndPolygon**](glutessendpolygon.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="caba0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="caba0-118">Requirements</span></span>



| <span data-ttu-id="caba0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="caba0-119">Requirement</span></span> | <span data-ttu-id="caba0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="caba0-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="caba0-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="caba0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="caba0-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="caba0-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="caba0-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="caba0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="caba0-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="caba0-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="caba0-125">Header</span><span class="sxs-lookup"><span data-stu-id="caba0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="caba0-126"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="caba0-126"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="caba0-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="caba0-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="caba0-128"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="caba0-128"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="caba0-129">DLL</span><span class="sxs-lookup"><span data-stu-id="caba0-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caba0-130"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caba0-130"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caba0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="caba0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caba0-132">**glunewtess**</span><span class="sxs-lookup"><span data-stu-id="caba0-132">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="caba0-133">**glutess beginpolygon**</span><span class="sxs-lookup"><span data-stu-id="caba0-133">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="caba0-134">*glutesscallback*</span><span class="sxs-lookup"><span data-stu-id="caba0-134">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="caba0-135">**glutessendpolygon**</span><span class="sxs-lookup"><span data-stu-id="caba0-135">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="caba0-136">**glutess normal**</span><span class="sxs-lookup"><span data-stu-id="caba0-136">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="caba0-137">**glutessproperty**</span><span class="sxs-lookup"><span data-stu-id="caba0-137">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="caba0-138">**glutess Vertex**</span><span class="sxs-lookup"><span data-stu-id="caba0-138">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





