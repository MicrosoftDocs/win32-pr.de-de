---
title: MPRESOURCE_STATS Struktur (mpclient. h)
description: Ressourcenbezogene Statistiken.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- MPRESOURCE_STATS Struktur Funktionen der Legacy-Windows-Umgebung
- PMPRESOURCE_STATS Struktur Zeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: afbe1ce6734aabd1093f7acd886af757c51ed83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477658"
---
# <a name="mpresource_stats-structure"></a>Mpresource- \_ Statistik Struktur

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

**Ppmprogress**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der ungefähre Fortschritt für die Überprüfung in ppm (Teile pro Million). Legen Sie auf **mpprogress \_ ungültig** fest, wenn keine Fortschrittsinformationen verfügbar sind.

</dd> <dt>

**ProcessCount**
</dt> <dd>

Typ: **UINT64**

</dd> <dd>

Anzahl der gescannten Prozesse.

</dd> <dt>

**FileCount**
</dt> <dd>

Typ: **UINT64**

</dd> <dd>

Anzahl der gescannten Dateien.

</dd> <dt>

**Filebytescount**
</dt> <dd>

Typ: **UINT64**

</dd> <dd>

Anzahl von Bytes, die für Dateien gescannt wurden.

</dd> <dt>

**Regkeycount**
</dt> <dd>

Typ: **UINT64**

</dd> <dd>

Anzahl der gescannten Regkeys.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





