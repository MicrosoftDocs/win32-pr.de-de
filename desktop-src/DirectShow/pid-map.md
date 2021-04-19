---
description: Die PID \_ -Karten Struktur enthält den Inhalt einer MPEG-2-Transportdaten Strom-Paket-ID.
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: PID_MAP-Struktur (bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PID_MAP
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 98b238c61ccfcfb93e4ddcc0a051d9084228f604
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361679"
---
# <a name="pid_map-structure"></a>PID- \_ Karten Struktur

Die- `PID_MAP` Struktur enthält den Inhalt einer MPEG-2-Transportdaten Strom-Paket-ID.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a>Member

<dl> <dt>

**ulpid**
</dt> <dd>

Gibt die Paket-ID (PID) an.

</dd> <dt>

**Mediasamplecontent**
</dt> <dd>

Gibt den Inhalt der Paket Nutzlast als den Enumerationstyp " [**Media \_ Sample \_ Content**](media-sample-content.md) " an.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Bdatypes. h (Include bmolface. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Strukturen](directshow-structures.md)
</dt> <dt>

[**Ienumpidmap-Schnittstelle**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




