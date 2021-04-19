---
description: Material Merkmale für die präberechnete Glanz Farbe (SH) (SH).
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: D3DXSHMATERIAL-Struktur (D3dx9mesh. h)
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
ms.openlocfilehash: 0600cc0c1ebe086f0d6679182125350b1ee8ca98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367362"
---
# <a name="d3dxshmaterial-structure"></a>D3DXSHMATERIAL-Struktur

Material Merkmale für die präberechnete Glanz Farbe (SH) (SH).

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

Diffuses Albedo der Oberfläche. Dieser Wert wird ignoriert, wenn das Objekt eine Spiegelung ist.

</dd> <dt>

**bmirror**
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Muss auf " **false**" festgelegt werden.

</dd> <dt>

**bsubsurf**
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Auf " **true** " festlegen, um unter Oberflächen-Scattering zu aktivieren; jedes Objekt, das die unter oberflächenzererung durchführt, darf kein Spiegel sein.

</dd> <dt>

**Relativeingedexofrebruchteil**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der relative Index der abbrechungs Rate ist das Verhältnis zwischen zwei absoluten Indizes der abbrechungs Rate. Ein Index der abbrechungs Rate ist das Verhältnis des Sinus des Winkels in den Sinus des Winkels der abbrechungs Spitze.

</dd> <dt>

**Übernahme**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Der Absorptionskoeffizienten ist ein Parameter für die volumerenderinggleichung, mit der die Licht Weitergabe auf einem teilnehmenden Medium modelliert wird

</dd> <dt>

**Reducedscattering**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Der reduzierte Streuungs Koeffizienten ist ein Parameter für die volumerenderinggleichung, die zum Modellieren der Licht Weitergabe in einem teilnehmenden Medium verwendet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Nicht--spektrale Szenen verwenden den roten Kanal aus den Materialien anstelle des Leuchtkraft Werts.

Weitere Informationen zu PRT finden Sie unter:

-   Jensen, Henrik wann, et al. SIGGRAPH-Prozess: ein praktisches Modell für den subsurface Light-Transport, 2001.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
