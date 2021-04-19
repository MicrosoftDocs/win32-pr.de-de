---
description: Definiert den hellen Typ.
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: D3DLIGHTTYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHTTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 83c94db3126443f757f01a69d7d773417f70683a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357246"
---
# <a name="d3dlighttype-enumeration"></a>D3DLIGHTTYPE-Enumeration

Definiert den hellen Typ.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DLIGHTTYPE { 
  D3DLIGHT_POINT        = 1,
  D3DLIGHT_SPOT         = 2,
  D3DLIGHT_DIRECTIONAL  = 3,
  D3DLIGHT_FORCE_DWORD  = 0x7fffffff
} D3DLIGHTTYPE, *LPD3DLIGHTTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**D3DLIGHT \_ Punkt**
</dt> <dd>

Light ist eine Punktquelle. Das Licht hat eine Position im Raum und strahlt das Licht in alle Richtungen aus.

</dd> <dt>

<span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT \_ Spot**
</dt> <dd>

Light ist eine Spotlight-Quelle. Dieses Licht ist wie ein Punktlicht, mit dem Unterschied, dass die Beleuchtung auf einen Kegel beschränkt ist. Dieser Light-Typ hat eine Richtung und einige andere Parameter, die die Form des von ihm erzeugten Diagrammes bestimmen. Weitere Informationen zu diesen Parametern finden Sie in der [**D3DLIGHT9**](d3dlight9.md) -Struktur.

</dd> <dt>

<span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT \_ direktional**
</dt> <dd>

Light ist eine direktionale Lichtquelle. Dies entspricht der Verwendung einer Point Light-Quelle in unbegrenzter Entfernung.

</dd> <dt>

<span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Direktionale Lichter sind etwas schneller als Punktlicht Quellen, aber die Punkt Lichter sehen etwas besser aus. Die Scheinwerfer bieten interessante visuelle Effekte, sind aber Rechenzeit aufwändig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DLIGHT9**](d3dlight9.md)
</dt> </dl>

 

 




