---
description: Enthält Informationen über das Laufwerk, das im aktiven Datei-Manager-Fenster ausgewählt wurde (das Verzeichnisfenster oder das Fenster Suchergebnisse).
title: FMS_GETDRIVEINFO-Struktur (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 14f8a90b-d0ed-4818-a719-8fc4ea617bef
ms.openlocfilehash: 107e12e1076a2fc928ecb9b578ab01d64898a83a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842231"
---
# <a name="fms_getdriveinfo-structure"></a>FMS \_ GETDRIVEINFO-Struktur

Enthält Informationen über das Laufwerk, das im aktiven Datei-Manager-Fenster ausgewählt wurde (das Verzeichnisfenster oder das Fenster Suchergebnisse).

## <a name="syntax"></a>Syntax


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**dwTotalSpace**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Gesamtmenge des Speicherplatzes in Bytes auf dem Datenträger, der dem Laufwerk zugeordnet ist.

</dd> <dt>

**dwFreeSpace**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Menge des freien Speicherplatzes in Bytes auf dem Datenträger, der dem Laufwerk zugeordnet ist.

</dd> <dt>

**szPath**
</dt> <dd>

Typ: **TCHAR \[ 260 \]**

</dd> <dd>

der mit NULL endende Pfad des aktuellen Verzeichnisses.

</dd> <dt>

**szVolume**
</dt> <dd>

Typ: **TCHAR \[ 14 \]**

</dd> <dd>

Die auf NULL endende Volumebezeichnung des Datenträgers, der dem Laufwerk zugeordnet ist.

</dd> <dt>

**szShare**
</dt> <dd>

Typ: **TCHAR \[ 128 \]**

</dd> <dd>

Der auf NULL endende Name der Netzwerkressource (wenn über ein Netzwerk auf das Laufwerk zugegriffen wird).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FM \_ GETDRIVEINFO**](fm-getdriveinfo.md)
</dt> </dl>

 

 




