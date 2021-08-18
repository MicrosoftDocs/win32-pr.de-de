---
description: Die MXDC \_ PRINTTICKET \_ DATA \_ T-Struktur enthält ein XPS-Dokumentdruckticket, das Drucker- und Druckauftragseinstellungen enthält, das ohne Verarbeitung an die Ausgabedatei von Microsoft XPS Document Converter (MXDC) übergeben werden kann.
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: MXDC_PRINTTICKET_DATA_T-Struktur (Mxdc.h)
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
ms.openlocfilehash: 3cf778781340323a78495f87b1408e1011641797ed52a3565bafe41ca450d551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471641"
---
# <a name="mxdc_printticket_data_t-structure"></a>MXDC \_ PRINTTICKET \_ DATA \_ T-Struktur

Die **MXDC \_ PRINTTICKET \_ DATA \_ T-Struktur** enthält ein XPS-Dokumentdruckticket, das Drucker- und Druckauftragseinstellungen enthält, das ohne Verarbeitung an die Ausgabedatei von Microsoft XPS Document Converter (MXDC) übergeben werden kann.

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

Die Größe des Drucktickets in Bytes.

</dd> <dt>

**bData**
</dt> <dd>

Das XPS-Dokumentdruckticket.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird an eine [**MXDC \_ ESCAPE HEADER \_ \_ T-Struktur**](mxdcescapeheader.md) angefügt, bei der der **opCode-Member** auf **MXDCOP \_ PRINTTICKET FIXED \_ \_ PAGE,** **MXDCOP \_ PRINTTICKET FIXED \_ \_ DOC** oder **MXDCOP \_ PRINTTICKET FIXED DOC \_ \_ \_ SEQ** festgelegt ist, um eine [**MXDC \_ PRINTTICKET ESCAPE \_ \_ T-Struktur**](mxdcprintticketescape.md) zu erstellen. Die **MXDC \_ PRINTTICKET \_ ESCAPE \_ T-Struktur** wird dann an den *lpszInData-Parameter* der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) übergeben, wenn sie mit dem [**MXDC \_ ESCAPE-Escapewert**](mxdc-escape.md) aufgerufen wird. Die Auswirkung besteht darin, das Druckticket in die XPS-Dokumentdatei zu schreiben.

Wenn **opCode** auf **MXDCOP \_ PRINTTICKET \_ FIXED \_ PAGE** festgelegt ist, muss der Aufruf von [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) zwischen einem Aufruf von [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufruf von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)erfolgen. Wenn **opCode** entweder auf **MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC** oder **MXDCOP \_ PRINTTICKET \_ FIXED DOC \_ \_ SEQ** festgelegt ist, muss der Aufruf von **ExtEscape** zwischen einem Aufruf von [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) und einem Aufruf von [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)erfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                    |
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

 

