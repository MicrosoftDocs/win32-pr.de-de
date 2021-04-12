---
description: Enthält Informationen zur Größe eines Geräts. Dies wird vom IOCTL- \_ Speicher \_ Lese- \_ Kapazitäts Steuerungs Code zurückgegeben.
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: STORAGE_READ_CAPACITY Struktur (ntddstor. h)
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
ms.openlocfilehash: e57a9f4420b977598e15f9aae219c060665c9d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392990"
---
# <a name="storage_read_capacity-structure"></a>\_Kapazitäts Struktur zum Lesen des Speichers \_

Enthält Informationen zur Größe eines Geräts. Dies wird vom [**IOCTL- \_ Speicher \_ Lese- \_ Kapazitäts**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) Steuerungs Code zurückgegeben.

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

Die Version dieser-Struktur. Der Aufrufer muss diesen Member auf festlegen `sizeof(STORAGE_READ_CAPACITY)` .

</dd> <dt>

**Größe**
</dt> <dd>

Die Größe der zurückgegebenen Daten.

</dd> <dt>

**Blocklength**
</dt> <dd>

Die Anzahl der Bytes pro Block.

</dd> <dt>

**NumberOfBlocks**
</dt> <dd>

Die Gesamtanzahl der Blöcke auf dem Datenträger.

</dd> <dt>

**Disklength**
</dt> <dd>

Die Datenträger Größe in Byte.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Header Datei "ntddstor. h" ist im Windows-Treiberkit (WDK) verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2003 mit SP1<br/>                          |
| Header<br/>                   | <dl> <dt>Ntddstor. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOCTL- \_ Speicher \_ Lese \_ Kapazität**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




