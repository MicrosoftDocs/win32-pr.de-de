---
description: Die getprinterdata-Funktion ruft Konfigurationsdaten für den angegebenen Drucker oder Druckserver ab.
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: Getprinterdata-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterData
- GetPrinterDataA
- GetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: cb18936d6d3c1d82f4a52a874883cdcdfaae4815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362350"
---
# <a name="getprinterdata-function"></a>Getprinterdata-Funktion

Die **getprinterdata** -Funktion ruft Konfigurationsdaten für den angegebenen Drucker oder Druckserver ab.

In Windows 2000 und neueren Versionen von Windows entspricht das Aufrufen von **getprinterdata** dem Aufrufen von [**getprinterdataex**](/windows/desktop/printdocs/getprinterdataex) , wobei der *pkeyname* -Parameter auf "printerdriverdata" festgelegt ist.

## <a name="syntax"></a>Syntax


```C++
DWORD GetPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker oder Druckserver, für das die Funktion Konfigurationsdaten abruft. Verwenden Sie die Funktion " [**OpenPrinter**](openprinter.md)", " [**OpenPrinter2**](openprinter2.md)" oder " [**addprinter**](addprinter.md) ", um ein Drucker Handle abzurufen.

</dd> <dt>

*pvaluename* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die abzurufenden Daten identifiziert.

Bei Druckern ist diese Zeichenfolge der Name eines Registrierungs Werts unter dem Schlüssel "printerdriverdata" des Druckers in der Registrierung.

Bei Druckservern handelt es sich bei dieser Zeichenfolge um eine der vordefinierten Zeichen folgen, die im folgenden Abschnitt mit Hinweisen aufgeführt sind.

</dd> <dt>

*pType* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Wert empfängt, der den Typ der in *pData* abgerufenen Daten angibt. Die-Funktion gibt den Typ zurück, der im [**setprinterdata**](setprinterdata.md) -oder [**setprinterdataex**](setprinterdataex.md) -aufrufen angegeben ist, der die Daten gespeichert hat. Legen Sie diesen Parameter auf **null** fest, wenn Sie den-Datentyp nicht benötigen.

</dd> <dt>

*pData* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Konfigurationsdaten empfängt.

</dd> <dt>

*nSize* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pData* verweist.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der Konfigurationsdaten in Bytes empfängt. Wenn die von *nSize* angegebene Puffergröße zu klein ist, gibt die Funktion **Fehler \_ Weitere \_ Daten** zurück, und *pcbrequired* gibt die erforderliche Puffergröße an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **Fehler \_ erfolgreich**. Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlerwert.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

**Getprinterdata** ruft Drucker Konfigurationsdaten ab, die von der [**setprinterdataex**](setprinterdataex.md) -Funktion oder der [**setprinterdata**](setprinterdata.md) -Funktion festgelegt wurden.

**Getprinterdata** löst möglicherweise einen Windows-Befehl an [**getprinterdatafromport**](/previous-versions//ff550506(v=vs.85))aus, der in die Registrierung schreiben könnte. Wenn dies der Fall ist, können Nebeneffekte auftreten, z. b. das Auslösen einer Update-oder upgradedrucker-Ereignis-ID 20 im Client, wenn der Drucker in einem Netzwerk freigegeben ist.

Wenn *hprinter* ein Handle für einen Druckserver ist, kann *pvaluename* einen der folgenden vordefinierten Werte angeben.



| Wert                                                               | Kommentare                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **splreg \_ Allow \_ User \_ manageforms**                                | Windows XP mit Service Pack 2 (SP2) und höher<br/> Windows Server 2003 mit Service Pack 1 (SP1) und höher<br/>                                                                                                    |
| **splreg- \_ Architektur**                                            |                                                                                                                                                                                                                                 |
| **splreg \_ Beep \_ aktiviert**                                           |                                                                                                                                                                                                                                 |
| **splreg \_ - \_ Standard \_ Spoolverzeichnis**                               |                                                                                                                                                                                                                                 |
| **Name der splreg \_ DNS- \_ Maschine \_**                                      |                                                                                                                                                                                                                                 |
| **splreg \_ DS \_ vorhanden**                                             | Bei erfolgreicher Rückgabe enthält *pData* 0x0001, wenn sich der Computer in einer DS-Domäne befindet, andernfalls 0.<br/>                                                                                                                         |
| **splreg \_ DS \_ \_ für \_ Benutzer vorhanden**                                  | Bei erfolgreicher Rückgabe enthält *pData* 0x0001, wenn der Benutzer bei einer DS-Domäne angemeldet ist, andernfalls 0.<br/>                                                                                                                   |
| **splreg- \_ Ereignis \_ Protokoll**                                              |                                                                                                                                                                                                                                 |
| **splreg- \_ Haupt \_ Version**                                          |                                                                                                                                                                                                                                 |
| **splreg- \_ neben \_ Version**                                          |                                                                                                                                                                                                                                 |
| **splreg \_ net- \_ Popup**                                              | Wird in Windows Server 2003 und höher nicht unterstützt.<br/>                                                                                                                                                                       |
| **splreg \_ net- \_ Popup \_ auf \_ Computer**                                | Bei erfolgreicher Rückgabe enthält *pData* 1, wenn Auftrags Benachrichtigungen an den Client Computer gesendet werden sollen, oder 0, wenn Auftrags Benachrichtigungen an den Benutzer gesendet werden sollen.<br/> Wird in Windows Server 2003 und höher nicht unterstützt.<br/> |
| **splreg \_ OS- \_ Version**                                             | Windows XP und höher<br/>                                                                                                                                                                                                 |
| **splreg \_ OS \_ versionex**                                           |                                                                                                                                                                                                                                 |
| **standardmäßige \_ \_ Thread \_ Priorität \_ für den splreg-Port**                         |                                                                                                                                                                                                                                 |
| **\_ \_ Thread \_ Priorität des splreg-Ports**                                  |                                                                                                                                                                                                                                 |
| **splreg \_ - \_ drucktreiberisolations- \_ \_ Gruppen**                        | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **Dauer der \_ Druck \_ Treiber \_ Isolation \_ \_ vor \_ der Wiederverwendung**         | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **maximale Anzahl von Objekten für die \_ Druck \_ Treiber \_ Isolation \_ \_ \_ vor \_ der Wiederverwendung** | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **Leerlauf Timeout der splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**                 | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **Ausführungs Richtlinie der splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**             | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **Außerkraftsetzungs Richtlinie für die splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**              | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **splreg- \_ Remote \_ Fax**                                             | Bei erfolgreicher Rückgabe enthält *pData* 0x0001, wenn der Faxdienst Remote Clients unterstützt, andernfalls 0.<br/>                                                                                                               |
| **splreg- \_ Wiederholungs- \_ Popup**                                            | Bei erfolgreicher Rückgabe enthält *pData* 1, wenn der Server für die Wiederherstellung von Popup Fenstern für alle Aufträge festgelegt ist, oder 0, wenn der Server keine Popup Fenster für alle Aufträge erneut versucht.<br/> Wird in Windows Server 2003 und höher nicht unterstützt.<br/> |
| **splreg \_ Scheduler \_ Thread \_ Priorität**                             |                                                                                                                                                                                                                                 |
| **standardmäßige \_ \_ Thread \_ Priorität \_ für den splreg-Scheduler**                    |                                                                                                                                                                                                                                 |
| **splreg \_ websharemgmt**                                            | Windows Server 2003 und höher<br/>                                                                                                                                                                                        |



 

Die folgenden Werte von *pvaluename* geben das Druck Verhalten des Pools an, wenn ein Fehler auftritt.



| Wert                                       | Kommentare                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_Fehler beim Fehler "splreg Restart \_ Job \_ on \_ Pool \_ ".**   | Der Wert von *pData* gibt die Zeit in Sekunden an, nach der ein Auftrag an einem anderen Port neu gestartet wird, nachdem ein Fehler aufgetreten ist. Diese Einstellung wird mit dem **Auftrag "splreg \_ Restart" \_ \_ bei \_ \_ aktiviertem Pool** verwendet.<br/> |
| **splreg- \_ Neustart \_ Auftrag \_ für \_ Pool \_ aktiviert** | Ein Wert ungleich 0 (null) in *pData* gibt an, dass der **Fehler "splreg \_ Restart \_ Job \_ on \_ Pool \_** " aktiviert ist.<br/>                                                                                            |



 

Die im Fehler des **Auftrags "splreg \_ Restart \_ Job \_ on \_ Pool \_** " angegebene Zeit ist eine minimale Zeit. Die tatsächliche Zeit kann je nach den folgenden Port Monitoreinstellungen, bei denen es sich um Registrierungs Werte unter diesem Registrierungsschlüssel handelt, länger sein:

**HKLM \\ System \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *Monitorname* > \\ Ports**

Aufrufen der [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) -Funktion, um diese Werte abzufragen.



| Port Monitor Einstellung     | Datentyp      | Bedeutung                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **Statusupdateaktivierte**  | **REG \_ DWORD** | Wenn ein Wert ungleich NULL ist, wird es dem Port Monitor ermöglicht, den Spooler mit dem Port Status zu aktualisieren.<br/>            |
| **Statusupdateinterval** | **REG \_ DWORD** | Gibt das Intervall (in Minuten) an, in dem der Port Monitor den Spooler mit dem Port Status aktualisiert.<br/> |



 

In Windows 7 und höheren Versionen von Windows werden Druckaufträge, die an einen Druckserver gesendet werden, standardmäßig auf dem Client gerendert. Die folgenden Werte konfigurieren das Client seitige Rendering von Druckaufträgen und können gelesen werden, wenn Sie die folgenden Werte in " *pvaluename*" festlegen.



| Einstellung                      | Datentyp      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMF despoolingsetting**     | **REG \_ DWORD** | Der Wert 0 (null), oder wenn dieser Wert nicht in der Registrierung vorhanden ist, aktiviert das Client seitige Standard Rendering von Druckaufträgen.<br/> Der Wert 1 deaktiviert das Client seitige Rendering von Druckaufträgen.<br/>                                                                                                                                                                                                          |
| **Forceclientsiderderdering** | **REG \_ DWORD** | Der Wert 0 oder, wenn dieser Wert nicht in der Registrierung vorhanden ist, bewirkt, dass die Druckaufträge auf dem Client gerendert werden. Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, wird er auf dem Server gerendert. Wenn ein Druckauftrag nicht auf dem Server gerendert werden kann, tritt ein Fehler auf.<br/> Bei einem Wert von 1 werden Druckaufträge auf dem Client ausgegeben. Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, tritt ein Fehler auf.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Getprinterdataw** (Unicode) und **getprinterdataa** (ANSI)<br/>                                   |



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

[**Setprinterdata**](setprinterdata.md)
</dt> <dt>

[**Setprinterdataex**](setprinterdataex.md)
</dt> <dt>

[**PrintProcessor-Ober \_ Grenzen \_ 1**](printprocessor-caps-1.md)
</dt> </dl>

 

