---
description: Gibt Materialeigenschaften an.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: D3DMATERIAL9-Struktur (D3D9Types.h)
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
ms.openlocfilehash: 640fd4ce0110f47aa20a04d0df595b0ae8bf5052c229825dd93e1066150c6306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527580"
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

Wert, der die diffuse Farbe des Materials angibt. Siehe [**D3DCOLORVALUE.**](d3dcolorvalue.md)

</dd> <dt>

**Umgebend**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Wert, der die Umgebungsfarbe des Materials angibt. Siehe [**D3DCOLORVALUE.**](d3dcolorvalue.md)

</dd> <dt>

**Glänzend**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Wert, der die Glanzfarbe des Materials angibt. Siehe [**D3DCOLORVALUE.**](d3dcolorvalue.md)

</dd> <dt>

**Selbstleuchtend**
</dt> <dd>

Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Wert, der die freizügige Farbe des Materials angibt. Siehe [**D3DCOLORVALUE.**](d3dcolorvalue.md)

</dd> <dt>

**Energie**
</dt> <dd>

Typ: **float**

</dd> <dd>

Gleitkommawert, der die Schärfe von Glanzlichter angibt. Je höher der Wert, desto schärfer die Hervorhebung.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um Glanzlichter zu deaktivieren, legen Sie D3DRS \_ SPECULARENABLE mithilfe von [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)auf **FALSE** fest. Dies ist die schnellste Option, da keine Glanzlichter berechnet werden.

Weitere Informationen zur Verwendung des Beleuchtungsmoduls zum Berechnen der Glanzlichter finden Sie unter [Specular Lighting (Direct3D 9) ( Glanzlicht (Direct3D 9)](specular-lighting.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DDevice9::GetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
