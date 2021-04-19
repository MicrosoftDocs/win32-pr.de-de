---
description: Der Prozentsatz der Zeit, die shaderdaten verarbeitet.
ms.assetid: 388bb943-c25f-4b50-b7e4-d6259f1186c2
title: D3DDEVINFO_D3D9STAGETIMINGS-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9STAGETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cf8c9522decfcbb09a60aff0bee65ca05a0f5eeb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355796"
---
# <a name="d3ddevinfo_d3d9stagetimings-structure"></a>D3DDEVINFO \_ D3D9STAGETIMINGS-Struktur

Der Prozentsatz der Zeit, die shaderdaten verarbeitet.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DDEVINFO_D3D9STAGETIMINGS {
  FLOAT MemoryProcessingPercent;
  FLOAT ComputationProcessingPercent;
} D3DDEVINFO_D3D9STAGETIMINGS, *LPD3DDEVINFO_D3D9STAGETIMINGS;
```



## <a name="members"></a>Member

<dl> <dt>

**Memoryprocessingprozent**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Prozentsatz der Zeit im Shader, der für Speicherzugriffe aufgewendet wurde.

</dd> <dt>

**Computationprocessingprozent**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz der Zeit Verarbeitung (Verschieben von Daten in Registern oder Durchführung mathematischer Vorgänge).

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

 

 
