---
description: Semantik ordnen einen Parameter Vertex- oder Pixel-Shaderregistern zu. Sie können auch optionale beschreibende Zeichenfolgen sein, die an Nicht-Registerparameter angefügt sind.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: D3DXSEMANTIC-Struktur (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSEMANTIC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 2534df72c246fdec361597a8e156f7f19b341ae35fcc04b3bdc6eb71c2903fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631020"
---
# <a name="d3dxsemantic-structure"></a>D3DXSEMANTIC-Struktur

Semantik ordnen einen Parameter Vertex- oder Pixel-Shaderregistern zu. Sie können auch optionale beschreibende Zeichenfolgen sein, die an Nicht-Registerparameter angefügt sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXSEMANTIC {
  UINT Usage;
  UINT UsageIndex;
} D3DXSEMANTIC, *LPD3DXSEMANTIC;
```



## <a name="members"></a>Member

<dl> <dt>

**Verwendung**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Optionen, die bestimmen, wie Ressourcen verwendet werden. Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

**UsageIndex**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Optionen, die ändern, wie die Verwendung interpretiert wird. Der Nutzungs- und Nutzungsindex bilden eine Scheitelpunktdeklaration. Weitere Informationen finden Sie unter [Vertexdeklaration (Direct3D 9).](vertex-declaration.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Semantik ist für Scheitelpunkt- und Pixel-Shader, Eingabe- und Ausgaberegister erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effektstrukturen](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
