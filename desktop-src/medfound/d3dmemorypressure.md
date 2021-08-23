---
description: Diese Struktur enthält Daten für die Berichterstellung zur Arbeitsspeicherauslastung.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: D3DMEMORYPRESSURE-Struktur (D3d9types.h) für Microsoft Media Foundation
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
ms.openlocfilehash: ec6fdf0d27edb5e1cafa575664b07dfe0807c8d124e1b066161734e75247709f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449420"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a>D3DMEMORYPRESSURE-Struktur (D3d9types.h) für Microsoft Media Foundation

Enthält Daten für die Berichterstellung zur Arbeitsspeicherauslastung.

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

**BytesEvictedFromProcess**
</dt> <dd>

Die Anzahl der Bytes, die während der Dauer der Abfrage vom Prozess entfernt wurden.

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

Die Gesamtanzahl von Bytes, die aufgrund unzureichenden Speicherplatzes innerhalb der bevorzugten Speichersegmente in nicht optimalen Speichersegmenten platziert werden.

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

Die Gesamteffizienz der Speicherbelegungen, die im nicht optimalen Speicher platziert wurden. Der Wert wird als Prozentsatz ausgedrückt. Der Wert 95 gibt beispielsweise an, dass die Zuordnungen, die in nicht abgeleiteten Speichersegmenten platziert werden, zu 95 % effizient sind. Diese Zahl sollte nicht als genaue Messung betrachtet werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | nur Windows 7 \[ Desktop-Apps\]                                                              |
| Unterstützte Mindestversion (Server) | Windows Nur Server 2008 \[ R2-Desktop-Apps\]                                                 |
| Header                  | D3d9types.h (einschließlich D3d9.h) |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Videostrukturen](direct3d-video-structures.md)
</dt> <dt>

[Berichterstellung zu Auslastung des Arbeitsspeichers](memory-pressure-reporting.md)
</dt> </dl>

 

 




