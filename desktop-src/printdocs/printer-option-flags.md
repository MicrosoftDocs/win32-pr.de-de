---
description: Gibt das Zwischenspeichern eines Handles für einen mit OpenPrinter2 geöffneten Drucker an.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: PRINTER_OPTION_FLAGS -Enumeration (Winspool.h)
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
ms.openlocfilehash: b8541ec00f0d53bf58a826ceb7d8b8a821008fb6a66c0fe3917ebc12822e0e5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091800"
---
# <a name="printer_option_flags-enumeration"></a>PRINTER \_ OPTION \_ FLAGS-Enumeration

Gibt das Zwischenspeichern eines Handles für einen mit [**OpenPrinter2 geöffneten Drucker an.**](openprinter2.md)

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

<span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**DRUCKEROPTION \_ \_ KEIN \_ CACHE**
</dt> <dd>

Das Handle wird nicht zwischengespeichert. Alle Funktionen, die auf ein von [**OpenPrinter2**](openprinter2.md) zurückgegebenes Handle angewendet werden, werden an den Remotecomputer übertragen.

</dd> <dt>

<span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**\_ \_ DRUCKEROPTIONSCACHE**
</dt> <dd>

Das Handle wird zwischengespeichert. Alle Funktionen, die auf ein von [**OpenPrinter2**](openprinter2.md) zurückgegebenes Handle angewendet werden, werden in den lokalen Cache übertragen.

</dd> <dt>

<span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**\_DRUCKEROPTION \_ \_ CLIENTÄNDERUNG**
</dt> <dd>

Das von [**OpenPrinter2 zurückgegebene**](openprinter2.md) Handle kann von [**SetPrinter**](setprinter.md) verwendet werden, um die Druckerverbindung umzubenennen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 




