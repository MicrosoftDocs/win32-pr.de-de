---
description: Die getprinterdataex-Funktion ruft Konfigurationsdaten für den angegebenen Drucker oder Druckserver ab.
ms.assetid: 5d9183a7-97cc-46de-848e-e37ce51396eb
title: Getprinterdataex-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDataEx
- GetPrinterDataExA
- GetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bdadf2e1259445ca5285e5b12bc906140a137cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759661"
---
# <a name="getprinterdataex-function"></a>Getprinterdataex-Funktion

Die **getprinterdataex** -Funktion ruft Konfigurationsdaten für den angegebenen Drucker oder Druckserver ab. **Getprinterdataex** kann Werte abrufen, die von der [**setprinterdata**](setprinterdata.md) -Funktion gespeichert wurden. Außerdem kann **getprinterdataex** Werte abrufen, die von der [**setprinterdataex**](setprinterdataex.md) -Funktion unter einem angegebenen Schlüssel gespeichert wurden.

## <a name="syntax"></a>Syntax


```C++
DWORD GetPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _In_  LPCTSTR pValueName,
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

*pkeyname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Schlüssel mit dem abzurufenden Wert angibt. Verwenden Sie den umgekehrten Schrägstrich ( \\ ) als Trennzeichen, um einen Pfad anzugeben, der über mindestens einen Unterschlüssel verfügt.

Wenn *hprinter* ein Handle für einen Drucker ist und *pkeyname* **null** oder eine leere Zeichenfolge ist, gibt **getprinterdataex** einen **\_ ungültigen \_ Parameter** zurück.

Wenn *hprinter* ein Handle für einen Druckserver ist, wird *pkeyname* ignoriert.

</dd> <dt>

*pvaluename* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die abzurufenden Daten identifiziert.

Bei Druckern gibt diese Zeichenfolge den Namen eines Werts unter dem *pkeyname* -Schlüssel an.

Bei Druckservern handelt es sich bei dieser Zeichenfolge um eine der vordefinierten Zeichen folgen, die im folgenden Abschnitt mit Hinweisen aufgeführt sind.

</dd> <dt>

*pType* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die den Typ der im-Wert gespeicherten Daten empfängt. Die-Funktion gibt den Typ zurück, der im [**setprinterdataex**](setprinterdataex.md) -Befehl angegeben wurde, als die Daten gespeichert wurden. Dieser Parameter kann **null** sein, wenn Sie die Informationen nicht benötigen. **Getprinterdataex** übergibt *pType* als den *lpdwtype* -Parameter eines [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) -Funktions Aufrufes.

</dd> <dt>

*pData* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Konfigurationsdaten empfängt.

</dd> <dt>

*nSize* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pData* zeigt.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der Konfigurationsdaten in Bytes empfängt. Wenn die von *nSize* angegebene Puffergröße zu klein ist, gibt die Funktion **Fehler \_ Weitere \_ Daten** zurück, und *pcbrequired* gibt die erforderliche Puffergröße an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **Fehler \_ erfolgreich**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlerwert.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

**Getprinterdataex** ruft Drucker Konfigurationsdaten ab, die von den Funktionen [**setprinterdataex**](setprinterdataex.md) und [**setprinterdata**](setprinterdata.md) festgelegt wurden.

Der Aufruf von **getprinterdataex** mit dem *pkeyname* -Parameter, der auf "printerdriverdata" festgelegt ist, entspricht dem Aufrufen der [**getprinterdata**](getprinterdata.md) -Funktion.

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



 

Wenn *pkeyname* einer der vordefinierten Verzeichnisdienst (DS)-Schlüssel ist (siehe [**SetPrinter**](setprinter.md)) und *pvaluename* ein Komma (",") enthält, ist der Teil von " *pvaluename* " vor dem Komma der Wertname, und der Teil von " *pvaluename* " rechts neben dem Komma ist die DS-Eigenschaften-OID. Ein Unterschlüssel namens OID wird erstellt, und ein neuer Wert, der aus dem Wertnamen und der OID besteht, wird unter dem OID-Schlüssel eingegeben. [**Setprinterdataex**](setprinterdataex.md) fügt auch den Wertnamen und die Daten unter dem DS-Schlüssel hinzu.

In Windows 7 und höheren Versionen von Windows werden Druckaufträge, die an einen Druckserver gesendet werden, standardmäßig auf dem Client gerendert. Die Konfiguration des Client seitigen Renderings für einen Drucker kann gelesen werden, indem *pkeyname* auf "printerdriverdata" und *pvaluename* auf den Einstellungs Wert in der folgenden Tabelle festgelegt wird.



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
| Unicode- und ANSI-Name<br/>   | **Getprinterdataexw** (Unicode) und **getprinterdataexa** (ANSI)<br/>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Setprinterdataex**](setprinterdataex.md)
</dt> </dl>

 

