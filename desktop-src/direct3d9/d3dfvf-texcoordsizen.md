---
description: Konstruiert Bitmuster, die zum Identifizieren von Texturkoordinaten Formaten innerhalb einer FVF-Beschreibung verwendet werden. Die Ergebnisse dieser Makros können mithilfe des OR-Operators in einer Beschreibung des "or" kombiniert werden.
ms.assetid: c3076d7c-7935-40ee-b513-7ff6551a535f
title: D3DFVF_TEXCOORDSIZEN (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFVF_TEXCOORDSIZEN
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 58288667954e3414aa3d8ae1550e02e7216ffb4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355205"
---
# <a name="d3dfvf_texcoordsizen"></a>D3DFVF \_ texcoordsizen

Konstruiert Bitmuster, die zum Identifizieren von Texturkoordinaten Formaten innerhalb einer FVF-Beschreibung verwendet werden. Die Ergebnisse dieser Makros können mithilfe des OR-Operators in einer Beschreibung des "or" kombiniert werden.

``` syntax
#define D3DFVF_TEXCOORDSIZEN(CoordIndex) 
#define D3DFVF_TEXCOORDSIZE1(CoordIndex) (D3DFVF_TEXTUREFORMAT1 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE2(CoordIndex) (D3DFVF_TEXTUREFORMAT2) 
#define D3DFVF_TEXCOORDSIZE3(CoordIndex) (D3DFVF_TEXTUREFORMAT3 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE4(CoordIndex) (D3DFVF_TEXTUREFORMAT4 << (CoordIndex*2 + 16))
```

## <a name="parameters"></a>Parameter



| Parameter                                                                                                    | BESCHREIBUNG                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>Coordindex<br/> | Ein Wert, der den Texturkoordinaten Satz identifiziert, bei dem die Texturkoordinaten Größe (1-, 2-, 3-oder 4dimensional) angewendet wird. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **D3DFVF \_ texcoordsizen** -Makros verwenden die folgenden Konstanten.


```C++
#define D3DFVF_TEXTUREFORMAT1 3 // one floating point value
#define D3DFVF_TEXTUREFORMAT2 0 // two floating point values
#define D3DFVF_TEXTUREFORMAT3 1 // three floating point values
#define D3DFVF_TEXTUREFORMAT4 2 // four floating point values
```



In der folgenden Beschreibung von "f" wird ein Scheitelpunkt Format identifiziert, das über eine Position verfügt. normal; diffuse und Glanz Farben; und zwei Sätze von Texturkoordinaten. Der erste Satz von Texturkoordinaten umfasst ein einzelnes-Element, und der zweite Satz enthält zwei Elemente:


```C++
DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE |
              D3DFVF_SPECULAR | D3DFVF_TEX2 |
              D3DFVF_TEXCOORDSIZE1(0) |  // Uses 1D texture coordinates for
                                         // texture coordinate set 1 (index 0).
              D3DFVF_TEXCOORDSIZE2(1);   // And 2D texture coordinates for 
                                         // texture coordinate set 2 (index 1).
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DFVF](d3dfvf.md)
</dt> </dl>

 

 




