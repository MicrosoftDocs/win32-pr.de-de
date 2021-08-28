---
description: Beschreibt die Auflösung des Schatten-Z-Puffers, der in der direkten Beleuchtungssimulation precomputed Radiance Transfer (PRT) auf der GPU verwendet wird.
ms.assetid: 05354328-9b6f-45f5-a913-47ede170b03f
title: D3DXSLKPUSLIPPT-Enumeration (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHGPUSIMOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a73323dc9d6596f848fa50fe6dc21e236a5b9f2d4362b3c2a27cf773d3939fac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849750"
---
# <a name="d3dxshgpusimopt-enumeration"></a>D3DXSLKPUSLIPPT-Enumeration

Beschreibt die Auflösung des Schatten-Z-Puffers, der in der direkten Beleuchtungssimulation precomputed Radiance Transfer (PRT) auf der GPU verwendet wird. Es kann auch ein qualitativ hochwertigerer Z-Puffer angegeben werden, um Rauschen in den Ergebnissen der direkten Beleuchtungssimulation zu reduzieren, obwohl die Simulation langsamer ist.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXSHGPUSIMOPT { 
  D3DXSHGPUSIMOPT_SHADOWRES256   = 1,
  D3DXSHGPUSIMOPT_SHADOWRES512   = 0,
  D3DXSHGPUSIMOPT_SHADOWRES1024  = 2,
  D3DXSHGPUSIMOPT_SHADOWRES2048  = 3,
  D3DXSHGPUSIMOPT_HIGHQUALITY    = 4,
  D3DXSHGPUSIMOPT_FORCE_DWORD    = 0x7fffffff
} D3DXSHGPUSIMOPT, *LPD3DXSHGPUSIMOPT;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSLKPUSLIPPT \_ SHADOWRES256**
</dt> <dd>

Simulation mit niedriger Auflösung. In der Simulation wird eine Textur mit 256 x 256 Pixeln verwendet, um den Schatten-Z-Puffer zu codieren.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSLKPUSLIPPT \_ SHADOWRES512**
</dt> <dd>

Simulation mit mittlerer Auflösung. Eine Textur mit 512 x 512 Pixeln wird in der Simulation verwendet, um den Schatten-Z-Puffer zu codieren. Dies ist der Standardwert.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSLKPUSLIPPT \_ SHADOWRES1024**
</dt> <dd>

Simulation mit hoher Auflösung. Eine Textur mit 1024 x 1024 Pixel wird in der Simulation verwendet, um den Schatten z-Puffer zu codieren.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSLKPUSLIPPT \_ SHADOWRES2048**
</dt> <dd>

Simulation mit der höchsten Auflösung. Eine Textur mit 2048 x 2048 Pixel wird in der Simulation verwendet, um den Schatten z-Puffer zu codieren.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSLKPUSLIPPT \_ HIGHQUALITY**
</dt> <dd>

Die Simulation ist unabhängig von der ausgewählten Auflösung von hoher Genauigkeit. Wenn Sie diesen Wert festlegen, wird das Rauschen in den Ergebnissen der simulation der direkten Beleuchtung reduziert, obwohl die Simulation langsamer ist. Kann mit einem der Auflösungswerte kombiniert werden.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSLKPUSLIPPT \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Es kann nur einer der Auflösungswerte angegeben und mit dem hochwertigen Wert kombiniert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




