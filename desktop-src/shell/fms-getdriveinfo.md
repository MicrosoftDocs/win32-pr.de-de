---
description: Enthält Informationen über das im aktiven Datei-Manager-Fenster (im Verzeichnis Fenster oder im Fenster "Suchergebnisse") ausgewählte Laufwerk.
title: FMS_GETDRIVEINFO-Struktur (WF. h)
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
ms.openlocfilehash: b19b54d89f74fa122effa5853beb2961e0ddf1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979697"
---
# <a name="fms_getdriveinfo-structure"></a>FMS \_ getdriveingefo-Struktur

Enthält Informationen über das im aktiven Datei-Manager-Fenster (im Verzeichnis Fenster oder im Fenster "Suchergebnisse") ausgewählte Laufwerk.

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

**dwtotalspace**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Gesamtmenge des Speicherplatzes in Bytes auf dem Datenträger, der dem Laufwerk zugeordnet ist.

</dd> <dt>

**dwfreespace**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der freie Speicherplatz in Bytes auf dem Datenträger, der dem Laufwerk zugeordnet ist.

</dd> <dt>

**szpath**
</dt> <dd>

Typ: **TCHAR \[ 260 \]**

</dd> <dd>

der NULL terminierte Pfad des aktuellen Verzeichnisses.

</dd> <dt>

**szvolume**
</dt> <dd>

Typ: **TCHAR \[ 14 \]**

</dd> <dd>

Die mit NULL terminierte Volumebezeichnung des Datenträgers, der dem Laufwerk zugeordnet ist.

</dd> <dt>

**szshare**
</dt> <dd>

Typ: **TCHAR \[ 128 \]**

</dd> <dd>

Der NULL-terminierte Name der Netzwerkressource (wenn über ein Netzwerk auf das Laufwerk zugegriffen wird).

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"F"**](fmextensionproc.md)
</dt> <dt>

[**FM \_ getdriveingefo**](fm-getdriveinfo.md)
</dt> </dl>

 

 




