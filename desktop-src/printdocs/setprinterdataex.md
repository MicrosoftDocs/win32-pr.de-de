---
description: Die SetPrinterDataEx-Funktion legt die Konfigurationsdaten für einen Drucker oder Druckerserver fest. Die Funktion speichert die Konfigurationsdaten unter dem Registrierungsschlüssel des Druckers.
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: SetPrinterDataEx-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterDataEx
- SetPrinterDataExA
- SetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 6d2904c853510efeb379c9d590852c8f082a4644315560c4dfa5a7f51daca6ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460350"
---
# <a name="setprinterdataex-function"></a>SetPrinterDataEx-Funktion

Die **SetPrinterDataEx-Funktion** legt die Konfigurationsdaten für einen Drucker oder Druckerserver fest. Die Funktion speichert die Konfigurationsdaten unter dem Registrierungsschlüssel des Druckers.

## <a name="syntax"></a>Syntax


```C++
DWORD SetPrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName,
  _In_ DWORD   Type,
  _In_ LPBYTE  pData,
  _In_ DWORD   cbData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker oder Druckerserver, für den die Funktion Konfigurationsdaten festlegt. Verwenden Sie die [**Funktion OpenPrinter,**](openprinter.md) [**OpenPrinter2**](openprinter2.md)oder [**AddPrinter,**](addprinter.md) um ein Druckerhandle abzurufen.

</dd> <dt>

*pKeyName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Schlüssel angibt, der den festzulegenden Wert enthält. Wenn der angegebene Schlüssel oder die angegebenen Unterschlüssel nicht vorhanden sind, erstellt die Funktion sie.

Um Konfigurationsdaten zu speichern, die im Verzeichnisdienst (Directory Service, DS) veröffentlicht werden können, geben Sie einen der folgenden vordefinierten Registrierungsschlüssel an.



| Wert                                                                                                                                                                      | Bedeutung                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <dt>**SPLDS_DRIVER_KEY**</dt> </dl>    | Druckertreiber verwenden diesen Schlüssel, um Treibereigenschaften zu speichern.<br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <dt>**SPLDS_SPOOLER_KEY**</dt> </dl> | Reserviert. Wird nur vom Druckspooler zum Speichern interner Spoolereigenschaften verwendet.<br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <dt>**SPLDS_USER_KEY**</dt> </dl>          | Anwendungen verwenden diesen Schlüssel, um Druckereigenschaften wie Druckerobjektnummern zu speichern.<br/> |



 

Werte, die unter dem SPLDS_USER_KEY Schlüssel gespeichert sind, werden nur dann im Verzeichnisdienst veröffentlicht, wenn im Schema eine entsprechende Eigenschaft vorhanden ist. Ein Domänenadministrator muss die Eigenschaft erstellen, wenn sie noch nicht vorhanden ist. Um eine benutzerdefinierte Eigenschaft zu veröffentlichen, nachdem Sie **SetPrinterDataEx** zum Hinzufügen oder Ändern eines Werts verwendet haben, rufen [**Sie SetPrinter**](setprinter.md) mit *Level* = 7 und mit dem **dwAction-Member** von [**PRINTER_INFO_7 auf**](printer-info-7.md) **DSPRINT_UPDATE** auf.

Sie können andere Schlüssel angeben, um Nicht-DS-Konfigurationsdaten zu speichern. Verwenden Sie den umgekehrten Schrägstrich \\ () als Trennzeichen, um einen Pfad anzugeben, der über einen oder mehrere Unterschlüssel verfügt.

Wenn *hPrinter* ein Handle für einen Drucker und *pKeyName* **NULL** oder eine leere Zeichenfolge ist, gibt **SetPrinterDataEx** **ERROR_INVALID_PARAMETER** zurück.

Wenn *hPrinter* ein Handle für einen Druckserver ist, wird *pKeyName* ignoriert.

Verwenden Sie nicht **SPLDS_SPOOLER_KEY**. Um die Eigenschaften des Spoolerdruckers zu ändern, verwenden [**Sie SetPrinter**](setprinter.md) mit *Level* = 2.

</dd> <dt>

*pValueName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die festzulegenden Daten identifiziert.

Bei Druckern gibt diese Zeichenfolge den Namen eines Werts unter dem *pKeyName-Schlüssel* an.

Bei Druckservern ist diese Zeichenfolge eine der vordefinierten Zeichenfolgen, die im folgenden Abschnitt "Hinweise" aufgeführt sind.

</dd> <dt>

*Typ* \[ In\]
</dt> <dd>

Ein Code, der den Datentyp angibt, auf den der *pData-Parameter* zeigt. Eine Liste der möglichen Typcodes finden Sie unter [Registrierungswerttypen.](/windows/desktop/SysInfo/registry-value-types)

Wenn *pKeyName* einen der vordefinierten Verzeichnisdienstschlüssel angibt, muss *Type* **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD** oder **REG_BINARY** sein. Wenn **REG_BINARY** verwendet wird, muss *cbData* gleich 1 sein, und der Verzeichnisdienst behandelt die Daten als booleschen Wert.

</dd> <dt>

*pData* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Druckerkonfigurationsdaten enthält.

</dd> <dt>

*cbData* \[ In\]
</dt> <dd>

Die Größe des Arrays in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird der Rückgabewert **ERROR_SUCCESS**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlerwert.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Um vorhandene Konfigurationsdaten für einen Drucker oder Druckspooler abzurufen, rufen Sie die [**GetPrinterDataEx-Funktion**](getprinterdataex.md) auf.

Das Aufrufen von **SetPrinterDataEx** mit dem *parameter pKeyName,* der auf "PrinterDriverData" festgelegt ist, entspricht dem Aufrufen der [**SetPrinterData-Funktion.**](setprinterdata.md)

Wenn *hPrinter* ein Handle für einen Druckserver ist, kann *pValueName* einen der folgenden vordefinierten Werte angeben.



| Wert                                                               | Kommentare                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_ALLOW_USER_MANAGEFORMS**                                | Windows XP mit Service Pack 2 (SP2) und höher<br/> Windows Server 2003 mit Service Pack 1 (SP1) und höher<br/>                                                                                                    |
| **SPLREG_BEEP_ENABLED**                                           |                                                                                                                                                                                                                                 |
| **SPLREG_DEFAULT_SPOOL_DIRECTORY**                               |                                                                                                                                                                                                                                 |
| **SPLREG_EVENT_LOG**                                              |                                                                                                                                                                                                                                 |
| **SPLREG_NET_POPUP**                                              | Wird in Windows Server 2003 und höher nicht unterstützt<br/>                                                                                                                                                                       |
| **SPLREG_PORT_THREAD_PRIORITY_DEFAULT**                         |                                                                                                                                                                                                                                 |
| **SPLREG_PORT_THREAD_PRIORITY**                                  |                                                                                                                                                                                                                                 |
| **SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**                        | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**         | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE** | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**                 | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**             | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**              | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG_RETRY_POPUP**                                            | Bei erfolgreicher Rückgabe enthält *pData* 1, wenn der Server so festgelegt ist, dass popupfenster für alle Aufträge erneut versucht werden, oder 0, wenn der Server keine Popupfenster für alle Aufträge erneut versucht.<br/> Wird in Windows Server 2003 und höher nicht unterstützt<br/> |
| **SPLREG_SCHEDULER_THREAD_PRIORITY**                             |                                                                                                                                                                                                                                 |
| **SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**                    |                                                                                                                                                                                                                                 |
| **SPLREG_WEBSHAREMGMT**                                            | Windows Server 2003 und höher<br/>                                                                                                                                                                                        |



 

Durch Übergeben eines der folgenden vordefinierten Werte als *pValueName* wird das Druckverhalten des Pools festgelegt, wenn ein Fehler auftritt.



| Wert                                       | Kommentare                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_RESTART_JOB_ON_POOL_ERROR**   | Der Wert von *pData* gibt die Zeit in Sekunden an, zu der ein Auftrag an einem anderen Port neu gestartet wird, nachdem ein Fehler aufgetreten ist. Diese Einstellung wird mit **SPLREG_RESTART_JOB_ON_POOL_ENABLED** verwendet.<br/> |
| **SPLREG_RESTART_JOB_ON_POOL_ENABLED** | Ein Wert ungleich 0 (null) in *pData* gibt an, dass **SPLREG_RESTART_JOB_ON_POOL_ERROR** aktiviert ist.<br/>                                                                                            |



 

Die in **SPLREG_RESTART_JOB_ON_POOL_ERROR** angegebene Zeit ist eine Mindestzeit. Die tatsächliche Zeit kann abhängig von den folgenden Portmonitoreinstellungen länger sein, bei denen es sich um Registrierungswerte unter diesem Registrierungsschlüssel handelt:

**HKLM \\ SYSTEM \\ CurrentControlSet-Steuerelement \\ \\ \\ \\ < *Druckmonitore MonitorName-Ports* > \\**

Rufen Sie die [**RegSetValueEx-Funktion**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) auf, um diese Werte festzulegen.



| Portmonitoreinstellung     | Datentyp      | Bedeutung                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG_DWORD** | Wenn ein Wert ungleich 0 (null) ist, kann der Portmonitor den Spooler mit dem Portstatus aktualisieren.<br/>            |
| **StatusUpdateInterval** | **REG_DWORD** | Gibt das Intervall in Minuten an, in dem der Portmonitor den Spooler mit dem Portstatus aktualisiert.<br/> |



 

Um sicherzustellen, dass der Spooler Aufträge an den nächsten verfügbaren Drucker im Pool umleitet (wenn der Druckauftrag nicht innerhalb der festgelegten Zeit gedruckt wird), muss der Portmonitor SNMP unterstützen, und die Netzwerkports im Pool müssen als "SNMP-Status aktiviert" konfiguriert werden. Der Portmonitor, der SNMP unterstützt, ist tcp/IP-Standardportmonitor.

In Windows 7 und höher von Windows werden Druckaufträge, die an einen Druckserver gesendet werden, standardmäßig auf dem Client gerendert. Das clientseitige Rendering von Druckaufträgen kann durch Festlegen von *pKeyName* auf "PrinterDriverData" und *pValueName* auf den Einstellungswert in der folgenden Tabelle konfiguriert werden.



| Einstellung                      | Datentyp      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG_DWORD** | Der Wert 0 oder , wenn dieser Wert nicht in der Registrierung vorhanden ist, aktiviert das clientseitige Standardrendering von Druckaufträgen.<br/> Der Wert 1 deaktiviert das clientseitige Rendering von Druckaufträgen.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG_DWORD** | Der Wert 0 oder , wenn dieser Wert nicht in der Registrierung vorhanden ist, wird dazu führen, dass die Druckaufträge auf dem Client gerendert werden. Wenn ein Druckauftrag auf dem Client nicht gerendert werden kann, wird er auf dem Server gerendert. Wenn ein Druckauftrag nicht auf dem Server gerendert werden kann, wird ein Fehler angezeigt.<br/> Der Wert 1 rendert Druckaufträge auf dem Client. Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, wird ein Fehler angezeigt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **SetPrinterDataExW** (Unicode) und **SetPrinterDataExA** (ANSI)<br/>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**PRINTER_INFO_7**](printer-info-7.md)
</dt> </dl>

 

