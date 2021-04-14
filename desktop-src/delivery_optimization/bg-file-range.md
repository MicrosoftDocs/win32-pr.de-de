---
title: BG_FILE_RANGE-Struktur (deliveryoptimization. h)
description: Die BG_FILE_RANGE-Struktur identifiziert einen Bereich von Bytes, der aus einer Datei heruntergeladen werden soll.
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- BG_FILE_RANGE Struktur
topic_type:
- apiref
api_name:
- BG_FILE_RANGE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cedabfb066a5905adb2ed8eac9996fd77c0e12be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392129"
---
# <a name="bg_file_range-structure"></a>BG_FILE_RANGE Struktur

Die **BG_FILE_RANGE** -Struktur identifiziert einen Bereich von Bytes, der aus einer Datei heruntergeladen werden soll.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a>Member

<dl> <dt>

**Initialoffset**
</dt> <dd>

NULL basierter Offset am Anfang des Bereichs von Bytes, der aus einer Datei heruntergeladen werden soll.

</dd> <dt>

**Länge**
</dt> <dd>

Die Länge des Bereichs in Bytes. Geben Sie keine Byte Länge von 0 (null) an. Um anzugeben, dass der Bereich bis zum Ende der Datei reicht, geben Sie **BG_LENGTH_TO_EOF** an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Bereich muss in der Datei vorhanden sein, oder es wird ein **DO_E_INVALID_RANGE** Fehler generiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyFile2:: getfileranges**](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 





