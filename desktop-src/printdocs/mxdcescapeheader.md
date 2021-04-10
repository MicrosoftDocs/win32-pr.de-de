---
description: Die mxdc- \_ Escape-Header-T- \_ \_ Struktur enthält den Vorgangs Code für einen extescape-extescape mit mxdc-Escapezeichen \_ als Nescape-Parameter. Außerdem werden die Größen der Eingabe-und Ausgabepuffer bereitstellt.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: MXDC_ESCAPE_HEADER_T-Struktur (mxdc. h)
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
ms.openlocfilehash: a16e0d5bb1a8ce48e071fe1b32543610d8433e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868528"
---
# <a name="mxdc_escape_header_t-structure"></a>Mxdc- \_ Escape-Header-T- \_ \_ Struktur

Die **mxdc- \_ Escape- \_ Header- \_ T** -Struktur enthält den Vorgangs Code für einen [**extescape-extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit [**mxdc \_**](mxdc-escape.md) -Escapezeichen als *Nescape* -Parameter. Außerdem werden die Größen der Eingabe-und Ausgabepuffer bereitstellt.

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

**cbinput**
</dt> <dd>

Die Größe des Eingabe Puffers, der an den *lpszoutdata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben wird.

</dd> <dt>

**cboutput**
</dt> <dd>

Die Größe des Ausgabepuffers. Dies ist der gleiche Wert wie der *cboutput* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion.

</dd> <dt>

**opCode**
</dt> <dd>

Die Code Konstante, die mxdc mitteilt, was zu tun ist.



| Vorgangs Code                      | BESCHREIBUNG                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mxdcop \_ get \_ filename                | Gibt im *lpszoutdata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion entweder den vollständigen Pfad der Ausgabedatei als NULL-terminierte Zeichenfolge oder die Größe der Zeichenfolge zurück. Siehe Hinweise.                   |
| mxdcop \_ PrintTicket \_ festes \_ doc-Dokument \_ | Ordnet ein Druck Ticket einer XPS-Fixed-Dokument Sequenz zu.                                                                                                                                                         |
| Festes doc für mxdcop \_ PrintTicket \_ \_      | Verknüpft ein Druck Ticket mit einem XPS-Dokument.                                                                                                                                                                        |
| Fixed-Seite für mxdcop \_ PrintTicket \_ \_     | Ordnet ein Druck Ticket einer XPS-Seite zu.                                                                                                                                                                            |
| Mxdcop \_ Set \_ S0PAGE                  | Sendet das XPS-Markup der aktuellen Seite an die Ausgabe.                                                                                                                                                                |
| Mxdcop \_ Set \_ S0PAGE- \_ Ressource        | Sendet eine Ressource auf der Seite, z. b. ein Bild oder eine Schriftart, an die Ausgabe.                                                                                                                                                 |
| mxdcop- \_ Set- \_ xpspassthru- \_ Modus       | Versetzt den mxdc in einen Pass-Through-Zustand, sodass eine Anwendung XPS direkt in die Ausgabedatei schreiben kann, ohne dass der mxdc verarbeitet werden muss. Auf diese Weise kann ein gesamtes Dokument oder sogar eine Dokument Sequenz geschrieben werden. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Vor dem Aufrufen von [**mxdc \_**](mxdc-escape.md)-Escapezeichen \_ sollten Anwendungen zuerst überprüfen, ob der Treiber mxdc ist, indem Sie [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit dem [**gettechnology**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) -Escapezeichen aufrufen Wenn der Treiber der mxdc ist, gibt die Funktion die mit 0 (null) beendete Zeichenfolge " http://schemas.microsoft.com/xps/2005/06 " zurück.

Diese Struktur befindet sich immer am Anfang der Daten, die in Ihrem *lpszindata* -Parameter an die [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben werden.

Wenn **Opcode** "mxdcop \_ get \_ filename" ist:

-   Der *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion besteht nur aus der **mxdc- \_ Escape-Header- \_ \_ T** -Struktur.
-   Rufen Sie den Ausgabedatei Namen ab, indem Sie [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) zweimal aufrufen.
    1.  Übergeben Sie beim ersten Mal 4 an den *cboutput* -Parameter von [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Legen Sie den *lpszoutdata* -Parameter so fest, dass er auf zugeordnete 4 Bytes an Arbeitsspeicher verweist. Der voll qualifizierte Dateipfad wird im *lpszoutdata* -Parameter von **extescape** zurückgegeben.
    2.  Anschließend wird die Funktion erneut aufgerufen. Legen Sie diesmal sowohl *cboutput* als auch *cbinput* auf 4 + *DataSize* fest. Der voll qualifizierte Dateipfad wird in einer [**mxdcgetfileamedata**](mxdcgetfilenamedata.md) -Struktur zurückgegeben.

Wenn **Opcode** "mxdcop \_ PrintTicket \_ Fixed \_ doc/ \_ q" oder "mxdcop \_ PrintTicket \_ Fixed \_ doc" ist:

-   Der *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion besteht aus der **mxdc- \_ Escape-Header- \_ \_ T** -Struktur und einer [**mxdcprintticketpassthrough**](mxdcprintticketpassthrough.md) -Struktur, die in eine [**mxdcprintticketescape**](mxdcprintticketescape.md) -Struktur verkettet ist.
-   Der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -aufrufsausdruck muss zwischen einem Aufrufen von [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) und einem- [**Endpunkt**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)auftreten.

Wenn **Opcode** die festgelegte mxdcop- \_ PrintTicket- \_ Seite ist \_ :

-   Der *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion besteht aus der **mxdc- \_ Escape-Header- \_ \_ T** -Struktur und einer [**mxdcprintticketpassthrough**](mxdcprintticketpassthrough.md) -Struktur, die in eine [**mxdcprintticketescape**](mxdcprintticketescape.md) -Struktur verkettet ist.
-   Der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Aufrufe muss zwischen einem Aufrufen von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufrufen von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)erfolgen.

Wenn **Opcode** auf mxdcop \_ festgelegt ist \_ S0PAGE:

-   Der *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion besteht aus der **mxdc- \_ Escape-Header- \_ \_ T** -Struktur und einer [**MxdcS0PageData**](mxdcs0pagedata.md) -Struktur, die in eine [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) -Struktur verkettet ist.
-   Der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Aufrufe muss zwischen einem Aufrufen von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufrufen von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)erfolgen.
-   Die aufrufende Anwendung ist für die Validierung des XML-Codes verantwortlich.
-   Der Streamingverbrauch ist effizienter, wenn Sie [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit mxdcop \_ Set \_ S0PAGE \_ Resource als **Opcode** für jede Ressource auf der Seite aufruft, bevor Sie Sie mit mxdcop \_ Set S0PAGE aufzurufen \_ .

Wenn **Opcode** auf mxdcop \_ Set \_ S0PAGE Resource festgelegt ist \_ :

-   Der *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion besteht aus der **mxdc- \_ Escape-Header- \_ \_ T** -Struktur und einer [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) -Struktur, die in eine [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) -Struktur verkettet ist.
-   Der Aufruf von [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) muss zwischen einem Aufruf von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufruf von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)erfolgen, aber es können mehrere solcher Aufrufe zwischen den Aufrufen **Startpage** und **EndPage** vorhanden sein.
-   Der Streamingverbrauch ist effizienter, wenn Sie [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit mxdcop \_ Set \_ S0PAGE \_ Resource als **Opcode** für jede Ressource auf der Seite aufruft, bevor Sie Sie mit mxdcop \_ Set S0PAGE aufzurufen \_ .

Wenn **Opcode** auf mxdcop festgelegt ist, wird der \_ \_ xpspassthru- \_ Modus ausgeführt:

-   Der *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion besteht nur aus der **mxdc- \_ Escape-Header- \_ \_ T** -Struktur.
-   Dieser Rückruf muss vor dem Aufrufen von [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)erfolgen.

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

 

