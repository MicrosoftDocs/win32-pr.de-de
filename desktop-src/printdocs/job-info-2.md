---
description: Die Struktur der Auftrags \_ Informationen \_ 2 beschreibt einen vollständigen Satz von Werten, die einem Auftrag zugeordnet sind.
ms.assetid: 0cc61e35-4ac9-47bd-bb0d-ff43854bdee5
title: JOB_INFO_2 Struktur (winspool. h)
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
ms.openlocfilehash: d6b582267afceb01fd7ced7d6d46144664bb9d2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218219"
---
# <a name="job_info_2-structure"></a>Struktur von Auftrags \_ Informationen \_ 2

Die Struktur der **Auftrags \_ Informationen \_ 2** beschreibt einen vollständigen Satz von Werten, die einem Auftrag zugeordnet sind.

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

**JobId**
</dt> <dd>

Ein Auftrags Bezeichnerwert.

</dd> <dt>

**pprintername**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckers angibt, für den der Auftrag gespoolkt ist.

</dd> <dt>

**pmachinename**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Computers angibt, der den Druckauftrag erstellt hat.

</dd> <dt>

**pusername**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Benutzers angibt, der den Druckauftrag besitzt.

</dd> <dt>

**pdocument**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckauftrags angibt (z. b. "MS-Word: Review.doc").

</dd> <dt>

**pnotifyname**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Benutzers angibt, der benachrichtigt werden soll, wenn der Auftrag gedruckt wurde oder wenn beim Drucken des Auftrags ein Fehler auftritt.

</dd> <dt>

**pdatatype**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp angibt, der zum Aufzeichnen des Druckauftrags verwendet wird.

</dd> <dt>

**pprintprocessor**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druck Prozessors angibt, der zum Drucken des Auftrags verwendet werden soll.

</dd> <dt>

**pParameters**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die Druck Prozessor Parameter angibt.

</dd> <dt>

**pdrivername**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druckertreibers angibt, der zum Verarbeiten des Druckauftrags verwendet werden soll.

</dd> <dt>

**pdevmode**
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die Geräte Initialisierungs-und Umgebungs Daten für den Druckertreiber enthält.

</dd> <dt>

**pstatus**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Status des Druckauftrags angibt. Dieser Member sollte vor dem **Status** geprüft werden, und wenn **pstatus** den Wert **null** hat, wird der Status durch den Inhalt des statusmembers definiert.

</dd> <dt>

**psecuritydescriptor**
</dt> <dd>

Der Wert dieses Members ist **null**. Das Abrufen und Festlegen von Dokument Sicherheits Deskriptoren wird in dieser Version nicht unterstützt.

</dd> <dt>

**Status**
</dt> <dd>

Der Status des Auftrags. Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.

| Wert                           | Bedeutung                                                      |
|---------------------------------|--------------------------------------------------------------|
| der Auftrags \_ Status ist \_ blockiert \_ devq.      | Der Treiber kann den Auftrag nicht drucken.                             |
| Auftrags \_ Status \_ gelöscht            | Der Auftrag wurde gelöscht.                                        |
| Auftrags \_ Status wird \_ gelöscht           | Der Auftrag wird gelöscht.                                        |
| Auftrags \_ Status \_ Fehler              | Dem Auftrag ist ein Fehler zugeordnet.                         |
| Auftrags \_ Status \_ Offline            | Der Drucker ist offline.                                          |
| Ausgabe des Auftrags \_ Status \_           | Der Drucker ist nicht mehr im Papier.                                     |
| Auftrags \_ Status \_ angehalten             | Der Auftrag wurde angehalten.                                               |
| Auftrags \_ Status \_ gedruckt            | Der Auftrag hat gedruckt.                                             |
| Drucken von Auftrags \_ Status \_           | Der Auftrag wird gedruckt.                                             |
| Auftrags \_ Status \_ neu starten            | Der Auftrag wurde neu gestartet.                                      |
| Auftrags \_ Status \_ Spoolvorgang           | Auftrag ist Spoolvorgang.                                             |
| Auftrags \_ Status \_ Benutzer \_ Eingriff | Der Drucker weist einen Fehler auf, der erfordert, dass der Benutzer etwas tut. |



 

In Windows XP und höheren Versionen von Windows können auch die folgenden Werte verwendet werden:

| Wert                 | Bedeutung                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| Auftrags \_ Status ist \_ fertiggestellt | Der Auftrag wird an den Drucker gesendet, aber möglicherweise noch nicht gedruckt. Weitere Informationen finden Sie unter Hinweise. |
| Auftrags \_ Status \_ beibehalten | Der Auftrag wurde nach dem Drucken in der Druck Warteschlange beibehalten.                              |



 

</dd> <dt>

**Priority**
</dt> <dd>

Die Auftrags Priorität. Bei diesem Element kann es sich um einen der folgenden Werte oder im Bereich zwischen 1 und 99 (minimale \_ Priorität bis Max \_ . Priorität) handeln.



| Wert         | Bedeutung           |
|---------------|-------------------|
| minimale \_ Priorität | Minimale Priorität. |
| maximale \_ Priorität | Maximale Priorität. |
| DEF- \_ Priorität | Standardpriorität. |



 

</dd> <dt>

**Position**
</dt> <dd>

Die Position des Auftrags in der Druck Warteschlange.

</dd> <dt>

**StartTime**
</dt> <dd>

Der früheste Zeitpunkt, an dem der Auftrag gedruckt werden kann.

</dd> <dt>

**UntilTime**
</dt> <dd>

Der letzte Zeitpunkt, zu dem der Auftrag gedruckt werden kann.

</dd> <dt>

**TotalPages**
</dt> <dd>

Die Anzahl der Seiten, die für den Auftrag benötigt werden. Dieser Wert kann NULL sein, wenn der Druckauftrag keine Seiten Begrenzungs Informationen enthält.

</dd> <dt>

**Größe**
</dt> <dd>

Die Größe (in Bytes) des Auftrags.

</dd> <dt>

**Gesendet**
</dt> <dd>

Eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die Uhrzeit angibt, zu der der Auftrag übermittelt wurde.

Dieser Zeitwert liegt im UTC-Format (Universal Time Koordinate) vor. Sie sollten Sie in einen lokalen Uhrzeitwert konvertieren, bevor Sie Sie anzeigen. Sie können die [**filetimetolocalfiletime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) -Funktion verwenden, um die Konvertierung auszuführen.

</dd> <dt>

**Time**
</dt> <dd>

Die Gesamtzeit in Millisekunden, die seit dem Drucken des Auftrags verstrichen ist.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Die Anzahl der Seiten, die gedruckt wurden. Dieser Wert kann NULL sein, wenn der Druckauftrag keine Seiten Begrenzungs Informationen enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Port Monitore, die trueendofjob nicht unterstützen, legen den Auftrag als Auftrags Status fest, \_ \_ nachdem der Auftrag an den Drucker gesendet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Auftrags \_ Informationen \_ 2W** (Unicode) und **\_ Auftrags \_ Informationen \_ 2a** (ANSI)<br/>                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**Setjob**](setjob.md)
</dt> </dl>

 

