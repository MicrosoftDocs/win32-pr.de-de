---
description: Die \_ PRINTER INFO \_ 3-Struktur gibt Druckersicherheitsinformationen an.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: PRINTER_INFO_3-Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c6b9bc249921b3247f5df898c2810d735dc1a75c8e643e965b3fd249d9496f78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867925"
---
# <a name="printer_info_3-structure"></a>PRINTER \_ INFO \_ 3-Struktur

Die **PRINTER \_ INFO \_ 3-Struktur** gibt Druckersicherheitsinformationen an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a>Member

<dl> <dt>

**pSecurityDescriptor**
</dt> <dd>

Zeiger auf eine [**SECURITY \_ DESCRIPTOR-Struktur,**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) die die Sicherheitsinformationen eines Druckers angibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Mit der **PRINTER \_ INFO \_ 3-Struktur** kann eine Anwendung die Sicherheitsbeschreibung eines Druckers abrufen und festlegen. Der Aufrufer kann dies auch tun, wenn ihm bestimmte Druckerberechtigungen fehlen, solange er über die in [**SetPrinter**](setprinter.md) und [**GetPrinter**](getprinter.md)beschriebenen Standardrechte verfügt. Daher kann eine Anwendung vorübergehend jeglichen Zugriff auf einen Drucker verweigern, während der Besitzer des Druckers Zugriff auf die bedingte Zugriffssteuerungsliste des Druckers haben kann.

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

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**\_SICHERHEITSBESCHREIBUNG**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

