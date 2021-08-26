---
description: Beschreibt ein Off-Screen-Renderziel, das von einer Instanz von ID3DXRenderToEnvMap verwendet wird.
ms.assetid: 805df4da-e882-4d54-bf2c-49cfcbc59ac6
title: D3DXRTE_DESC -Struktur (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 91efe4dff2b392310ed2fd6bdc30db12c883c5d08e6b2cf110c2cb29d73c54ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027280"
---
# <a name="d3dxrte_desc-structure"></a>D3DXRTE \_ DESC-Struktur

Beschreibt ein Off-Screen-Renderziel, das von einer Instanz von [**ID3DXRenderToEnvMap verwendet wird.**](id3dxrendertoenvmap.md)

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXRTE_DESC {
  UINT      Size;
  UINT      MipLevels;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTE_DESC, *LPD3DXRTE_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Größe**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite und Höhe in Pixel.

</dd> <dt>

**MipLevels**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Maximale Detailstufe (LOD).

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Farbpufferformat.

</dd> <dt>

**Tiefenstencil**
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Gibt an, ob der Z-Puffer benötigt wird.

</dd> <dt>

**DepthStencilFormat**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Format des Tiefenpuffers.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Methode wird verwendet, um die Erstellungsparameter zurückzuerlangen, die beim Erstellen eines [**ID3DXRenderToEnvMap-Objekts verwendet**](id3dxrendertoenvmap.md) werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9core.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
