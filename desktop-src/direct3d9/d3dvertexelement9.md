---
description: Definiert das Vertex-Datenlayout. Jeder Scheitelpunkt kann einen oder mehrere Datentypen enthalten, und jeder Datentyp wird von einem Vertex-Element beschrieben.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: D3DVERTEXELEMENT9-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXELEMENT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e6c5e9508185124673ca7464b31d741cdf8035c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354387"
---
# <a name="d3dvertexelement9-structure"></a>D3DVERTEXELEMENT9-Struktur

Definiert das Vertex-Datenlayout. Jeder Scheitelpunkt kann einen oder mehrere Datentypen enthalten, und jeder Datentyp wird von einem Vertex-Element beschrieben.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DVERTEXELEMENT9 {
  WORD Stream;
  WORD Offset;
  BYTE Type;
  BYTE Method;
  BYTE Usage;
  BYTE UsageIndex;
} D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9;
```



## <a name="members"></a>Member

<dl> <dt>

**Datenstrom**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Die streamnummer.

</dd> <dt>

**Offset**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset vom Anfang der Scheitelpunkt Daten zu den Daten, die dem jeweiligen Datentyp zugeordnet sind.

</dd> <dt>

**Type**
</dt> <dd>

Type: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Der als [**D3DDECLTYPE**](./d3ddecltype.md)angegebene Datentyp. Einer von mehreren vordefinierten Typen, die die Datengröße definieren. Einige Methoden haben einen impliziten Typ.

</dd> <dt>

**Methode**
</dt> <dd>

Type: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Die-Methode gibt die Verarbeitung von Mosaik Operatoren an, die bestimmt, wie der Mosaik Prozess die Scheitelpunkt Daten interpretiert (oder verarbeitet). Weitere Informationen finden Sie unter [**D3DDECLMETHOD**](./d3ddeclmethod.md).

</dd> <dt>

**Verwendung**
</dt> <dd>

Type: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Definiert, wofür die Daten verwendet werden. Das heißt, die Interoperabilität zwischen Scheitelpunkt Daten Layouts und Vertex-Shadern. Jede Verwendung dient zum Binden einer Scheitelpunkt Deklaration an einen Scheitelpunkt-Shader. In einigen Fällen haben Sie eine spezielle Interpretation. Beispielsweise wird ein Element, das die Position "D3DDECLUSAGE normal" oder "D3DDECLUSAGE" angibt, \_ \_ vom N-Patch-Mosaik Prozess verwendet, um das Mosaik zu richten. Eine Liste der verfügbaren Semantik finden Sie unter [**D3DDECLUSAGE**](./d3ddeclusage.md) . D3DDECLUSAGE \_ texcoord kann für benutzerdefinierte Felder verwendet werden (für die keine vorhandene Verwendung definiert ist).

</dd> <dt>

**Start Index**
</dt> <dd>

Type: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Ändert die Verwendungs Daten, um dem Benutzer das Angeben mehrerer Verwendungs Typen zu ermöglichen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Vertex-Daten werden mit einem Array von **D3DVERTEXELEMENT9** -Strukturen definiert. Verwenden Sie [**D3DDECL \_ End**](d3ddecl-end.md) , um das letzte Element in der Deklaration zu deklarieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Vertex-Deklaration (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 
