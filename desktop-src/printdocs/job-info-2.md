---
description: Die JOB \_ INFO \_ 2-Struktur beschreibt einen vollständigen Satz von Werten, die einem Auftrag zugeordnet sind.
ms.assetid: 0cc61e35-4ac9-47bd-bb0d-ff43854bdee5
title: JOB_INFO_2 -Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_2
- _JOB_INFO_2A
- _JOB_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2c41ea46f9226990fc28b5c629f3b36785d4bf4b0ee6ecd6e39477251f765b3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971319"
---
# <a name="job_info_2-structure"></a>JOB \_ INFO \_ 2-Struktur

Die **JOB \_ INFO \_ 2-Struktur** beschreibt einen vollständigen Satz von Werten, die einem Auftrag zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct _JOB_INFO_2 {
  DWORD                JobId;
  LPTSTR               pPrinterName;
  LPTSTR               pMachineName;
  LPTSTR               pUserName;
  LPTSTR               pDocument;
  LPTSTR               pNotifyName;
  LPTSTR               pDatatype;
  LPTSTR               pPrintProcessor;
  LPTSTR               pParameters;
  LPTSTR               pDriverName;
  LPDEVMODE            pDevMode;
  LPTSTR               pStatus;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Status;
  DWORD                Priority;
  DWORD                Position;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                TotalPages;
  DWORD                Size;
  SYSTEMTIME           Submitted;
  DWORD                Time;
  DWORD                PagesPrinted;
} JOB_INFO_2, *PJOB_INFO_2;
```



## <a name="members"></a>Member

<dl> <dt>

**Jobid**
</dt> <dd>

Ein Auftragsbezeichnerwert.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Druckers angibt, für den der Auftrag in einen Pool gesetzt wird.

</dd> <dt>

**pMachineName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Computers angibt, der den Druckauftrag erstellt hat.

</dd> <dt>

**pUserName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Benutzers angibt, der den Druckauftrag besitzt.

</dd> <dt>

**pDocument**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Druckauftrags angibt (z. B. "MS-WORD: Review.doc").

</dd> <dt>

**pNotifyName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Benutzers angibt, der benachrichtigt werden soll, wenn der Auftrag gedruckt wurde oder wenn beim Drucken des Auftrags ein Fehler auftritt.

</dd> <dt>

**pDatatype**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Datentyp angibt, der zum Aufzeichnen des Druckauftrags verwendet wird.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Druckprozessors angibt, der zum Drucken des Auftrags verwendet werden soll.

</dd> <dt>

**pParameters**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die Druckprozessorparameter angibt.

</dd> <dt>

**pDriverName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Druckertreibers angibt, der zum Verarbeiten des Druckauftrags verwendet werden soll.

</dd> <dt>

**pDevMode**
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die Gerätein initialisierungs- und Umgebungsdaten für den Druckertreiber enthält.

</dd> <dt>

**pStatus**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Status des Druckauftrags angibt. Dieses Member sollte vor  Status überprüft werden, und wenn **pStatus** **NULL** ist, wird der Status durch den Inhalt des Status-Mitglieds definiert.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

Der Wert dieses -Members ist **NULL.** Das Abrufen und Festlegen von Dokumentsicherheitsdeskriptoren wird in dieser Version nicht unterstützt.

</dd> <dt>

**Status**
</dt> <dd>

Der Auftragsstatus. Dieser Member kann mindestens einer der folgenden Werte sein.

| Wert                           | Bedeutung                                                      |
|---------------------------------|--------------------------------------------------------------|
| AUFTRAGSSTATUS \_ \_ BLOCKIERT \_ DEVQ      | Der Treiber kann den Auftrag nicht drucken.                             |
| AUFTRAGSSTATUS \_ \_ GELÖSCHT            | Der Auftrag wurde gelöscht.                                        |
| AUFTRAGSSTATUS \_ \_ WIRD GELÖSCHT           | Der Auftrag wird gelöscht.                                        |
| \_ \_ AUFTRAGSSTATUSFEHLER              | Dem Auftrag ist ein Fehler zugeordnet.                         |
| AUFTRAGSSTATUS \_ \_ OFFLINE            | Der Drucker ist offline.                                          |
| AUFTRAGSSTATUS \_ \_ PAPEROUT           | Der Drucker ist ohne Papier.                                     |
| AUFTRAGSSTATUS \_ \_ ANGEHALTEN             | Der Auftrag wurde angehalten.                                               |
| AUFTRAGSSTATUS \_ \_ GEDRUCKT            | Der Auftrag wurde gedruckt.                                             |
| DRUCKEN DES \_ \_ AUFTRAGSSTATUS           | Der Auftrag wird gedruckt.                                             |
| \_ \_ AUFTRAGSSTATUSNEUSTART            | Der Auftrag wurde neu gestartet.                                      |
| \_ \_ AUFTRAGSSTATUS-SPOOLING           | Der Auftrag wird spoolt.                                             |
| \_AUFTRAGSSTATUS \_ \_ BENUTZEREINGRIFF | Der Drucker hat einen Fehler, der erfordert, dass der Benutzer etwas macht. |



 

In Windows XP und neueren Versionen von Windows können auch die folgenden Werte verwendet werden:

| Wert                 | Bedeutung                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| AUFTRAGSSTATUS \_ \_ ABGESCHLOSSEN | Der Auftrag wird an den Drucker gesendet, aber möglicherweise noch nicht gedruckt. Weitere Informationen finden Sie unter Hinweise. |
| AUFTRAGSSTATUS \_ \_ BEIBEHALTEN | Der Auftrag wurde nach dem Drucken in der Druckwarteschlange beibehalten.                              |



 

</dd> <dt>

**Priority**
</dt> <dd>

Die Auftragspriorität. Dieser Member kann einer der folgenden Werte oder im Bereich zwischen 1 und 99 sein (MIN \_ PRIORITY bis MAX \_ PRIORITY).



| Wert         | Bedeutung           |
|---------------|-------------------|
| MIN \_ PRIORITY | Mindestpriorität. |
| MAX \_ PRIORITY | Maximale Priorität. |
| DEF \_ PRIORITY | Standardpriorität. |



 

</dd> <dt>

**Position**
</dt> <dd>

Die Position des Auftrags in der Druckwarteschlange.

</dd> <dt>

**StartTime**
</dt> <dd>

Der früheste Zeitpunkt, zu dem der Auftrag gedruckt werden kann.

</dd> <dt>

**UntilTime**
</dt> <dd>

Der letzte Zeitpunkt, zu dem der Auftrag gedruckt werden kann.

</dd> <dt>

**TotalPages**
</dt> <dd>

Die Anzahl der seiten, die für den Auftrag erforderlich sind. Dieser Wert kann 0 (null) sein, wenn der Druckauftrag keine Informationen zum Seitentrennzeichen enthält.

</dd> <dt>

**Größe**
</dt> <dd>

Die Größe des Auftrags in Bytes.

</dd> <dt>

**Gesendet**
</dt> <dd>

Eine [**SYSTEMTIME-Struktur,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) die die Zeit angibt, zu der der Auftrag übermittelt wurde.

Dieser Zeitwert liegt im UTC-Format (Universal Time Coordinate) vor. Sie sollten es in einen lokalen Zeitwert konvertieren, bevor Sie ihn anzeigen. Sie können die [**FileTimeToLocalFileTime-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) verwenden, um die Konvertierung durchzuführen.

</dd> <dt>

**Time**
</dt> <dd>

Die Gesamtzeit in Millisekunden, die seit beginn des Drucks des Auftrags verstrichen ist.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Die Anzahl der seiten, die gedruckt wurden. Dieser Wert kann 0 (null) sein, wenn der Druckauftrag keine Seitentrenninformationen enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Portmonitore, die TrueEndOfJob nicht unterstützen, legen den Auftrag direkt nach der Übermittlung des Auftrags an den Drucker als \_ AUFTRAGSSTATUS \_ GEDRUCKT fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ JOB \_ INFO \_ 2W** (Unicode) und **\_ JOB INFO \_ \_ 2A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

