---
description: Definiert Konstanten, die den Modus "Mode" beschreiben.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: D3DFOGMODE-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFOGMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6b94992d94779932301c271ca46dc7466344b40b68c62855d4c57bfe8b780a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791973"
---
# <a name="d3dfogmode-enumeration"></a>D3DFOGMODE-Enumeration

Definiert Konstanten, die den Modus "Mode" beschreiben.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DFOGMODE { 
  D3DFOG_NONE         = 0,
  D3DFOG_EXP          = 1,
  D3DFOG_EXP2         = 2,
  D3DFOG_LINEAR       = 3,
  D3DFOG_FORCE_DWORD  = 0x7fffffff
} D3DFOGMODE, *LPD3DFOGMODE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ NONE**
</dt> <dd>

Kein Effekt.

</dd> <dt>

<span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ EXP**
</dt> <dd>

Der Effekt "Effect" wird exponentiell gemäß der folgenden Formel potenziert.

![Formel der Intensität des Effekts "1"](images/fogexp.png)

</dd> <dt>

<span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ EXP2**
</dt> <dd>

Der Effekt "Effect Effect" wird exponentiell mit dem Quadrat der Entfernung gemäß der folgenden Formel potenziert.

![Formel der Intensität des Effekts", die auf dem Quadrat der Entfernung basiert](images/fogexp2.png)

</dd> <dt>

<span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG \_ LINEAR**
</dt> <dd>

Der Effekt "Lichteffekt" wird gemäß der folgenden Formel linear zwischen dem Start- und dem Endpunkte geschwennt.

![Formel der Intensität von Effekten auf der Grundlage von Start- und Endpunkten](images/fogliner.png)

Dies ist der einzige derzeit unterstützte Modus.

</dd> <dt>

<span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Werte in diesem Enumerationstyp werden von den Renderzuständen D3DRSTABLEMODE und \_ D3DRSRSVERTEXMODE \_ verwendet.

Die Sichtbarkeit kann als Maß für die Sichtbarkeit angesehen werden: Wenn der durch eine Gleichung erzeugte Maßwert niedriger ist, desto weniger sichtbar ist ein Objekt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
