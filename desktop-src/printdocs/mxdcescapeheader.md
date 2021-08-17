---
description: Die MXDC \_ ESCAPE \_ HEADER \_ T-Struktur enthält den Vorgangscode für einen Aufruf von ExtEscape mit MXDC \_ ESCAPE als nEscape-Parameter. Sie stellt auch die Größen der Eingabe- und Ausgabepuffer bereit.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: MXDC_ESCAPE_HEADER_T-Struktur (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE_HEADER_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 53dd83e362ab21938121a986ee2402076d72f870460bc9db608b9a048cee0f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099074"
---
# <a name="mxdc_escape_header_t-structure"></a>MXDC \_ ESCAPE \_ HEADER \_ T-Struktur

Die **MXDC \_ ESCAPE HEADER \_ \_ T-Struktur** enthält den Vorgangscode für einen Aufruf von [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit [**MXDC \_ ESCAPE**](mxdc-escape.md) als *nEscape-Parameter.* Sie stellt auch die Größen der Eingabe- und Ausgabepuffer bereit.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMxdcEscapeHeader {
  ULONG cbInput;
  ULONG cbOutput;
  ULONG opCode;
} MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T;
```



## <a name="members"></a>Member

<dl> <dt>

**cbInput**
</dt> <dd>

Die Größe des Eingabepuffers, der an den *lpszOutData-Parameter* der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) übergeben wird.

</dd> <dt>

**cbOutput**
</dt> <dd>

Die Größe des Ausgabepuffers. Dies ist der gleiche Wert wie der *cbOutput-Parameter* der [**ExtEscape-Funktion.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)

</dd> <dt>

**Opcode**
</dt> <dd>

Die Codekonstante, die MXDC mit informationen zu den entsprechenden Codeausführungen informiert.



| Operations-Code                      | Beschreibung                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MXDCOP \_ GET \_ FILENAME                | Gibt im *lpszOutData-Parameter* der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) entweder den vollständigen Pfad der Ausgabedatei als auf null endende Zeichenfolge oder die Größe dieser Zeichenfolge zurück. Siehe Hinweise.                   |
| MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC \_ SEQ | Ordnet ein Druckticket einer festen XPS-Dokumentsequenz zu.                                                                                                                                                         |
| MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC      | Ordnet einem XPS-Dokument ein Druckticket zu.                                                                                                                                                                        |
| MXDCOP \_ PRINTTICKET \_ – FESTE \_ SEITE     | Ordnet einer XPS-Seite ein Druckticket zu.                                                                                                                                                                            |
| MXDCOP \_ SET \_ S0PAGE                  | Sendet das XPS-Markup der aktuellen Seite an die Ausgabe.                                                                                                                                                                |
| MXDCOP \_ SET \_ S0PAGE-RESSOURCE \_        | Sendet eine Ressource auf der Seite, z. B. ein Bild oder eine Schriftart, an die Ausgabe.                                                                                                                                                 |
| MXDCOP \_ SET \_ XPSPASSTHRU \_ MODE       | Versetzt den MXDC in einen Pass-Through-Zustand, sodass eine Anwendung XPS direkt in die Ausgabedatei schreiben kann, ohne dass der MXDC verarbeitet wird. Ein gesamtes Dokument oder sogar eine Dokumentsequenz kann auf diese Weise geschrieben werden. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Vor dem Aufrufen von [**MXDC \_ ESCAPE**](mxdc-escape.md) \_ sollten Anwendungen zunächst überprüfen, ob der Treiber MXDC ist, indem [**Sie ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit dem [**GETTECHNOLOGY-Escape**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) aufrufen. Wenn der Treiber das MXDC ist, gibt die Funktion die auf null endende Zeichenfolge http://schemas.microsoft.com/xps/2005/06 "" zurück.

Diese Struktur befindet sich immer am Anfang der Daten, die in ihrem *lpszInData-Parameter* an die [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) übergeben werden.

Wenn **opCode** MXDCOP \_ GET \_ FILENAME ist:

-   Der *lpszInData-Parameter* der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) besteht nur aus der **MXDC \_ ESCAPE HEADER \_ \_ T-Struktur.**
-   Rufen Sie den Ausgabedateinamen ab, indem [**Sie ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) zweimal aufrufen.
    1.  Übergeben Sie beim ersten Mal 4 an den *cbOutput-Parameter* von [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Legen Sie den *LpszOutData-Parameter* so fest, dass er auf alle zugeordneten 4 Bytes an Arbeitsspeicher verweist. Die Größe des vollqualifizierten Dateipfads wird im *lpszOutData-Parameter* von **ExtEscape** zurückgegeben.
    2.  Rufen Sie dann die Funktion erneut auf. Legen Sie dieses Mal sowohl *cbOutput* als *auch cbInput* auf 4+ *DataSize* fest. Der vollqualifizierte Dateipfad wird in einer [**MxdcGetFileNameData-Struktur**](mxdcgetfilenamedata.md) zurückgegeben.

Wenn **opCode** MXDCOP \_ PRINTTICKET \_ FIXED DOC \_ \_ SEQ oder MXDCOP \_ PRINTTICKET FIXED DOC \_ \_ ist:

-   Der *lpszInData-Parameter* der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) besteht aus der **MXDC \_ ESCAPE HEADER \_ \_ T-Struktur** und einer [**MxdcPrintTicketPassthrough-Struktur,**](mxdcprintticketpassthrough.md) die zu einer [**MxdcPrintTicketEscape-Struktur**](mxdcprintticketescape.md) verkettet ist.
-   Der Aufruf von [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) muss zwischen einem Aufruf von [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) und einem Aufruf von [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)erfolgen.

Wenn **opCode** MXDCOP \_ PRINTTICKET \_ FIXED PAGE \_ ist:

-   Der *lpszInData-Parameter* der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) besteht aus der **MXDC \_ ESCAPE HEADER \_ \_ T-Struktur** und einer [**MxdcPrintTicketPassthrough-Struktur,**](mxdcprintticketpassthrough.md) die zu einer [**MxdcPrintTicketEscape-Struktur**](mxdcprintticketescape.md) verkettet ist.
-   Der Aufruf von [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) muss zwischen einem Aufruf von [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufruf von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)erfolgen.

Wenn **opCode** MXDCOP \_ SET \_ S0PAGE ist:

-   Der *lpszInData-Parameter* der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) besteht aus der **MXDC \_ ESCAPE HEADER \_ \_ T-Struktur** und einer [**MxdcS0PageData-Struktur,**](mxdcs0pagedata.md) die in eine [**MxdcS0PagePassthroughEscape-Struktur**](mxdcs0pagepassthroughescape.md) verkettet ist.
-   Der Aufruf von [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) muss zwischen einem Aufruf von [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufruf von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)erfolgen.
-   Die aufrufende Anwendung ist für die Überprüfung des XML-Code verantwortlich.
-   Die Streamingnutzung ist effizienter, wenn Sie [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit MXDCOP \_ SET \_ S0PAGE RESOURCE als \_ **opCode** für jede Ressource auf der Seite aufrufen, bevor Sie sie mit MXDCOP \_ SET \_ S0PAGE aufrufen.

Wenn **opCode** MXDCOP \_ SET \_ S0PAGE \_ RESOURCE ist:

-   Der *lpszInData-Parameter* der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) besteht aus der **MXDC \_ ESCAPE HEADER \_ \_ T-Struktur** und einer [**MxdcXpsS0PageResource-Struktur,**](mxdcxpss0pageresource.md) die in eine [**MxdcS0PageResourceEscape-Struktur**](mxdcs0pageresourceescape.md) verkettet ist.
-   Der Aufruf von [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) muss zwischen einem Aufruf von [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufruf von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)erfolgen. Zwischen den **Aufrufen von StartPage** und **EndPage** kann es jedoch mehrere solcher Aufrufe geben.
-   Die Streamingnutzung ist effizienter, wenn Sie [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit MXDCOP \_ SET \_ S0PAGE RESOURCE als \_ **opCode** für jede Ressource auf der Seite aufrufen, bevor Sie sie mit MXDCOP \_ SET \_ S0PAGE aufrufen.

Wenn **opCode** MXDCOP \_ SET \_ XPSPASSTHRU \_ MODE ist:

-   Der *lpszInData-Parameter* der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) besteht nur aus der **MXDC \_ ESCAPE HEADER \_ \_ T-Struktur.**
-   Dieser Aufruf muss vor dem Aufruf von [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)erfolgen.

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

 

