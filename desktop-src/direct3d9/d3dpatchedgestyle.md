---
description: Definiert, ob der aktuelle Mosaik Modus diskret oder kontinuierlich ist.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: D3DPATCHEDGESTYLE-Enumeration (D3D9Types. h)
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
ms.openlocfilehash: e625b7c4ff12f9859efdcc2b10b551a2223adab6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870131"
---
# <a name="d3dpatchedgestyle-enumeration"></a>D3DPATCHEDGESTYLE-Enumeration

Definiert, ob der aktuelle Mosaik Modus diskret oder kontinuierlich ist.

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

<span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ diskret**
</dt> <dd>

Diskreter Randstil. Im diskreten Modus können Sie das%%%%%%%%%%%%%%%%%%%%%%%%

</dd> <dt>

<span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ fortlaufend**
</dt> <dd>

Fortlaufender Edge-Stil. Im kontinuierlichen Modus wird das Mosaik als float-Werte angegeben, die problemlos variieren können, um "Popping"-Artefakte zu verringern.

</dd> <dt>

<span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass das kontinuierliche Mosaik Modell ein vollkommen anderes Mosaikmuster als das diskrete Mosaikmuster für die gleichen Mosaik Werte erzeugt (Dies ist im Draht Modell deutlicher erkennbar). Daher ist 4,0 Continuous nicht mit 4 diskret identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




