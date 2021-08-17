---
description: 'D3DCOLORVALUE-Struktur (D3D9Types.h): Beschreibt Farbwerte.'
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: D3DCOLORVALUE-Struktur (D3D9Types.h)
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
ms.openlocfilehash: b8c188e1b50905abd61184c7e1fe67d4253e920aa26d5d1782c1633d843bd282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733352"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a>D3DCOLORVALUE-Struktur (D3D9Types.h)

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

Gleitkommawert, der die rote Komponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt an, dass die rote Komponente vollständig fehlt, während der Wert 1.0 angibt, dass Rot vollständig vorhanden ist.

</dd> <dt>

**g**
</dt> <dd>

Typ: **float**

</dd> <dd>

Gleitkommawert, der die grüne Komponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt an, dass die grüne Komponente vollständig fehlt, während der Wert 1,0 angibt, dass Grün vollständig vorhanden ist.

</dd> <dt>

**b**
</dt> <dd>

Typ: **float**

</dd> <dd>

Gleitkommawert, der die blaue Komponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt das vollständige Fehlen der blauen Komponente an, während der Wert 1,0 angibt, dass Blau vollständig vorhanden ist.

</dd> <dt>

**Eine**
</dt> <dd>

Typ: **float**

</dd> <dd>

Gleitkommawert, der die Alphakomponente einer Farbe angibt. Dieser Wert liegt im Allgemeinen im Bereich von 0,0 bis 1,0. Der Wert 0,0 gibt vollständig transparent an, während der Wert 1.0 für vollständig deckend steht.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können die Member dieser Struktur auf Werte außerhalb des Bereichs von 0 bis 1 festlegen, um einige ungewöhnliche Effekte zu implementieren. Werte größer als 1 erzeugen starke Lichtlichter, die tendenziell eine Szene hervorholen. Negative Werte erzeugen dunkle Lichtlichter, die tatsächlich Licht aus einer Szene entfernen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




