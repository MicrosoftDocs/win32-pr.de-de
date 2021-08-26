---
description: Gibt den Anweisungssatz an, für den D3DX derzeit optimiert ist.
ms.assetid: 5fc97028-4a9d-4bc7-9c90-236a70e570e1
title: D3DX_CPU_OPTIMIZATION-Enumeration (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_CPU_OPTIMIZATION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 7bb36b3aeb448933416148b087cb7e82619beef04186637c0bb3fa944a143da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989540"
---
# <a name="d3dx_cpu_optimization-enumeration"></a>D3DX \_ CPU \_ OPTIMIZATION-Enumeration

Gibt den Anweisungssatz an, für den D3DX derzeit optimiert ist.

## <a name="syntax"></a>Syntax


```C++
typedef enum _D3DX_CPU_OPTIMIZATION { 
  D3DX_NOT_OPTIMIZED    = 0,
  D3DX_3DNOW_OPTIMIZED  = 1,
  D3DX_SSE2_OPTIMIZED   = 2,
  D3DX_SSE_OPTIMIZED    = 3
} D3DX_CPU_OPTIMIZATION;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX_NOT_OPTIMIZED"></span><span id="d3dx_not_optimized"></span>**D3DX \_ NICHT \_ OPTIMIERT**
</dt> <dd>

Optimieren Sie nicht.

</dd> <dt>

<span id="D3DX_3DNOW_OPTIMIZED"></span><span id="d3dx_3dnow_optimized"></span>**D3DX \_ 3DNOW \_ OPTIMIERT**
</dt> <dd>

Optimieren für 3DNow! -Anweisungssatz.

</dd> <dt>

<span id="D3DX_SSE2_OPTIMIZED"></span><span id="d3dx_sse2_optimized"></span>**D3DX \_ SSE2 \_ OPTIMIERT**
</dt> <dd>

Optimieren sie für einen SSE2-Anweisungssatz.

</dd> <dt>

<span id="D3DX_SSE_OPTIMIZED"></span><span id="d3dx_sse_optimized"></span>**D3DX \_ SSE \_ OPTIMIZED**
</dt> <dd>

Optimieren für einen SSE-Anweisungssatz.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




