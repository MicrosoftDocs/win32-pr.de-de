---
description: Beschreibt Farbwerte.
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: D3DCOLORVALUE-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1fe2f187921749207bbbf51d7fcfd75357a70858
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354407"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a>D3DCOLORVALUE-Struktur (D3D9Types. h)

Beschreibt Farbwerte.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a>Member

<dl> <dt>

**r**
</dt> <dd>

Typ: **float**

</dd> <dd>

Ein Gleit Komma Wert, der die rote Komponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt das vollständige Fehlen der roten Komponente an, während der Wert 1,0 angibt, dass Rot vollständig vorhanden ist.

</dd> <dt>

**g**
</dt> <dd>

Typ: **float**

</dd> <dd>

Ein Gleit Komma Wert, der die grüne Komponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt das vollständige Fehlen der grünen Komponente an, während der Wert 1,0 angibt, dass grün vollständig vorhanden ist.

</dd> <dt>

**b**
</dt> <dd>

Typ: **float**

</dd> <dd>

Ein Gleit Komma Wert, der die blaue Komponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt das vollständige Fehlen der blauen Komponente an, während der Wert 1,0 angibt, dass Blue vollständig vorhanden ist.

</dd> <dt>

**ein**
</dt> <dd>

Typ: **float**

</dd> <dd>

Ein Gleit Komma Wert, der die Alpha Komponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt vollständig transparent an, während der Wert 1,0 vollständig deckend angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können die Member dieser Struktur auf Werte außerhalb des Bereichs von 0 bis 1 festlegen, um ungewöhnliche Effekte zu implementieren. Werte, die größer als 1 sind, führen zu starken Lichtern, die tendenziell eine Szene auslagern. Durch negative Werte werden dunkle Lichter erzeugt, die das Licht aus einer Szene entfernen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




