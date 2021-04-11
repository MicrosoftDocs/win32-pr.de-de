---
description: Die Funktion setprinterdataex legt die Konfigurationsdaten für einen Drucker oder Druckserver fest. Die-Funktion speichert die Konfigurationsdaten unter dem Drucker Registrierungsschlüssel.
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: Setprinterdataex-Funktion (winspool. h)
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
ms.openlocfilehash: 9f384c9c9d6f0d956264b45ec8b52043ad20e897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217839"
---
# <a name="setprinterdataex-function"></a>Setprinterdataex-Funktion

Die Funktion **setprinterdataex** legt die Konfigurationsdaten für einen Drucker oder Druckserver fest. Die-Funktion speichert die Konfigurationsdaten unter dem-Registrierungsschlüssel des Druckers.

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

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker oder Druckserver, für das die Funktion Konfigurationsdaten festlegt. Verwenden Sie die Funktion " [**OpenPrinter**](openprinter.md)", " [**OpenPrinter2**](openprinter2.md)" oder " [**addprinter**](addprinter.md) ", um ein Drucker Handle abzurufen.

</dd> <dt>

*pkeyname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Schlüssel mit dem festzulegenden Wert angibt. Wenn die angegebenen Schlüssel oder Unterschlüssel nicht vorhanden sind, werden Sie von der Funktion erstellt.

Zum Speichern von Konfigurationsdaten, die im Verzeichnisdienst (DS) veröffentlicht werden können, geben Sie einen der folgenden vordefinierten Registrierungsschlüssel an.



| Wert                                                                                                                                                                      | Bedeutung                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <dt>**SPLDS_DRIVER_KEY**</dt> </dl>    | Druckertreiber verwenden diesen Schlüssel zum Speichern von Treiber Eigenschaften.<br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <dt>**SPLDS_SPOOLER_KEY**</dt> </dl> | Reserviert. Wird nur vom Druck Spooler verwendet, um Eigenschaften interner Spooler zu speichern.<br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <dt>**SPLDS_USER_KEY**</dt> </dl>          | Anwendungen verwenden diesen Schlüssel zum Speichern von Druckereigenschaften, z. b. Drucker Medienobjekt Nummern.<br/> |



 

Werte, die unter dem SPLDS_USER_KEY Schlüssel gespeichert werden, werden nur im Verzeichnisdienst veröffentlicht, wenn im Schema eine entsprechende Eigenschaft vorhanden ist. Ein Domänen Administrator muss die-Eigenschaft erstellen, wenn er nicht bereits vorhanden ist. Um eine benutzerdefinierte Eigenschaft zu veröffentlichen, nachdem Sie **setprinterdataex** zum Hinzufügen oder Ändern eines Werts verwendet haben, nennen Sie [**SetPrinter**](setprinter.md) mit *Level* = 7, und der **dwAction** -Member von [**PRINTER_INFO_7**](printer-info-7.md) auf **DSPRINT_UPDATE** festgelegt.

Sie können andere Schlüssel angeben, um nicht-DS-Konfigurationsdaten zu speichern. Verwenden Sie den umgekehrten Schrägstrich ( \\ ) als Trennzeichen, um einen Pfad anzugeben, der über mindestens einen Unterschlüssel verfügt.

Wenn *hprinter* ein Handle für einen Drucker ist und *pkeyname* **null** oder eine leere Zeichenfolge ist, gibt **setprinterdataex** **ERROR_INVALID_PARAMETER** zurück.

Wenn *hprinter* ein Handle für einen Druckserver ist, wird *pkeyname* ignoriert.

Verwenden Sie **SPLDS_SPOOLER_KEY** nicht. Verwenden Sie [**SetPrinter**](setprinter.md) mit *Level* = 2, um die Eigenschaften des Spooler-Druckers zu ändern.

</dd> <dt>

*pvaluename* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die festzulegenden Daten identifiziert.

Bei Druckern gibt diese Zeichenfolge den Namen eines Werts unter dem *pkeyname* -Schlüssel an.

Bei Druckservern handelt es sich bei dieser Zeichenfolge um eine der vordefinierten Zeichen folgen, die im folgenden Abschnitt mit Hinweisen aufgeführt sind.

</dd> <dt>

*Typ* \[ in\]
</dt> <dd>

Ein Code, der den Typ der Daten angibt, auf die der *pData* -Parameter verweist. Eine Liste der möglichen Typcodes finden Sie unter [Registrierungs Werttypen](/windows/desktop/SysInfo/registry-value-types).

Wenn " *pkeyname* " einen der vordefinierten Verzeichnisdienst Schlüssel angibt, muss der *Typ* " **REG_SZ**", " **REG_MULTI_SZ**", " **REG_DWORD**" oder " **REG_BINARY**" lauten. Wenn **REG_BINARY** verwendet wird, müssen *cbData* gleich 1 sein, und der Verzeichnisdienst behandelt die Daten als booleschen Wert.

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Drucker Konfigurationsdaten enthält.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Die Größe des Arrays in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird der Rückgabewert **ERROR_SUCCESS**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlerwert.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Um vorhandene Konfigurationsdaten für einen Drucker oder Druck Spooler abzurufen, rufen Sie die [**getprinterdataex**](getprinterdataex.md) -Funktion auf.

Das Aufrufen von **setprinterdataex** mit dem *pkeyname* -Parameter, der auf "printerdriverdata" festgelegt ist, entspricht dem Aufrufen der [**setprinterdata**](setprinterdata.md) -Funktion.

Wenn *hprinter* ein Handle für einen Druckserver ist, kann *pvaluename* einen der folgenden vordefinierten Werte angeben.



| Wert                                                               | Kommentare                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_ALLOW_USER_MANAGEFORMS**                                | Windows XP mit Service Pack 2 (SP2) und höher<br/> Windows Server 2003 mit Service Pack 1 (SP1) und höher<br/>                                                                                                    |
| **SPLREG_BEEP_ENABLED**                                           |                                                                                                                                                                                                                                 |
| **SPLREG_DEFAULT_SPOOL_DIRECTORY**                               |                                                                                                                                                                                                                                 |
| **SPLREG_EVENT_LOG**                                              |                                                                                                                                                                                                                                 |
| **SPLREG_NET_POPUP**                                              | Wird in Windows Server 2003 und höher nicht unterstützt.<br/>                                                                                                                                                                       |
| **SPLREG_PORT_THREAD_PRIORITY_DEFAULT**                         |                                                                                                                                                                                                                                 |
| **SPLREG_PORT_THREAD_PRIORITY**                                  |                                                                                                                                                                                                                                 |
| **SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**                        | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**         | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE** | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**                 | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**             | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**              | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG_RETRY_POPUP**                                            | Bei erfolgreicher Rückgabe enthält *pData* 1, wenn der Server für die Wiederherstellung von Popup Fenstern für alle Aufträge festgelegt ist, oder 0, wenn der Server keine Popup Fenster für alle Aufträge erneut versucht.<br/> Wird in Windows Server 2003 und höher nicht unterstützt.<br/> |
| **SPLREG_SCHEDULER_THREAD_PRIORITY**                             |                                                                                                                                                                                                                                 |
| **SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**                    |                                                                                                                                                                                                                                 |
| **SPLREG_WEBSHAREMGMT**                                            | Windows Server 2003 und höher<br/>                                                                                                                                                                                        |



 

Wenn Sie einen der folgenden vordefinierten Werte als *pvaluename* übergeben, wird das Druck Verhalten des Pools festgelegt, wenn ein Fehler auftritt.



| Wert                                       | Kommentare                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_RESTART_JOB_ON_POOL_ERROR**   | Der Wert von *pData* gibt die Zeit in Sekunden an, nach der ein Auftrag an einem anderen Port neu gestartet wird, nachdem ein Fehler aufgetreten ist. Diese Einstellung wird mit **SPLREG_RESTART_JOB_ON_POOL_ENABLED** verwendet.<br/> |
| **SPLREG_RESTART_JOB_ON_POOL_ENABLED** | Ein Wert ungleich 0 (null) in *pData* gibt an, dass **SPLREG_RESTART_JOB_ON_POOL_ERROR** aktiviert ist.<br/>                                                                                            |



 

Die in **SPLREG_RESTART_JOB_ON_POOL_ERROR** angegebene Zeit ist eine minimale Zeit. Die tatsächliche Zeit kann je nach den folgenden Port Monitoreinstellungen, bei denen es sich um Registrierungs Werte unter diesem Registrierungsschlüssel handelt, länger sein:

**HKLM \\ System \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *Monitorname* > \\ Ports**

Um diese Werte festzulegen, können Sie die [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) -Funktion aufrufen.



| Port Monitor Einstellung     | Datentyp      | Bedeutung                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **Statusupdateaktivierte**  | **REG_DWORD** | Wenn ein Wert ungleich NULL ist, wird es dem Port Monitor ermöglicht, den Spooler mit dem Port Status zu aktualisieren.<br/>            |
| **Statusupdateinterval** | **REG_DWORD** | Gibt das Intervall (in Minuten) an, in dem der Port Monitor den Spooler mit dem Port Status aktualisiert.<br/> |



 

Um sicherzustellen, dass der Spooler Aufträge an den nächsten verfügbaren Drucker im Pool umleitet (wenn der Druckauftrag nicht innerhalb der festgelegten Zeit gedruckt wird), muss der Port Monitor SNMP unterstützen, und die Netzwerkports im Pool müssen als "aktivierter SNMP-Status" konfiguriert sein. Der Port Monitor, der SNMP unterstützt, ist der TCP/IP-Port Monitor (Standard).

In Windows 7 und höheren Versionen von Windows werden Druckaufträge, die an einen Druckserver gesendet werden, standardmäßig auf dem Client gerendert. Das Client seitige Rendering von Druckaufträgen kann konfiguriert werden, indem *pkeyname* auf "printerdriverdata" und *pvaluename* auf den Einstellungs Wert in der folgenden Tabelle festgelegt wird.



| Einstellung                      | Datentyp      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMF despoolingsetting**     | **REG_DWORD** | Der Wert 0 (null), oder wenn dieser Wert nicht in der Registrierung vorhanden ist, aktiviert das Client seitige Standard Rendering von Druckaufträgen.<br/> Der Wert 1 deaktiviert das Client seitige Rendering von Druckaufträgen.<br/>                                                                                                                                                                                                          |
| **Forceclientsiderderdering** | **REG_DWORD** | Der Wert 0 oder, wenn dieser Wert nicht in der Registrierung vorhanden ist, bewirkt, dass die Druckaufträge auf dem Client gerendert werden. Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, wird er auf dem Server gerendert. Wenn ein Druckauftrag nicht auf dem Server gerendert werden kann, tritt ein Fehler auf.<br/> Bei einem Wert von 1 werden Druckaufträge auf dem Client ausgegeben. Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, tritt ein Fehler auf.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Setprinterdataexw** (Unicode) und **setprinterdataexa** (ANSI)<br/>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Getprinterdataex**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**PRINTER_INFO_7**](printer-info-7.md)
</dt> </dl>

 

