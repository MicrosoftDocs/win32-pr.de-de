---
description: Definiert die primitiven, die von Direct3D unterstützt werden.
ms.assetid: 89e697f9-02b9-4ae1-9e86-6178da0cb008
title: D3DPRIMITIVETYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRIMITIVETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 933bbec72950bd2c73fda8b3781dd46393ca4c96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132357"
---
# <a name="d3dprimitivetype-enumeration"></a>D3DPRIMITIVETYPE-Enumeration

Definiert die primitiven, die von Direct3D unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DPRIMITIVETYPE { 
  D3DPT_POINTLIST      = 1,
  D3DPT_LINELIST       = 2,
  D3DPT_LINESTRIP      = 3,
  D3DPT_TRIANGLELIST   = 4,
  D3DPT_TRIANGLESTRIP  = 5,
  D3DPT_TRIANGLEFAN    = 6,
  D3DPT_FORCE_DWORD    = 0x7fffffff
} D3DPRIMITIVETYPE, *LPD3DPRIMITIVETYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT \_ PointList**
</dt> <dd>

Rendert die Scheitel Punkte als Auflistung isolierter Punkte. Dieser Wert wird für indizierte primitive nicht unterstützt.

</dd> <dt>

<span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT- \_ LineList**
</dt> <dd>

Rendert die Scheitel Punkte als Liste der isolierten geraden Liniensegmente.

</dd> <dt>

<span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT \_ linestrip**
</dt> <dd>

Rendert die Scheitel Punkte als eine einzelne Polylinie.

</dd> <dt>

<span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT- \_ Liste**
</dt> <dd>

Rendert die angegebenen Scheitel Punkte als Sequenz isolierter Dreiecke. Jede Gruppe von drei Vertices definiert ein separates Dreieck.

Der aktuelle renderingstatus wirkt sich auf die Hintergrund Erkennung aus.

</dd> <dt>

<span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT-Test \_ Strip**
</dt> <dd>

Rendert die Scheitel Punkte als Dreiecks Streifen. Das Flag für die Hintergrund Erkennung wird automatisch bei geraden Dreiecke gekippt.

</dd> <dt>

<span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT \_ -Test**
</dt> <dd>

Rendert die Scheitel Punkte als Dreiecks Lüfter.

</dd> <dt>

<span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Verwendung von [Dreiecks Streifen](triangle-strips.md) oder [Dreiecks Lüfter (Direct3D 9)](triangle-fans.md) ist oft effizienter als die Verwendung von Dreiecks Listen, da weniger Vertices dupliziert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::D rawindexedprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)
</dt> <dt>

[**IDirect3DDevice9::D rawindexedprimitiveup**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)
</dt> <dt>

[**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
</dt> <dt>

[**IDirect3DDevice9::D rawprimitiveup**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
</dt> </dl>

 

 
