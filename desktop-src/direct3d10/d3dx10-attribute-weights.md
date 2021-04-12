---
description: Gibt Gitter Gewichtungs Attribute an.
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: D3DX10_ATTRIBUTE_WEIGHTS-Struktur (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 4f137c1ecc29c184c4dec3995fb0202741ce9f09
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355107"
---
# <a name="d3dx10_attribute_weights-structure"></a>D3dx10- \_ Attribut \_ Gewichtungs Struktur

Gibt Gitter Gewichtungs Attribute an.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
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

Der LPD3DX- \_ Attribut \_ Gewichtungs Typ wird als Zeiger auf die D3DX- \_ Attribut \_ Gewichtungs Struktur definiert.


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx10. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
