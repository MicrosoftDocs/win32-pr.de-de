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
# <a name="d3dclipstatus9-structure"></a>D3DCLIPSTATUS9-Struktur

Beschreibt den aktuellen Clip Status.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a>Member

<dl> <dt>

**ClipUnion**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Clip-Union-Flags, die den aktuellen Clip Status beschreiben. Dieser Member kann eines oder mehrere der folgenden Flags sein:



| Wert                                                                                                                                                      | Bedeutung                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <dt>**D3DCS \_**</dt> </dl>          | Kombination aller Clip-Flags.<br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <dt>**D3DCS \_ Links**</dt> </dl>       | Alle Scheitel Punkte werden von der linken Ebene der Anzeige-Frustum abgeschnitten.<br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <dt>**D3DCS \_ Rechts**</dt> </dl>    | Alle Scheitel Punkte werden von der rechten Ebene der Anzeige Frust Fläche abgeschnitten.<br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <dt>**D3DCS \_ oben**</dt> </dl>          | Alle Scheitel Punkte werden von der obersten Ebene der Anzeige "Frustum" abgeschnitten.<br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <dt>**D3DCS \_ unten**</dt> </dl> | Alle Scheitel Punkte werden von der untersten Ebene der Anzeige-Frustum abgeschnitten.<br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <dt>**D3DCS- \_ Front**</dt> </dl>    | Alle Vertices werden von der Vorderseite der Anzeige Frust Fläche abgeschnitten.<br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <dt>**D3DCS \_ zurück**</dt> </dl>       | Alle Scheitel Punkte werden von der Rückseite der Anzeige Frust Fläche abgeschnitten.<br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <dt>**D3DCS \_ PLANE0**</dt> </dl> | Anwendungs definierte Clippingebenen.<br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <dt>**D3DCS \_ PLANE1**</dt> </dl> | Anwendungs definierte Clippingebenen.<br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <dt>**D3DCS \_ PLANE2**</dt> </dl> | Anwendungs definierte Clippingebenen.<br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <dt>**D3DCS \_ PLANE3**</dt> </dl> | Anwendungs definierte Clippingebenen.<br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <dt>**D3DCS \_ PLANE4**</dt> </dl> | Anwendungs definierte Clippingebenen.<br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <dt>**D3DCS \_ PLANE5**</dt> </dl> | Anwendungs definierte Clippingebenen.<br/>                                 |



 

</dd> <dt>

**Clipschnittmenge**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Clip schnittstellerflags, die den aktuellen Clip Status beschreiben. Dieser Member kann die gleichen Flags wie ClipUnion annehmen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn das Clipping während der Scheitelpunkt Verarbeitung (von [**ProcessVertices**](/windows/desktop/api), [**drawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)oder anderen Zeichnungsfunktionen) aktiviert ist, berechnet Direct3D einen Clip Code für jeden Scheitelpunkt. Der Clip Code ist eine Kombination aus D3DCS \_ \* Bits. Wenn ein Scheitelpunkt außerhalb einer bestimmten Clippingebene liegt, wird das entsprechende Bit im Clippingcode festgelegt. Direct3D verwaltet den Clip Status mithilfe von **D3DCLIPSTATUS9**, der über ClipUnion-und clipschnittmember verfügt. ClipUnion ist ein bitweises OR aller Scheitelpunkt-Clip Codes, und clipschnittmenge ist ein bitweises and aller Scheitelpunkt-Clip Codes. Anfangswerte sind für ClipUnion und 0xFFFFFFFF für clipschnitt 0 (null). Wenn D3DRS \_ Clipping auf **false** festgelegt ist, werden ClipUnion und clipschnitt auf NULL festgelegt. Direct3D aktualisiert den Clip Status während Zeichnungs aufrufen. Legen Sie zum Berechnen des Clip Status eines bestimmten Objekts ClipUnion und clipschnitt auf Ihren Anfangswert fest, und setzen Sie die Zeichnung fort.

Der Clip Status wird nicht von " [**drawrectpatch**](/windows/desktop/api) " und " [**drawtpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) " aktualisiert, weil keine Software Emulation für Sie vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Getclipstatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[**Setclipstatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
