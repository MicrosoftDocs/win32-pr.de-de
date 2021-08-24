---
description: Prozentsatz der Zeit für die Verarbeitung von Daten in der Pipeline.
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: D3DDEVINFO_D3D9PIPELINETIMINGS-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9PIPELINETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4d938fd2e1ca0f52d2ea7787f54b430a84907ad5f04f066bc90f0867825745a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676740"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a>D3DDEVINFO \_ D3D9PIPELINETIMINGS-Struktur

Prozentsatz der Zeit für die Verarbeitung von Daten in der Pipeline.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DDEVINFO_D3D9PIPELINETIMINGS {
  FLOAT VertexProcessingTimePercent;
  FLOAT PixelProcessingTimePercent;
  FLOAT OtherGPUProcessingTimePercent;
  FLOAT GPUIdleTimePercent;
} D3DDEVINFO_D3D9PIPELINETIMINGS, *LPD3DDEVINFO_D3D9PIPELINETIMINGS;
```



## <a name="members"></a>Member

<dl> <dt>

**VertexProcessingTimePercent**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz der Zeit, die für die Ausführung von Vertex-Shadern aufgewendet wurde.

</dd> <dt>

**PixelProcessingTimePercent**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz der Zeit, die für die Ausführung von Pixel-Shadern aufgewendet wurde.

</dd> <dt>

**OtherGPUProcessingTimePercent**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz der Für andere Verarbeitung aufgewendeten Zeit.

</dd> <dt>

**GPUIdleTimePercent**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz der Zeit, in der nichts verarbeitet wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Für eine optimale Leistung wird eine ausgeglichene Last empfohlen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
