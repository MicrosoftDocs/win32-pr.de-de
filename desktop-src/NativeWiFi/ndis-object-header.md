---
description: Packt die Objekttyp-, Versions- und Größeninformationen, die in vielen NDIS 6.0-Strukturen erforderlich sind.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: NDIS_OBJECT_HEADER-Struktur (Ntddndis.h)
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
ms.openlocfilehash: f9f4a4ef2a833081cde0c3c7ca4d395e59743944291a95d7680c241191988b35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065050"
---
# <a name="ndis_object_header-structure"></a>NDIS \_ OBJECT \_ HEADER-Struktur

Die **NDIS \_ OBJECT \_ HEADER-Struktur** packt die Objekttyp-, Versions- und Größeninformationen, die in vielen NDIS 6.0-Strukturen erforderlich sind.

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

**Typ**
</dt> <dd>

Gibt den Typ des NDIS-Objekts an, das von einer -Struktur beschrieben wird.

</dd> <dt>

**Revision**
</dt> <dd>

Gibt die Revisionsnummer dieser Struktur an.

</dd> <dt>

**Größe**
</dt> <dd>

Gibt die Gesamtgröße der NDIS-Struktur in Bytes an, die den **NDIS \_ OBJECT \_ HEADER** enthält. Diese Größe schließt die Größe des **NDIS \_ OBJECT \_ HEADER-Elements** und aller anderen Member der -Struktur ein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP nur mit \[ SP3-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                       |
| Verteilbare Komponente<br/>          | WLAN-API für Windows XP mit SP2<br/>                                                        |
| Header<br/>                   | <dl> <dt>Ntddndis.h (einschließlich Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DOT11 \_ BSSID \_ LIST**](dot11-bssid-list.md)
</dt> </dl>

 

 




