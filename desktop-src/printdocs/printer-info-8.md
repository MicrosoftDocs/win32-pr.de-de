---
description: Die \_ PRINTER INFO \_ 8-Struktur gibt die globalen Standarddruckereinstellungen an.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: PRINTER_INFO_8-Struktur (Winspool.h)
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
ms.openlocfilehash: 0aa5d516dd099caeba5699a8328fa52add64f14ea970e6ccec28ea8bfbe87271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947670"
---
# <a name="printer_info_8-structure"></a>PRINTER \_ INFO \_ 8-Struktur

Die **PRINTER \_ INFO \_ 8-Struktur** gibt die globalen Standarddruckereinstellungen an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a>Member

<dl> <dt>

**pDevMode**
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die die globalen Standarddruckerdaten definiert, z. B. die Papierausrichtung und die Auflösung.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die globalen Standardwerte werden vom Administrator eines Druckers festgelegt, der von jedem verwendet werden kann. Im Gegensatz dazu wirken sich die Standardwerte pro Benutzer auf einen bestimmten Benutzer oder jede andere Person aus, die das Profil verwendet. Verwenden Sie für Standardeinstellungen pro Benutzer [**PRINTER \_ INFO \_ 9**](printer-info-9.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ PRINTER \_ INFO \_ 8W** (Unicode) und **\_ PRINTER INFO \_ \_ 8A** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 9**](printer-info-9.md)
</dt> </dl>

 

 




