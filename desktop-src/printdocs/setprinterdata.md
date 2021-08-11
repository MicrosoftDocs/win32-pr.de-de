---
description: Die SetPrinterData-Funktion legt die Konfigurationsdaten für einen Drucker oder Druckerserver fest.
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: SetPrinterData-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterData
- SetPrinterDataA
- SetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7b28c61030271b9de2e946fd59cddf5253a80cd4faec40ee66ceb2ae6cefdce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233949"
---
# <a name="setprinterdata-function"></a>SetPrinterData-Funktion

Die **SetPrinterData-Funktion** legt die Konfigurationsdaten für einen Drucker oder Druckerserver fest.

Um den Registrierungsschlüssel anzugeben, unter dem die Daten gespeichert werden sollen, rufen Sie die [**SetPrinterDataEx-Funktion**](setprinterdataex.md) auf. Das Aufrufen von **SetPrinterData** entspricht dem Aufrufen der **SetPrinterDataEx-Funktion,** wobei der *pKeyName-Parameter* auf "PrinterDriverData" festgelegt ist.

## <a name="syntax"></a>Syntax


```C++
DWORD SetPrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName,
  _In_ DWORD  Type,
  _In_ LPBYTE pData,
  _In_ DWORD  cbData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker oder Druckerserver, für den die Funktion Konfigurationsdaten festlegt. Verwenden Sie die [**Funktion OpenPrinter,**](openprinter.md) [**OpenPrinter2**](openprinter2.md)oder [**AddPrinter,**](addprinter.md) um ein Druckerhandle abzurufen.

</dd> <dt>

*pValueName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die festzulegenden Daten identifiziert.

Bei Druckern ist diese Zeichenfolge der Name eines Registrierungswerts unter dem Druckerschlüssel "PrinterDriverData" in der Registrierung.

Bei Druckservern ist diese Zeichenfolge eine der vordefinierten Zeichenfolgen, die im folgenden Abschnitt "Hinweise" aufgeführt sind.

</dd> <dt>

*Typ* \[ In\]
</dt> <dd>

Ein Code, der den Datentyp angibt, auf den der *pData-Parameter* zeigt. Eine Liste der möglichen Typcodes finden Sie unter [Registrierungswerttypen.](/windows/desktop/SysInfo/registry-value-types)

</dd> <dt>

*pData* \[ In\]
</dt> <dd>

Ein Zeiger auf ein Bytearray, das die Druckerkonfigurationsdaten enthält.

</dd> <dt>

*cbData* \[ In\]
</dt> <dd>

Die Größe des Arrays in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert **ERROR \_ SUCCESS**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlerwert.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Um vorhandene Konfigurationsdaten für einen Drucker abzurufen, rufen Sie die Funktion [**GetPrinterDataEx**](getprinterdataex.md) oder [**GetPrinterData**](getprinterdata.md) auf.

Wenn *hPrinter* ein Handle für einen Druckserver ist, kann *pValueName* einen der folgenden vordefinierten Werte angeben.



| Wert                                                               | Kommentare                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ ALLOW \_ USER \_ MANAGEFORMS**                                | Windows XP mit Service Pack 2 (SP2) und höher<br/> Windows Server 2003 mit Service Pack 1 (SP1) und höher<br/>                                                                                                    |
| **SPLREG \_ BEEP \_ AKTIVIERT**                                           |                                                                                                                                                                                                                                 |
| **SPLREG \_ DEFAULT \_ SPOOL \_ DIRECTORY**                               |                                                                                                                                                                                                                                 |
| **\_SPLREG-EREIGNISPROTOKOLL \_**                                              |                                                                                                                                                                                                                                 |
| **SPLREG \_ NET \_ POPUP**                                              | In Windows Server 2003 und höher nicht unterstützt<br/>                                                                                                                                                                       |
| **SPLREG \_ PORT \_ THREAD \_ PRIORITY \_ DEFAULT**                         |                                                                                                                                                                                                                                 |
| **PRIORITÄT DES \_ SPLREG-PORTTHREADS \_ \_**                                  |                                                                                                                                                                                                                                 |
| **ISOLATIONSGRUPPEN FÜR \_ SPLREG-DRUCKERTREIBER \_ \_ \_**                        | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **\_ISOLATIONSZEIT DES SPLREG-DRUCKERTREIBERS \_ VOR DEM \_ \_ \_ \_ WIEDERVERWENDEN**         | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG \_ PRINT \_ DRIVER \_ ISOLATION \_ MAX \_ OBJECTS \_ BEFORE \_ RECYCLE** | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **ISOLATION DES \_ SPLREG-DRUCKERTREIBERS \_ \_ IM \_ \_ LEERLAUFTIMEOUT**                 | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **\_ \_ \_ \_ ISOLATIONSAUSFÜHRUNGSRICHTLINIE FÜR \_ SPLREG-DRUCKERTREIBER**             | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG \_ PRINT \_ DRIVER \_ ISOLATION \_ OVERRIDE \_ POLICY**              | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **SPLREG \_ RETRY \_ POPUP**                                            | Bei erfolgreicher Rückgabe enthält *pData* 1, wenn der Server so festgelegt ist, dass popupfenster für alle Aufträge erneut versucht werden, oder 0, wenn der Server keine Popupfenster für alle Aufträge erneut versucht.<br/> In Windows Server 2003 und höher nicht unterstützt<br/> |
| **PRIORITÄT DES SPLREG \_ \_ SCHEDULER-THREADS \_**                             |                                                                                                                                                                                                                                 |
| **SPLREG \_ SCHEDULER \_ THREAD \_ PRIORITY \_ DEFAULT**                    |                                                                                                                                                                                                                                 |
| **SPLREG \_ WEBSHAREMGMT**                                            | Windows Server 2003 und höher<br/>                                                                                                                                                                                        |



 

Die folgenden Werte von *pValueName* bestimmen das Druckverhalten des Pools, wenn ein Fehler auftritt.



| Wert                                       | Kommentare                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ RESTART JOB ON POOL ERROR \_ (SPLREG-NEUSTARTAUFTRAG \_ BEI \_ \_ POOLFEHLER)**   | Der Wert von *pData* gibt die Zeit in Sekunden an, zu der ein Auftrag an einem anderen Port neu gestartet wird, nachdem ein Fehler aufgetreten ist. Diese Einstellung wird mit **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ENABLED** verwendet.<br/> |
| **\_SPLREG-NEUSTARTAUFTRAG \_ \_ FÜR POOL \_ \_ AKTIVIERT** | Ein Wert ungleich 0 (null) in *pData* gibt an, dass **SPLREG \_ RESTART JOB ON \_ POOL \_ \_ \_ ERROR** aktiviert ist.<br/>                                                                                            |



 

Die in **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ERROR** angegebene Zeit ist eine Mindestzeit. Die tatsächliche Zeit kann abhängig von den folgenden Portmonitoreinstellungen länger sein, bei denen es sich um Registrierungswerte unter diesem Registrierungsschlüssel handelt:

**HKLM \\ SYSTEM \\ CurrentControlSet-Steuerelement \\ \\ \\ \\ < *Druckmonitore MonitorName-Ports* > \\**

Rufen Sie die [**RegSetValueEx-Funktion**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) auf, um diese Werte festzulegen.



| Portmonitoreinstellung     | Datentyp      | Bedeutung                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG \_ DWORD** | Wenn ein Wert ungleich 0 (null) ist, kann der Portmonitor den Spooler mit dem Portstatus aktualisieren.<br/>            |
| **StatusUpdateInterval** | **REG \_ DWORD** | Gibt das Intervall in Minuten an, in dem der Portmonitor den Spooler mit dem Portstatus aktualisiert.<br/> |



 

In Windows 7 und höher von Windows werden Druckaufträge, die an einen Druckserver gesendet werden, standardmäßig auf dem Client gerendert. Das clientseitige Rendering eines Druckaufträges kann für jeden Drucker konfiguriert werden, indem die folgenden Werte in *pValueName* festgelegt werden.



| Einstellung                      | Datentyp      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG \_ DWORD** | Der Wert 0 oder , wenn dieser Wert nicht in der Registrierung vorhanden ist, aktiviert das clientseitige Standardrendering von Druckaufträgen.<br/> Der Wert 1 deaktiviert das clientseitige Rendern von Druckaufträgen.<br/>                                                                                                                                                                                                      |
| **ForceClientSideRendering** | **REG \_ DWORD** | Der Wert 0 oder , wenn dieser Wert nicht in der Registrierung vorhanden ist, bewirkt, dass die Druckaufträge auf dem Client gerendert werden. Wenn ein Druckauftrag auf dem Client nicht gerendert werden kann, wird er auf dem Server gerendert. Wenn ein Druckauftrag auf dem Server nicht gerendert werden kann, tritt ein Fehler auf.<br/> Der Wert 1 rendert Druckaufträge auf dem Client. Wenn ein Druckauftrag auf dem Client nicht gerendert werden kann, tritt ein Fehler auf.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **SetPrinterDataW** (Unicode) und **SetPrinterDataA** (ANSI)<br/>                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

