---
description: Die Drucker \_ Info \_ 8-Struktur gibt die globalen Standarddrucker Einstellungen an.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: PRINTER_INFO_8 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_8
- _PRINTER_INFO_8A
- _PRINTER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e17780dc2f39dc3041e690de1ef7b5728c8743e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868340"
---
# <a name="printer_info_8-structure"></a>Drucker \_ Info \_ 8-Struktur

Die **Drucker \_ Info \_ 8** -Struktur gibt die globalen Standarddrucker Einstellungen an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a>Member

<dl> <dt>

**pdevmode**
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die globalen Standarddrucker Daten definiert, z. b. die Papier Ausrichtung und die Auflösung.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die globalen Standardwerte werden vom Administrator eines Druckers festgelegt, der von jedem verwendet werden kann. Im Gegensatz dazu wirken sich die benutzerspezifischen Standardeinstellungen auf einen bestimmten Benutzer oder andere Benutzer aus, die das Profil verwenden. Verwenden Sie für benutzerspezifische Standardeinstellungen [**Drucker \_ Informationen \_ 9**](printer-info-9.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Drucker \_ Info \_ 8W** (Unicode) und **\_ Drucker \_ Info \_ 8a** (ANSI)<br/>                           |



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

[**Drucker \_ Informationen \_ 9**](printer-info-9.md)
</dt> </dl>

 

 




