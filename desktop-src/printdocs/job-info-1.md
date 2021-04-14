---
description: Die Struktur der Auftrags \_ Informationen \_ 1 gibt Druckauftrags Informationen an, z. b. den Wert des Auftrags Bezeichners, den Namen des Druckers, für den der Auftrag gespoolte ist, den Namen des Computers, der den Druckauftrag erstellt hat, den Namen des Benutzers, der den Druckauftrag besitzt, usw.
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: JOB_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_1
- _JOB_INFO_1A
- _JOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d56d4d6bce15a661ce141d8e22d27a15837a9f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349079"
---
# <a name="job_info_1-structure"></a>Struktur von Auftrags \_ Informationen \_ 1

Die Struktur der **Auftrags \_ Informationen \_ 1** gibt Druckauftrags Informationen an, z. b. den Wert des Auftrags Bezeichners, den Namen des Druckers, für den der Auftrag gespoolte ist, den Namen des Computers, der den Druckauftrag erstellt hat, den Namen des Benutzers, der den Druckauftrag besitzt, usw.

## <a name="syntax"></a>Syntax


```C++
typedef struct _JOB_INFO_1 {
  DWORD      JobId;
  LPTSTR     pPrinterName;
  LPTSTR     pMachineName;
  LPTSTR     pUserName;
  LPTSTR     pDocument;
  LPTSTR     pDatatype;
  LPTSTR     pStatus;
  DWORD      Status;
  DWORD      Priority;
  DWORD      Position;
  DWORD      TotalPages;
  DWORD      PagesPrinted;
  SYSTEMTIME Submitted;
} JOB_INFO_1, *PJOB_INFO_1;
```



## <a name="members"></a>Member

<dl> <dt>

**JobId**
</dt> <dd>

Ein Auftrags Bezeichner.

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

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Benutzers angibt, der Besitzer des Druckauftrags ist.

</dd> <dt>

**pdocument**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Druckauftrags angibt (z. b. "MS-Word: Review.doc").

</dd> <dt>

**pdatatype**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp angibt, der zum Aufzeichnen des Druckauftrags verwendet wird.

</dd> <dt>

**pstatus**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Status des Druckauftrags angibt. Dieser Member sollte vor dem *Status* geprüft werden, und wenn *pstatus* den Wert **null** hat, wird der Status durch den Inhalt des statusmembers definiert.

</dd> <dt>

**Status**
</dt> <dd>

Der Status des Auftrags. Der Wert dieses Members kann 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte sein. Der Wert 0 (null) gibt an, dass die Druck Warteschlange angehalten wurde, nachdem das Spoolvorgang abgeschlossen wurde.



| Wert                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| der Auftrags \_ Status ist \_ blockiert \_ devq.      | Der Treiber kann den Auftrag nicht drucken.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Auftrags \_ Status ist \_ fertiggestellt           | **Windows XP und höher:** Der Auftrag wird an den Drucker gesendet, aber der Auftrag wurde möglicherweise noch nicht gedruckt.<br/> Weitere Informationen finden Sie unter Hinweise.<br/>                                                                                                                                                                                                                                                                                                                           |
| Auftrags \_ Status \_ gelöscht            | Der Auftrag wurde gelöscht.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Auftrags \_ Status wird \_ gelöscht           | Der Auftrag wird gelöscht.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Auftrags \_ Status \_ Fehler              | Dem Auftrag ist ein Fehler zugeordnet.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Auftrags \_ Status \_ Offline            | Der Drucker ist offline.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Ausgabe des Auftrags \_ Status \_           | Der Drucker ist nicht mehr im Papier.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Auftrags \_ Status \_ angehalten             | Der Auftrag wurde angehalten.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Auftrags \_ Status \_ gedruckt            | Der Auftrag hat gedruckt.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Drucken von Auftrags \_ Status \_           | Der Auftrag wird gedruckt.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Auftrags \_ Status \_ neu starten            | Der Auftrag wurde neu gestartet.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Auftrags \_ Status \_ beibehalten           | **Windows Vista und höher:** Der Auftrag wurde in der Druck Warteschlange beibehalten und kann nicht gelöscht werden. Dies kann folgende Ursachen haben:<br/> 1) der Auftrag wurde manuell durch einen Aufrufen von setjob aufbewahrt, und der Spooler wartet auf die Freigabe des Auftrags.<br/> 2) der Auftrag wurde nicht beendet, und das Drucken muss abgeschlossen sein, bevor er automatisch gelöscht werden kann.<br/> Weitere Informationen zu Druckauftrags Befehlen finden Sie unter [**setjob**](setjob.md) .<br/> |
| Auftrags \_ Status \_ Spoolvorgang           | Auftrag ist Spoolvorgang.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Auftrags \_ Status \_ Benutzer \_ Eingriff | Der Drucker weist einen Fehler auf, der erfordert, dass der Benutzer etwas tut.                                                                                                                                                                                                                                                                                                                                                                                                                |



 

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

**TotalPages**
</dt> <dd>

Die Gesamtanzahl der Seiten, die im Dokument enthalten sind. Dieser Wert kann NULL sein, wenn der Druckauftrag keine Seiten Begrenzungs Informationen enthält.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Die Anzahl der Seiten, die gedruckt wurden. Dieser Wert kann NULL sein, wenn der Druckauftrag keine Seiten Begrenzungs Informationen enthält.

</dd> <dt>

**Gesendet**
</dt> <dd>

Eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die Uhrzeit angibt, zu der dieses Dokument spoolte.

Dieser Zeitwert liegt im UTC-Format (Universal Time Koordinate) vor. Sie sollten Sie in einen lokalen Uhrzeitwert konvertieren, bevor Sie Sie anzeigen. Sie können die [**filetimetolocalfiletime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) -Funktion verwenden, um die Konvertierung auszuführen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Port Monitore, die trueendofjob nicht unterstützen, legen den Auftrag als Auftrags Status fest, \_ \_ nachdem der Auftrag an den Drucker gesendet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Auftrags \_ Informationen \_ 1W** (Unicode) und **\_ Auftrags \_ Informationen \_ 1a** (ANSI)<br/>                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**Setjob**](setjob.md)
</dt> </dl>

 

