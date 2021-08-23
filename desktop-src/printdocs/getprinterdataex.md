---
description: Die GetPrinterDataEx-Funktion ruft Konfigurationsdaten für den angegebenen Drucker oder Druckerserver ab.
ms.assetid: 5d9183a7-97cc-46de-848e-e37ce51396eb
title: GetPrinterDataEx-Funktion (Winspool.h)
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
ms.openlocfilehash: 146c4f650b646e5b2be9e0ec809221beebe9f596fcb591fe148be615417faa04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034178"
---
# <a name="getprinterdataex-function"></a>GetPrinterDataEx-Funktion

Die **GetPrinterDataEx-Funktion** ruft Konfigurationsdaten für den angegebenen Drucker oder Druckerserver ab. **GetPrinterDataEx** kann Werte abrufen, die von der [**SetPrinterData-Funktion**](setprinterdata.md) gespeichert wurden. Darüber hinaus kann **GetPrinterDataEx** Werte abrufen, die die [**SetPrinterDataEx-Funktion**](setprinterdataex.md) unter einem angegebenen Schlüssel gespeichert hat.

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

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker oder Druckerserver, für den die Funktion Konfigurationsdaten abruft. Verwenden Sie die [**Funktion OpenPrinter,**](openprinter.md) [**OpenPrinter2**](openprinter2.md)oder [**AddPrinter,**](addprinter.md) um ein Druckerhandle abzurufen.

</dd> <dt>

*pKeyName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Schlüssel angibt, der den abzurufenden Wert enthält. Verwenden Sie den umgekehrten Schrägstrich \\ () als Trennzeichen, um einen Pfad anzugeben, der über einen oder mehrere Unterschlüssel verfügt.

Wenn *hPrinter* ein Handle für einen Drucker und *pKeyName* **NULL** oder eine leere Zeichenfolge ist, gibt **GetPrinterDataEx** **ERROR INVALID \_ \_ PARAMETER** zurück.

Wenn *hPrinter* ein Handle für einen Druckserver ist, wird *pKeyName* ignoriert.

</dd> <dt>

*pValueName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die abzurufenden Daten identifiziert.

Bei Druckern gibt diese Zeichenfolge den Namen eines Werts unter dem *pKeyName-Schlüssel* an.

Bei Druckservern ist diese Zeichenfolge eine der vordefinierten Zeichenfolgen, die im folgenden Abschnitt "Hinweise" aufgeführt sind.

</dd> <dt>

*pType* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die den Typ der im Wert gespeicherten Daten empfängt. Die Funktion gibt den Typ zurück, der im [**SetPrinterDataEx-Aufruf**](setprinterdataex.md) angegeben wurde, als die Daten gespeichert wurden. Dieser Parameter kann **NULL** sein, wenn Sie die Informationen nicht benötigen. **GetPrinterDataEx** übergibt *pType* als *lpdwType-Parameter* eines [**RegQueryValueEx-Funktionsaufrufs.**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Konfigurationsdaten empfängt.

</dd> <dt>

*nSize* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pData* zeigt.

</dd> <dt>

*"Needed"* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der Konfigurationsdaten in Bytes empfängt. Wenn die von *nSize* angegebene Puffergröße zu klein ist, gibt die Funktion **ERROR \_ MORE \_ DATA** zurück, und *"pwNeeded"* gibt die erforderliche Puffergröße an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, lautet der Rückgabewert **ERROR \_ SUCCESS**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlerwert.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

**GetPrinterDataEx** ruft Druckerkonfigurationsdaten ab, die von den Funktionen [**SetPrinterDataEx**](setprinterdataex.md) und [**SetPrinterData**](setprinterdata.md) festgelegt wurden.

Das Aufrufen von **GetPrinterDataEx** mit dem *pKeyName-Parameter,* der auf "PrinterDriverData" festgelegt ist, entspricht dem Aufrufen der [**GetPrinterData-Funktion.**](getprinterdata.md)

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



 

Wenn *pKeyName* einer der vordefinierten DS-Schlüssel (Directory Service) ist (siehe [**SetPrinter**](setprinter.md)) und *pValueName* ein Komma (',') enthält, ist der Teil von *pValueName* vor dem Komma der Wertname, und der Teil von *pValueName* rechts neben dem Komma ist die DS-Eigenschaften-OID. Ein Unterschlüssel namens OID wird erstellt, und ein neuer Wert, der aus dem Wertnamen und der OID besteht, wird unter dem OID-Schlüssel eingegeben. [**SetPrinterDataEx**](setprinterdataex.md) fügt auch den Wertnamen und die Daten unter dem DS-Schlüssel hinzu.

In Windows 7 und höher von Windows werden Druckaufträge, die an einen Druckserver gesendet werden, standardmäßig auf dem Client gerendert. Die Konfiguration des clientseitigen Renderings für einen Drucker kann gelesen werden, indem *pKeyName* auf "PrinterDriverData" und *pValueName* auf den Einstellungswert in der folgenden Tabelle festgelegt wird.



| Einstellung                      | Datentyp      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG \_ DWORD** | Der Wert 0 oder , wenn dieser Wert in der Registrierung nicht vorhanden ist, aktiviert das clientseitige Standardrendering von Druckaufträgen.<br/> Der Wert 1 deaktiviert das clientseitige Rendern von Druckaufträgen.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG \_ DWORD** | Der Wert 0 oder , wenn dieser Wert nicht in der Registrierung vorhanden ist, bewirkt, dass die Druckaufträge auf dem Client gerendert werden. Wenn ein Druckauftrag auf dem Client nicht gerendert werden kann, wird er auf dem Server gerendert. Wenn ein Druckauftrag auf dem Server nicht gerendert werden kann, tritt ein Fehler auf.<br/> Der Wert 1 rendert Druckaufträge auf dem Client. Wenn ein Druckauftrag auf dem Client nicht gerendert werden kann, tritt ein Fehler auf.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **GetPrinterDataExW** (Unicode) und **GetPrinterDataExA** (ANSI)<br/>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

