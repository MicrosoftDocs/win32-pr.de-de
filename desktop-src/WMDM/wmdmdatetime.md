---
title: WMDMDATETIME-Struktur
description: Die WMDMDATETIME-Struktur enthält ein Datum und eine Uhrzeit.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- WMDMDATETIME-Strukturfenster Media Geräte-Manager
- PWMDMDATETIME-Strukturzeigerfenster Media Geräte-Manager
topic_type:
- apiref
api_name:
- WMDMDATETIME
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9648b4c2d1272dcf00d45277119b51f438dba23d9eaf5e7810451fb693e8cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004630"
---
# <a name="wmdmdatetime-structure"></a>WMDMDATETIME-Struktur

Die **WMDMDATETIME-Struktur** enthält ein Datum und eine Uhrzeit.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WMDMDATETIME {
  WORD wYear;
  WORD wMonth;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
} WMDMDATETIME, *PWMDMDATETIME;
```



## <a name="members"></a>Member

<dl> <dt>

**wYear**
</dt> <dd>

Wort, das das vierstellige Jahr enthält.

</dd> <dt>

**wMonth**
</dt> <dd>

Wort, das den Monat enthält (1-12).

</dd> <dt>

**wDay**
</dt> <dd>

Wort, das den Tag des Monats (1-31) enthält.

</dd> <dt>

**wHour**
</dt> <dd>

Wort, das die Stunde enthält (0-23).

</dd> <dt>

**wMinute**
</dt> <dd>

Wort, das die Minute (0-59) enthält.

</dd> <dt>

**wSecond**
</dt> <dd>

Wort, das das zweite (0-59) enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMDSPStorage::GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[**IWMDMStorage::GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[**WMDMRIGHTS**](wmdmrights.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





