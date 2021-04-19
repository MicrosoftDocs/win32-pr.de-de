---
description: Mit der setjob-Funktion wird ein Druckauftrag auf einem angegebenen Drucker angehalten, fortgesetzt, abgebrochen oder neu gestartet. Sie können auch die setjob-Funktion verwenden, um Druckauftrags Parameter festzulegen, z. b. die Druckauftrags Priorität und den Dokumentnamen.
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: Setjob-Funktion (winspool. h)
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
ms.openlocfilehash: 34dfc8c0239a10d7e7f036beed457d57329f4c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349541"
---
# <a name="setjob-function"></a>Setjob-Funktion

Mit der **setjob** -Funktion wird ein Druckauftrag auf einem angegebenen Drucker angehalten, fortgesetzt, abgebrochen oder neu gestartet. Sie können auch die **setjob** -Funktion verwenden, um Druckauftrags Parameter festzulegen, z. b. die Druckauftrags Priorität und den Dokumentnamen.

Mit der **setjob** -Funktion können Sie einem Druckauftrag einen Befehl übergeben, Druckauftrags Parameter festlegen oder beide im gleichen-Befehl ausführen. Der Wert des *Command* -Parameters wirkt sich nicht darauf aus, wie die Funktion die Parameter " *Level* " und " *pjob* " verwendet. Außerdem können Sie **setjob** mit [**Auftrags \_ Info \_ 3**](job-info-3.md) verwenden, um einen Satz von Druckaufträgen miteinander zu verknüpfen. Weitere Informationen finden Sie unter Hinweise.

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

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für das gewünschte Drucker Objekt. Verwenden Sie die Funktion " [**OpenPrinter**](openprinter.md)", " [**OpenPrinter2**](openprinter2.md)" oder " [**addprinter**](addprinter.md) ", um ein Drucker Handle abzurufen.

</dd> <dt>

*JobID* \[ in\]
</dt> <dd>

Bezeichner, der den Druckauftrag angibt. Sie erhalten einen Druckauftrags Bezeichner, indem Sie die [**AddJob**](addjob.md) -Funktion oder die [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) -Funktion aufrufen.

Wenn der *Ebenenparameter* auf 3 festgelegt ist, muss der *JobID* -Parameter mit dem **JobID** -Member der [**Auftrags \_ Info \_ 3**](job-info-3.md) -Struktur, auf die von *pjob* verwiesen wird, stimmen.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Der Typ der Auftrags Informationsstruktur, auf die durch den *pjob* -Parameter verwiesen wird.

**Alle Versionen von Windows**: Sie können den *Level* -Parameter auf 0, 1 oder 2 festlegen. Wenn Sie die *Ebene* auf 0 festlegen, sollte *pjob* **null** sein. Verwenden Sie diese Werte, wenn Sie keine Druckauftrags Parameter festlegen.

Sie können auch den *Level* -Parameter auf 3 festlegen.

Ab **Windows Vista**: Sie können den *Level* -Parameter auch auf 4 festlegen.

</dd> <dt>

*pjob* \[ in\]
</dt> <dd>

Ein Zeiger auf eine-Struktur, die die Druckauftrags Parameter festlegt.

**Alle Versionen von Windows**: *pjob* können auf eine [**Auftrags \_ Info \_ 1**](job-info-1.md) oder eine [**Auftrags \_ Info \_ 2**](job-info-2.md) -Struktur zeigen.

*pjob* kann auch auf eine [**Auftrags \_ Info \_ 3**](job-info-3.md) -Struktur verweisen. Sie müssen über die Berechtigung Zugriffsberechtigung **\_ \_ Verwalten** für die Aufträge verfügen, die von den Membern **JobID** und **nextjobid** der Struktur **Job \_ Info \_ 3** angegeben werden.

Ab **Windows Vista**: *pjob* kann auch auf eine [**Auftrags \_ Info \_ 4**](job-info-4.md) -Struktur verweisen.

Wenn der *Level* -Parameter 0 ist, sollte *pjob* **null** sein.

</dd> <dt>

*Befehl* \[ in\]
</dt> <dd>

Der auszuführende Druckauftrags Vorgang. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                            | Bedeutung                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <dt>**Abbrechen der Auftrags \_ Steuerung \_**</dt> </dl>                                    | Darf nicht verwendet werden. Verwenden Sie zum Löschen eines Druckauftrags **das \_ \_ Löschen von Auftrags Steuer** Elementen.<br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <dt>**Anhalten der Auftrags \_ Steuerung \_**</dt> </dl>                                       | Halten Sie den Druckauftrag an.<br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <dt>**Neustarten der Auftrags \_ Steuerung \_**</dt> </dl>                                 | Starten Sie den Druckauftrag neu. Ein Auftrag kann nur neu gestartet werden, wenn er gedruckt wurde.<br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <dt>**Fortsetzen der Auftrags \_ Steuerung \_**</dt> </dl>                                    | Fortsetzen eines angehaltenen Druckauftrags<br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <dt>**Löschen von Auftrags \_ Steuerelementen \_**</dt> </dl>                                    | Löschen Sie den Druckauftrag.<br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <dt>**\_ \_ \_ an den Drucker gesendete Auftragssteuerung \_**</dt> </dl>       | Wird von Port Monitoren zum Beenden des Druckauftrags verwendet.<br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <dt>**\_ \_ Letzte \_ Seite \_ der Auftragssteuerung**</dt> </dl> | Wird von sprach Monitoren zum Beenden des Druckauftrags verwendet.<br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <dt>**beibehalten der Auftrags \_ Kontrolle \_**</dt> </dl>                                    | **Windows Vista und** höher: behalten Sie den Auftrag in der Warteschlange, nachdem er gedruckt wurde.<br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <dt>**Freigabe der Auftrags \_ Kontrolle \_**</dt> </dl>                                 | **Windows Vista und** höher: Geben Sie den Druckauftrag frei.<br/>                     |



 

Sie können den gleichen **calljob** -Befehl verwenden, um Druckauftrags Parameter festzulegen und einem Druckauftrag einen Befehl zu übergeben. Folglich muss der *Befehl* nicht 0 sein, wenn Sie Druckauftrags Parameter festlegen, obwohl dies der Fall sein kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Mit der **setjob** -Funktion können Sie verschiedene Druckauftrags Parameter festlegen, indem Sie einen Zeiger auf die Struktur " [**Job \_ Info \_ 1**](job-info-1.md)", " [**Job \_ Info \_ 2**](job-info-2.md)", " [**Job \_ Info \_ 3**](job-info-3.md)" oder " [**Job \_ Info \_ 4**](job-info-4.md) " bereitstellen, die die erforderlichen Daten enthält.

Wenn Sie alle Druckaufträge für einen bestimmten Drucker entfernen oder löschen möchten, müssen Sie die Funktion [**SetPrinter**](setprinter.md) aufrufen, wobei der *Befehls* Parameter auf Löschung der **Drucker \_ Steuerung \_** festgelegt ist.

Die folgenden Member der Struktur [**Auftrags \_ Informationen \_ 1**](job-info-1.md), [**Job \_ Info \_ 2**](job-info-2.md)oder [**Job \_ Info \_ 4**](job-info-4.md) werden bei einem Aufruf von **setjob** ignoriert: **JobID**, **pprintername**, **pmachinename**, **pusername**, **pdrivername**, **size**, **Submitted**, **time** und **TotalPages**.

Um die Position eines Druckauftrags in der Druck Warteschlange zu ändern, müssen Sie über die Zugriffsberechtigung " **Drucker \_ Zugriff \_ Verwalten** " verfügen.

Wenn Sie die Position eines Druckauftrags nicht in der Druck Warteschlange festlegen möchten, sollten Sie das **Positions** Element der Struktur [**Auftrags \_ Informationen \_ 1**](job-info-1.md), [**Auftrags \_ Informationen \_ 2**](job-info-2.md)oder [**Auftrags \_ Info \_ 4**](job-info-4.md) auf die **Auftrags Position nicht \_ \_ angegeben** festlegen.

Verwenden Sie die **setjob** -Funktion mit der [**Auftrags \_ Info \_ 3**](job-info-3.md) -Struktur, um einen Satz von Druckaufträgen (auch als Kette bezeichnet) zu verknüpfen. Dies ist in Situationen nützlich, in denen ein einzelnes Dokument aus mehreren Teilen besteht, die Sie separat Rendering möchten. Um die Aufträge A, b, c und D in der richtigen Reihenfolge zu drucken, nennen Sie **setjob** mit [**Auftrags \_ Info \_ 4**](job-info-4.md) , um A mit b, b mit c und c bis D zu verknüpfen.

Beachten Sie beim Verknüpfen von Druckaufträgen Folgendes:

-   Aufträge können am Anfang oder Ende einer Kette hinzugefügt werden.
-   Alle Aufträge in der Kette müssen denselben Datentyp aufweisen.
-   Die Kette muss vollständig verknüpft sein, bevor der Spoolvorgang beginnt. andernfalls kann der Spooler Spoolaufträge drucken und löschen, bevor Sie alle verknüpft werden. Es gibt zwei Möglichkeiten, den Druck von der Kette vorzeitig zu halten:

    -   Hält den ersten Auftrag in der Kette an, bis die Kette vollständig verknüpft ist. Der angehaltene Status des ersten Auftrags steuert den Status aller Aufträge in der Kette.
    -   Lassen Sie den ersten Auftrag unvollständig, d. h., Sie dürfen [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) oder [**schedulejob**](schedulejob.md) nicht für den ersten Auftrag aufzurufen. Wenn jedoch ' Drucken beim Spoolvorgang ' aktiviert ist (Standardeinstellung), blockiert diese Methode den Port, während die Kette erstellt wird. Dadurch wird auch das Drucken nicht verknüpfter Aufträge verhindert.

-   Die Anwendung muss den Fall behandeln, in dem der Benutzer einen Auftrag in der Kette löscht, bevor der Druck der Kette abgeschlossen ist. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen **ungültigen \_ Parameter** zurück, wenn keine JobID vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Setjobw** (Unicode) und **setjoba** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**Auftrags \_ Informationen \_ 1**](job-info-1.md)
</dt> <dt>

[**Auftrags \_ Informationen \_ 2**](job-info-2.md)
</dt> <dt>

[**Auftrags \_ Informationen \_ 3**](job-info-3.md)
</dt> <dt>

[**Auftrags \_ Informationen \_ 4**](job-info-4.md)
</dt> </dl>

 

