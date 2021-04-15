---
description: Semantik ordnet einem Scheitelpunkt-oder Pixel-Shader-Register einen Parameter zu. Sie können auch optionale beschreibende Zeichen folgen sein, die an nicht-Register Parameter angefügt sind.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: D3DXSEMANTIC-Struktur (D3dx9shader. h)
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
ms.openlocfilehash: 08a30ac4d669beb5b93f2823219cb167d9e8d67f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394105"
---
# <a name="d3dxsemantic-structure"></a>D3DXSEMANTIC-Struktur

Semantik ordnet einem Scheitelpunkt-oder Pixel-Shader-Register einen Parameter zu. Sie können auch optionale beschreibende Zeichen folgen sein, die an nicht-Register Parameter angefügt sind.

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

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Optionen, die bestimmen, wie Ressourcen verwendet werden. Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

**Start Index**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Optionen, die die Interpretation der Verwendung ändern. Der Verwendungs-und Verwendungs Index bilden eine Scheitelpunkt Deklaration. Siehe [Vertex-Deklaration (Direct3D 9)](vertex-declaration.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Semantik ist für Scheitelpunkt-und Pixel-Shader, Eingabe-und Ausgabe Register erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Strukturen](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
