---
title: WINBIO_BIR_DATA Struktur (winbio \_ types. h)
description: Gibt die Größe (in Bytes) und den Offset eines Blocks biometrischer Informationen an.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- WINBIO_BIR_DATA Struktur Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ebf7b157c5bd806442cdc120350a89ce646f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391881"
---
# <a name="winbio_bir_data-structure"></a>Winbio \_ Bir- \_ Datenstruktur

Die **\_ \_ Datenstruktur "winbio Bir** " gibt die Größe, in Bytes und den Offset eines Blocks biometrischer Informationen an. Diese Struktur wird von der [**winbio \_ Bir**](winbio-bir.md) -Struktur verwendet, um anzugeben, wo sich die verschiedenen Teile eines biometrischen Informations Satzes befinden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**Größe**
</dt> <dd>

Größe (in Bytes) der biometrischen Informationen.

</dd> <dt>

**Offset**
</dt> <dd>

Der Offset der biometrischen Informationen in Bytes vom Anfang der [**winbio \_**](winbio-bir.md) -Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Verwendung von Offsets anstelle von Zeigern ermöglicht die einfache Serialisierung von Bir und für eine weniger komplizierte Übersetzung zwischen 32-und 64-Bit-Umgebungen oder zwischen Benutzer-und Kernel Modus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Strukturen](client-application-structures.md)
</dt> <dt>

[**winbio \_ Bir**](winbio-bir.md)
</dt> <dt>

[**winbio- \_ Bir- \_ Header**](winbio-bir-header.md)
</dt> </dl>

 

 





