---
description: Die Funktion findnextprinterchangenotifiruft Informationen über die aktuellste Änderungs Benachrichtigung für ein Änderungs Benachrichtigungs Objekt ab, das einem Drucker oder Druckserver zugeordnet ist.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: Findnextprinterchangenotifi-Funktion (winspool. h)
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
ms.openlocfilehash: ef3ece0d4831409d79e2152cf7b6a37d6bbdc8b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866180"
---
# <a name="findnextprinterchangenotification-function"></a>Findnextprinterchangenotifi-Funktion

Die Funktion **findnextprinterchangenotifiruft** Informationen über die aktuellste Änderungs Benachrichtigung für ein Änderungs Benachrichtigungs Objekt ab, das einem Drucker oder Druckserver zugeordnet ist. Diese Funktion wird aufgerufen, wenn ein warte Vorgang für das Änderungs Benachrichtigungs Objekt erfüllt ist.

Die-Funktion setzt auch das Änderungs Benachrichtigungs Objekt auf den nicht signalisierten Zustand zurück. Anschließend können Sie das Objekt in einem anderen warte Vorgang verwenden, um die Überwachung des Druckers oder des Druck Servers fortzusetzen. Das Betriebssystem legt das Objekt auf den signalisierten Zustand fest, wenn ein bestimmter Satz von Änderungen für den Drucker oder den Druckserver das nächste Mal ausgeführt wird. Die Funktion [**findfirstprinterchangenotifierstellt**](findfirstprinterchangenotification.md) das Änderungs Benachrichtigungs Objekt und gibt die Gruppe der zu überwachenden Änderungen an.

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

*hchange* \[ in\]
</dt> <dd>

Ein Handle für ein Änderungs Benachrichtigungs Objekt, das einem Drucker oder Druckserver zugeordnet ist. Sie erhalten ein solches handle, indem Sie die [**findfirstprinterchangenotifizierungsfunktion**](findfirstprinterchangenotification.md) aufrufen. Das Betriebssystem legt dieses Änderungs Benachrichtigungs Objekt auf den signalisierten Zustand fest, wenn eine der im Änderungs Benachrichtigungs Filter des Objekts angegebenen Änderungen erkannt wird.

</dd> <dt>

*pdwchange* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, deren Bits festgelegt ist, um die Änderungen anzugeben, die aufgetreten sind, um die letzte Benachrichtigung zu verursachen. Die Bitflags, die festgelegt werden können, entsprechen den Werten, die im *fdwfilter* -Parameter des [**findfirstprinterchangenotifizierungsaufrufes**](findfirstprinterchangenotification.md) angegeben sind. Das System legt mindestens eines der folgenden Bitflags fest.



| Wert                                                                                                                                                                                                                                             | Bedeutung                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <dt>**Formular "Drucker \_ Änderung \_ Hinzufügen" \_**</dt> </dl>                                                     | Dem Server wurde ein Formular hinzugefügt.<br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <dt>**Drucker \_ Änderung \_ Auftrag hinzufügen \_**</dt> </dl>                                                        | Ein Druckauftrag wurde an den Drucker gesendet.<br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <dt>**Drucker \_ Änderung \_ " \_ Port hinzufügen"**</dt> </dl>                                                     | Dem Server wurde ein Port oder Monitor hinzugefügt.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <dt>**Drucker \_ Änderung \_ Hinzufügen eines \_ Druck \_ Prozessors**</dt> </dl>                   | Ein Druck Prozessor wurde dem Server hinzugefügt.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <dt>**Drucker \_ Änderung \_ Drucker hinzufügen \_**</dt> </dl>                                            | Ein Drucker wurde dem Server hinzugefügt.<br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <dt>**Drucker \_ Änderung \_ Drucker \_ Treiber hinzufügen \_**</dt> </dl>                      | Ein Druckertreiber wurde dem Server hinzugefügt.<br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <dt>**Port für die Drucker \_ Änderung \_ konfigurieren \_**</dt> </dl>                                   | Auf dem Server wurde ein Port konfiguriert.<br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <dt>**Formular für das Löschen von Drucker \_ Änderungen \_ \_**</dt> </dl>                                            | Ein Formular wurde vom Server gelöscht.<br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <dt>**Auftrag zum Löschen der Drucker \_ Änderung \_ \_**</dt> </dl>                                               | Ein Auftrag wurde gelöscht.<br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <dt>**\_druckeränderungsport \_ Löschen \_**</dt> </dl>                                            | Ein Port oder Monitor wurde vom Server gelöscht.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <dt>**Drucker \_ Änderung \_ Delete- \_ Druck \_ Prozessor**</dt> </dl>          | Ein Druck Prozessor wurde vom Server gelöscht.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <dt>**Drucker \_ Änderung Drucker \_ Löschen \_**</dt> </dl>                                   | Ein Drucker wurde gelöscht.<br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <dt>**Drucker \_ Änderung zum \_ Löschen des \_ Drucker \_ Treibers**</dt> </dl>             | Ein Druckertreiber wurde vom Server gelöscht.<br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <dt>**Fehler beim Drucker \_ Änderungs \_ \_ Verbindungs \_ Drucker.**</dt> </dl> | Fehler bei einer Druckerverbindung.<br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <dt>**Formular für den Drucker \_ Änderungs \_ Satz \_**</dt> </dl>                                                     | Auf dem Server wurde ein Formular festgelegt.<br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <dt>**Auftrag für Drucker \_ Änderungs \_ Satz \_**</dt> </dl>                                                        | Ein Auftrag wurde festgelegt.<br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <dt>**Drucker \_ Änderungs \_ Satz- \_ Drucker**</dt> </dl>                                            | Ein Drucker wurde festgelegt.<br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <dt>**Drucker \_ \_ Treiber- \_ Drucker \_ Treiber**</dt> </dl>                      | Ein Druckertreiber wurde festgelegt.<br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <dt>**\_ \_ Schreib \_ Auftrag für Drucker Änderung**</dt> </dl>                                                  | Es wurden Auftragsdaten geschrieben.<br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <dt>**Drucker \_ Änderungs \_ Timeout**</dt> </dl>                                                         | Timeout des Auftrags.<br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**Drucker \_ Änderungs \_ Server**</dt> </dl>                                                            | Windows 7: auf dem Server ist eine Änderung aufgetreten.<br/>    |



 

</dd> <dt>

*pprinternotifyoptions* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf die Struktur der [**Drucker \_ Benachrichtigungs \_ Optionen**](printer-notify-options.md) . Legen Sie den **Flags** -Member dieser Struktur auf **Drucker \_ Benachrichtigungs \_ Optionen \_ Aktualisieren** fest, damit die Funktion die aktuellen Daten für alle überwachten Drucker Informationsfelder zurückgibt. Die-Funktion ignoriert alle anderen Member der-Struktur. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*ppprinternotifyinfo* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Zeiger Variable, die einen Zeiger auf einen vom System zugewiesenen, schreibgeschützten Puffer empfängt. Wenn Sie damit fertig sind, können Sie die [**freeprinternotifyinfo**](freeprinternotifyinfo.md) -Funktion aufzurufen, um den Puffer freizugeben. Dieser Parameter kann **null** sein, wenn keine Informationen erforderlich sind.

Der Puffer enthält eine [**Drucker \_ Benachrichtigungs \_**](printer-notify-info.md) Struktur, die ein Array von [**Informationen zur \_ Drucker \_ Benachrichtigung \_**](printer-notify-info-data.md) enthält. Jedes Element des Arrays enthält Informationen zu einem der Felder, die im *pprinternotifyoptions* -Parameter des [**findfirstprinterchangenotifizierungsaufrufes**](findfirstprinterchangenotification.md) angegeben sind. In der Regel stellt die Funktion Daten nur für die Felder bereit, die geändert wurden, um die letzte Benachrichtigung zu verursachen. Wenn jedoch die Struktur, auf die der *pprinternotifyoptions* -Parameter verweist, die **\_ Option zur \_ \_ Aktualisierung von Drucker Benachrichtigungen** angibt, stellt die Funktion Daten für alle überwachten Felder bereit.

Wenn das **\_ \_ \_ verworfene** Element für den Drucker Benachrichtigen in der **Flags** - [**Information der \_ Drucker \_ Informations**](printer-notify-info.md) Struktur festgelegt ist, ist ein Überlauf oder Fehler aufgetreten, und die Benachrichtigungen sind möglicherweise verloren gegangen. In diesem Fall werden keine weiteren Benachrichtigungen gesendet, bis Sie einen zweiten **findnextprinterchangenotifizierungsbefehl** ausführen, der die **Aktualisierung der Drucker \_ Benachrichtigungs \_ Optionen \_** angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Rufen Sie die Funktion " **findnextprinterchangenotifitifitifitifitifitifitifitifitifitifitifitifitifiup** " auf, nachdem ein warte Vorgang für ein von [**findfirstprinterchangenotifi**](findfirstprinterchangenotification.md) Durch Aufrufen von **findnextprinterchangenotifikönnen** Sie Informationen zu der Änderung abrufen, die den warte Vorgang erfüllt hat, und das Benachrichtigungs Objekt zurücksetzen, damit es signalisiert werden kann, wenn die nächste Änderung auftritt.

Rufen Sie die **findnextprinterchangenotifi-** Funktion mit einer Ausnahme nicht auf, wenn sich das Änderungs Benachrichtigungs Objekt nicht im signalisierten Zustand befindet. Wenn eine wait-Funktion den **\_ Timeout** Wert der Wartezeit zurückgibt, befindet sich das Änderungs Objekt nicht im signalisierten Zustand. Rufen Sie die Funktion " **findnextprinterchangenotifitifitifitifitifitifitifitifitifitifitifitifitifitifi"** nur auf Eine Ausnahme bildet die Verwendung von **findnextprinterchangenotifizierung** mit dem im Parameter *pprinternotifyoptions* festgelegten **\_ \_ \_ Refresh** -Bit für die Drucker Benachrichtigung. Beachten Sie, dass auch dann, wenn dieses Flag festgelegt ist, das Flag für das **\_ \_ \_ verworfene Drucker Benachrichtigen** weiterhin im *ppprinternotifyinfo* -Parameter festgelegt werden kann.

Wenn Sie die Überwachung des Druckers oder des Druck Servers fortsetzen möchten, wiederholen Sie den Vorgang, indem Sie eine der [Wait-Funktionen](/windows/desktop/Sync/wait-functions) aufrufen und dann die **findnextprinterchangenotifi-** Funktion aufrufen, um die Änderung zu überprüfen und das Benachrichtigungs Objekt zurückzusetzen.

**Findnextprinterchangenotifizierung** kann mehrere Änderungen am gleichen Drucker Informationsfeld in einer einzelnen Benachrichtigung kombinieren. In diesem Fall reduziert die Funktion in der Regel alle Änderungen für das Feld in einem einzelnen Eintrag im Array der [**Drucker \_ \_ Info- \_ Daten**](printer-notify-info-data.md) Strukturen, die in *ppprinternotifyinfo* angezeigt werden. der einzige Eintrag meldet nur die aktuellsten Informationen. Für einige Auftrags-und Drucker Informationsfelder kann die Funktion jedoch mehrere Array Einträge für dasselbe Feld zurückgeben. In diesem Fall meldet der letzte Array Eintrag für das Feld die aktuellen Daten, und die früheren Einträge enthalten die Daten für die Zwischenstufen.

Wenn das Änderungs Benachrichtigungs Objekt nicht mehr benötigt wird, schließen Sie es, indem Sie die [**findcloseprinterchangenotifi-**](findcloseprinterchangenotification.md) Funktion aufrufen.

> [!Note]  
> In Windows XP mit Service Pack 2 (SP2) und höher blockiert die Internetverbindungs Firewall (ICF) standardmäßig Drucker Anschlüsse, eine Ausnahme für die Datei-und Druckfreigabe kann jedoch aktiviert werden. Wenn ein Benutzer eine Druckerverbindung mit einem anderen Computer herstellt und die Ausnahme nicht aktiviert ist, empfängt der Benutzer keine Drucker Änderungs Benachrichtigungen vom Server. Ein Computer Administrator muss die Ausnahme aktivieren.

 

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
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Findcloseprinterchangenotifizierung**](findcloseprinterchangenotification.md)
</dt> <dt>

[**Findfirstprinterchangenotifizierung**](findfirstprinterchangenotification.md)
</dt> <dt>

[**Drucker \_ Benachrichtigungs \_ Informationen**](printer-notify-info.md)
</dt> <dt>

[**\_ \_ Info \_ Daten für Drucker Benachrichtigen**](printer-notify-info-data.md)
</dt> <dt>

[**Drucker \_ Benachrichtigungs \_ Optionen**](printer-notify-options.md)
</dt> </dl>

 

