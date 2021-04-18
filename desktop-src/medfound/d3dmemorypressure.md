---
description: Diese Struktur enthält Daten für die Arbeitsspeicher Auslastung.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: D3DMEMORYPRESSURE-Struktur (D3d9types. h) für Microsoft Media Foundation
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
ms.openlocfilehash: 7400c4822b61a84ab288f0424cfa84e825e69dc9
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106371590"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a>D3DMEMORYPRESSURE-Struktur (D3d9types. h) für Microsoft Media Foundation

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

Die Anzahl der Bytes, die während der Abfrage Dauer vom Prozess entfernt wurden.

</dd> <dt>

**Sizeofinefficientallocation**
</dt> <dd>

Die Gesamtanzahl der Bytes, die in nicht optimalen Speicher Segmenten abgelegt werden, aufgrund unzureichenden Speicherplatzes innerhalb der bevorzugten Speichersegmente.

</dd> <dt>

**Levelofefficiency**
</dt> <dd>

Die Gesamteffizienz der Speicher Belegungen, die im nicht optimalen Arbeitsspeicher platziert wurden. Der Wert wird als Prozentsatz ausgedrückt. Der Wert 95 gibt beispielsweise an, dass die in nicht bevorzugten Speicher Segmenten platzierten Zuordnungen 95% effizient sind. Diese Zahl sollte nicht als exakte Messung angesehen werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows 7 \[ -Desktop-Apps\]                                                              |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]                                                 |
| Header                  | D3d9types. h (Include d3d9. h) |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Video Strukturen](direct3d-video-structures.md)
</dt> <dt>

[Berichterstellung für Speicherauslastung](memory-pressure-reporting.md)
</dt> </dl>

 

 




