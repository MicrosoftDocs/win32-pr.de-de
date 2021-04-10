---
description: Die mxdc \_ PrintTicket \_ Data \_ T-Struktur enthält ein XPS-Dokument-Druck Ticket, das Drucker-und Druckauftrags Einstellungen enthält, die an die Microsoft XPS Document Converter (mxdc)-Ausgabedatei ohne Verarbeitung übergeben werden.
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: MXDC_PRINTTICKET_DATA_T-Struktur (mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 94308527437316dda75fc5a50a6a7829e9315c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864960"
---
# <a name="mxdc_printticket_data_t-structure"></a>Mxdc- \_ PrintTicket- \_ Daten \_ Struktur

Die **mxdc \_ PrintTicket \_ Data \_ T** -Struktur enthält ein XPS-Dokument-Druck Ticket, das Drucker-und Druckauftrags Einstellungen enthält, die an die Microsoft XPS Document Converter (mxdc)-Ausgabedatei ohne Verarbeitung übergeben werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMxdcPrintTicketData {
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_PRINTTICKET_DATA_T, *P_MXDC_PRINTTICKET_DATA_T;
```



## <a name="members"></a>Member

<dl> <dt>

**dwDataSize**
</dt> <dd>

Die Größe des Druck Tickets in Bytes.

</dd> <dt>

**bData**
</dt> <dd>

Das XPS-Dokument-Druck Ticket.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird an eine [**mxdc- \_ Escape- \_ Header- \_ T**](mxdcescapeheader.md) -Struktur angehängt, bei der der **Opcode** -Member auf **mxdcop \_ PrintTicket \_ Fixed \_ Page**, **mxdcop \_ PrintTicket \_ Fixed \_ doc** oder **mxdcop \_ PrintTicket Fixed \_ \_ doc \_** festgelegt ist, um eine [**mxdc \_ PrintTicket \_ Escape- \_ t**](mxdcprintticketescape.md) -Struktur zu erstellen. Die **mxdc \_ PrintTicket \_ Escape \_ T** -Struktur wird dann an den *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben, wenn Sie mit dem Escapezeichen " [**mxdc \_**](mxdc-escape.md) " aufgerufen wird. Der Effekt besteht darin, das Druck Ticket in die XPS-Dokument Datei zu schreiben.

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

 

