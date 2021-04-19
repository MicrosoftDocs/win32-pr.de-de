---
description: Definiert die unterstützten Blend-Vorgänge. Siehe Hinweise zu Definitionen von Begriffen.
ms.assetid: ae750d84-ed7d-4a76-bf64-eae8828c66c7
title: D3DBLENDOP-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLENDOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3ad23d3fb2a93734047f55a46c14335069c95ea9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353346"
---
# <a name="d3dblendop-enumeration"></a>D3DBLENDOP-Enumeration

Definiert die unterstützten Blend-Vorgänge. Siehe Hinweise zu Definitionen von Begriffen.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DBLENDOP { 
  D3DBLENDOP_ADD          = 1,
  D3DBLENDOP_SUBTRACT     = 2,
  D3DBLENDOP_REVSUBTRACT  = 3,
  D3DBLENDOP_MIN          = 4,
  D3DBLENDOP_MAX          = 5,
  D3DBLENDOP_FORCE_DWORD  = 0x7fffffff
} D3DBLENDOP, *LPD3DBLENDOP;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP \_ Hinzufügen**
</dt> <dd>

Das Ergebnis ist das Ziel, das der Quelle hinzugefügt wird. Result = Quelle + Ziel

</dd> <dt>

<span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**D3DBLENDOP \_ subtrahieren**
</dt> <dd>

Das Ergebnis ist das Ziel, das von an die Quelle subtrahiert wird. Result = Quelle-Ziel

</dd> <dt>

<span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP \_ revsubtract**
</dt> <dd>

Das Ergebnis ist die Quelle, die vom Ziel subtrahiert wird. Result = Ziel-Quelle

</dd> <dt>

<span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP \_ Min.**
</dt> <dd>

Das Ergebnis ist das Minimalwert der Quelle und des Ziels. Ergebnis = min (Quelle, Ziel)

</dd> <dt>

<span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP \_ Max**
</dt> <dd>

Das Ergebnis ist der Höchstwert der Quelle und des Ziels. Result = Max (Quelle, Ziel)

</dd> <dt>

<span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Quelle, Ziel und Ergebnis werden wie folgt definiert:



| Begriff        | type   | BESCHREIBUNG                                                            |
|-------------|--------|------------------------------------------------------------------------|
| `Source`      | Eingabe  | Farbe des Quell Pixels vor dem Vorgang.                        |
| Destination | Eingabe  | Farbe des Pixels im Ziel Puffer vor dem Vorgang.     |
| Ergebnis      | Ausgabe | Der zurückgegebene Wert, der die aus dem Vorgang resultierende gemischte Farbe ist. |



 

Dieser enumerierte Typ definiert die Werte, die von den folgenden Rendering-Zuständen verwendet werden:

-   D3DRS \_ blendop
-   D3DRS \_ blendopalpha

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
