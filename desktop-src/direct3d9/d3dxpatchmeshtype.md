---
description: Mesh-Patchtypen.
ms.assetid: 229d01b2-781c-48a8-93f2-9dd9dbd67f3e
title: D3DXPATCHMESHTYPE-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHMESHTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d6a663e983b339d79ec89bf1b4ddfe7b4eaa9f1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355157"
---
# <a name="d3dxpatchmeshtype-enumeration"></a>D3DXPATCHMESHTYPE-Enumeration

Mesh-Patchtypen.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXPATCHMESHTYPE { 
  D3DXPATCHMESH_RECT         = 0x001,
  D3DXPATCHMESH_TRI          = 0x002,
  D3DXPATCHMESH_NPATCH       = 0x003,
  D3DXPATCHMESH_FORCE_DWORD  = 0x7fffffff
} D3DXPATCHMESHTYPE, *LPD3DXPATCHMESHTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH \_ Rect**
</dt> <dd>

Messtyp des Rechteck Patches.

</dd> <dt>

<span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH \_ Tri**
</dt> <dd>

Messtyp des Dreiecks Patches.

</dd> <dt>

<span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH \_ npatch**
</dt> <dd>

N-patchmesh-Typ.

</dd> <dt>

<span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dreiecks Patches haben drei Seiten und werden in [**D3DTRIPATCH \_ Info**](d3dtripatch-info.md)beschrieben. Rechteck-Patches sind vierseitig und werden in [**D3DRECTPATCH \_ Info**](d3drectpatch-info.md)beschrieben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[Verwenden von Higher-Order primitiven (Direct3D 9)](using-higher-order-primitives.md)
</dt> </dl>

 

 




