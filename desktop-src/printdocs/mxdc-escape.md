---
description: Die MXDC \_ ESCAPE-Drucker-Escapefunktion ermöglicht Anwendungen das Schreiben von Dokumenten in eine Datei oder in einen Drucker im XPS-Format (XML Paper Specification) mithilfe des Microsoft XPS Document Converter (MXDC).
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: MXDC_ESCAPE-Funktion (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7ace79404808db750a15b2c17b6fedb336dbd1d72b1581888324a4d87bb7cd67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460880"
---
# <a name="mxdc_escape-function"></a>MXDC \_ ESCAPE-Funktion

Die **MXDC ESCAPE-Drucker-Escapefunktion \_** ermöglicht Anwendungen das Schreiben von Dokumenten in eine Datei oder in einen Drucker im XPS-Format (XML Paper Specification) mithilfe des Microsoft XPS Document Converter (MXDC).

Rufen Sie zum Ausführen dieses Vorgangs die [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit den folgenden Parametern auf.

## <a name="syntax"></a>Syntax


```C++
int MXDC_ESCAPE(
    hdc,
    cbInput,
    lpszInData,
    cbOutput,
    lpszOutData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hdc* 
</dt> <dd>

Ein Handle für den Druckergerätekontext.

</dd> <dt>

*cbInput* 
</dt> <dd>

Die Größe der Daten, auf die der *lpszInData-Parameter* zeigt, in Bytes.

</dd> <dt>

*lpszInData* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Eingabedaten enthält, die immer in einer der folgenden Strukturen gespeichert sind.

<dl> <dd><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></dd> <dd><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></dd> <dd><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></dd> <dd><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></dd> </dl>

Jede dieser Strukturen verfügt über einen Opcodemember, der angibt, was der MXDC tun soll. Ausführliche Hinweise zu diesen Codes finden Sie unter MxdcEscapeHeader.



| Betriebscode (opcode)                                                                                                                                                                                                  | Aktion                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <dt>**MXDCOP \_ GET \_ FILENAME**</dt> </dl>                                          | Legt den *lpszOutData-Parameter* der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) auf fest, entweder den vollständigen Pfad der Ausgabedatei als auf null endende Zeichenfolge oder andernfalls die Größe dieser Zeichenfolge.<br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <dt>**MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC \_ SEQ**</dt> </dl> | Ordnet ein Druckticket einer festen XPS-Dokumentsequenz zu.<br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <dt>**MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC**</dt> </dl>              | Ordnet einem XPS-Dokument ein Druckticket zu.<br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <dt>**MXDCOP \_ PRINTTICKET \_ – FESTE \_ SEITE**</dt> </dl>           | Ordnet einer XPS-Seite ein Druckticket zu.<br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <dt>**MXDCOP \_ SET \_ S0PAGE**</dt> </dl>                                                | Sendet das XPS-Markup der aktuellen Seite an die Ausgabe.<br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <dt>**MXDCOP \_ SET \_ S0PAGE-RESSOURCE \_**</dt> </dl>                    | Sendet eine Ressource auf der Seite, z. B. ein Bild oder eine Schriftart, an die Ausgabe.<br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <dt>**MXDCOP \_ SET \_ XPSPASSTHRU \_ MODE**</dt> </dl>                 | Versetzt den MXDC in einen Pass-Through-Zustand, sodass eine Anwendung XPS direkt in die Ausgabedatei schreiben kann, ohne dass der MXDC verarbeitet wird. Ein gesamtes Dokument oder sogar eine Dokumentsequenz kann auf diese Weise geschrieben werden.<br/> |



 

</dd> <dt>

*cbOutput* 
</dt> <dd>

Die Größe der Daten in Bytes, auf die der *lpszOutData-Parameter* zeigt.

</dd> <dt>

*lpszOutData* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Ausgabedaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert größer als 0 (null). Wenn die Funktion fehlschlägt oder nicht unterstützt wird, ist der Rückgabewert kleiner oder gleich 0 (null).

## <a name="remarks"></a>Hinweise

Dieses Escape wird von MXDC und XPSDrv unterstützt, jedoch nicht von GDI.

Um zu ermitteln, ob der Druckertreiber das MXDC ist, rufen [**Sie ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit dem [**GETTECHNOLOGY-Escape**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) auf. Wenn es sich bei dem Treiber um den MXDC handelt, gibt **ExtEscape** die auf Null endende Zeichenfolge " http://schemas.microsoft.com/xps/2005/06 " " zurück. Stellen Sie sicher, dass der Puffer, auf den der *lpszOutData-Parameter* verweist, groß genug ist, um diese Zeichenfolge aufzunehmen.

Um zu ermitteln, ob der Druckertreiber der Windows im Lieferumfang enthaltenen Microsoft XPS Document Writer-Treiber ist, vergewissern Sie sich, dass der Druckertreiber das MXDC ist, und bestimmen Sie dann, ob der Name des Druckertreibers "Microsoft XPS Document Writer" lautet.

Verwenden Sie eine der folgenden Verfahren, um den Namen des Druckertreibers abzurufen. <dl> Rufen [**Sie GetPrinterDriver**](getprinterdriver.md) auf, wobei der *Level-Parameterwert* auf 1 festgelegt ist. Der Name des Druckertreibers wird im **pName-Member** der [**DRIVER INFO \_ \_ 1-Struktur**](driver-info-1.md) zurückgegeben.  
oder  
Rufen [**Sie GetPrinter**](getprinter.md) auf, wobei der *Level-Parameterwert* auf 2 festgelegt ist. Der Druckertreibername wird im **pDriverName-Member** der [**PRINTER INFO \_ \_ 2-Struktur**](printer-info-2.md) zurückgegeben.  
</dl>

Die folgende Tabelle zeigt, wo verschiedene Objekte in der XPS-Datei zu finden sind. Verschiedene Objekttypen werden geschrieben.



| Object       | Speicherort in der Ausgabedatei    |
|--------------|--------------------------------|
| Seite "Behoben"   | /Documents/1/Pages/Esc%d.fpage |
| Miniaturansicht    | /Documents/1/Metadata          |
| Drucken eines Tickets | /Documents/1/Metadata          |
| Schriftart         | /Documents/1/Resources/Fonts   |
| Image        | /Documents/1/Resources/Images  |



 

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

[Escapefunktionen für Drucker](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

