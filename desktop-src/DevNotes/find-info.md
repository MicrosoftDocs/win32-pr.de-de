---
description: Enthält Such Kontextinformationen.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: FIND_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIND_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7d6b6dea42c008178c22f6e342a64b2f8d193ec5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345609"
---
# <a name="find_info-structure"></a>\_Informationsstruktur suchen

Enthält Such Kontextinformationen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _FIND_INFO {
  TAGID     tiIndex;
  TAGID     tiCurrent;
  TAGID     tiEndIndex;
  TAG       tName;
  DWORD     dwIndexRec;
  DWORD     dwFlags;
  ULONGLONG ullKey;
  union {
    LPCTSTR szName;
    DWORD   dwName;
    GUID    *pguidName;
  };
} FIND_INFO, *PFIND_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**tiindex**
</dt> <dd>

Die **TagID** für den Index, der gesucht werden soll.

</dd> <dt>

**ticurrent**
</dt> <dd>

Die **TagID** für das aktuelle Element, das gefunden wurde.

</dd> <dt>

**tikodindex**
</dt> <dd>

Die **TagID** für den letzten Datensatz nach FindFirst, wenn der Index eindeutig ist.

</dd> <dt>

**tName**
</dt> <dd>

Der Typ des zu suchenden Elements. Siehe [Tagtypen](tag-types.md).

</dd> <dt>

**dwindexrec**
</dt> <dd>

Ein interner Indikator, mit dem nachverfolgt wird, wo im Index der nächste Suchvorgang beginnen soll.

</dd> <dt>

**dwFlags**
</dt> <dd>

Dieser Member kann 0 oder ein eindeutiger **shimdb- \_ Index \_ \_** (0x00000001) sein, was darauf hinweist, dass es sich hierbei um einen eindeutigen Schlüssel Index handelt.

</dd> <dt>

**ullkey**
</dt> <dd>

Der Schlüssel für den aktuellen Eintrag.

</dd> <dt>

**szName**
</dt> <dd>

Die aktuelle Zeichenfolge (wenn der Tagtyp **" \_ TagType \_**" ist).

</dd> <dt>

**dwname**
</dt> <dd>

Der aktuelle **DWORD** -Wert (wenn der Tagtyp **\_ \_ DWORD** ist).

</dd> <dt>

**pguidname**
</dt> <dd>

Der aktuelle GUID-Wert (wenn der Tagtyp **\_ \_ Binär** ist und das Tag eine **\_ Tagdatenbank- \_ ID** ist).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbfindfirstdwordindexedtag**](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




