---
title: MPRESOURCE_STATS -Struktur (MpClient.h)
description: Ressourcenbezogene Statistiken.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- MPRESOURCE_STATS struktur Legacy Windows Umgebungsfeatures
- PMPRESOURCE_STATS strukturzeiger Legacy-Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPRESOURCE_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72a21bf0ec020c1fc2cf5ba1394b4cd5ed04dc32721a4aac9f8349034907b49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848470"
---
# <a name="mpresource_stats-structure"></a>MPRESOURCE \_ STATS-Struktur

Ressourcenbezogene Statistiken.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPRESOURCE_STATS {
  DWORD  PPMProgress;
  UINT64 ProcessCount;
  UINT64 FileCount;
  UINT64 FileBytesCount;
  UINT64 RegKeyCount;
  UINT64 Reserved[4];
} MPRESOURCE_STATS, *PMPRESOURCE_STATS;
```



## <a name="members"></a>Member

<dl> <dt>

**PPMProgress**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Ungefährer Fortschritt für die Überprüfung in ppm (Teile pro Million). Legen Sie **auf MPPROGRESS \_ INVALID fest,** wenn keine Statusinformationen verfügbar sind.

</dd> <dt>

**ProcessCount**
</dt> <dd>

Typ: **UINT64**

</dd> <dd>

Anzahl der überprüften Prozesse.

</dd> <dt>

**FileCount**
</dt> <dd>

Typ: **UINT64**

</dd> <dd>

Anzahl der gescannten Dateien.

</dd> <dt>

**FileBytesCount**
</dt> <dd>

Typ: **UINT64**

</dd> <dd>

Anzahl von Bytes, die auf Dateien überprüft wurden.

</dd> <dt>

**RegKeyCount**
</dt> <dd>

Typ: **UINT64**

</dd> <dd>

Anzahl der überprüften RegKeys.

</dd> <dt>

**Reserved**
</dt> <dd>

Typ: **UINT64 \[ 4 \]**

</dd> <dd>

Felder, die für die zukünftige Verwendung reserviert sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





