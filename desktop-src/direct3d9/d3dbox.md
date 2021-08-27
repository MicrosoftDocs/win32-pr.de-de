---
description: Definiert ein Volume.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: D3DBOX-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9b7e01641348594e962f546a431700db799600a08571bbb7cfaf13396e671036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805513"
---
# <a name="d3dbox-structure"></a>D3DBOX-Struktur

Definiert ein Volume.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DBOX {
  UINT Left;
  UINT Top;
  UINT Right;
  UINT Bottom;
  UINT Front;
  UINT Back;
} D3DBOX, *LPD3DBOX;
```



## <a name="members"></a>Member

<dl> <dt>

**Left**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Position der linken Seite des Felds auf der x-Achse.

</dd> <dt>

**Top**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Position des oberen Rands des Felds auf der y-Achse.

</dd> <dt>

**Right**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Position der rechten Seite des Felds auf der x-Achse.

</dd> <dt>

**bottom**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Position des unteren Rands des Felds auf der y-Achse.

</dd> <dt>

**Front**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Position der Vorderseite des Felds auf der Z-Achse.

</dd> <dt>

**Zurück**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Position der Rückseite des Felds auf der Z-Achse.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**D3DBOX** enthält die linken, oberen und oberen Ränder. die rechten, unteren und hinteren Ränder sind jedoch nicht enthalten. Beispielsweise wird ein Feld, das 100 Einheiten breit ist und bei 0 beginnt (also einschließlich der Punkte bis einschließlich 99), mit dem Wert 0 für das linke Element und dem Wert 100 für das Rechte Element ausgedrückt. Beachten Sie, dass der Wert 99 nicht für den Right-Member verwendet wird.

Die für **D3DBOX** beobachteten Einschränkungen bei der Seitenreihenfolge sind von links nach rechts, von oben nach unten und von vorn nach rechts.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
