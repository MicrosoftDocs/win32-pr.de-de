---
description: Definiert den Lichttyp.
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: D3DLIGHTTYPE-Enumeration (D3D9Types.h)
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
ms.openlocfilehash: 66aefec5d614e5fc51f82741fbb30ace71222997273b7647c0bf51f2d5038878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804775"
---
# <a name="d3dlighttype-enumeration"></a>D3DLIGHTTYPE-Enumeration

Definiert den Lichttyp.

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

<span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**D3DLIGHT \_ POINT**
</dt> <dd>

Licht ist eine Punktquelle. Das Licht hat eine Position im Raum und glüht in alle Richtungen.

</dd> <dt>

<span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT \_ SPOT**
</dt> <dd>

Licht ist eine Spotlightquelle. Dieses Licht ist wie ein Punktlicht, mit der Ausnahme, dass die Glühbirnen auf einen Kegel beschränkt sind. Dieser Lichttyp hat eine Richtung und mehrere andere Parameter, die die Form des Kegels bestimmen, den er erzeugt. Informationen zu diesen Parametern finden Sie in der [**D3DLIGHT9-Struktur.**](d3dlight9.md)

</dd> <dt>

<span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT \_ DIRECTIONAL**
</dt> <dd>

Licht ist eine direktionale Lichtquelle. Dies entspricht der Verwendung einer Punktlichtquelle in unendlicher Entfernung.

</dd> <dt>

<span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Richtungslichter sind etwas schneller als Punktlichtquellen, aber Punktlichter sehen etwas besser aus. Spotlights bieten interessante visuelle Effekte, sind aber rechenintensiv.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DLIGHT9**](d3dlight9.md)
</dt> </dl>

 

 




