---
description: Die MXDC PRINTTICKET ESCAPE T-Struktur ist eine MXDC ESCAPE HEADER T-Struktur, die mit einer \_ \_ \_ \_ \_ \_ MXDC \_ PRINTTICKET \_ DATA \_ T-Struktur verkettet ist.
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: MXDC_PRINTTICKET_ESCAPE_T -Struktur (Mxdc.h)
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
ms.openlocfilehash: eca1858bbbf09d4e3c3af8a91f9bb91550eddfd703f59e86112e65c56a43d553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099064"
---
# <a name="mxdc_printticket_escape_t-structure"></a>MXDC \_ PRINTTICKET \_ ESCAPE \_ T-Struktur

Die **MXDC \_ PRINTTICKET \_ ESCAPE \_ T-Struktur** ist eine [**MXDC ESCAPE HEADER \_ \_ \_ T-Struktur,**](mxdcescapeheader.md) die mit einer [**MXDC \_ PRINTTICKET DATA \_ \_ T-Struktur verkettet**](mxdcprintticketpassthrough.md) ist.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a>Member

<dl> <dt>

**mxdcEscape**
</dt> <dd>

Eine [**MXDC \_ ESCAPE HEADER \_ \_ T-Struktur,**](mxdcescapeheader.md) deren **opCode-Member** auf \_ MXDCOP PRINTTICKET \_ FIXED \_ PAGE, MXDCOP PRINTTICKET FIXED DOC oder \_ \_ \_ MXDCOP \_ PRINTTICKET FIXED DOC \_ \_ \_ SEQ festgelegt ist.

</dd> <dt>

**printTicketData**
</dt> <dd>

Eine [**MXDC \_ PRINTTICKET \_ DATA \_ T-Struktur,**](mxdcprintticketpassthrough.md) die das Druckticket enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird im *lpszInData-Parameter* der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) übergeben, wenn diese Funktion mit dem ESCAPE-Escape-Element [**MXDC \_**](mxdc-escape.md) aufgerufen wird und der **opCode-Member** der [**MXDC \_ ESCAPE HEADER \_ \_ T-Struktur**](mxdcescapeheader.md) **MXDCOP \_ PRINTTICKET FIXED \_ \_ PAGE,** **MXDCOP \_ PRINTTICKET FIXED \_ \_ DOC** oder **MXDCOP \_ PRINTTICKET FIXED DOC \_ \_ \_ SEQ ist.** Das Ergebnis ist das Schreiben des Drucktickets in die XPS-Dokumentdatei.

Ordnen Sie arbeitsspeicher für das Escape-Escapefeld zu, wie unten gezeigt, legen Sie die Felder nach Bedarf fest, und rufen Sie [**dann ExtEscape auf.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)


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



Wenn **opCode auf** **MXDCOP \_ PRINTTICKET FIXED \_ \_ PAGE** festgelegt ist, muss der Aufruf von [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) zwischen einem Aufruf von [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufruf von [**EndPage erfolgen.**](/windows/desktop/api/Wingdi/nf-wingdi-endpage) Wenn **der opCode** auf **MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC** oder **MXDCOP \_ PRINTTICKET \_ FIXED DOC \_ \_ SEQ** festgelegt ist, muss der Aufruf von **ExtEscape** zwischen einem Aufruf von [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) und einem Aufruf von [**EndDoc erfolgen.**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mxdc.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[GDI-Drucker-Escapefunktionen](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

