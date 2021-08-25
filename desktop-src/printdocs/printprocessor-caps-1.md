---
description: Die PRINTPROCESSOR \_ CAPS \_ 1-Struktur ist das Format für die Druckerfunktionsinformationen, die von der GetPrinterData-Funktion in dem von der pData-Variablen angegebenen Puffer zurückgegeben werden.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: PRINTPROCESSOR_CAPS_1-Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d057914ef9a77c7a545817b205f919afa66fdd3bc154363f7e33a9a5ba43c446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824790"
---
# <a name="printprocessor_caps_1-structure"></a>PRINTPROCESSOR \_ CAPS \_ 1-Struktur

Die **PRINTPROCESSOR \_ CAPS \_ 1-Struktur** ist das Format für die Druckerfunktionsinformationen, die von der [**GetPrinterData-Funktion**](getprinterdata.md) in dem von der *pData-Variablen* angegebenen Puffer zurückgegeben werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a>Member

<dl> <dt>

**dwLevel**
</dt> <dd>

Die Versionsnummer der Struktur. Dieser Wert muss 1 sein.

</dd> <dt>

**dwNupOptions**
</dt> <dd>

Eine Bitmaske, die die verschiedenen Zahlen von Dokumentseiten darstellt, die der Drucker auf einer physischen Seite drucken kann. Das am wenigsten signifikante Bit stellt eine Dokumentseite pro Seite dar, das nächste Bit stellt 2 Dokumentseiten pro Seite dar usw. 0x0000810B gibt beispielsweise an, dass der Drucker 1, 2, 4, 9 und 16 Dokumentseiten pro physischer Seite unterstützt.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

Die Reihenfolge, in der Seiten gedruckt werden. Dieser Wert kann NORMAL \_ PRINT, REVERSE \_ PRINT oder PRINT \_ PRINT sein.

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

Die maximale Anzahl von Kopien, die der Drucker verarbeiten kann.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Werte für alle Strukturmember werden von der [**GetPrintProcessorCapabilities-Funktion**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) bereitgestellt, die im Windows Driver Kit (WDK) dokumentiert ist.

Der Spooler ruft die [**GetPrintProcessorCapabilities-Funktion**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) eines Druckprozessors auf, wenn eine Anwendung [**GetPrinterData**](getprinterdata.md)aufruft und einen Wertnamen mit dem Format PrintProcCaps-Datentyp \_ angibt, wobei *datatype* der Name eines Eingabedatentyps ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

