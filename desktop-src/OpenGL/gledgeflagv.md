---
title: gledgeflagv-Funktion (GL. h)
description: Markiert Kanten entweder als Begrenzung oder als nicht Grenze. | gledgeflagv-Funktion (GL. h)
ms.assetid: 69b5ddbd-7c0c-47f0-a358-d8bf81755c88
keywords:
- gledgeflagv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe031ab3981e3daa2e6b1aefd51c9eaa62c84483
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353169"
---
# <a name="gledgeflagv-function"></a><span data-ttu-id="a3cef-105">gledgeflagv-Funktion</span><span class="sxs-lookup"><span data-stu-id="a3cef-105">glEdgeFlagv function</span></span>

<span data-ttu-id="a3cef-106">Markiert Kanten entweder als Begrenzung oder als nicht Grenze.</span><span class="sxs-lookup"><span data-stu-id="a3cef-106">Flags edges as either boundary or nonboundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3cef-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3cef-107">Syntax</span></span>


```C++
void WINAPI glEdgeFlagv(
   const GLboolean *flag
);
```



## <a name="parameters"></a><span data-ttu-id="a3cef-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3cef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3cef-109">*flag*</span><span class="sxs-lookup"><span data-stu-id="a3cef-109">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="a3cef-110">Gibt einen Zeiger auf ein Array an, das ein einzelnes boolesches Element enthält, das den aktuellen Edge-Flag-Wert ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a3cef-110">Specifies a pointer to an array that contains a single Boolean element, which replaces the current edge flag value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3cef-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3cef-111">Return value</span></span>

<span data-ttu-id="a3cef-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a3cef-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3cef-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3cef-113">Remarks</span></span>

<span data-ttu-id="a3cef-114">Jeder Scheitelpunkt eines Polygon, eines separaten Dreiecks oder eines separaten vierends, das zwischen einem [**glBegin**](/windows/desktop/OpenGL/glbegin)- / [**glEnd**](/windows/desktop/OpenGL/glend) -Paar angegeben ist, wird als Start einer Grenze oder einer nicht-Begrenzungs Kante gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a3cef-114">Each vertex of a polygon, separate triangle, or separate quadrilateral specified between a [**glBegin**](/windows/desktop/OpenGL/glbegin)/[**glEnd**](/windows/desktop/OpenGL/glend) pair is marked as the start of either a boundary or nonboundary edge.</span></span> <span data-ttu-id="a3cef-115">Wenn das aktuelle Edge-Flag **true** ist, wenn der Scheitelpunkt angegeben ist, wird der Scheitelpunkt als Anfang eines Begrenzungs Rands markiert.</span><span class="sxs-lookup"><span data-stu-id="a3cef-115">If the current edge flag is **TRUE** when the vertex is specified, the vertex is marked as the start of a boundary edge.</span></span> <span data-ttu-id="a3cef-116">Wenn das aktuelle Edge-Flag den Wert **false** hat, wird der Scheitelpunkt als Anfang eines nicht Begrenzungs Randes markiert.</span><span class="sxs-lookup"><span data-stu-id="a3cef-116">If the current edge flag is **FALSE**, the vertex is marked as the start of a nonboundary edge.</span></span> <span data-ttu-id="a3cef-117">Die Funktion **gledgeflagv** legt das edgeflag auf **true** fest, wenn das Flag ungleich 0 (null) ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="a3cef-117">The **glEdgeFlagv** function sets the edge flag to **TRUE** if flag is nonzero, **FALSE** otherwise.</span></span>

<span data-ttu-id="a3cef-118">Die Scheitel Punkte verbundener Dreiecke und verbundener Vierecke werden immer als Grenze gekennzeichnet, unabhängig vom Wert des Edge-Flags.</span><span class="sxs-lookup"><span data-stu-id="a3cef-118">The vertices of connected triangles and connected quadrilaterals are always marked as boundary, regardless of the value of the edge flag.</span></span>

<span data-ttu-id="a3cef-119">Border-und nonborder-edgeflags für Scheitel Punkte sind nur dann von Bedeutung, wenn der GL- \_ Polygon \_ Modus auf GL \_ Point oder GL Line festgelegt ist \_</span><span class="sxs-lookup"><span data-stu-id="a3cef-119">Boundary and nonboundary edge flags on vertices are significant only if GL\_POLYGON\_MODE is set to GL\_POINT or GL\_LINE.</span></span> <span data-ttu-id="a3cef-120">Siehe [**glpolygonmode**](/windows/desktop/OpenGL/glpolygonmode).</span><span class="sxs-lookup"><span data-stu-id="a3cef-120">See [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span></span>

<span data-ttu-id="a3cef-121">Anfänglich ist das Edge-Flag " **true**".</span><span class="sxs-lookup"><span data-stu-id="a3cef-121">Initially, the edge flag bit is **TRUE**.</span></span>

<span data-ttu-id="a3cef-122">Das aktuelle Edge-Flag kann jederzeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a3cef-122">The current edge flag can be updated at any time.</span></span> <span data-ttu-id="a3cef-123">Insbesondere kann **gledgeflagv** zwischen einem Aufruf von [**glBegin**](/windows/desktop/OpenGL/glbegin) und dem entsprechenden Aufruf von [**glEnd**](/windows/desktop/OpenGL/glend)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a3cef-123">In particular, **glEdgeFlagv** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](/windows/desktop/OpenGL/glend).</span></span>

<span data-ttu-id="a3cef-124">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **gledgeflagv** ab:</span><span class="sxs-lookup"><span data-stu-id="a3cef-124">The following functions retrieve information related to **glEdgeFlagv**:</span></span>

<span data-ttu-id="a3cef-125">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ Edge- \_ Flag</span><span class="sxs-lookup"><span data-stu-id="a3cef-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG</span></span>

## <a name="requirements"></a><span data-ttu-id="a3cef-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3cef-126">Requirements</span></span>



| <span data-ttu-id="a3cef-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3cef-127">Requirement</span></span> | <span data-ttu-id="a3cef-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a3cef-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3cef-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3cef-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a3cef-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3cef-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a3cef-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3cef-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a3cef-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3cef-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a3cef-133">Header</span><span class="sxs-lookup"><span data-stu-id="a3cef-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3cef-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3cef-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a3cef-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a3cef-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3cef-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3cef-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a3cef-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a3cef-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3cef-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3cef-138"><dt>Opengl32.dll</dt></span></span> </dl> |



 

