---
description: Die \_ PRINTER INFO \_ 9-Struktur gibt die Standarddruckereinstellungen pro Benutzer an.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: PRINTER_INFO_9-Struktur (Winspool.h)
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
ms.openlocfilehash: 684ffc6ccfc4f94c036bde42faec9458c8bb60911fc8c9398006f58631baa791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234235"
---
# <a name="printer_info_9-structure"></a>PRINTER \_ INFO \_ 9-Struktur

Die **PRINTER \_ INFO \_ 9-Struktur** gibt die Standarddruckereinstellungen pro Benutzer an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a>Member

<dl> <dt>

**pDevMode**
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die die Standarddruckerdaten pro Benutzer definiert, z. B. die Papierausrichtung und die Auflösung. **DevMODE** wird in der Registrierung des Benutzers gespeichert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Standardwerte pro Benutzer wirken sich nur auf einen bestimmten Benutzer oder jede Person aus, die das Profil verwendet. Im Gegensatz dazu werden die globalen Standardwerte vom Administrator eines Druckers festgelegt, der von jedem verwendet werden kann. Verwenden Sie für globale Standardwerte [**PRINTER \_ INFO \_ 8.**](printer-info-8.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ PRINTER \_ INFO \_ 9W** (Unicode) und **\_ PRINTER INFO \_ \_ 9A** (ANSI)<br/>                           |



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

[**DRUCKERINFORMATIONEN \_ \_ 8**](printer-info-8.md)
</dt> </dl>

 

 




