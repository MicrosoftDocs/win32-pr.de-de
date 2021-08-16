---
description: Enthält Informationen zur Größe eines Geräts. Dies wird vom IOCTL \_ STORAGE \_ READ \_ CAPACITY-Steuerungscode zurückgegeben.
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: STORAGE_READ_CAPACITY -Struktur (Ntddstor.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_READ_CAPACITY
api_type:
- HeaderDef
api_location:
- Ntddstor.h
ms.openlocfilehash: 3a138f6594e241c96526ebf6955c61374aa0f48a5aa66f364ef82c1591b64594
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404971"
---
# <a name="storage_read_capacity-structure"></a>\_ \_ SPEICHERLESEKAPAZITÄTsstruktur

Enthält Informationen zur Größe eines Geräts. Dies wird vom [**IOCTL \_ STORAGE READ \_ \_ CAPACITY-Steuerungscode**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) zurückgegeben.

## <a name="syntax"></a>Syntax


```C++
typedef struct _STORAGE_READ_CAPACITY {
  ULONG         Version;
  ULONG         Size;
  ULONG         BlockLength;
  LARGE_INTEGER NumberOfBlocks;
  LARGE_INTEGER DiskLength;
} STORAGE_READ_CAPACITY, *PSTORAGE_READ_CAPACITY;
```



## <a name="members"></a>Member

<dl> <dt>

**Version**
</dt> <dd>

Die Version dieser -Struktur. Der Aufrufer muss diesen Member auf `sizeof(STORAGE_READ_CAPACITY)` festlegen.

</dd> <dt>

**Größe**
</dt> <dd>

Die Größe der zurückgegebenen Daten.

</dd> <dt>

**BlockLength**
</dt> <dd>

Die Anzahl der Bytes pro Block.

</dd> <dt>

**NumberOfBlocks**
</dt> <dd>

Die Gesamtanzahl der Blöcke auf dem Datenträger.

</dd> <dt>

**DiskLength**
</dt> <dd>

Die Datenträgergröße in Bytes.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Headerdatei Ntddstor.h ist im Windows Driver Kit (WDK) verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2003 mit SP1<br/>                          |
| Header<br/>                   | <dl> <dt>Ntddstor.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LESEKAPAZITÄT FÜR \_ \_ IOCTL-SPEICHER \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




