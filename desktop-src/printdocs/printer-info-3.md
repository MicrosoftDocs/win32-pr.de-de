---
description: Die Drucker \_ Info \_ 3-Struktur gibt Drucker Sicherheitsinformationen an.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: PRINTER_INFO_3 Struktur (winspool. h)
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
ms.openlocfilehash: aad24e56d43f6fadd3da3f627b2399249a7ff8a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360725"
---
# <a name="printer_info_3-structure"></a>Drucker \_ Info \_ 3-Struktur

Die **Drucker \_ Info \_ 3** -Struktur gibt Drucker Sicherheitsinformationen an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a>Member

<dl> <dt>

**psecuritydescriptor**
</dt> <dd>

Ein Zeiger auf eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , die die Sicherheitsinformationen eines Druckers angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Drucker \_ Info \_ 3** -Struktur ermöglicht es einer Anwendung, die Sicherheits Beschreibung eines Druckers zu erhalten und festzulegen. Der Aufrufer kann dies auch dann tun, wenn ihm bestimmte Drucker Berechtigungen fehlen, sofern er über die in " [**SetPrinter**](setprinter.md) " und " [**GetPrinter**](getprinter.md)" beschriebenen Standardrechte verfügt. Folglich kann eine Anwendung vorübergehend den gesamten Zugriff auf einen Drucker verweigern, während der Besitzer des Druckers auf die freigegebene ACL des Druckers zugreifen kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 1**](printer-info-1.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 2**](printer-info-2.md)
</dt> <dt>

[**Drucker \_ Info \_ 4**](printer-info-4.md)
</dt> <dt>

[**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

