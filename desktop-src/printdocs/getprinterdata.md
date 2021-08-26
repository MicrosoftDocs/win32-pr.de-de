---
description: Die GetPrinterData-Funktion ruft Konfigurationsdaten für den angegebenen Drucker oder Druckerserver ab.
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: GetPrinterData-Funktion (Winspool.h)
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
ms.openlocfilehash: d4cf7d1d1b668974f792c6535f1667f127c78541f4786b32201209553e452c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948790"
---
# <a name="getprinterdata-function"></a>GetPrinterData-Funktion

Die **GetPrinterData-Funktion** ruft Konfigurationsdaten für den angegebenen Drucker oder Druckerserver ab.

In Windows 2000 und höher von Windows entspricht der Aufruf von **GetPrinterData** dem Aufrufen von [**GetPrinterDataEx,**](/windows/desktop/printdocs/getprinterdataex) wobei der *Parameter pKeyName* auf "PrinterDriverData" festgelegt ist.

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

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker oder Druckerserver, für den die Funktion Konfigurationsdaten abruft. Verwenden Sie die [**Funktion OpenPrinter,**](openprinter.md) [**OpenPrinter2**](openprinter2.md)oder [**AddPrinter,**](addprinter.md) um ein Druckerhandle abzurufen.

</dd> <dt>

*pValueName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die abzurufenden Daten identifiziert.

Bei Druckern ist diese Zeichenfolge der Name eines Registrierungswerts unter dem Druckerschlüssel "PrinterDriverData" in der Registrierung.

Bei Druckservern ist diese Zeichenfolge eine der vordefinierten Zeichenfolgen, die im folgenden Abschnitt "Hinweise" aufgeführt sind.

</dd> <dt>

*pType* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Wert empfängt, der den Typ der in *pData* abgerufenen Daten angibt. Die Funktion gibt den im [**SetPrinterData-**](setprinterdata.md) oder [**SetPrinterDataEx-Aufruf**](setprinterdataex.md) angegebenen Typ zurück, der die Daten gespeichert hat. Legen Sie diesen Parameter auf **NULL** fest, wenn Sie den Datentyp nicht benötigen.

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Konfigurationsdaten empfängt.

</dd> <dt>

*nSize* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pData* verweist.

</dd> <dt>

*"Needed"* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der Konfigurationsdaten in Bytes empfängt. Wenn die von *nSize* angegebene Puffergröße zu klein ist, gibt die Funktion **ERROR \_ MORE \_ DATA** zurück, und *"pwNeeded"* gibt die erforderliche Puffergröße an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, lautet der Rückgabewert **ERROR \_ SUCCESS**. Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlerwert.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

**GetPrinterData** ruft Druckerkonfigurationsdaten ab, die von der [**SetPrinterDataEx-**](setprinterdataex.md) oder [**SetPrinterData-Funktion**](setprinterdata.md) festgelegt wurden.

**GetPrinterData** löst möglicherweise einen Windows Aufruf von [**GetPrinterDataFromPort aus,**](/previous-versions//ff550506(v=vs.85))der möglicherweise in die Registrierung schreibt. Wenn dies der Fall ist, können Nebeneffekte auftreten, z. B. das Auslösen eines Updates oder ein Upgrade der Druckerereignis-ID 20 auf dem Client, wenn der Drucker in einem Netzwerk freigegeben ist.

Wenn *hPrinter* ein Handle für einen Druckserver ist, kann *pValueName* einen der folgenden vordefinierten Werte angeben.



| Wert                                                               | Kommentare                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ ALLOW \_ USER \_ MANAGEFORMS**                                | Windows XP mit Service Pack 2 (SP2) und höher<br/> Windows Server 2003 mit Service Pack 1 (SP1) und höher<br/>                                                                                                    |
| **\_SPLREG-ARCHITEKTUR**                                            |                                                                                                                                                                                                                                 |
| **SPLREG \_ BEEP \_ AKTIVIERT**                                           |                                                                                                                                                                                                                                 |
| **SPLREG \_ DEFAULT \_ SPOOL \_ DIRECTORY**                               |                                                                                                                                                                                                                                 |
| **NAME DES \_ SPLREG-DNS-COMPUTERS \_ \_**                                      |                                                                                                                                                                                                                                 |
| **SPLREG \_ DS \_ PRESENT**                                             | Bei erfolgreicher Rückgabe enthält *pData* 0x0001, wenn sich der Computer in einer DS-Domäne befindet, andernfalls 0.<br/>                                                                                                                         |
| **SPLREG \_ DS \_ PRESENT \_ FOR \_ USER**                                  | Bei erfolgreicher Rückgabe enthält *pData* 0x0001, wenn der Benutzer bei einer DS-Domäne angemeldet ist, andernfalls 0.<br/>                                                                                                                   |
| **\_SPLREG-EREIGNISPROTOKOLL \_**                                              |                                                                                                                                                                                                                                 |
| **\_SPLREG-HAUPTVERSION \_**                                          |                                                                                                                                                                                                                                 |
| **\_SPLREG-NEBENVERSION \_**                                          |                                                                                                                                                                                                                                 |
| **SPLREG \_ NET \_ POPUP**                                              | In Windows Server 2003 und höher nicht unterstützt<br/>                                                                                                                                                                       |
| **SPLREG \_ NET \_ POPUP \_ TO \_ COMPUTER**                                | Bei erfolgreicher Rückgabe enthält *pData* 1, wenn Auftragsbenachrichtigungen an den Clientcomputer gesendet werden sollen, oder 0, wenn Auftragsbenachrichtigungen an den Benutzer gesendet werden sollen.<br/> In Windows Server 2003 und höher nicht unterstützt<br/> |
| **\_SPLREG-BETRIEBSSYSTEMVERSION \_**                                             | Windows XP und höher<br/>                                                                                                                                                                                                 |
| **SPLREG \_ OS \_ VERSIONEX**                                           |                                                                                                                                                                                                                                 |
| **SPLREG \_ PORT \_ THREAD \_ PRIORITY \_ DEFAULT**                         |                                                                                                                                                                                                                                 |
| **PRIORITÄT DES \_ SPLREG-PORTTHREADS \_ \_**                                  |                                                                                                                                                                                                                                 |
| **ISOLATIONSGRUPPEN FÜR \_ SPLREG-DRUCKERTREIBER \_ \_ \_**                        | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **\_ISOLATIONSZEIT DES SPLREG-DRUCKERTREIBERS \_ VOR DEM \_ \_ \_ \_ WIEDERVERWENDEN**         | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG \_ PRINT \_ DRIVER \_ ISOLATION \_ MAX \_ OBJECTS \_ BEFORE \_ RECYCLE** | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **ISOLATION DES \_ SPLREG-DRUCKERTREIBERS \_ \_ IM \_ \_ LEERLAUFTIMEOUT**                 | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **\_ \_ \_ \_ ISOLATIONSAUSFÜHRUNGSRICHTLINIE FÜR \_ SPLREG-DRUCKERTREIBER**             | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG \_ PRINT \_ DRIVER \_ ISOLATION \_ OVERRIDE \_ POLICY**              | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG \_ REMOTE \_ FAX**                                             | Bei erfolgreicher Rückgabe enthält *pData* 0x0001, wenn der FAX-Dienst Remoteclients unterstützt, andernfalls 0.<br/>                                                                                                               |
| **SPLREG \_ RETRY \_ POPUP**                                            | Bei erfolgreicher Rückgabe enthält *pData* 1, wenn der Server so festgelegt ist, dass popupfenster für alle Aufträge erneut versucht werden, oder 0, wenn der Server keine Popupfenster für alle Aufträge erneut versucht.<br/> In Windows Server 2003 und höher nicht unterstützt<br/> |
| **PRIORITÄT DES SPLREG \_ \_ SCHEDULER-THREADS \_**                             |                                                                                                                                                                                                                                 |
| **SPLREG \_ SCHEDULER \_ THREAD \_ PRIORITY \_ DEFAULT**                    |                                                                                                                                                                                                                                 |
| **SPLREG \_ WEBSHAREMGMT**                                            | Windows Server 2003 und höher<br/>                                                                                                                                                                                        |



 

Die folgenden Werte von *pValueName* geben das Druckverhalten des Pools an, wenn ein Fehler auftritt.



| Wert                                       | Kommentare                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ RESTART JOB ON POOL ERROR \_ (SPLREG-NEUSTARTAUFTRAG \_ BEI \_ \_ POOLFEHLER)**   | Der Wert von *pData* gibt die Zeit in Sekunden an, zu der ein Auftrag nach einem Fehler an einem anderen Port neu gestartet wird. Diese Einstellung wird mit **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ENABLED** verwendet.<br/> |
| **\_SPLREG-NEUSTARTAUFTRAG \_ \_ FÜR POOL \_ \_ AKTIVIERT** | Ein Wert ungleich 0 (null) in *pData* gibt an, dass **SPLREG \_ RESTART JOB ON \_ POOL \_ \_ \_ ERROR** aktiviert ist.<br/>                                                                                            |



 

Die in **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ERROR** angegebene Zeit ist eine Mindestzeit. Die tatsächliche Zeit kann abhängig von den folgenden Portmonitoreinstellungen länger sein, bei denen es sich um Registrierungswerte unter diesem Registrierungsschlüssel handelt:

**HKLM \\ SYSTEM \\ CurrentControlSet-Steuerelement \\ \\ \\ \\ < *Druckmonitore MonitorName-Ports* > \\**

Rufen Sie die [**RegQueryValueEx-Funktion**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) auf, um diese Werte abzufragen.



| Portmonitoreinstellung     | Datentyp      | Bedeutung                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG \_ DWORD** | Wenn ein Wert ungleich 0 (null) ist, kann der Portmonitor den Spooler mit dem Portstatus aktualisieren.<br/>            |
| **StatusUpdateInterval** | **REG \_ DWORD** | Gibt das Intervall in Minuten an, in dem der Portmonitor den Spooler mit dem Portstatus aktualisiert.<br/> |



 

In Windows 7 und neueren Versionen von Windows werden Druckaufträge, die an einen Druckerserver gesendet werden, standardmäßig auf dem Client gerendert. Die folgenden Werte konfigurieren das clientseitige Rendering eines Druckauftrags und können gelesen werden, wenn Sie die folgenden Werte in *pValueName festlegen.*



| Einstellung                      | Datentyp      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG \_ DWORD** | Der Wert 0 oder , wenn dieser Wert nicht in der Registrierung vorhanden ist, aktiviert das clientseitige Standardrendering von Druckaufträgen.<br/> Der Wert 1 deaktiviert das clientseitige Rendering von Druckaufträgen.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG \_ DWORD** | Der Wert 0 oder , wenn dieser Wert nicht in der Registrierung vorhanden ist, verursacht, dass die Druckaufträge auf dem Client gerendert werden. Wenn ein Druckauftrag auf dem Client nicht gerendert werden kann, wird er auf dem Server gerendert. Wenn ein Druckauftrag nicht auf dem Server gerendert werden kann, wird ein Fehler angezeigt.<br/> Der Wert 1 rendert Druckaufträge auf dem Client. Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, wird ein Fehler angezeigt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **GetPrinterDataW** (Unicode) und **GetPrinterDataA** (ANSI)<br/>                                   |



## <a name="see-also"></a>Siehe auch

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

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> <dt>

[**PRINTPROCESSOR \_ CAPS \_ 1**](printprocessor-caps-1.md)
</dt> </dl>

 

