---
description: Die SetJob-Funktion hält einen Druckauftrag auf einem angegebenen Drucker an, setzt ihn wieder auf, bricht ihn ab oder startet ihn neu. Sie können auch die SetJob-Funktion verwenden, um Druckauftragsparameter wie die Druckauftragspriorität und den Dokumentnamen zu festlegen.
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: SetJob-Funktion (WinSpool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetJob
- SetJobA
- SetJobW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9259429a7696e832bbbe6d0dd4bbb6fb46e7bce2bf7157122c10ca47656af346
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060020"
---
# <a name="setjob-function"></a>SetJob-Funktion

Die **SetJob-Funktion** hält einen Druckauftrag auf einem angegebenen Drucker an, setzt ihn wieder auf, bricht ihn ab oder startet ihn neu. Sie können auch die **SetJob-Funktion** verwenden, um Druckauftragsparameter wie die Druckauftragspriorität und den Dokumentnamen zu festlegen.

Sie können die **SetJob-Funktion** verwenden, um einem Druckauftrag einen Befehl zu geben, Druckauftragsparameter oder beides im selben Aufruf zu tun. Der Wert des *Command-Parameters* wirkt sich nicht darauf aus, wie die Funktion die *Parameter Level* und *pJob* verwendet. Außerdem können Sie **SetJob** mit [**JOB INFO \_ \_ 3 verwenden,**](job-info-3.md) um einen Satz von Druckaufträgen zu verknüpfen. Weitere Informationen finden Sie unter Hinweise.

## <a name="syntax"></a>Syntax


```C++
BOOL SetJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  JobId,
  _In_ DWORD  Level,
  _In_ LPBYTE pJob,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für das druckerorientierte Objekt. Verwenden Sie [**die OpenPrinter-,**](openprinter.md) [**OpenPrinter2-**](openprinter2.md)oder [**AddPrinter-Funktion,**](addprinter.md) um ein Druckerhand handle abzurufen.

</dd> <dt>

*JobId* \[ In\]
</dt> <dd>

Bezeichner, der den Druckauftrag angibt. Sie erhalten eine Druckauftrags-ID, indem Sie die [**AddJob-Funktion**](addjob.md) oder die [**StartDoc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) aufrufen.

Wenn der *Level-Parameter* auf 3 festgelegt ist, muss der *JobId-Parameter* mit dem **JobId-Member** der [**JOB INFO \_ \_ 3-Struktur**](job-info-3.md) übereinstimmen, auf die *pJob zeigt.*

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Der Typ der Auftragsinformationsstruktur, auf die der *pJob-Parameter* zeigt.

**Alle Versionen von Windows:** Sie können den *Level-Parameter* auf 0, 1 oder 2 festlegen. Wenn Sie Level *auf* 0 festlegen, sollte *pJob* NULL **sein.** Verwenden Sie diese Werte, wenn Sie keine Druckauftragsparameter festlegen.

Sie können den *Level-Parameter* auch auf 3 festlegen.

Ab Windows **Vista:** Sie können den *Level-Parameter* auch auf 4 festlegen.

</dd> <dt>

*pJob* \[ In\]
</dt> <dd>

Ein Zeiger auf eine -Struktur, die die Druckauftragsparameter fest legt.

**Alle Versionen von Windows:** *pJob* kann auf eine [**JOB INFO \_ \_ 1-**](job-info-1.md) oder [**JOB INFO \_ \_ 2-Struktur**](job-info-2.md) verweisen.

*pJob* kann auch auf eine [**JOB \_ INFO \_ 3-Struktur**](job-info-3.md) verweisen. Sie müssen über **die Zugriffsberechtigung JOB \_ ACCESS \_ ADMINISTER** für die Aufträge verfügen, die von **den JobId-** und **NextJobId-Membern** der **JOB INFO \_ \_ 3-Struktur angegeben** werden.

Ab Windows **Vista:** *pJob* kann auch auf eine [**JOB INFO \_ \_ 4-Struktur**](job-info-4.md) verweisen.

Wenn der *Level-Parameter* 0 ist, *sollte pJob* NULL **sein.**

</dd> <dt>

*Befehl* \[ In\]
</dt> <dd>

Der durchzuführende Druckauftragsvorgang. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                            | Bedeutung                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <dt>**AUFTRAGSSTEUERUNG \_ \_ ABBRECHEN**</dt> </dl>                                    | Darf nicht verwendet werden. Um einen Druckauftrag zu löschen, verwenden Sie **JOB \_ CONTROL \_ DELETE**.<br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <dt>**AUFTRAGSSTEUERUNG \_ \_ ANHALTEN**</dt> </dl>                                       | Halten Sie den Druckauftrag an.<br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <dt>**NEUSTART \_ DER \_ AUFTRAGSSTEUERUNG**</dt> </dl>                                 | Starten Sie den Druckauftrag neu. Ein Auftrag kann nur neu gestartet werden, wenn er gedruckt wurde.<br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <dt>**AUFTRAGSSTEUERUNG \_ \_ FORTSETZEN**</dt> </dl>                                    | Setzen Sie einen angehaltenen Druckauftrag wieder auf.<br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <dt>**AUFTRAGSSTEUERUNG \_ \_ LÖSCHEN**</dt> </dl>                                    | Löschen Sie den Druckauftrag.<br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <dt>**AN \_ DRUCKER \_ \_ GESENDETE \_ AUFTRAGSSTEUERUNG**</dt> </dl>       | Wird von Portmonitoren verwendet, um den Druckauftrag zu beenden.<br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <dt>**AUFTRAGSSTEUERUNG \_ \_ LETZTE SEITE \_ \_ AUSJIZIERT**</dt> </dl> | Wird von Sprachmonitoren verwendet, um den Druckauftrag zu beenden.<br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <dt>**AUFTRAGSSTEUERUNG \_ \_ BEIBEHALTEN**</dt> </dl>                                    | **Windows Vista und höher:** Behalten Sie den Auftrag in der Warteschlange bei, nachdem er gedruckt wurde.<br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <dt>**\_ \_ AUFTRAGSSTEUERUNGSFREIGABE**</dt> </dl>                                 | **Windows Vista und höher:** Geben Sie den Druckauftrag frei.<br/>                     |



 

Sie können denselben Aufruf der **SetJob-Funktion** verwenden, um Druckauftragsparameter und einen Befehl an einen Druckauftrag zu übergeben. Daher muss *Command* nicht 0 sein, wenn Sie Druckauftragsparameter festlegen, obwohl dies möglich ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Mit der **SetJob-Funktion** können Sie verschiedene Druckauftragsparameter festlegen, indem Sie einen Zeiger auf eine [**JOB \_ INFO \_ 1-,**](job-info-1.md) [**JOB INFO \_ \_ 2-,**](job-info-2.md) [**JOB INFO \_ \_ 3-**](job-info-3.md)oder [**JOB INFO \_ \_ 4-Struktur**](job-info-4.md) angeben, die die erforderlichen Daten enthält.

Um alle Druckaufträge für einen bestimmten Drucker zu entfernen oder zu löschen, rufen Sie die [**Funktion SetPrinter**](setprinter.md) auf, deren *Command-Parameter* auf **PRINTER CONTROL \_ \_ PURGE festgelegt ist.**

Die folgenden Member einer [**JOB \_ INFO \_ 1-,**](job-info-1.md) [**JOB INFO \_ \_ 2-**](job-info-2.md)oder [**JOB INFO \_ \_ 4-Struktur**](job-info-4.md) werden bei einem Aufruf von **SetJob ignoriert:** **JobId**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **Size**, **Submitted**, **Time** und **TotalPages**.

Sie müssen über **die Zugriffsberechtigung PRINTER \_ ACCESS \_ ADMINISTER** für einen Drucker verfügen, um die Position eines Druckauftrags in der Druckwarteschlange zu ändern.

Wenn Sie die Position eines Druckauftrags in der Druckwarteschlange nicht  festlegen möchten, sollten Sie das Position-Member der Struktur [**JOB \_ INFO \_ 1,**](job-info-1.md) [**JOB INFO \_ \_ 2**](job-info-2.md)oder [**JOB INFO \_ \_ 4**](job-info-4.md) auf **JOB POSITION \_ \_ UNSPECIFIED festlegen.**

Verwenden Sie **die SetJob-Funktion** mit [**der JOB INFO \_ \_ 3-Struktur,**](job-info-3.md) um einen Satz von Druckaufträgen (auch als Kette bekannt) zu verknüpfen. Dies ist nützlich in Situationen, in denen ein einzelnes Dokument aus mehreren Teilen besteht, die Sie separat rendern möchten. Um die Aufträge A, B, C und D in der Reihenfolge zu drucken, rufen Sie **SetJob** mit [**JOB INFO \_ \_ 4**](job-info-4.md) auf, um A mit B, B mit C und C mit D zu verknüpfen.

Beachten Sie Folgendes, wenn Sie Druckaufträge verknüpfen:

-   Aufträge können am Anfang oder Ende einer Kette hinzugefügt werden.
-   Alle Aufträge in der Kette müssen denselben Datentyp haben.
-   Die Kette muss vollständig verknüpft sein, bevor das Spooling beginnt. Andernfalls kann der Spooler aufträge drucken und löschen, bevor Sie alle verknüpfen. Es gibt zwei Möglichkeiten, die Kette vor dem vorzeitigen Drucken zu bewahren:

    -   Halten Sie den ersten Auftrag in der Kette an, bis die Kette vollständig verknüpft ist. Der angehaltene Zustand des ersten Auftrags steuert den Status aller Aufträge in der Kette.
    -   Keep the first job incomplete, that is, do not call [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) or [**ScheduleJob**](schedulejob.md) for the first job. Wenn jedoch "drucken während des Spoolens" aktiviert ist (Standardeinstellung), blockiert diese Methode den Port, während die Kette erstellt wird, was auch das Drucken nicht verwandter Aufträge verhindert.

-   Die Anwendung muss den Fall behandeln, in dem der Benutzer einen Auftrag in der Kette löscht, bevor die Kette den Druckvorgang beendet. [**GetLastError gibt**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) **INVALID PARAMETER \_ zurück,** wenn keine JobID vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>WinSpool.h (einschließlich Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WinSpool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **SetJobW** (Unicode) und **SetJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addjob**](addjob.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**AUFTRAGSINFORMATIONEN \_ \_ 1**](job-info-1.md)
</dt> <dt>

[**AUFTRAGSINFORMATIONEN \_ \_ 2**](job-info-2.md)
</dt> <dt>

[**AUFTRAGSINFORMATIONEN \_ \_ 3**](job-info-3.md)
</dt> <dt>

[**AUFTRAGSINFORMATIONEN \_ \_ 4**](job-info-4.md)
</dt> </dl>

 

