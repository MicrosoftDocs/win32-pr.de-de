---
description: Definiert das Scheitelpunkt-Datenlayout. Jeder Scheitelpunkt kann einen oder mehrere Datentypen enthalten, und jeder Datentyp wird durch ein Scheitelpunktelement beschrieben.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: D3DVERTEXELEMENT9-Struktur (D3D9Types.h)
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
ms.openlocfilehash: cda5b92170ef21f7bb66233f0748afe0c780837bbcb0eee9ef3c970880070422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527294"
---
# <a name="d3dvertexelement9-structure"></a>D3DVERTEXELEMENT9-Struktur

Definiert das Scheitelpunkt-Datenlayout. Jeder Scheitelpunkt kann einen oder mehrere Datentypen enthalten, und jeder Datentyp wird durch ein Scheitelpunktelement beschrieben.

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

**Stream**
</dt> <dd>

Typ: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Streamnummer.

</dd> <dt>

**Offset**
</dt> <dd>

Typ: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset vom Anfang der Scheitelpunktdaten zu den Daten, die dem jeweiligen Datentyp zugeordnet sind.

</dd> <dt>

**Typ**
</dt> <dd>

Typ: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Der als [**D3DDECLTYPE**](./d3ddecltype.md)angegebene Datentyp. Einer von mehreren vordefinierten Typen, die die Datengröße definieren. Einige Methoden haben einen impliziten Typ.

</dd> <dt>

**Methode**
</dt> <dd>

Typ: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Die -Methode gibt die Mosaikverarbeitung an, die bestimmt, wie der Mosaikator die Scheitelpunktdaten interpretiert (oder verarbeitet). Weitere Informationen finden Sie unter [**D3DDECLMETHOD**](./d3ddeclmethod.md).

</dd> <dt>

**Verwendung**
</dt> <dd>

Typ: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Definiert, wofür die Daten verwendet werden. das heißt, die Interoperabilität zwischen Vertexdatenlayouts und Vertex-Shadern. Jede Verwendung dient dazu, eine Scheitelpunktdeklaration an einen Vertex-Shader zu binden. In einigen Fällen haben sie eine besondere Interpretation. Beispielsweise wird ein Element, das D3DDECLUSAGE NORMAL oder \_ D3DDECLUSAGE POSITION angibt, vom N-Patch-Mosaik zum Einrichten des Mosaiks \_ verwendet. Eine Liste der verfügbaren Semantik finden Sie unter [**D3DDECLUSAGE.**](./d3ddeclusage.md) D3DDECLUSAGE TEXCOORD kann für benutzerdefinierte Felder verwendet werden (für die keine \_ vorhandene Verwendung definiert ist).

</dd> <dt>

**UsageIndex**
</dt> <dd>

Typ: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Ändert die Verwendungsdaten, damit der Benutzer mehrere Verwendungstypen angeben kann.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Vertexdaten werden mithilfe eines Arrays von **D3DVERTEXELEMENT9-Strukturen** definiert. Verwenden [**Sie D3DDECL \_ END,**](d3ddecl-end.md) um das letzte Element in der Deklaration zu deklarieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Scheitelpunktdeklaration (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 
