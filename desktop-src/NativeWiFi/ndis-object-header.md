---
description: Verpackt die Objekttyp-, Versions-und Größen Informationen, die in vielen NDIS 6,0-Strukturen benötigt werden.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: NDIS_OBJECT_HEADER Struktur (ntddndis. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDIS_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- ntddndis.h
ms.openlocfilehash: fe28a87eeb1457bace0b72a386bcb07667b24a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347563"
---
# <a name="ndis_object_header-structure"></a>NDIS- \_ Objekt \_ Header Struktur

Die **NDIS- \_ Objekt \_ Header** Struktur verpackt die Objekttyp-, Versions-und Größen Informationen, die in vielen NDIS 6,0-Strukturen benötigt werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _NDIS_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Size;
} NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**Type**
</dt> <dd>

Gibt den Typ des NDIS-Objekts an, das von einer Struktur beschrieben wird.

</dd> <dt>

**Novel**
</dt> <dd>

Gibt die Revisionsnummer dieser Struktur an.

</dd> <dt>

**Größe**
</dt> <dd>

Gibt die Gesamtgröße der NDIS-Struktur (in Bytes) an, die den **NDIS- \_ Objekt \_ Header** enthält. Diese Größe enthält die Größe des **NDIS- \_ Objekt \_ Header** Members und aller anderen Member der Struktur.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                       |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                                                        |
| Header<br/>                   | <dl> <dt>Ntddndis. h (Include Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_BSSID- \_ Liste DOT11**](dot11-bssid-list.md)
</dt> </dl>

 

 




