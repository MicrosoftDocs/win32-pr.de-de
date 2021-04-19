---
description: Mithilfe der escapefunktion "mxdc \_ Escape Printer" können Anwendungen Dokumente in eine Datei oder einen Drucker im XPS-Format (XML Paper Specification) über den Microsoft XPS Document Converter (mxdc) schreiben.
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: MXDC_ESCAPE-Funktion (mxdc. h)
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
ms.openlocfilehash: 08b5ae7e44f7b9c35d6a395b78ce514aee050e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363458"
---
# <a name="mxdc_escape-function"></a>Mxdc- \_ Escape-Funktion

Mithilfe der escapefunktion " **mxdc \_ Escape** Printer" können Anwendungen Dokumente in eine Datei oder einen Drucker im XPS-Format (XML Paper Specification) über den Microsoft XPS Document Converter (mxdc) schreiben.

Um diesen Vorgang auszuführen, nennen Sie die [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion mit den folgenden Parametern.

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

*HDC* 
</dt> <dd>

Ein Handle für den Drucker Gerätekontext.

</dd> <dt>

*cbinput* 
</dt> <dd>

Die Größe (in Bytes) der Daten, auf die durch den *lpszindata* -Parameter verwiesen wird.

</dd> <dt>

*lpszindata* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Eingabedaten enthält, die immer in einer der folgenden-Strukturen gespeichert werden.

<dl> <dd><a href="mxdcescapeheader.md">**Mxdcescapeheader**</a></dd> <dd><a href="mxdcprintticketescape.md">**Mxdcprintticketescape**</a></dd> <dd><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></dd> <dd><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></dd> </dl>

Jede dieser Strukturen verfügt über einen OpCode-Member, der angibt, was der mxdc tun soll. Ausführliche Hinweise zu diesen Codes finden Sie unter mxdcescapeheader.



| Vorgangs Code (OpCode)                                                                                                                                                                                                  | Aktion                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <dt>**mxdcop \_ get \_ filename**</dt> </dl>                                          | Legt den *lpszoutdata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion auf fest, entweder den vollständigen Pfad der Ausgabedatei als NULL-terminierte Zeichenfolge oder andernfalls die Größe dieser Zeichenfolge.<br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <dt>**mxdcop \_ PrintTicket \_ festes \_ doc-Dokument \_**</dt> </dl> | Ordnet ein Druck Ticket einer XPS-Fixed-Dokument Sequenz zu.<br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <dt>**Festes doc für mxdcop \_ PrintTicket \_ \_**</dt> </dl>              | Verknüpft ein Druck Ticket mit einem XPS-Dokument.<br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <dt>**Fixed-Seite für mxdcop \_ PrintTicket \_ \_**</dt> </dl>           | Ordnet ein Druck Ticket einer XPS-Seite zu.<br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <dt>**Mxdcop \_ Set \_ S0PAGE**</dt> </dl>                                                | Sendet das XPS-Markup der aktuellen Seite an die Ausgabe.<br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <dt>**Mxdcop \_ Set \_ S0PAGE- \_ Ressource**</dt> </dl>                    | Sendet eine Ressource auf der Seite, z. b. ein Bild oder eine Schriftart, an die Ausgabe.<br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <dt>**mxdcop- \_ Set- \_ xpspassthru- \_ Modus**</dt> </dl>                 | Versetzt den mxdc in einen Pass-Through-Zustand, sodass eine Anwendung XPS direkt in die Ausgabedatei schreiben kann, ohne dass der mxdc verarbeitet werden muss. Auf diese Weise kann ein gesamtes Dokument oder sogar eine Dokument Sequenz geschrieben werden.<br/> |



 

</dd> <dt>

*cboutput* 
</dt> <dd>

Die Größe (in Bytes) der Daten, auf die durch den *lpszoutdata* -Parameter verwiesen wird.

</dd> <dt>

*lpszoutdata* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Ausgabedaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert größer als 0 (null). Wenn die Funktion fehlschlägt oder nicht unterstützt wird, ist der Rückgabewert kleiner oder gleich 0 (null).

## <a name="remarks"></a>Bemerkungen

Diese Escapesequenz wird von mxdc und XPSDrv unterstützt, aber nicht durch GDI.

Um zu ermitteln, ob der Druckertreiber der mxdc ist, nennen Sie [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit der [**gettechnology**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) -Escapezeichen. Wenn der Treiber der mxdc ist, gibt " **extescape** " die mit 0 (null) beendete Zeichenfolge ("") zurück http://schemas.microsoft.com/xps/2005/06 . Stellen Sie sicher, dass der vom *lpszoutdata* -Parameter referenzierte Puffer groß genug ist, um diese Zeichenfolge zu speichern.

Vergewissern Sie sich, dass es sich bei dem Druckertreiber um den Microsoft XPS Document Writer-Treiber handelt, um zu bestimmen, ob es sich bei dem Druckertreiber um den mxdc handelt, und legen Sie dann fest, ob der Name des Druckertreibers "Microsoft XPS Document Writer" ist.

Verwenden Sie eine der folgenden Verfahren, um den Namen des Druckertreibers zu erhalten. <dl> Aufrufen von [**getprinterdriver**](getprinterdriver.md) , bei dem der *Level* -Parameter auf 1 festgelegt ist. Der Name des Druckertreibers wird im Mitglied " **PName** " der Struktur " [**Driver \_ Info \_ 1**](driver-info-1.md) " zurückgegeben.  
oder  
Ruft [**GetPrinter**](getprinter.md) auf, wobei der *Level* -Parameter auf 2 festgelegt ist. Der Name des Druckertreibers wird im **pdrivername** -Element der [**Drucker \_ Info \_ 2**](printer-info-2.md) -Struktur zurückgegeben.  
</dl>

In der folgenden Tabelle wird gezeigt, wo verschiedene Objekte in der XPS-Datei gefunden werden, in der verschiedene Objekttypen geschrieben werden.



| Object       | Speicherort in der Ausgabedatei    |
|--------------|--------------------------------|
| Seite "korrigiert"   | /Documents/1/Pages/Esc%d.fpage |
| Miniaturansicht    | /Documents/1/Metadata          |
| Ticket drucken | /Documents/1/Metadata          |
| Schriftart         | /Documents/1/Resources/Fonts   |
| Image        | /Documents/1/Resources/Images  |



 

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

[Druckerescapefunktionen](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**Extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

