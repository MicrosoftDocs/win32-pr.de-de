---
description: Definiert Konstanten, die den Nebel Modus beschreiben.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: D3DFOGMODE-Enumeration (D3D9Types. h)
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
ms.openlocfilehash: 8436a52edbb9460c6945c1526513629939ec444b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355237"
---
# <a name="d3dfogmode-enumeration"></a>D3DFOGMODE-Enumeration

Definiert Konstanten, die den Nebel Modus beschreiben.

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

<span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ None**
</dt> <dd>

Kein Nebeleffekt.

</dd> <dt>

<span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG- \_ Exp**
</dt> <dd>

Der Nebeleffekt wird entsprechend der folgenden Formel exponentiell verstärkt.

![Formel der Nebeleffekt Intensität](images/fogexp.png)

</dd> <dt>

<span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ exp2**
</dt> <dd>

Der Nebeleffekt wird exponentiell mit dem Quadrat der Entfernung entsprechend der folgenden Formel verstärkt.

![Formel der Nebel Wirkungs Intensität basierend auf dem Quadrat der Entfernung](images/fogexp2.png)

</dd> <dt>

<span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG \_ linear**
</dt> <dd>

Der Nebeleffekt wird linear zwischen dem Start-und dem Endpunkt entsprechend der folgenden Formel verstärkt.

![Formel der Nebel Wirkungs Intensität basierend auf Start-und Endpunkten](images/fogliner.png)

Dies ist der einzige derzeit unterstützte Nebelmodus.

</dd> <dt>

<span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Werte in diesem enumerierten Typ werden von den \_ renderzuständen D3DRS fogtablemode und D3DRS \_ fogvertexmode verwendet.

Nebel kann als Maß der Sichtbarkeit betrachtet werden: je niedriger der von einer Nebel Gleichung erzeugte Nebelwert ist, desto weniger sichtbar ist ein Objekt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
