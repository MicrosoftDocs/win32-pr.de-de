---
description: Beschreibt den aktuellen Clip Status.
ms.assetid: 3ea8631c-a967-4d24-a49a-1751b3ee6077
title: D3DCLIPSTATUS9-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPSTATUS9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3b22fdfcc136c05ec8fe03ae491612606b2df62f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370416"
---
# <a name="d3dclipstatus9-structure"></a><span data-ttu-id="775c1-103">D3DCLIPSTATUS9-Struktur</span><span class="sxs-lookup"><span data-stu-id="775c1-103">D3DCLIPSTATUS9 structure</span></span>

<span data-ttu-id="775c1-104">Beschreibt den aktuellen Clip Status.</span><span class="sxs-lookup"><span data-stu-id="775c1-104">Describes the current clip status.</span></span>

## <a name="syntax"></a><span data-ttu-id="775c1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="775c1-105">Syntax</span></span>


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a><span data-ttu-id="775c1-106">Member</span><span class="sxs-lookup"><span data-stu-id="775c1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="775c1-107">**ClipUnion**</span><span class="sxs-lookup"><span data-stu-id="775c1-107">**ClipUnion**</span></span>
</dt> <dd>

<span data-ttu-id="775c1-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="775c1-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="775c1-109">Clip-Union-Flags, die den aktuellen Clip Status beschreiben.</span><span class="sxs-lookup"><span data-stu-id="775c1-109">Clip union flags that describe the current clip status.</span></span> <span data-ttu-id="775c1-110">Dieser Member kann eines oder mehrere der folgenden Flags sein:</span><span class="sxs-lookup"><span data-stu-id="775c1-110">This member can be one or more of the following flags:</span></span>



| <span data-ttu-id="775c1-111">Wert</span><span class="sxs-lookup"><span data-stu-id="775c1-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="775c1-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="775c1-112">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <span data-ttu-id="775c1-113"><dt>**D3DCS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="775c1-113"><dt>**D3DCS\_ALL**</dt></span></span> </dl>          | <span data-ttu-id="775c1-114">Kombination aller Clip-Flags.</span><span class="sxs-lookup"><span data-stu-id="775c1-114">Combination of all clip flags.</span></span><br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <span data-ttu-id="775c1-115"><dt>**D3DCS \_ Links**</dt></span><span class="sxs-lookup"><span data-stu-id="775c1-115"><dt>**D3DCS\_LEFT**</dt></span></span> </dl>       | <span data-ttu-id="775c1-116">Alle Scheitel Punkte werden von der linken Ebene der Anzeige-Frustum abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="775c1-116">All vertices are clipped by the left plane of the viewing frustum.</span></span><br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <span data-ttu-id="775c1-117"><dt>**D3DCS \_ Rechts**</dt></span><span class="sxs-lookup"><span data-stu-id="775c1-117"><dt>**D3DCS\_RIGHT**</dt></span></span> </dl>    | <span data-ttu-id="775c1-118">Alle Scheitel Punkte werden von der rechten Ebene der Anzeige Frust Fläche abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="775c1-118">All vertices are clipped by the right plane of the viewing frustum.</span></span><br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <span data-ttu-id="775c1-119"><dt>**D3DCS \_ oben**</dt></span><span class="sxs-lookup"><span data-stu-id="775c1-119"><dt>**D3DCS\_TOP**</dt></span></span> </dl>          | <span data-ttu-id="775c1-120">Alle Scheitel Punkte werden von der obersten Ebene der Anzeige "Frustum" abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="775c1-120">All vertices are clipped by the top plane of the viewing frustum.</span></span><br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <span data-ttu-id="775c1-121"><dt>**D3DCS \_ unten**</dt></span><span class="sxs-lookup"><span data-stu-id="775c1-121"><dt>**D3DCS\_BOTTOM**</dt></span></span> </dl> | <span data-ttu-id="775c1-122">Alle Scheitel Punkte werden von der untersten Ebene der Anzeige-Frustum abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="775c1-122">All vertices are clipped by the bottom plane of the viewing frustum.</span></span><br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <span data-ttu-id="775c1-123"><dt>**D3DCS- \_ Front**</dt></span><span class="sxs-lookup"><span data-stu-id="775c1-123"><dt>**D3DCS\_FRONT**</dt></span></span> </dl>    | <span data-ttu-id="775c1-124">Alle Vertices werden von der Vorderseite der Anzeige Frust Fläche abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="775c1-124">All vertices are clipped by the front plane of the viewing frustum.</span></span><br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <span data-ttu-id="775c1-125"><dt>**D3DCS \_ zurück**</dt></span><span class="sxs-lookup"><span data-stu-id="775c1-125"><dt>**D3DCS\_BACK**</dt></span></span> </dl>       | <span data-ttu-id="775c1-126">Alle Scheitel Punkte werden von der Rückseite der Anzeige Frust Fläche abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="775c1-126">All vertices are clipped by the back plane of the viewing frustum.</span></span><br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <span data-ttu-id="775c1-127"><dt>**D3DCS \_ PLANE0**</dt></span><span class="sxs-lookup"><span data-stu-id="775c1-127"><dt>**D3DCS\_PLANE0**</dt></span></span> </dl> | <span data-ttu-id="775c1-128">Anwendungs definierte Clippingebenen.</span><span class="sxs-lookup"><span data-stu-id="775c1-128">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <span data-ttu-id="775c1-129"><dt>**D3DCS \_ PLANE1**</dt></span><span class="sxs-lookup"><span data-stu-id="775c1-129"><dt>**D3DCS\_PLANE1**</dt></span></span> </dl> | <span data-ttu-id="775c1-130">Anwendungs definierte Clippingebenen.</span><span class="sxs-lookup"><span data-stu-id="775c1-130">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <span data-ttu-id="775c1-131"><dt>**D3DCS \_ PLANE2**</dt></span><span class="sxs-lookup"><span data-stu-id="775c1-131"><dt>**D3DCS\_PLANE2**</dt></span></span> </dl> | <span data-ttu-id="775c1-132">Anwendungs definierte Clippingebenen.</span><span class="sxs-lookup"><span data-stu-id="775c1-132">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <span data-ttu-id="775c1-133"><dt>**D3DCS \_ PLANE3**</dt></span><span class="sxs-lookup"><span data-stu-id="775c1-133"><dt>**D3DCS\_PLANE3**</dt></span></span> </dl> | <span data-ttu-id="775c1-134">Anwendungs definierte Clippingebenen.</span><span class="sxs-lookup"><span data-stu-id="775c1-134">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <span data-ttu-id="775c1-135"><dt>**D3DCS \_ PLANE4**</dt></span><span class="sxs-lookup"><span data-stu-id="775c1-135"><dt>**D3DCS\_PLANE4**</dt></span></span> </dl> | <span data-ttu-id="775c1-136">Anwendungs definierte Clippingebenen.</span><span class="sxs-lookup"><span data-stu-id="775c1-136">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <span data-ttu-id="775c1-137"><dt>**D3DCS \_ PLANE5**</dt></span><span class="sxs-lookup"><span data-stu-id="775c1-137"><dt>**D3DCS\_PLANE5**</dt></span></span> </dl> | <span data-ttu-id="775c1-138">Anwendungs definierte Clippingebenen.</span><span class="sxs-lookup"><span data-stu-id="775c1-138">Application-defined clipping planes.</span></span><br/>                                 |



 

</dd> <dt>

<span data-ttu-id="775c1-139">**Clipschnittmenge**</span><span class="sxs-lookup"><span data-stu-id="775c1-139">**ClipIntersection**</span></span>
</dt> <dd>

<span data-ttu-id="775c1-140">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="775c1-140">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="775c1-141">Clip schnittstellerflags, die den aktuellen Clip Status beschreiben.</span><span class="sxs-lookup"><span data-stu-id="775c1-141">Clip intersection flags that describe the current clip status.</span></span> <span data-ttu-id="775c1-142">Dieser Member kann die gleichen Flags wie ClipUnion annehmen.</span><span class="sxs-lookup"><span data-stu-id="775c1-142">This member can take the same flags as ClipUnion.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="775c1-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="775c1-143">Remarks</span></span>

<span data-ttu-id="775c1-144">Wenn das Clipping während der Scheitelpunkt Verarbeitung (von [**ProcessVertices**](/windows/desktop/api), [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)oder anderen Zeichnungsfunktionen) aktiviert ist, berechnet Direct3D einen Clip Code für jeden Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="775c1-144">When clipping is enabled during vertex processing (by [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), or other drawing functions), Direct3D computes a clip code for every vertex.</span></span> <span data-ttu-id="775c1-145">Der Clip Code ist eine Kombination aus D3DCS \_ \* Bits.</span><span class="sxs-lookup"><span data-stu-id="775c1-145">The clip code is a combination of D3DCS\_\* bits.</span></span> <span data-ttu-id="775c1-146">Wenn ein Scheitelpunkt außerhalb einer bestimmten Clippingebene liegt, wird das entsprechende Bit im Clippingcode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="775c1-146">When a vertex is outside a particular clipping plane, the corresponding bit is set in the clipping code.</span></span> <span data-ttu-id="775c1-147">Direct3D verwaltet den Clip Status mithilfe von **D3DCLIPSTATUS9**, der über ClipUnion-und clipschnittmember verfügt.</span><span class="sxs-lookup"><span data-stu-id="775c1-147">Direct3D maintains the clip status using **D3DCLIPSTATUS9**, which has ClipUnion and ClipIntersection members.</span></span> <span data-ttu-id="775c1-148">ClipUnion ist ein bitweises OR aller Scheitelpunkt-Clip Codes, und clipschnittmenge ist ein bitweises and aller Scheitelpunkt-Clip Codes.</span><span class="sxs-lookup"><span data-stu-id="775c1-148">ClipUnion is a bitwise OR of all vertex clip codes and ClipIntersection is a bitwise AND of all vertex clip codes.</span></span> <span data-ttu-id="775c1-149">Anfangswerte sind für ClipUnion und 0xFFFFFFFF für clipschnitt 0 (null).</span><span class="sxs-lookup"><span data-stu-id="775c1-149">Initial values are zero for ClipUnion and 0xFFFFFFFF for ClipIntersection.</span></span> <span data-ttu-id="775c1-150">Wenn D3DRS \_ Clipping auf **false** festgelegt ist, werden ClipUnion und clipschnitt auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="775c1-150">When D3DRS\_CLIPPING is set to **FALSE**, ClipUnion and ClipIntersection are set to zero.</span></span> <span data-ttu-id="775c1-151">Direct3D aktualisiert den Clip Status während Zeichnungs aufrufen.</span><span class="sxs-lookup"><span data-stu-id="775c1-151">Direct3D updates the clip status during drawing calls.</span></span> <span data-ttu-id="775c1-152">Legen Sie zum Berechnen des Clip Status eines bestimmten Objekts ClipUnion und clipschnitt auf Ihren Anfangswert fest, und setzen Sie die Zeichnung fort.</span><span class="sxs-lookup"><span data-stu-id="775c1-152">To compute clip status for a particular object, set ClipUnion and ClipIntersection to their initial value and continue drawing.</span></span>

<span data-ttu-id="775c1-153">Der Clip Status wird nicht von " [**drawrectpatch**](/windows/desktop/api) " und " [**drawtpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) " aktualisiert, weil keine Software Emulation für Sie vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="775c1-153">Clip status is not updated by [**DrawRectPatch**](/windows/desktop/api) and [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) because there is no software emulation for them.</span></span>

## <a name="requirements"></a><span data-ttu-id="775c1-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="775c1-154">Requirements</span></span>



| <span data-ttu-id="775c1-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="775c1-155">Requirement</span></span> | <span data-ttu-id="775c1-156">Wert</span><span class="sxs-lookup"><span data-stu-id="775c1-156">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="775c1-157">Header</span><span class="sxs-lookup"><span data-stu-id="775c1-157">Header</span></span><br/> | <dl> <span data-ttu-id="775c1-158"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="775c1-158"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="775c1-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="775c1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="775c1-160">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="775c1-160">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="775c1-161">**Getclipstatus**</span><span class="sxs-lookup"><span data-stu-id="775c1-161">**GetClipStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[<span data-ttu-id="775c1-162">**Setclipstatus**</span><span class="sxs-lookup"><span data-stu-id="775c1-162">**SetClipStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
