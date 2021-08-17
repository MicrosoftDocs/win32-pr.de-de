---
description: Definiert Bitmuster, die benutzerdefinierte Clippingebenen ermöglichen. Diese Makros werden als Praktisches definiert, wenn Werte für den D3DRS \_ CLIPPLANEENABLE-Renderzustand festgelegt werden.
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: D3DCLIPPLANEn-Makro (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPPLANEn
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 315f1cdd8f8835b869f04edd9869243f3e05a9c2c9a08a41eeffc014727b3fc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805467"
---
# <a name="d3dclipplanen-macro"></a>D3DCLIPPLANEn-Makro

Definiert Bitmuster, die benutzerdefinierte Clippingebenen ermöglichen. Diese Makros werden als Praktisches definiert, wenn Werte für den D3DRS \_ CLIPPLANEENABLE-Renderzustand festgelegt werden.

## <a name="syntax"></a>Syntax


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a>Parameter

Dieses Makro verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Benutzerdefinierte Clippingebenen werden aktiviert, wenn der im D3DRS \_ CLIPPLANEENABLE-Renderzustand festgelegte Wert ein oder mehrere festgelegte Bits enthält (d.amp;quot;nicht 0%%amp;quot;). Der Wert des Renderzustands ist nicht wichtig. das System interpretiert den Wert nicht als Zahl. Stattdessen aktiviert der Wert die Clippingebene, deren entsprechendes Bit festgelegt ist. Bit 0 steuert den Zustand der ersten Clippingebene (bei Index 0), Bit 1 die zweite Ebene usw.

Die Bitmuster, die diese Makros erstellen, können mithilfe eines logischen OR-Vorgangs kombiniert werden, um gleichzeitig mehrere Clippingebenen zu aktivieren. Wenn Sie eines dieser Makros aus der Kombination weglassen, wird die Clippingebene an diesem Index effektiv deaktiviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




