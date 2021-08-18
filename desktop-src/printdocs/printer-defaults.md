---
description: Die PRINTER \_ DEFAULTS-Struktur gibt den Standarddatentyp, die Umgebung, die Initialisierungsdaten und die Zugriffsrechte für einen Drucker an.
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: PRINTER_DEFAULTS -Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_DEFAULTS
- _PRINTER_DEFAULTSA
- _PRINTER_DEFAULTSW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: f1419948dddcd579e559ed084ce0af092cec373a7cd7f6d4b05d41f104f6666b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731688"
---
# <a name="printer_defaults-structure"></a>PRINTER \_ DEFAULTS-Struktur

Die **PRINTER \_ DEFAULTS-Struktur** gibt den Standarddatentyp, die Umgebung, die Initialisierungsdaten und die Zugriffsrechte für einen Drucker an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_DEFAULTS {
  LPTSTR      pDatatype;
  LPDEVMODE   pDevMode;
  ACCESS_MASK DesiredAccess;
} PRINTER_DEFAULTS, *PPRINTER_DEFAULTS;
```



## <a name="members"></a>Member

<dl> <dt>

**pDatatype**
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die den Standarddatentyp für einen Drucker angibt.

</dd> <dt>

**pDevMode**
</dt> <dd>

Zeiger auf eine [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die die Standardumgebung und initialisierungsdaten für einen Drucker identifiziert.

</dd> <dt>

**DesiredAccess**
</dt> <dd>

Gibt die gewünschten Zugriffsrechte für einen Drucker an. Die [**OpenPrinter-Funktion**](openprinter.md) verwendet diesen Member, um Zugriffsrechte für den Drucker zu festlegen. Diese Rechte können sich auf den Betrieb der [**Funktionen SetPrinter**](setprinter.md) [**und DeletePrinter**](deleteprinter.md) auswirken. Die Zugriffsrechte können wie folgt sein.



| Wert                                       | Bedeutung                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ DRUCKERZUGRIFFSVERWALTUNG                 | So führen Sie administrative Aufgaben aus, z. B. die von [**SetPrinter bereitgestellten.**](setprinter.md)                                                                                                 |
| \_ \_ DRUCKERZUGRIFFSNUTZUNG                        | So führen Sie grundlegende Druckvorgänge aus.                                                                                                                                                        |
| DRUCKERZUGRIFF \_ \_ VERWALTEN \_ EINGESCHRÄNKT            | So führen Sie administrative Aufgaben aus, z. B. die von [**SetPrinter**](setprinter.md) und [**SetPrinterData bereitgestellten.**](setprinterdata.md) Dieser Wert ist ab dem Windows 8.1. |
| DRUCKERZUGRIFF \_ \_ AUF ALLE                        | So führen Sie alle administrativen Aufgaben und grundlegenden Druckvorgänge mit Ausnahme von SYNCHRONIZE aus (siehe [Standardzugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) ).                                   |
| Generische Sicherheitswerte, z. B. WRITE \_ DAC | So lassen Sie bestimmte Zugriffsberechtigungen für die Steuerung zu. Weitere Informationen [finden Sie unter Standardzugriffsrechte.](/windows/desktop/SecAuthZ/standard-access-rights)                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ PRINTER \_ DEFAULTSW** (Unicode) und **\_ PRINTER \_ DEFAULTSA** (ANSI)<br/>                         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

