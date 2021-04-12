---
title: glutess Vertex-Funktion (glu. h)
description: Die Funktion "glutess Vertex" gibt einen Scheitelpunkt auf einem Polygon an.
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- glutess Vertex-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluTessVertex
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546bbad2be1205f62c7889fbb18f23d5b0e38b8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518857"
---
# <a name="glutessvertex-function"></a><span data-ttu-id="bd99e-104">glutess Vertex-Funktion</span><span class="sxs-lookup"><span data-stu-id="bd99e-104">gluTessVertex function</span></span>

<span data-ttu-id="bd99e-105">Die Funktion " **glutess Vertex** " gibt einen Scheitelpunkt auf einem Polygon an.</span><span class="sxs-lookup"><span data-stu-id="bd99e-105">The **gluTessVertex** function specifies a vertex on a polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd99e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd99e-106">Syntax</span></span>


```C++
void WINAPI gluTessVertex(
   GLUtesselator *tess,
   GLdouble      coords[3],
   void          *data
);
```



## <a name="parameters"></a><span data-ttu-id="bd99e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd99e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd99e-108">*ATI*</span><span class="sxs-lookup"><span data-stu-id="bd99e-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="bd99e-109">Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="bd99e-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="bd99e-110">*CoOrds*</span><span class="sxs-lookup"><span data-stu-id="bd99e-110">*coords*</span></span> 
</dt> <dd>

<span data-ttu-id="bd99e-111">Der Speicherort des Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="bd99e-111">The location of the vertex.</span></span>

</dd> <dt>

<span data-ttu-id="bd99e-112">*data*</span><span class="sxs-lookup"><span data-stu-id="bd99e-112">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="bd99e-113">Ein Zeiger, der mit dem Vertex-Rückruf an das Programm zurückgegeben wurde (wie von " [*glutesscallback*](glutess.md)" angegeben).</span><span class="sxs-lookup"><span data-stu-id="bd99e-113">An pointer passed back to the program with the vertex callback (as specified by [*gluTessCallback*](glutess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd99e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd99e-114">Return value</span></span>

<span data-ttu-id="bd99e-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bd99e-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd99e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd99e-116">Remarks</span></span>

<span data-ttu-id="bd99e-117">Die Funktion " **glutess Vertex** " beschreibt einen Scheitelpunkt auf einem Polygon, den der Benutzer definiert.</span><span class="sxs-lookup"><span data-stu-id="bd99e-117">The **gluTessVertex** function describes a vertex on a polygon that the user is defining.</span></span> <span data-ttu-id="bd99e-118">Aufeinander folgende " **glutess Vertex** "-Aufrufe beschreiben eine geschlossene Kontur.</span><span class="sxs-lookup"><span data-stu-id="bd99e-118">Successive **gluTessVertex** calls describe a closed contour.</span></span> <span data-ttu-id="bd99e-119">Um z. b. einen vierfachen zu beschreiben, nennen Sie " **glutess Vertex** " viermal.</span><span class="sxs-lookup"><span data-stu-id="bd99e-119">For example, to describe a quadrilateral, call **gluTessVertex** four times.</span></span> <span data-ttu-id="bd99e-120">Sie können " **glutess Vertex** " nur zwischen " [**glutess begincontour**](glutessbegincontour.md) " und " [**gluTessEndContour**](glutessendcontour.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bd99e-120">You can only call **gluTessVertex** between [**gluTessBeginContour**](glutessbegincontour.md) and [**gluTessEndContour**](glutessendcontour.md).</span></span>

<span data-ttu-id="bd99e-121">Der *Data* -Parameter zeigt normalerweise auf eine-Struktur, die den Scheitelpunkt Speicherort enthält, sowie auf andere pro-Vertex-Attribute wie Farbe und normal.</span><span class="sxs-lookup"><span data-stu-id="bd99e-121">The *data* parameter normally points to a structure containing the vertex location, as well as other per-vertex attributes such as color and normal.</span></span> <span data-ttu-id="bd99e-122">Dieser Zeiger wird nach dem Mosaik Prozess über den glu-Vertex-Rückruf an das Programm zurückgegeben \_ (siehe [*glutesscallback*](glutess.md)).</span><span class="sxs-lookup"><span data-stu-id="bd99e-122">This pointer is passed back to the program through the GLU\_VERTEX callback after tessellation (see [*gluTessCallback*](glutess.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd99e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd99e-123">Requirements</span></span>



| <span data-ttu-id="bd99e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd99e-124">Requirement</span></span> | <span data-ttu-id="bd99e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="bd99e-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bd99e-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd99e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bd99e-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd99e-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bd99e-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd99e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bd99e-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd99e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bd99e-130">Header</span><span class="sxs-lookup"><span data-stu-id="bd99e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd99e-131"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd99e-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="bd99e-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bd99e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="bd99e-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd99e-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bd99e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bd99e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd99e-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd99e-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd99e-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd99e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd99e-137">**glunewtess**</span><span class="sxs-lookup"><span data-stu-id="bd99e-137">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="bd99e-138">**glutess begincontour**</span><span class="sxs-lookup"><span data-stu-id="bd99e-138">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="bd99e-139">**glutess beginpolygon**</span><span class="sxs-lookup"><span data-stu-id="bd99e-139">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="bd99e-140">*glutesscallback*</span><span class="sxs-lookup"><span data-stu-id="bd99e-140">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="bd99e-141">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="bd99e-141">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="bd99e-142">**glutess normal**</span><span class="sxs-lookup"><span data-stu-id="bd99e-142">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="bd99e-143">**glutessproperty**</span><span class="sxs-lookup"><span data-stu-id="bd99e-143">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> </dl>

 

 





