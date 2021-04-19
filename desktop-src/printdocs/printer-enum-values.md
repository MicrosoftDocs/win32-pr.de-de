---
description: Die \_ Struktur der druckeraufgabenwerte \_ gibt den Wert Namen, den Typ und die Daten für einen von der enumprinterdataex-Funktion zurückgegebenen Drucker Konfigurations Wert an.
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: PRINTER_ENUM_VALUES Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_ENUM_VALUES
- _PRINTER_ENUM_VALUESA
- _PRINTER_ENUM_VALUESW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ea73318db7a91fa4d422624b1c3c0c6f09d97cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362310"
---
# <a name="printer_enum_values-structure"></a>Struktur der druckerenumerationswerte \_ \_

Die Struktur der **druckeraufgabenwerte \_ \_** gibt den Wert Namen, den Typ und die Daten für einen von der [**enumprinterdataex**](enumprinterdataex.md) -Funktion zurückgegebenen Drucker Konfigurations Wert an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_ENUM_VALUES {
  LPTSTR pValueName;
  DWORD  cbValueName;
  DWORD  dwType;
  LPBYTE pData;
  DWORD  cbData;
} PRINTER_ENUM_VALUES, *PPRINTER_ENUM_VALUES;
```



## <a name="members"></a>Member

<dl> <dt>

**pvaluename**
</dt> <dd>

Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des abgerufenen Werts angibt.

</dd> <dt>

**cbvaluename**
</dt> <dd>

Die Anzahl der Bytes im **pvaluename** -Member, einschließlich des abschließenden NULL-Zeichens.

</dd> <dt>

**dwType**
</dt> <dd>

Ein Code, der den Typ der Daten angibt, auf die der **pData** -Member verweist. Eine Liste der möglichen Typcodes finden Sie unter [Registrierungs Werttypen](/windows/desktop/SysInfo/registry-value-types).

</dd> <dt>

**pData**
</dt> <dd>

Zeiger auf einen Puffer, der die Daten für den abgerufenen Wert enthält.

</dd> <dt>

**cbData**
</dt> <dd>

Die Anzahl von Bytes, die im **pData** -Puffer abgerufen wurden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ \_ Druckerenum \_ valuesw** (Unicode) und **\_ Printer \_ Enum \_ valuesa** (ANSI)<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Enumprinterdataex**](enumprinterdataex.md)
</dt> </dl>

 

