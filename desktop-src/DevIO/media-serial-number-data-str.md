---
description: Enthält die Seriennummer eines USB-Geräts. Sie wird vom IOCTL \_ STORAGE GET MEDIA SERIAL \_ \_ \_ \_ NUMBER-Steuerungscode verwendet.
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: MEDIA_SERIAL_NUMBER_DATA-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SERIAL_NUMBER_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: cbb007769238f0e6a4239366e8fe9956e61f892f7d3c98f2b638dc425dc9359f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053480"
---
# <a name="media_serial_number_data-structure"></a>MEDIA \_ SERIAL \_ NUMBER \_ DATA-Struktur

Enthält die Seriennummer eines USB-Geräts. Sie wird vom [**IOCTL \_ STORAGE GET MEDIA SERIAL \_ \_ \_ \_ NUMBER-Steuerungscode**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct _MEDIA_SERIAL_NUMBER_DATA {
  ULONG SerialNumberLength;
  ULONG Result;
  ULONG Reserved[2];
  UCHAR SerialNumberData[];
} MEDIA_SERIAL_NUMBER_DATA, *PMEDIA_SERIAL_NUMBER_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**SerialNumberLength**
</dt> <dd>

Die Größe der **SerialNumberData-Zeichenfolge** in Bytes.

</dd> <dt>

**Ergebnis**
</dt> <dd>

Der Status der Anforderung.

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**SerialNumberData**
</dt> <dd>

Die Seriennummer des Geräts.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Für die MEDIA SERIAL NUMBER DATA-Struktur ist **\_ keine \_ \_ Headerdatei** verfügbar. Fügen Sie die Strukturdefinition oben auf dieser Seite in Ihren Quellcode ein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOCTL \_ STORAGE \_ GET \_ MEDIA \_ SERIAL \_ NUMBER**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




