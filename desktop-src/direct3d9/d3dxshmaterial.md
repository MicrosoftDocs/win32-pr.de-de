---
description: Sh-Materialmerkmale (SphericalIcal, pherical- oder SH)-Radiance Transfer (PRT) vorberechnunget.
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: D3DXSHMATERIAL-Struktur (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 4bfbf00c7d8654ad851ca8c691c9f028c09648219dbe76bb4ef07fe3b830e4d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849720"
---
# <a name="d3dxshmaterial-structure"></a>D3DXSHMATERIAL-Struktur

Sh-Materialmerkmale (SphericalIcal, pherical- oder SH)-Radiance Transfer (PRT) vorberechnunget.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXSHMATERIAL {
  D3DCOLORVALUE Diffuse;
  BOOL          bMirror;
  BOOL          bSubSurf;
  FLOAT         RelativeIndexOfRefraction;
  D3DCOLORVALUE Absorption;
  D3DCOLORVALUE ReducedScattering;
} D3DXSHMATERIAL, *LPD3DXSHMATERIAL;
```



## <a name="members"></a>Member

<dl> <dt>

**Diffus**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Diffuses Albedo der Oberfläche. Dieser Wert wird ignoriert, wenn das -Objekt ein Spiegel ist.

</dd> <dt>

**bMirror**
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Muss auf FALSE festgelegt **werden.**

</dd> <dt>

**bSubSurf**
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Legen Sie diese Option **auf TRUE** fest, um die Subsurface-Punktung zu aktivieren. Jedes Objekt, das untergeordnetes Streuen vor sich geht, kann kein Spiegel sein.

</dd> <dt>

**RelativeIndexOfRefraction**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Der relative Index der Refraction ist das Verhältnis zwischen zwei absoluten Indizes der Refraction. Ein Index der Refraktion ist das Verhältnis des Sinus des Winkels des Verhältnisses zum Sinus des Refraktionswinkels.

</dd> <dt>

**Absorption**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Der Lichtkoeffizient ist ein Parameter für die Volumenrenderinggleichung, die verwendet wird, um die Lichtpropagierung in einem beteiligten Medium zu modellieren.

</dd> <dt>

**ReducedScattering**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Der reduzierte Punktzahlkoeffizient ist ein Parameter für die Volumerenderinggleichung, die verwendet wird, um die Lichtweitergabe in einem beteiligten Medium zu modellieren.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Nicht-Szenen verwenden den roten Kanal aus den Materialien anstelle des Leuchtdichtewerts.

Weitere Informationen zum PRT finden Sie unter:

-   Siggraph Proceedings: A Practical Model for Subsurface Light Transport, 2001. (Siggraph Proceedings: A Practical Model for Subsurface Light Transport, 2001)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
