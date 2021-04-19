---
title: gledgeflag-Funktion (GL. h)
description: Markiert Kanten entweder als Begrenzung oder als nicht Grenze. | gledgeflag-Funktion (GL. h)
ms.assetid: cebaa4af-a3bc-4396-9ee0-8cc10bcaf256
keywords:
- gledgeflag-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlag
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 599a0b539e32d0e457f92c256e2cb0b678b05b59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106364318"
---
# <a name="gledgeflag-function"></a><span data-ttu-id="97d56-105">gledgeflag-Funktion</span><span class="sxs-lookup"><span data-stu-id="97d56-105">glEdgeFlag function</span></span>

<span data-ttu-id="97d56-106">Markiert Kanten entweder als Begrenzung oder als nicht Grenze.</span><span class="sxs-lookup"><span data-stu-id="97d56-106">Flags edges as either boundary or nonboundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="97d56-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="97d56-107">Syntax</span></span>


```C++
void WINAPI glEdgeFlag(
   GLboolean flag
);
```



## <a name="parameters"></a><span data-ttu-id="97d56-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="97d56-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97d56-109">*flag*</span><span class="sxs-lookup"><span data-stu-id="97d56-109">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="97d56-110">Gibt den aktuellen Edge-Flag-Wert an, entweder **true** oder **false**.</span><span class="sxs-lookup"><span data-stu-id="97d56-110">Specifies the current edge flag value, either **TRUE** or **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97d56-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97d56-111">Return value</span></span>

<span data-ttu-id="97d56-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="97d56-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="97d56-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97d56-113">Remarks</span></span>

<span data-ttu-id="97d56-114">Jeder Scheitelpunkt eines Polygon, eines separaten Dreiecks oder eines separaten vierends, das zwischen einem [**glBegin**](/windows/desktop/OpenGL/glbegin)- / [**glEnd**](/windows/desktop/OpenGL/glend) -Paar angegeben ist, wird als Start einer Grenze oder einer nicht-Begrenzungs Kante gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="97d56-114">Each vertex of a polygon, separate triangle, or separate quadrilateral specified between a [**glBegin**](/windows/desktop/OpenGL/glbegin)/[**glEnd**](/windows/desktop/OpenGL/glend) pair is marked as the start of either a boundary or nonboundary edge.</span></span> <span data-ttu-id="97d56-115">Wenn das aktuelle Edge-Flag **true** ist, wenn der Scheitelpunkt angegeben ist, wird der Scheitelpunkt als Anfang eines Begrenzungs Rands markiert.</span><span class="sxs-lookup"><span data-stu-id="97d56-115">If the current edge flag is **TRUE** when the vertex is specified, the vertex is marked as the start of a boundary edge.</span></span> <span data-ttu-id="97d56-116">Wenn das aktuelle Edge-Flag den Wert **false** hat, wird der Scheitelpunkt als Anfang eines nicht Begrenzungs Randes markiert.</span><span class="sxs-lookup"><span data-stu-id="97d56-116">If the current edge flag is **FALSE**, the vertex is marked as the start of a nonboundary edge.</span></span> <span data-ttu-id="97d56-117">Die Funktion **gledgeflag** legt das edgeflag auf **true** fest, wenn Flag ungleich 0 (null) ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="97d56-117">The **glEdgeFlag** function sets the edge flag to **TRUE** if flag is nonzero, **FALSE** otherwise.</span></span>

<span data-ttu-id="97d56-118">Die Scheitel Punkte verbundener Dreiecke und verbundener Vierecke werden immer als Grenze gekennzeichnet, unabhängig vom Wert des Edge-Flags.</span><span class="sxs-lookup"><span data-stu-id="97d56-118">The vertices of connected triangles and connected quadrilaterals are always marked as boundary, regardless of the value of the edge flag.</span></span>

<span data-ttu-id="97d56-119">Border-und nonborder-edgeflags für Scheitel Punkte sind nur dann von Bedeutung, wenn der GL- \_ Polygon \_ Modus auf GL \_ Point oder GL Line festgelegt ist \_</span><span class="sxs-lookup"><span data-stu-id="97d56-119">Boundary and nonboundary edge flags on vertices are significant only if GL\_POLYGON\_MODE is set to GL\_POINT or GL\_LINE.</span></span> <span data-ttu-id="97d56-120">Siehe [**glpolygonmode**](/windows/desktop/OpenGL/glpolygonmode).</span><span class="sxs-lookup"><span data-stu-id="97d56-120">See [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span></span>

<span data-ttu-id="97d56-121">Anfänglich ist das Edge-Flag " **true**".</span><span class="sxs-lookup"><span data-stu-id="97d56-121">Initially, the edge flag bit is **TRUE**.</span></span>

<span data-ttu-id="97d56-122">Das aktuelle Edge-Flag kann jederzeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="97d56-122">The current edge flag can be updated at any time.</span></span> <span data-ttu-id="97d56-123">Insbesondere kann **gledgeflag** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd**](/windows/desktop/OpenGL/glend)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="97d56-123">In particular, **glEdgeFlag** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](/windows/desktop/OpenGL/glend).</span></span>

<span data-ttu-id="97d56-124">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **gledgeflag** ab:</span><span class="sxs-lookup"><span data-stu-id="97d56-124">The following functions retrieve information related to **glEdgeFlag**:</span></span>

<span data-ttu-id="97d56-125">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ Edge- \_ Flag</span><span class="sxs-lookup"><span data-stu-id="97d56-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG</span></span>

## <a name="requirements"></a><span data-ttu-id="97d56-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97d56-126">Requirements</span></span>



| <span data-ttu-id="97d56-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97d56-127">Requirement</span></span> | <span data-ttu-id="97d56-128">Wert</span><span class="sxs-lookup"><span data-stu-id="97d56-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97d56-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97d56-129">Minimum supported client</span></span><br/> | <span data-ttu-id="97d56-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97d56-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="97d56-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97d56-131">Minimum supported server</span></span><br/> | <span data-ttu-id="97d56-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97d56-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="97d56-133">Header</span><span class="sxs-lookup"><span data-stu-id="97d56-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="97d56-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="97d56-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="97d56-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="97d56-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="97d56-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97d56-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="97d56-137">DLL</span><span class="sxs-lookup"><span data-stu-id="97d56-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97d56-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97d56-138"><dt>Opengl32.dll</dt></span></span> </dl> |



 

