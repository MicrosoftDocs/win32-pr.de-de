---
description: Gibt eine Beschreibung des ursprünglichen Inhalts einer Bilddatei zurück.
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: D3DXIMAGE_INFO-Struktur (D3dx9tex. h)
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
ms.openlocfilehash: 6ec152dc56dcea3a718cf5cd42fb351d4fddf852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762036"
---
# <a name="d3dximage_info-structure"></a>D3DXIMAGE \_ Info-Struktur

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

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite des ursprünglichen Bilds in Pixel.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe des ursprünglichen Bilds in Pixel.

</dd> <dt>

**Tiefe**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Tiefe des ursprünglichen Bilds in Pixel.

</dd> <dt>

**MipLevels**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der MIP-Ebenen im ursprünglichen Bild.

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Ein Wert aus dem [D3DFORMAT](d3dformat.md) -Enumerationstyp, der die Daten im ursprünglichen Bild am ehesten beschreibt.

</dd> <dt>

**ResourceType**
</dt> <dd>

Typ: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Stellt den Typ der Textur dar, die in der Datei gespeichert ist. Dabei handelt es sich entweder um D3DRTYPE \_ Texture, D3DRTYPE \_ volumetexture oder D3DRTYPE \_ cubetexture.

</dd> <dt>

**Imagefileformat**
</dt> <dd>

Type: **[ **D3DXIMAGE \_ File Format**](./d3dximage-fileformat.md)**

</dd> <dd>

Stellt das Format der Bilddatei dar.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9tex. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
