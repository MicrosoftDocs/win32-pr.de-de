---
description: Gibt Gitter Gewichtungs Attribute an.
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: D3DXATTRIBUTEWEIGHTS-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTEWEIGHTS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 49725e410fb700c7ecb93fd56a8db367d7f982a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367378"
---
# <a name="d3dxattributeweights-structure"></a>D3DXATTRIBUTEWEIGHTS-Struktur

Gibt Gitter Gewichtungs Attribute an.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXATTRIBUTEWEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DXATTRIBUTEWEIGHTS, *LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="members"></a>Member

<dl> <dt>

**Position**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Position

</dd> <dt>

**Grenze**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Blend-Gewichtung.

</dd> <dt>

**Normal**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Normal.

</dd> <dt>

**Diffus**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Diffuses Beleuchtungs Wert.

</dd> <dt>

**Glänzend**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Glanzlicht Wert.

</dd> <dt>

**Texcoord**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Acht Texturkoordinaten.

</dd> <dt>

**Tangens**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangens.

</dd> <dt>

**Binormal**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormal.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur beschreibt, wie bei einem Vereinfachungs Vorgang Scheitelpunkt Daten bei der Berechnung relativer Kosten zwischen reduzierenden Kanten berücksichtigt werden. Wenn das normale Feld z. b. 0,0 ist, ignoriert der Vereinfachungs Vorgang die normale Scheitelpunkt Komponente bei der Berechnung des Fehlers für das reduzieren. Wenn das normale Feld jedoch 1,0 ist, wird für den Vereinfachungs Vorgang die normale Scheitelpunkt Komponente verwendet. Wenn das normale Feld 2,0 ist, doppelte die Fehler Menge. Wenn das normale Feld 4,0 ist, vervierfachen Sie die Anzahl der Fehler, usw.

Der LPD3DXATTRIBUTEWEIGHTS-Typ wird als Zeiger auf die **D3DXATTRIBUTEWEIGHTS** -Struktur definiert.


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSimplifyMesh**](d3dxsimplifymesh.md)
</dt> </dl>

 

 
