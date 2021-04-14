---
description: Gibt Materialeigenschaften an.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: D3DMATERIAL9-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIAL9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b9c3ad93fe2cb80fe758e2e66da37cce9d4267ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394157"
---
# <a name="d3dmaterial9-structure"></a>D3DMATERIAL9-Struktur

Gibt Materialeigenschaften an.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DMATERIAL9 {
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Ambient;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Emissive;
  float         Power;
} D3DMATERIAL9, *LPD3DMATERIAL9;
```



## <a name="members"></a>Member

<dl> <dt>

**Diffus**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Ein-Wert, der die diffuse Farbe des Materials angibt. Siehe [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Umgebend**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Ein-Wert, der die Ambiente-Farbe des Materials angibt. Siehe [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Glänzend**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Ein-Wert, der die Glanz Farbe des Materials angibt. Siehe [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Selbstleuchtend**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Ein-Wert, der die selbst leuchtendes Farbe des Materials angibt. Siehe [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Energie**
</dt> <dd>

Typ: **float**

</dd> <dd>

Ein Gleit Komma Wert, der die Schärfe von Glanzlichtern angibt. Je höher der Wert ist, desto stärker ist die Hervorhebung.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um Glanzlichter zu deaktivieren, legen Sie D3DRS \_ specularenable mithilfe von [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)auf **false** fest. Dies ist die schnellste Option, da keine Glanzlichter berechnet werden.

Weitere Informationen zur Berechnung Glanzlichter mithilfe der Beleuchtungs-Engine finden Sie unter Glanz [Beleuchtung (Direct3D 9)](specular-lighting.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DDevice9:: getmaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[**IDirect3DDevice9:: setmaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
