---
description: Gibt Material Informationen zurück, die in Direct3D-Dateien (. x) gespeichert sind.
ms.assetid: dfa021ba-61d8-4f99-9bbb-0cfbe11b787d
title: D3DXMATERIAL-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 89079b716a8c5808255b2bc660f1d364bb97315f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354984"
---
# <a name="d3dxmaterial-structure"></a>D3DXMATERIAL-Struktur

Gibt Material Informationen zurück, die in Direct3D-Dateien (. x) gespeichert sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXMATERIAL {
  D3DMATERIAL9 MatD3D;
  LPSTR        pTextureFilename;
} D3DXMATERIAL, *LPD3DXMATERIAL;
```



## <a name="members"></a>Member

<dl> <dt>

**MatD3D**
</dt> <dd>

Typ: **[ **D3DMATERIAL9**](d3dmaterial9.md)**

</dd> <dd>

[**D3DMATERIAL9**](d3dmaterial9.md) -Struktur, die die Materialeigenschaften beschreibt.

</dd> <dt>

**ptexturefilename**
</dt> <dd>

Typ: **LPSTR**

</dd> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Dateinamen der Textur angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) -Funktion und die [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) -Funktion geben ein Array von **D3DXMATERIAL** -Strukturen zurück, die die Material Farbe und den Namen der Textur für jedes Material im Mesh angeben. Die Anwendung muss dann die Textur laden.

Der LPD3DXMATERIAL-Typ wird als Zeiger auf die **D3DXMATERIAL** -Struktur definiert.


```
typedef struct D3DXMATERIAL* LPD3DXMATERIAL;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md)
</dt> <dt>

[**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)
</dt> </dl>

 

 




