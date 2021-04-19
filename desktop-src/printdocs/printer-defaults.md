---
description: Die Struktur der Drucker Standards \_ gibt den Standard Datentyp, die Umgebung, die Initialisierungs Daten und die Zugriffsrechte für einen Drucker an.
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: PRINTER_DEFAULTS Struktur (winspool. h)
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
ms.openlocfilehash: ad3f9b2a6647c620b2d947bca5ef5201076e23ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363553"
---
# <a name="printer_defaults-structure"></a>Struktur der Drucker Standards \_

Die **Struktur \_ der Drucker** Standards gibt den Standard Datentyp, die Umgebung, die Initialisierungs Daten und die Zugriffsrechte für einen Drucker an.

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

**pdatatype**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Standard Datentyp für einen Drucker angibt.

</dd> <dt>

**pdevmode**
</dt> <dd>

Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die Standardumgebung und die Initialisierungs Daten für einen Drucker identifiziert.

</dd> <dt>

**DesiredAccess**
</dt> <dd>

Gibt die gewünschten Zugriffsrechte für einen Drucker an. Die [**OpenPrinter**](openprinter.md) -Funktion verwendet dieses Element, um die Zugriffsrechte für den Drucker festzulegen. Diese Rechte können sich auf den Betrieb der Funktionen [**SetPrinter**](setprinter.md) und [**deleteprinter**](deleteprinter.md) auswirken. Die Zugriffsrechte können eines der folgenden sein:



| Wert                                       | Bedeutung                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Drucker \_ Zugriffs \_ Verwaltung                 | Zum Ausführen administrativer Aufgaben, wie z. b. die von [**SetPrinter**](setprinter.md)bereitgestellten.                                                                                                 |
| Drucker \_ Zugriffs \_ Verwendung                        | Zum Ausführen grundlegender Druckvorgänge.                                                                                                                                                        |
| Drucker \_ Zugriff \_ mit \_ eingeschränkter Verwaltung            | Zum Ausführen administrativer Aufgaben, wie z. b. die von [**SetPrinter**](setprinter.md) und [**setprinterdata**](setprinterdata.md)bereitgestellten. Dieser Wert ist ab Windows 8.1 verfügbar. |
| Drucker \_ \_ Zugriff                        | Zum Ausführen aller Verwaltungsaufgaben und grundlegenden Druckvorgänge mit Ausnahme von Synchronisierung (siehe [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) ).                                   |
| generische Sicherheitswerte, z. b. \_ DAC schreiben | , Um bestimmte Zugriffsrechte für das Steuerelement zuzulassen. Siehe [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Drucker \_ defaultsw** (Unicode) und **\_ Drucker \_ defaultsa** (ANSI)<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Deleteprinter**](deleteprinter.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

