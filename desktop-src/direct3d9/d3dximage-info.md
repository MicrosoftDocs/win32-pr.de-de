---
description: 'D3DXIMAGE_INFO struktur: Gibt eine Beschreibung des ursprünglichen Inhalts einer Bilddatei zurück.'
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: D3DXIMAGE_INFO -Struktur (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_INFO
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: ede879b288569b503257abeb189d93316ed2bd96dd4db99f6e22f32bbb4f98b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607820"
---
# <a name="d3dximage_info-structure"></a>D3DXIMAGE \_ INFO-Struktur

Gibt eine Beschreibung des ursprünglichen Inhalts einer Bilddatei zurück.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXIMAGE_INFO {
  UINT                 Width;
  UINT                 Height;
  UINT                 Depth;
  UINT                 MipLevels;
  D3DFORMAT            Format;
  D3DRESOURCETYPE      ResourceType;
  D3DXIMAGE_FILEFORMAT ImageFileFormat;
} D3DXIMAGE_INFO, *LPD3DXIMAGE_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Width**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite des ursprünglichen Bilds in Pixel.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe des ursprünglichen Bilds in Pixel.

</dd> <dt>

**Tiefe**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tiefe des ursprünglichen Bilds in Pixel.

</dd> <dt>

**MipLevels**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der MIP-Ebenen im originalen Bild.

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Ein Wert aus dem [aufzählten D3DFORMAT-Typ,](d3dformat.md) der die Daten im ursprünglichen Bild am besten beschreibt.

</dd> <dt>

**ResourceType**
</dt> <dd>

Typ: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Stellt den Typ der in der Datei gespeicherten Textur dar. Dies ist entweder D3DRTYPE \_ TEXTURE, D3DRTYPE \_ VOLUMETEXTURE oder D3DRTYPE \_ CubeTexture.

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Typ: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

</dd> <dd>

Stellt das Format der Bilddatei dar.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9tex.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
