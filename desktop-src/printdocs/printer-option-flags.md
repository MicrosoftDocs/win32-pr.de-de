---
description: Gibt das Caching eines Handles für einen mit OpenPrinter2 geöffneten Drucker an.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: PRINTER_OPTION_FLAGS-Enumeration (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTION_FLAGS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 683ad70b5db12c11a2bccd11905e7ef87fce1bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217538"
---
# <a name="printer_option_flags-enumeration"></a>\_Druckeroptionsflags- \_ Enumeration

Gibt das Caching eines Handles für einen mit [**OpenPrinter2**](openprinter2.md)geöffneten Drucker an.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**Drucker \_ Option " \_ kein \_ Cache"**
</dt> <dd>

Das Handle wird nicht zwischengespeichert. Alle Funktionen, die auf ein von [**OpenPrinter2**](openprinter2.md) zurück gegebenes handle angewendet werden, werden auf den Remote Computer übertragen.

</dd> <dt>

<span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**Drucker \_ options \_ Cache**
</dt> <dd>

Das Handle wird zwischengespeichert. Alle Funktionen, die auf ein von [**OpenPrinter2**](openprinter2.md) zurück gegebenes handle angewendet werden, werden in den lokalen Cache übertragen.

</dd> <dt>

<span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**Drucker \_ Option \_ Client \_ Änderung**
</dt> <dd>

Das von [**OpenPrinter2**](openprinter2.md) zurückgegebene Handle kann von [**SetPrinter**](setprinter.md) zum Umbenennen der Druckerverbindung verwendet werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 




