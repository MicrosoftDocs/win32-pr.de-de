---
description: Die \_ Job INFO \_ 1-Struktur gibt Druckauftragsinformationen an, z. B. den Auftragsbezeichnerwert, den Namen des Druckers, für den der Auftrag gespoolt wird, den Namen des Computers, der den Druckauftrag erstellt hat, den Namen des Benutzers, der den Druckauftrag besitzt usw.
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: JOB_INFO_1-Struktur (Winspool.h)
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
ms.openlocfilehash: c6e8d5900a0f2d0a2dce5c12d2629abfc80776cdc0ada1354070005e28fbcd37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971329"
---
# <a name="job_info_1-structure"></a>JOB \_ INFO \_ 1-Struktur

Die **Job \_ INFO \_ 1-Struktur** gibt Druckauftragsinformationen an, z. B. den Auftragsbezeichnerwert, den Namen des Druckers, für den der Auftrag gespoolt wird, den Namen des Computers, der den Druckauftrag erstellt hat, den Namen des Benutzers, der den Druckauftrag besitzt usw.

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

**Jobid**
</dt> <dd>

Ein Auftragsbezeichner.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druckers angibt, für den der Auftrag gespoolt wird.

</dd> <dt>

**pMachineName**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Computers angibt, der den Druckauftrag erstellt hat.

</dd> <dt>

**pUserName**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Benutzers angibt, der den Druckauftrag besitzt.

</dd> <dt>

**pDocument**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druckauftrags angibt (z. B. "MS-WORD: Review.doc").

</dd> <dt>

**pDatatype**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Datentyp angibt, der zum Aufzeichnen des Druckauftrags verwendet wird.

</dd> <dt>

**pStatus**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Status des Druckauftrags angibt. Dieser Member sollte vor *Status* überprüft werden. Wenn *pStatus* **NULL** ist, wird der Status durch den Inhalt des Statusmembers definiert.

</dd> <dt>

**Status**
</dt> <dd>

Der Auftragsstatus. Der Wert dieses Members kann 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte sein. Der Wert 0 (null) gibt an, dass die Druckwarteschlange angehalten wurde, nachdem das Spooling des Dokuments abgeschlossen wurde.



| Wert                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ AUFTRAGSSTATUS BLOCKIERT \_ DEVQ      | Der Treiber kann den Auftrag nicht drucken.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| AUFTRAGSSTATUS \_ \_ ABGESCHLOSSEN           | **Windows XP und höher:** Der Auftrag wird an den Drucker gesendet, aber der Auftrag ist möglicherweise noch nicht gedruckt.<br/> Weitere Informationen finden Sie unter Hinweise.<br/>                                                                                                                                                                                                                                                                                                                           |
| AUFTRAGSSTATUS \_ \_ GELÖSCHT            | Der Auftrag wurde gelöscht.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_LÖSCHEN DES AUFTRAGSSTATUS \_           | Der Auftrag wird gelöscht.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_ \_ AUFTRAGSSTATUSFEHLER              | Dem Auftrag wird ein Fehler zugeordnet.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| AUFTRAGSSTATUS \_ \_ OFFLINE            | Der Drucker ist offline.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| JOB \_ STATUS \_ PAPEROUT           | Der Drucker ist nicht mehr auf Papier.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| AUFTRAGSSTATUS \_ \_ ANGEHALTEN             | Der Auftrag wird angehalten.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| AUFTRAGSSTATUS \_ \_ GEDRUCKT            | Der Auftrag wurde gedruckt.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_DRUCKEN DES AUFTRAGSSTATUS \_           | Der Auftrag wird gedruckt.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_ \_ AUFTRAGSSTATUSNEUSTART            | Der Auftrag wurde neu gestartet.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| AUFTRAGSSTATUS \_ \_ BEIBEHALTEN           | **Windows Vista und höher:** Der Auftrag wurde in der Druckwarteschlange beibehalten und kann nicht gelöscht werden. Dies kann folgende Ursachen haben:<br/> 1) Der Auftrag wurde manuell durch einen Aufruf von SetJob beibehalten, und der Spooler wartet darauf, dass der Auftrag freigegeben wird.<br/> 2) Der Auftrag hat den Druck nicht abgeschlossen und muss den Druckvorgang abschließen, bevor er automatisch gelöscht werden kann.<br/> Weitere Informationen zu Druckauftragsbefehlen finden Sie unter [**SetJob.**](setjob.md)<br/> |
| \_ \_ AUFTRAGSSTATUSSPOOLING           | Der Auftrag wird gespoolt.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_BENUTZEREINGRIFF BEIM AUFTRAGSSTATUS \_ \_ | Drucker weist einen Fehler auf, der erfordert, dass der Benutzer etwas tut.                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**Priority**
</dt> <dd>

Die Auftragspriorität. Dieser Member kann einer der folgenden Werte oder im Bereich zwischen 1 und 99 (MIN \_ PRIORITY bis MAX \_ PRIORITY) sein.



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

**TotalPages**
</dt> <dd>

Die Gesamtanzahl der Seiten, die das Dokument enthält. Dieser Wert kann 0 (null) sein, wenn der Druckauftrag keine Seitentrenninformationen enthält.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Die Anzahl der seiten, die gedruckt wurden. Dieser Wert kann 0 (null) sein, wenn der Druckauftrag keine Seitentrenninformationen enthält.

</dd> <dt>

**Gesendet**
</dt> <dd>

Eine [**SYSTEMTIME-Struktur,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) die den Zeitpunkt angibt, zu dem dieses Dokument gespoolt wurde.

Dieser Zeitwert liegt im UTC-Format (Universal Time Coordinate) vor. Sie sollten ihn in einen Lokalen Zeitwert konvertieren, bevor Sie ihn anzeigen. Sie können die [**FileTimeToLocalFileTime-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) verwenden, um die Konvertierung durchzuführen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Portmonitore, die TrueEndOfJob nicht unterstützen, legen den Auftrag direkt nach der Übermittlung des Auftrags an den Drucker als \_ AUFTRAGSSTATUS \_ GEDRUCKT fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ JOB \_ INFO \_ 1W** (Unicode) und **\_ JOB INFO \_ \_ 1A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

