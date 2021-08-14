---
description: Definiert, ob der aktuelle Mosaikmodus diskret oder kontinuierlich ist.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: D3DPATCHEDGESTYLE-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 717139a33e260aa29bc8d0e244fa49b3cb324c5249614f513faf0624ccf21841
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987240"
---
# <a name="d3dpatchedgestyle-enumeration"></a>D3DPATCHEDGESTYLE-Enumeration

Definiert, ob der aktuelle Mosaikmodus diskret oder kontinuierlich ist.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ DISCRETE**
</dt> <dd>

Diskreter Edgestil. Im diskreten Modus können Sie float tessellation angeben, aber es wird auf ganze Zahlen abgeschnitten.

</dd> <dt>

<span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ CONTINUOUS**
</dt> <dd>

Fortlaufender Edgestil. Im fortlaufenden Modus wird das Mosaik als float-Werte angegeben, die reibungslos variiert werden können, um "Pop"-Artefakte zu reduzieren.

</dd> <dt>

<span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie, dass das kontinuierliche Mosaik ein völlig anderes Mosaikmuster als das diskrete Mosaikmuster für die gleichen Mosaikwerte erzeugt (dies ist im Wireframe-Modus offensichtlicher). Daher ist 4.0 continuous nicht identisch mit vier diskreten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




