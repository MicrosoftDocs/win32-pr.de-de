---
description: Die PRINTER \_ ENUM \_ VALUES-Struktur gibt den Wertnamen, den Typ und die Daten für einen Druckerkonfigurationswert an, der von der EnumPrinterDataEx-Funktion zurückgegeben wird.
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: PRINTER_ENUM_VALUES-Struktur (Winspool.h)
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
ms.openlocfilehash: a2b6fd8e548353dbede634d7b3bbaa08023d5e7bc2c8bc4cefbe37f7aba494ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470577"
---
# <a name="printer_enum_values-structure"></a>PRINTER \_ ENUM \_ VALUES-Struktur

Die **PRINTER \_ ENUM \_ VALUES-Struktur** gibt den Wertnamen, den Typ und die Daten für einen Druckerkonfigurationswert an, der von der [**EnumPrinterDataEx-Funktion**](enumprinterdataex.md) zurückgegeben wird.

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

**pValueName**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des abgerufenen Werts angibt.

</dd> <dt>

**cbValueName**
</dt> <dd>

Die Anzahl der Bytes im **pValueName-Member,** einschließlich des abschließenden NULL-Zeichens.

</dd> <dt>

**dwType**
</dt> <dd>

Ein Code, der den Datentyp angibt, auf den der **pData-Member** zeigt. Eine Liste der möglichen Typcodes finden Sie unter [Registrierungswerttypen.](/windows/desktop/SysInfo/registry-value-types)

</dd> <dt>

**Pdata**
</dt> <dd>

Zeiger auf einen Puffer, der die Daten für den abgerufenen Wert enthält.

</dd> <dt>

**cbData**
</dt> <dd>

Die Anzahl der im **pData-Puffer** abgerufenen Bytes.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ PRINTER \_ ENUM \_ VALUESW** (Unicode) und **\_ PRINTER \_ ENUM \_ VALUESA** (ANSI)<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> </dl>

 

