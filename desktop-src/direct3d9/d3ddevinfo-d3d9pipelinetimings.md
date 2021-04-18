---
description: Der Prozentsatz der Zeit, die Daten in der Pipeline verarbeitet.
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: D3DDEVINFO_D3D9PIPELINETIMINGS-Struktur (D3D9Types. h)
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
ms.openlocfilehash: 627eec0ea93181b14c308ab229ed603412511a91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354999"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a>D3DDEVINFO \_ D3D9PIPELINETIMINGS-Struktur

Der Prozentsatz der Zeit, die Daten in der Pipeline verarbeitet.

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

**Vertexprocessingtimeprozent**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Prozentsatz der Zeit für die Ausführung von Vertex-Shadern.

</dd> <dt>

**Pixelprocessingtimeprozent**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Prozentsatz der Zeit für die Ausführung von Pixelshadern.

</dd> <dt>

**Othergpuprocessingtimeprozent**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Prozentsatz der Zeit für die Verarbeitung anderer Verarbeitungsvorgänge.

</dd> <dt>

**Gpuidletimeprozent**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Prozentsatz der Zeit, die nichts verarbeitet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um eine optimale Leistung zu erzielen, wird eine ausgeglichene Auslastung empfohlen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
