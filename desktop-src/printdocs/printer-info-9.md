---
description: Die Drucker \_ Info \_ 9-Struktur gibt die Standarddrucker Einstellungen pro Benutzer an.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: PRINTER_INFO_9 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_9
- _PRINTER_INFO_9A
- _PRINTER_INFO_9W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c0ae3c099da17d7fc437a67035d8da2cd00136bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350905"
---
# <a name="printer_info_9-structure"></a>Drucker \_ Info \_ 9-Struktur

Die **Drucker \_ Info \_ 9** -Struktur gibt die Standarddrucker Einstellungen pro Benutzer an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a>Member

<dl> <dt>

**pdevmode**
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die Standarddrucker Daten des Benutzers definiert, z. b. die Papier Ausrichtung und die Auflösung. **DEVMODE** wird in der Registrierung des Benutzers gespeichert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die benutzerspezifischen Standardeinstellungen wirken sich nur auf einen bestimmten Benutzer oder auf alle Benutzer aus, die das Profil verwenden. Im Gegensatz dazu werden die globalen Standardwerte vom Administrator eines Druckers festgelegt, der von jedem verwendet werden kann. Verwenden Sie bei globalen Standardeinstellungen [**Drucker \_ Informationen \_ 8**](printer-info-8.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Drucker \_ Informationen \_ 9W** (Unicode) und **\_ Drucker \_ Info \_ 9a** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 8**](printer-info-8.md)
</dt> </dl>

 

 




