---
description: Definiert ein Volume.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: D3DBOX-Struktur (D3D9Types. h)
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
ms.openlocfilehash: 882f6aadf0d49284b30132d4f08a9c583e5c9d73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219463"
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

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Position der linken Seite des Felds auf der x-Achse.

</dd> <dt>

**Top**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Position des oberen Rands auf der y-Achse.

</dd> <dt>

**Right**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Position der rechten Seite des Felds auf der x-Achse.

</dd> <dt>

**bottom**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Position des unteren Feldes des Felds auf der y-Achse.

</dd> <dt>

**Front**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Position der Vorderseite des Felds auf der z-Achse.

</dd> <dt>

**Zurück**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Position der Rückseite des Felds auf der z-Achse.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**D3DBOX** schließt die linken, oberen und vorderen Ränder ein. der Rechte, der untere und der hintere Rand sind jedoch nicht enthalten. Beispielsweise wird ein Feld, das 100 Einheiten breit ist und bei 0 beginnt (d.h. die Punkte bis einschließlich und einschließlich 99), mit dem Wert 0 für das linke Element und dem Wert 100 für das Rechte Element ausgedrückt. Beachten Sie, dass der Wert 99 nicht für das Rechte Element verwendet wird.

Die Einschränkungen bei der für **D3DBOX** beobachteten Seiten Anordnung sind von links nach rechts, von oben nach unten und von vorne nach hinten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
