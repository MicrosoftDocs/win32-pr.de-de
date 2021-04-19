---
title: Wmdmdatetime-Struktur
description: Die wmdmdatetime-Struktur enthält ein Datum und eine Uhrzeit.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Wmdmdatetime-Struktur Windows Media Device Manager
- Pwmdmdatetime-Struktur Zeiger Windows Media-Device Manager
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
ms.openlocfilehash: 07acf706aa63a21edd27fb2ac206db3039249055
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359212"
---
# <a name="wmdmdatetime-structure"></a>Wmdmdatetime-Struktur

Die **wmdmdatetime** -Struktur enthält ein Datum und eine Uhrzeit.

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

Word, das die vierstellige Jahres Angabe enthält.

</dd> <dt>

**wMonth**
</dt> <dd>

Word, das den Monat (1-12) enthält.

</dd> <dt>

**wDay**
</dt> <dd>

Word, das den Tag des Monats enthält (1-31).

</dd> <dt>

**wHour**
</dt> <dd>

Word, das die Stunde (0-23) enthält.

</dd> <dt>

**wMinute**
</dt> <dd>

Word, das die Minute (0-59) enthält.

</dd> <dt>

**wSecond**
</dt> <dd>

Word, das das zweite enthält (0-59).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imdspstorage:: GETDATE**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[**Iwmdmstorage:: GETDATE**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[**Wmdmrights**](wmdmrights.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





