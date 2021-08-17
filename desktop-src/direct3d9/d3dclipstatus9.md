---
description: Beschreibt den aktuellen Clipstatus.
ms.assetid: 3ea8631c-a967-4d24-a49a-1751b3ee6077
title: D3DCLIPSTATUS9-Struktur (D3D9Types.h)
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
ms.openlocfilehash: 1820e0646d735a8e1f3817832172d11e83218bbe8748e639084c47b3f77ea5df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123367"
---
# <a name="d3dclipstatus9-structure"></a>D3DCLIPSTATUS9-Struktur

Beschreibt den aktuellen Clipstatus.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a>Member

<dl> <dt>

**Clipunion**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Ausschneiden von Union-Flags, die den aktuellen Clipstatus beschreiben. Dieser Member kann eines oder mehrere der folgenden Flags sein:



| Wert                                                                                                                                                      | Bedeutung                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <dt>**D3DCS \_ ALL**</dt> </dl>          | Kombination aller Clipflags.<br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <dt>**D3DCS \_ LEFT**</dt> </dl>       | Alle Scheitelpunkte werden von der linken Ebene des Anzeige-Frustums abgeschnitten.<br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <dt>**D3DCS \_ RIGHT**</dt> </dl>    | Alle Scheitelpunkte werden von der rechten Ebene des Anzeige-Frustums abgeschnitten.<br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <dt>**D3DCS \_ TOP**</dt> </dl>          | Alle Scheitelpunkte werden von der oberen Ebene des Anzeige-Frustums abgeschnitten.<br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <dt>**D3DCS \_ BOTTOM**</dt> </dl> | Alle Scheitelpunkte werden von der unteren Ebene des Anzeige-Frustums abgeschnitten.<br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <dt>**D3DCS \_ FRONT**</dt> </dl>    | Alle Scheitelpunkte werden von der vorderen Ebene des Anzeige-Frustums abgeschnitten.<br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <dt>**D3DCS \_ BACK**</dt> </dl>       | Alle Scheitelpunkte werden von der Hintergrundebene des Anzeige-Frustums abgeschnitten.<br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <dt>**D3DCS \_ PLANE0**</dt> </dl> | Anwendungsdefinierte Clippingebenen.<br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <dt>**D3DCS \_ PLANE1**</dt> </dl> | Anwendungsdefinierte Clippingebenen.<br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <dt>**D3DCS \_ PLANE2**</dt> </dl> | Anwendungsdefinierte Clippingebenen.<br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <dt>**D3DCS \_ PLANE3**</dt> </dl> | Anwendungsdefinierte Clippingebenen.<br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <dt>**D3DCS \_ PLANE4**</dt> </dl> | Anwendungsdefinierte Clippingebenen.<br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <dt>**D3DCS \_ PLANE5**</dt> </dl> | Anwendungsdefinierte Clippingebenen.<br/>                                 |



 

</dd> <dt>

**ClipIntersection**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Schnittmengenflags, die den aktuellen Clipstatus beschreiben. Dieser Member kann die gleichen Flags wie ClipUnion annehmen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn clipping während der Vertexverarbeitung aktiviert ist (durch [**ProcessVertices,**](/windows/desktop/api) [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)oder andere Zeichnungsfunktionen), berechnet Direct3D einen Clipcode für jeden Scheitelpunkt. Der Clipcode ist eine Kombination aus D3DCS-Bits. \_ \* Wenn sich ein Scheitelpunkt außerhalb einer bestimmten Clippingebene befindet, wird das entsprechende Bit im Clippingcode festgelegt. Direct3D verwaltet den Clipstatus mithilfe von **D3DCLIPSTATUS9,** das ClipUnion- und ClipIntersection-Member enthält. ClipUnion ist ein bitweises OR aller Scheitelpunkt-Clipcodes, und ClipIntersection ist ein bitweises AND aller Scheitelpunkt-Clipcodes. Die Anfangswerte sind 0 (null) für ClipUnion und 0xFFFFFFFF für ClipIntersection. Wenn D3DRS \_ CLIPPING auf **FALSE** festgelegt ist, werden ClipUnion und ClipIntersection auf 0 (null) festgelegt. Direct3D aktualisiert den Clipstatus während Zeichnungsaufrufen. Um den Clipstatus für ein bestimmtes Objekt zu berechnen, legen Sie ClipUnion und ClipIntersection auf ihren Anfangswert fest, und fahren Sie mit dem Zeichnen fort.

Der Clipstatus wird von [**DrawRectPatch**](/windows/desktop/api) und [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) nicht aktualisiert, da dafür keine Softwareemulation vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetClipStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[**SetClipStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
