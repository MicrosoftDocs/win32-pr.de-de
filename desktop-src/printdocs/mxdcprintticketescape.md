---
description: Die mxdc \_ PrintTicket \_ Escape \_ t-Struktur ist eine mxdc-Escape-Header-t-Struktur, die \_ \_ \_ mit einer mxdc \_ PrintTicket \_ Data T-Struktur verkettet ist \_ .
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: MXDC_PRINTTICKET_ESCAPE_T-Struktur (mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 158ee2038c83b74077d00e6922b2c7050b76bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369843"
---
# <a name="mxdc_printticket_escape_t-structure"></a>Mxdc \_ PrintTicket \_ Escape- \_ T-Struktur

Die **mxdc \_ PrintTicket \_ Escape \_ t** -Struktur ist eine [**mxdc- \_ Escape-Header- \_ \_ t**](mxdcescapeheader.md) -Struktur, die mit einer [**mxdc \_ PrintTicket \_ Data \_ T**](mxdcprintticketpassthrough.md) -Struktur verkettet ist.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a>Member

<dl> <dt>

**mxdcescape**
</dt> <dd>

Eine [**mxdc- \_ Escape- \_ Header- \_ T**](mxdcescapeheader.md) -Struktur, deren **Opcode** -Member auf mxdcop \_ PrintTicket \_ Fixed \_ Page, mxdcop \_ PrintTicket \_ Fixed \_ doc oder mxdcop \_ PrintTicket \_ Fixed doc (Fixed \_ doc \_ ) festgelegt ist.

</dd> <dt>

**printticketdata**
</dt> <dd>

Eine [**mxdc \_ PrintTicket \_ Data \_ T**](mxdcprintticketpassthrough.md) -Struktur, die das Druck Ticket enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird in den *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben, wenn diese Funktion mit der escapeescapezeichen [**mxdc \_**](mxdc-escape.md) aufgerufen wird und das **Opcode** -Element der [**mxdc- \_ Escape-Header- \_ \_ T**](mxdcescapeheader.md) -Struktur **mxdcop \_ PrintTicket \_ Fixed \_ Page**, **mxdcop \_ PrintTicket Fixed \_ \_ doc** oder **mxdcop \_ PrintTicket \_ Fixed \_ doc \_** Das Ergebnis ist, das Druck Ticket in die XPS-Dokument Datei zu schreiben.

Weisen Sie der Escapesequenz wie unten gezeigt den Speicher zu, legen Sie die Felder nach Bedarf fest, und nennen Sie dann [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



Wenn **Opcode** auf **mxdcop \_ PrintTicket \_ Fixed \_ Page** festgelegt ist, muss der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Aufrufe zwischen einem Aufrufen von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufrufen von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)erfolgen. Wenn der **Opcode** entweder auf **mxdcop \_ PrintTicket \_ Fixed \_ doc** oder **mxdcop \_ PrintTicket \_ Fixed \_ doc \_** festgelegt ist, muss der **extescape** -Befehl zwischen einem [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) -Befehl und einem- [**Endpunkt**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mxdc. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[Escapefunktionen für GDI-Drucker](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**Extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**mxdc-Escapezeichen \_**](mxdc-escape.md)
</dt> </dl>

 

