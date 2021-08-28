---
description: Die Funktion FindNextPrinterChangeNotification ruft Informationen zur letzten Änderungsbenachrichtigung für ein Änderungsbenachrichtigungsobjekt ab, das einem Drucker oder Druckerserver zugeordnet ist.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: FindNextPrinterChangeNotification-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 37b05603a75f7bc8e68ead2d0dffdec2e99e7618e5461360760f2d9c89ae52da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112480"
---
# <a name="findnextprinterchangenotification-function"></a>FindNextPrinterChangeNotification-Funktion

Die **Funktion FindNextPrinterChangeNotification** ruft Informationen zur letzten Änderungsbenachrichtigung für ein Änderungsbenachrichtigungsobjekt ab, das einem Drucker oder Druckerserver zugeordnet ist. Rufen Sie diese Funktion auf, wenn ein Wartevorgang für das Änderungsbenachrichtigungsobjekt erfüllt ist.

Die Funktion setzt auch das Änderungsbenachrichtigungsobjekt auf den nicht signalisierten Zustand zurück. Sie können das -Objekt dann in einem anderen Wartevorgang verwenden, um die Überwachung des Druckers oder Druckerservers fortzusetzen. Das Betriebssystem legt das Objekt auf den signalisierten Zustand fest, wenn eine der angegebenen Änderungen am Drucker oder Druckerserver das nächste Mal vorgenommen wird. Die [**Funktion FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) erstellt das Änderungsbenachrichtigungsobjekt und gibt den Zu überwachenden Änderungssatz an.

## <a name="syntax"></a>Syntax


```C++
BOOL FindNextPrinterChangeNotification(
  _In_      HANDLE hChange,
  _Out_opt_ PDWORD pdwChange,
  _In_opt_  LPVOID pPrinterNotifyOptions,
  _Out_opt_ LPVOID *ppPrinterNotifyInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hChange* \[ In\]
</dt> <dd>

Ein Handle für ein Änderungsbenachrichtigungsobjekt, das einem Drucker oder Druckerserver zugeordnet ist. Sie erhalten ein solches Handle, indem Sie die [**FindFirstPrinterChangeNotification-Funktion**](findfirstprinterchangenotification.md) aufrufen. Das Betriebssystem legt dieses Änderungsbenachrichtigungsobjekt auf den signalisierten Zustand fest, wenn es eine der Im Änderungsbenachrichtigungsfilter des Objekts angegebenen Änderungen erkennt.

</dd> <dt>

*pdwChange* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, deren Bits festgelegt sind, um die Änderungen anzugeben, die aufgetreten sind, um die letzte Benachrichtigung zu verursachen. Die Bitflags, die möglicherweise festgelegt werden, entsprechen den im *fdwFilter-Parameter* des [**FindFirstPrinterChangeNotification-Aufrufs**](findfirstprinterchangenotification.md) angegebenen Flags. Das System legt mindestens eines der folgenden Bitflags fest.



| Wert                                                                                                                                                                                                                                             | Bedeutung                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <dt>**\_FORMULAR \_ "DRUCKERÄNDERUNG HINZUFÜGEN" \_**</dt> </dl>                                                     | Dem Server wurde ein Formular hinzugefügt.<br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <dt>**DRUCKERÄNDERUNG \_ \_ AUFTRAG HINZUFÜGEN \_**</dt> </dl>                                                        | Ein Druckauftrag wurde an den Drucker gesendet.<br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <dt>**DRUCKERÄNDERUNG \_ \_ PORT HINZUFÜGEN \_**</dt> </dl>                                                     | Dem Server wurde ein Port oder Monitor hinzugefügt.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <dt>**\_DRUCKERÄNDERUNG \_ \_ \_ DRUCKPROZESSOR HINZUFÜGEN**</dt> </dl>                   | Dem Server wurde ein Druckprozessor hinzugefügt.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <dt>**DRUCKERÄNDERUNG \_ \_ DRUCKER HINZUFÜGEN \_**</dt> </dl>                                            | Dem Server wurde ein Drucker hinzugefügt.<br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <dt>**\_DRUCKERÄNDERUNG \_ \_ \_ DRUCKERTREIBER HINZUFÜGEN**</dt> </dl>                      | Dem Server wurde ein Druckertreiber hinzugefügt.<br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <dt>**DRUCKERÄNDERUNG \_ \_ PORT KONFIGURIEREN \_**</dt> </dl>                                   | Auf dem Server wurde ein Port konfiguriert.<br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <dt>**FORMULAR \_ ZUM LÖSCHEN VON DRUCKERÄNDERUNGEN \_ \_**</dt> </dl>                                            | Ein Formular wurde vom Server gelöscht.<br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <dt>**\_ \_ \_ DRUCKERÄNDERUNGSLÖSCHAUFTRAG**</dt> </dl>                                               | Ein Auftrag wurde gelöscht.<br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <dt>**DRUCKERÄNDERUNG \_ \_ – PORT LÖSCHEN \_**</dt> </dl>                                            | Ein Port oder Monitor wurde vom Server gelöscht.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <dt>**\_DRUCKERÄNDERUNG \_ \_ \_ DRUCKPROZESSOR LÖSCHEN**</dt> </dl>          | Ein Druckprozessor wurde vom Server gelöscht.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <dt>**DRUCKERÄNDERUNG \_ \_ DRUCKER LÖSCHEN \_**</dt> </dl>                                   | Ein Drucker wurde gelöscht.<br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <dt>**\_DRUCKERÄNDERUNG \_ \_ \_ DRUCKERTREIBER LÖSCHEN**</dt> </dl>             | Ein Druckertreiber wurde vom Server gelöscht.<br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <dt>**\_DRUCKERÄNDERUNG \_ \_ \_ VERBINDUNGSDRUCKER FEHLGESCHLAGEN**</dt> </dl> | Bei einer Druckerverbindung ist ein Fehler aufgetreten.<br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <dt>**\_FORMULAR FÜR \_ DRUCKERÄNDERUNGSSATZ \_**</dt> </dl>                                                     | Auf dem Server wurde ein Formular festgelegt.<br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <dt>**\_ \_ DRUCKERÄNDERUNGSSATZAUFTRAG \_**</dt> </dl>                                                        | Ein Auftrag wurde festgelegt.<br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <dt>**\_ \_ \_ DRUCKERÄNDERUNGSSATZDRUCKER**</dt> </dl>                                            | Ein Drucker wurde festgelegt.<br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <dt>**\_ \_ \_ \_ DRUCKERWECHSELSATZDRUCKERTREIBER**</dt> </dl>                      | Ein Druckertreiber wurde festgelegt.<br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <dt>**\_ \_ DRUCKERÄNDERUNGSSCHREIBAUFTRAG \_**</dt> </dl>                                                  | Auftragsdaten wurden geschrieben.<br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <dt>**TIMEOUT \_ FÜR DRUCKERWECHSEL \_**</dt> </dl>                                                         | Für den Auftrag ist ein Time out (Timetimeing) für den Auftrag erfolgt.<br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**\_ \_ DRUCKERÄNDERUNGSSERVER**</dt> </dl>                                                            | Windows 7: Auf dem Server ist eine Änderung aufgetreten.<br/>    |



 

</dd> <dt>

*pPrinterNotifyOptions* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**PRINTER \_ NOTIFY \_ OPTIONS-Struktur.**](printer-notify-options.md) Legen Sie den **Flags-Member** dieser Struktur auf **PRINTER NOTIFY OPTIONS \_ \_ \_ REFRESH** fest, damit die Funktion die aktuellen Daten für alle überwachten Druckerinformationsfelder zurückgibt. Die Funktion ignoriert alle anderen Member der -Struktur. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*ppPrinterNotifyInfo* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine Zeigervariable, die einen Zeiger auf einen vom System zugeordneten schreibgeschützten Puffer empfängt. Rufen Sie die [**FreePrinterNotifyInfo-Funktion**](freeprinternotifyinfo.md) auf, um den Puffer frei zu machen, wenn Sie damit fertig sind. Dieser Parameter kann **NULL** sein, wenn keine Informationen erforderlich sind.

Der Puffer enthält eine [**PRINTER \_ NOTIFY \_ INFO-Struktur,**](printer-notify-info.md) die ein Array von PRINTER NOTIFY INFO [**\_ \_ \_ DATA-Strukturen**](printer-notify-info-data.md) enthält. Jedes Element des Arrays enthält Informationen zu einem der Felder, die im *pPrinterNotifyOptions-Parameter* des [**FindFirstPrinterChangeNotification-Aufrufs**](findfirstprinterchangenotification.md) angegeben sind. In der Regel stellt die Funktion nur Daten für die Felder bereit, die geändert wurden, um die letzte Benachrichtigung zu verursachen. Wenn jedoch die Struktur, auf die der *Parameter pPrinterNotifyOptions* zeigt, **PRINTER NOTIFY OPTIONS \_ \_ \_ REFRESH** angibt, stellt die Funktion Daten für alle überwachten Felder bereit.

Wenn das **"PRINTER \_ NOTIFY INFO \_ \_ DISCARDED"-Bit** im **Flags-Member** der [**PRINTER NOTIFY \_ \_ INFO-Struktur**](printer-notify-info.md) festgelegt ist, ist ein Überlauf oder Fehler aufgetreten, und Benachrichtigungen sind möglicherweise verloren gegangen. In diesem Fall werden keine zusätzlichen Benachrichtigungen gesendet, bis Sie einen zweiten **FindNextPrinterChangeNotification-Aufruf** vornehmen, der **PRINTER NOTIFY OPTIONS \_ \_ \_ REFRESH** angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Rufen Sie die **Funktion FindNextPrinterChangeNotification** auf, nachdem ein Wartevorgang für ein von [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) erstelltes Benachrichtigungsobjekt erfüllt wurde. Durch Aufrufen von **FindNextPrinterChangeNotification** können Sie Informationen zu der Änderung abrufen, die den Wartevorgang erfüllt hat, und das Benachrichtigungsobjekt zurücksetzen, damit es bei der nächsten Änderung signalisiert werden kann.

Rufen Sie mit einer Ausnahme die **Funktion FindNextPrinterChangeNotification** nicht auf, wenn sich das Änderungsbenachrichtigungsobjekt nicht im signalisierten Zustand befindet. Wenn eine Wait-Funktion den Wert **WAIT \_ TIMEOUT** zurückgibt, befindet sich das Änderungsobjekt nicht im signalisierten Zustand. Rufen Sie die **Funktion FindNextPrinterChangeNotification** nur dann auf, wenn die Wait-Funktion ohne Timeout erfolgreich ist. Die Ausnahme ist, wenn **FindNextPrinterChangeNotification** aufgerufen wird, wobei das **REFRESH-Bit PRINTER NOTIFY \_ \_ OPTIONS \_** im *Parameter pPrinterNotifyOptions* festgelegt ist. Beachten Sie, dass das FLAG PRINTER NOTIFY **\_ INFO \_ \_ DISCARDED** auch bei Festlegung dieses Flags im *ppPrinterNotifyInfo-Parameter* festgelegt werden kann.

Um die Überwachung des Druckers oder Druckerservers auf Änderungen fortzusetzen, wiederholen Sie den Zyklus des Aufrufs einer der [Wartefunktionen](/windows/desktop/Sync/wait-functions) , und rufen Sie dann die **FindNextPrinterChangeNotification-Funktion** auf, um die Änderung zu untersuchen und das Benachrichtigungsobjekt zurückzusetzen.

**FindNextPrinterChangeNotification** kann mehrere Änderungen am gleichen Druckerinformationsfeld in einer einzigen Benachrichtigung kombinieren. In diesem Fall reduziert die Funktion in der Regel alle Änderungen für das Feld in einen einzelnen Eintrag im Array der [**PRINTER \_ NOTIFY INFO \_ \_ DATA-Strukturen**](printer-notify-info-data.md) in *ppPrinterNotifyInfo.* Der einzelne Eintrag meldet nur die aktuellen Informationen. Bei einigen Auftrags- und Druckerinformationsfeldern kann die Funktion jedoch mehrere Arrayeinträge für dasselbe Feld zurückgeben. In diesem Fall meldet der letzte Arrayeintrag für das Feld die aktuellen Daten, und die früheren Einträge enthalten die Daten für die Zwischenstufen.

Wenn Sie das Änderungsbenachrichtigungsobjekt nicht mehr benötigen, schließen Sie es, indem Sie die [**Funktion FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) aufrufen.

> [!Note]  
> In Windows XP mit Service Pack 2 (SP2) und höher blockiert die Internetverbindungsfirewall (ICF) standardmäßig Druckerports, aber eine Ausnahme für die Datei- und Druckfreigabe kann aktiviert werden. Wenn ein Benutzer eine Druckerverbindung mit einem anderen Computer herstellen und die Ausnahme nicht aktiviert ist, erhält der Benutzer keine Druckeränderungsbenachrichtigungen vom Server. Ein Computeradministrator muss die Ausnahme aktivieren.

 

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird veranschaulicht, wie Sie den Druckerstatus mithilfe dieser Funktionen überwachen können.


```C++
// Get change notification handle for the printer   
chgObject = FindFirstPrinterChangeNotification( 
                hPrinter, 
                PRINTER_CHANGE_JOB, 
                0, 
                NULL); 

if (chgObject != INVALID_HANDLE_VALUE) {
    while (bKeepMonitoring) {
        // Wait for the change notification 
        WaitForSingleObject(chgObject, INFINITE);

        fcnreturn = FindNextPrinterChangeNotification(
                        chgObject, 
                        pdwChange, 
                        NULL, 
                        NULL);

        if (fcnreturn) {
            // Check value of *pdwChange and 
            //  deal with the indicated change 
        }
        // Insert some mechanism to stop monitoring
        //  such as: 
        //
        // if (something happens) {
        //     bKeepMonitoring = false; 
        // }
        //
    }
    // Close Printer Change Notification handle when finished. 
    FindClosePrinterChangeNotification(chgObject);
} else {
    // Unable to open printer change notification handle 
    dwStatus = GetLastError();
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**\_ \_ DRUCKERBENACHRICHTIGUNGSINFORMATIONEN**](printer-notify-info.md)
</dt> <dt>

[**\_ \_ BENACHRICHTIGUNGSINFORMATIONSDATEN DES \_ DRUCKERS**](printer-notify-info-data.md)
</dt> <dt>

[**\_ \_ DRUCKERBENACHRICHTIGUNGSOPTIONEN**](printer-notify-options.md)
</dt> </dl>

 

