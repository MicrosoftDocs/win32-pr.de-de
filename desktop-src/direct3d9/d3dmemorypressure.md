---
description: Enthält Daten für die Arbeitsspeicher Auslastung.
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: D3DMEMORYPRESSURE-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5917d1e61817f401106ae14aa5a0f98cd75b0d42
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363150"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a>D3DMEMORYPRESSURE-Struktur (D3d9types. h)

Enthält Daten für die Arbeitsspeicher Auslastung.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a>Member

<dl> <dt>

**Bytesevictedfromprocess**
</dt> <dd>

Typ: **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Anzahl der Bytes, die während der Abfrage Dauer vom Prozess entfernt wurden.

</dd> <dt>

**Sizeofinefficientallocation**
</dt> <dd>

Typ: **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Gesamtanzahl der Bytes, die in nicht optimalen Speicher Segmenten abgelegt werden, aufgrund unzureichenden Speicherplatzes innerhalb der bevorzugten Speichersegmente.

</dd> <dt>

**Levelofefficiency**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Gesamteffizienz der Speicher Belegungen, die im nicht optimalen Arbeitsspeicher platziert wurden. Der Wert wird als Prozentsatz ausgedrückt. Der Wert 95 gibt beispielsweise an, dass die in nicht bevorzugten Speicher Segmenten platzierten Zuordnungen 95% effizient sind. Diese Zahl sollte nicht als exakte Messung angesehen werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
