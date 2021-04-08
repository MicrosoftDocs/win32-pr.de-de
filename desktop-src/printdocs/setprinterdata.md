---
description: Mit der setprinterdata-Funktion werden die Konfigurationsdaten für einen Drucker oder Druckserver festgelegt.
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: Setprinterdata-Funktion (winspool. h)
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
ms.openlocfilehash: 36af84fe665d68fd7996a0b81fbbf291314cc69e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864751"
---
# <a name="setprinterdata-function"></a>Setprinterdata-Funktion

Mit der **setprinterdata** -Funktion werden die Konfigurationsdaten für einen Drucker oder Druckserver festgelegt.

Um den Registrierungsschlüssel anzugeben, unter dem die Daten gespeichert werden sollen, müssen Sie die Funktion [**setprinterdataex**](setprinterdataex.md) aufrufen. Das Aufrufen von **setprinterdata** entspricht dem Aufrufen der **setprinterdataex** -Funktion, wobei der *pkeyname* -Parameter auf "printerdriverdata" festgelegt ist.

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

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker oder Druckserver, für das die Funktion Konfigurationsdaten festlegt. Verwenden Sie die Funktion " [**OpenPrinter**](openprinter.md)", " [**OpenPrinter2**](openprinter2.md)" oder " [**addprinter**](addprinter.md) ", um ein Drucker Handle abzurufen.

</dd> <dt>

*pvaluename* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die festzulegenden Daten identifiziert.

Bei Druckern ist diese Zeichenfolge der Name eines Registrierungs Werts unter dem Schlüssel "printerdriverdata" des Druckers in der Registrierung.

Bei Druckservern handelt es sich bei dieser Zeichenfolge um eine der vordefinierten Zeichen folgen, die im folgenden Abschnitt mit Hinweisen aufgeführt sind.

</dd> <dt>

*Typ* \[ in\]
</dt> <dd>

Ein Code, der den Datentyp angibt, auf den der *pData* -Parameter verweist. Eine Liste der möglichen Typcodes finden Sie unter [Registrierungs Werttypen](/windows/desktop/SysInfo/registry-value-types).

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Ein Zeiger auf ein Bytearray, das die Drucker Konfigurationsdaten enthält.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Die Größe des Arrays in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **Fehler \_ erfolgreich**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlerwert.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Um vorhandene Konfigurationsdaten für einen Drucker abzurufen, rufen Sie die Funktion [**getprinterdataex**](getprinterdataex.md) oder [**getprinterdata**](getprinterdata.md) auf.

Wenn *hprinter* ein Handle für einen Druckserver ist, kann *pvaluename* einen der folgenden vordefinierten Werte angeben.



| Wert                                                               | Kommentare                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **splreg \_ Allow \_ User \_ manageforms**                                | Windows XP mit Service Pack 2 (SP2) und höher<br/> Windows Server 2003 mit Service Pack 1 (SP1) und höher<br/>                                                                                                    |
| **splreg \_ Beep \_ aktiviert**                                           |                                                                                                                                                                                                                                 |
| **splreg \_ - \_ Standard \_ Spoolverzeichnis**                               |                                                                                                                                                                                                                                 |
| **splreg- \_ Ereignis \_ Protokoll**                                              |                                                                                                                                                                                                                                 |
| **splreg \_ net- \_ Popup**                                              | Wird in Windows Server 2003 und höher nicht unterstützt.<br/>                                                                                                                                                                       |
| **standardmäßige \_ \_ Thread \_ Priorität \_ für den splreg-Port**                         |                                                                                                                                                                                                                                 |
| **\_ \_ Thread \_ Priorität des splreg-Ports**                                  |                                                                                                                                                                                                                                 |
| **splreg \_ - \_ drucktreiberisolations- \_ \_ Gruppen**                        | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **Dauer der \_ Druck \_ Treiber \_ Isolation \_ \_ vor \_ der Wiederverwendung**         | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **maximale Anzahl von Objekten für die \_ Druck \_ Treiber \_ Isolation \_ \_ \_ vor \_ der Wiederverwendung** | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **Leerlauf Timeout der splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**                 | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **Ausführungs Richtlinie der splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**             | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **Außerkraftsetzungs Richtlinie für die splreg- \_ Druck \_ Treiber \_ Isolation \_ \_**              | Windows 7 und höher<br/>                                                                                                                                                                                                  |
| **splreg- \_ Wiederholungs- \_ Popup**                                            | Bei erfolgreicher Rückgabe enthält *pData* 1, wenn der Server für die Wiederherstellung von Popup Fenstern für alle Aufträge festgelegt ist, oder 0, wenn der Server keine Popup Fenster für alle Aufträge erneut versucht.<br/> Wird in Windows Server 2003 und höher nicht unterstützt.<br/> |
| **splreg \_ Scheduler \_ Thread \_ Priorität**                             |                                                                                                                                                                                                                                 |
| **standardmäßige \_ \_ Thread \_ Priorität \_ für den splreg-Scheduler**                    |                                                                                                                                                                                                                                 |
| **splreg \_ websharemgmt**                                            | Windows Server 2003 und höher<br/>                                                                                                                                                                                        |



 

Die folgenden Werte von *pvaluename* bestimmen das Druck Verhalten beim Pool, wenn ein Fehler auftritt.



| Wert                                       | Kommentare                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_Fehler beim Fehler "splreg Restart \_ Job \_ on \_ Pool \_ ".**   | Der Wert von *pData* gibt die Zeit in Sekunden an, nach der ein Auftrag an einem anderen Port neu gestartet wird, nachdem ein Fehler aufgetreten ist. Diese Einstellung wird mit dem **Auftrag "splreg \_ Restart" \_ \_ bei \_ \_ aktiviertem Pool** verwendet.<br/> |
| **splreg- \_ Neustart \_ Auftrag \_ für \_ Pool \_ aktiviert** | Ein Wert ungleich 0 (null) in *pData* gibt an, dass der **Fehler "splreg \_ Restart \_ Job \_ on \_ Pool \_** " aktiviert ist.<br/>                                                                                            |



 

Die im Fehler des **Auftrags "splreg \_ Restart \_ Job \_ on \_ Pool \_** " angegebene Zeit ist eine minimale Zeit. Die tatsächliche Zeit kann je nach den folgenden Port Monitoreinstellungen, bei denen es sich um Registrierungs Werte unter diesem Registrierungsschlüssel handelt, länger sein:

**HKLM \\ System \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *Monitorname* > \\ Ports**

Um diese Werte festzulegen, können Sie die [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) -Funktion aufrufen.



| Port Monitor Einstellung     | Datentyp      | Bedeutung                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **Statusupdateaktivierte**  | **REG \_ DWORD** | Wenn ein Wert ungleich NULL ist, wird es dem Port Monitor ermöglicht, den Spooler mit dem Port Status zu aktualisieren.<br/>            |
| **Statusupdateinterval** | **REG \_ DWORD** | Gibt das Intervall (in Minuten) an, in dem der Port Monitor den Spooler mit dem Port Status aktualisiert.<br/> |



 

In Windows 7 und höheren Versionen von Windows werden Druckaufträge, die an einen Druckserver gesendet werden, standardmäßig auf dem Client gerendert. Das Client seitige Rendering von Druckaufträgen kann für jeden Drucker konfiguriert werden, indem die folgenden Werte in " *pvaluename*" festgelegt werden.



| Einstellung                      | Datentyp      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMF despoolingsetting**     | **REG \_ DWORD** | Der Wert 0 (null), oder wenn dieser Wert nicht in der Registrierung vorhanden ist, aktiviert das Client seitige Standard Rendering von Druckaufträgen.<br/> Der Wert 1 deaktiviert das Client seitige Rendering von Druckaufträgen.<br/>                                                                                                                                                                                                      |
| **Forceclientsiderderdering** | **REG \_ DWORD** | Der Wert 0 oder, wenn dieser Wert nicht in der Registrierung vorhanden ist, bewirkt, dass die Druckaufträge auf dem Client gerendert werden. Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, wird er auf dem Server gerendert. Wenn ein Druckauftrag nicht auf dem Server gerendert werden kann, tritt ein Fehler auf.<br/> Bei einem Wert von 1 werden Druckaufträge auf dem Client ausgegeben. Wenn ein Druckauftrag nicht auf dem Client gerendert werden kann, tritt ein Fehler auf.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Setprinterdataw** (Unicode) und **setprinterdataa** (ANSI)<br/>                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**Getprinterdata**](getprinterdata.md)
</dt> <dt>

[**Getprinterdataex**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Setprinterdataex**](setprinterdataex.md)
</dt> </dl>

 

