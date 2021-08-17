---
description: Enthält Suchkontextinformationen.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: FIND_INFO-Struktur
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
ms.openlocfilehash: 1ee5eb66928322019a455c78d71abf5461e56b1296ae79d94b83c40c2d45379e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404783"
---
# <a name="find_info-structure"></a>FIND \_ INFO-Struktur

Enthält Suchkontextinformationen.

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

**tiIndex**
</dt> <dd>

Die **TAGID** für den index, der durchsucht werden soll.

</dd> <dt>

**tiCurrent**
</dt> <dd>

Die **TAGID** für das aktuelle Element, das sich befindet.

</dd> <dt>

**tiEndIndex**
</dt> <dd>

Die **TAGID** für den letzten Datensatz nach FindFirst, wenn der Index UNIQUE ist.

</dd> <dt>

**tName**
</dt> <dd>

Der Typ des elements, das gefunden werden soll. Weitere Informationen finden Sie unter [TAG-Typen.](tag-types.md)

</dd> <dt>

**dwIndexRec**
</dt> <dd>

Ein interner Indikator, mit dem nachverfolgt wird, wo im Index der nächste Suchvorgang beginnen soll.

</dd> <dt>

**dwFlags**
</dt> <dd>

Dieser Member kann 0 oder **SHIMDB \_ INDEX \_ UNIQUE \_ KEY** (0x00000001) sein. Dies gibt an, dass es sich um einen eindeutigen Schlüsselindex handelt.

</dd> <dt>

**ullKey**
</dt> <dd>

Der Schlüssel für den aktuellen Eintrag.

</dd> <dt>

**Szname**
</dt> <dd>

Die aktuelle Zeichenfolge (wenn der Tagtyp **TAG \_ TYPE \_ STRINGREF** ist).

</dd> <dt>

**dwName**
</dt> <dd>

Der aktuelle **DWORD-Wert** (wenn der Tagtyp **TAG TYPE \_ \_ DWORD** ist).

</dd> <dt>

**pguidName**
</dt> <dd>

Der aktuelle GUID-Wert (wenn der Tagtyp **\_ TAGTYP \_ BINARY** und das TAG **TAG DATABASE \_ \_ ID** ist).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




