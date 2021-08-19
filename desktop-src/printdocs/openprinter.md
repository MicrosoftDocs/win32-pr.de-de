---
description: Die OpenPrinter-Funktion ruft ein Handle für den angegebenen Drucker oder Druckerserver oder andere Handles im Drucksubsystem ab.
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: OpenPrinter-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter
- OpenPrinterA
- OpenPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 48f25f9c8aec314b997a4600335e22bea2f0bbd8eefa78235ddbb25192f556f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868602"
---
# <a name="openprinter-function"></a>OpenPrinter-Funktion

Die **OpenPrinter-Funktion** ruft ein Handle für den angegebenen Drucker oder Druckerserver oder andere Handles im Drucksubsystem ab.

## <a name="syntax"></a>Syntax


```C++
BOOL OpenPrinter(
  _In_  LPTSTR             pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPrinterName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine nullbeendigte Zeichenfolge, die den Namen des Druckers oder Druckerservers, des Druckerobjekts, des XcvMonitor oder des XcvPort angibt.

Verwenden Sie für ein Druckerobjekt: PrinterName, Job xxxx. Verwenden Sie für einen XcvMonitor ServerName, XcvMonitor MonitorName. Verwenden Sie für einen XcvPort ServerName, XcvPort PortName.

Wenn **DER WERT** NULL ist, wird der lokale Druckerserver angegeben.

</dd> <dt>

*phPrinter* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die ein Handle (nicht threadsicher) zum geöffneten Drucker- oder Druckerserverobjekt empfängt.

Der *phPrinter-Parameter* kann ein Xcv-Handle für die Verwendung mit der XcvData-Funktion zurückgeben. Weitere Informationen zu XcvData finden Sie im DDK.

</dd> <dt>

*pDefault* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**PRINTER \_ DEFAULTS-Struktur.**](printer-defaults.md) Dieser Wert kann NULL **sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode nicht in [**DllMain auf.**](/windows/desktop/Dlls/dllmain)

> [!Note]  
> Ein Handle, das durch einen Aufruf von **OpenPrinter** für einen Remotedrucker ermittelt wurde, greifen über einen lokalen Cache im Druckspoolerdienst auf den Drucker zu. Dieser Cache ist nicht in Echtzeit präzise. Um genaue Daten zu erhalten, ersetzen Sie den OpenPrinter-Aufruf durch [**OpenPrinter2**](openprinter2.md) durch pOptions.dwFlags, der auf PRINTER \_ OPTION NO CACHE festgelegt \_ \_ ist. Beachten Sie, dass nur OpenPrinter2W funktionsfähig ist. Die Funktion gibt ein Druckerhand handle zurück, das andere Druck-API-Aufrufe verwendet und den lokalen Cache umgeht. Diese Methode blockiert, während auf die Netzwerkkommunikation mit dem Remotedrucker gewartet wird, sodass sie möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Wenn Sie diese Funktion aus einem Thread aufrufen, der die Interaktion mit der Benutzeroberfläche verwaltet, reagiert die Anwendung möglicherweise nicht mehr.

 

> [!Note]  
> Ein Handle, das durch einen Aufruf von **OpenPrinter** für einen Remotedrucker ermittelt wird, wird über einen lokalen Cache im Druckspoolerdienst auf den Drucker zugreifen. Dieser Cache ist entwurfsweise nicht in Echtzeit genau. Wenn Sie genaue Daten abrufen müssen, ersetzen Sie den **OpenPrinter-Aufruf** durch [**OpenPrinter2**](openprinter2.md) durch *pOptions.dwFlags,* der auf [**PRINTER OPTION NO CACHE festgelegt \_ \_ \_ ist.**](printer-options.md) Beachten Sie, dass **nur OpenPrinter2W** funktionsfähig ist. Dadurch gibt die Funktion einen Druckerhandpunkt zurück, der andere Druck-API-Aufrufe zum Umgehen des lokalen Caches vorgibt. Beachten Sie, dass dieser Ansatz blockiert wird, während auf die Roundtrip-Netzwerkkommunikation mit dem Remotedrucker gewartet wird, sodass er möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Druckertreiberimplementierung ab– Faktoren, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Daher kann das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, dazu kommen, dass die Anwendung nicht reagiert.

 

Das Handle, auf das *phPrinter zeigt,* ist nicht threadsicher. Wenn Aufrufer sie gleichzeitig auf mehreren Threads verwenden müssen, müssen sie mithilfe der Synchronisierungsfunktionen benutzerdefinierten Synchronisierungszugriff auf das [Druckerhandler bereitstellen.](/windows/desktop/Sync/synchronization-functions) Um zu vermeiden, dass benutzerdefinierter Code geschrieben wird, kann die Anwendung bei Bedarf ein Druckerhand handle für jeden Thread öffnen.

Mit *dem Parameter pDefault* können Sie den Datentyp und die Gerätemoduswerte angeben, die zum Drucken von Dokumenten verwendet werden, die von der [**StartDocPrinter-Funktion übermittelt**](startdocprinter.md) werden. Sie können diese Werte jedoch mithilfe der [**SetJob-Funktion**](setjob.md) überschreiben, nachdem ein Dokument gestartet wurde.

Die [**DEVMODE-Einstellungen,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die in der [**PRINTER \_ DEFAULTS-Struktur**](printer-defaults.md) des *pDefault-Parameters* definiert sind, werden nicht verwendet, wenn der Wert des *pDatatype-Members* der [**DOC INFO \_ \_ 1-Struktur,**](doc-info-1.md) der im *pDocInfo-Parameter* des [**StartDocPrinter-Aufrufs**](startdocprinter.md) übergeben wurde, "RAW" ist. Wenn ein Dokument auf hoher Ebene (z. B. eine Adobe PDF- oder Microsoft Word-Datei) oder andere Druckerdaten (z. B. PCL, PS oder HPGL) direkt an einen Drucker gesendet werden, bei dem *pDatatype* auf "RAW" festgelegt ist, muss das Dokument die DevMODE-Druckauftragseinstellungen in der sprache, die von der Hardware verstanden wird, vollständig beschreiben. 

Sie können die **OpenPrinter-Funktion** aufrufen, um ein Handle für einen Druckerserver zu öffnen oder um die Zugriffsrechte zu bestimmen, die ein Client für einen Druckerserver hat. Geben Sie dazu den Namen des Druckerservers im *Parameter pPrinterName* an, legen Sie die Member **pDatatype** und **pDevMode** der [**PRINTER \_ DEFAULTS-Struktur**](printer-defaults.md) auf **NULL** fest, und legen Sie den **DesiredAccess-Member** so fest, dass ein Serverzugriffsmaskenwert wie SERVER ALL ACCESS angegeben \_ \_ wird. Wenn Sie mit dem Handle fertig sind, übergeben Sie es an die [**ClosePrinter-Funktion,**](closeprinter.md) um es zu schließen.

Verwenden Sie **das DesiredAccess-Mitglied** der [**PRINTER \_ DEFAULTS-Struktur,**](printer-defaults.md) um die Zugriffsrechte anzugeben, die Sie für den Drucker benötigen. Die Zugriffsrechte können wie folgt sein. (Wenn *pDefault* **NULL ist,** sind die Zugriffsrechte PRINTER. \_ ACCESS \_ USE.)



| Gewünschter Zugriffswert                        | Bedeutung                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ DRUCKERZUGRIFFSVERWALTUNG                 | So führen Sie administrative Aufgaben aus, z. B. die von [**SetPrinter bereitgestellten.**](setprinter.md)                                                                                                 |
| \_ \_ DRUCKERZUGRIFFSNUTZUNG                        | So führen Sie grundlegende Druckvorgänge aus.                                                                                                                                                        |
| DRUCKERZUGRIFF \_ \_ AUF ALLE                        | So führen Sie alle administrativen Aufgaben und grundlegenden Druckvorgänge mit Ausnahme von SYNCHRONIZE aus (siehe [Standardzugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights).                                     |
| DRUCKERZUGRIFF \_ \_ VERWALTEN \_ EINGESCHRÄNKT            | So führen Sie administrative Aufgaben aus, z. B. die von [**SetPrinter**](setprinter.md) und [**SetPrinterData bereitgestellten.**](setprinterdata.md) Dieser Wert ist ab dem Windows 8.1. |
| Generische Sicherheitswerte, z. B. WRITE \_ DAC | So lassen Sie bestimmte Zugriffsberechtigungen für die Steuerung zu. Weitere Informationen [finden Sie unter Standardzugriffsrechte.](/windows/desktop/SecAuthZ/standard-access-rights)                                                                                      |



 

Wenn ein Benutzer nicht über die Berechtigung verfügt, einen angegebenen Drucker oder Druckerserver mit dem gewünschten Zugriff zu öffnen, tritt beim **OpenPrinter-Aufruf** ein Fehler mit dem Rückgabewert 0 auf, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Wert ERROR \_ ACCESS \_ DENIED zurück.

## <a name="examples"></a>Beispiele

Ein Beispielprogramm, das diese Funktion verwendet, finden Sie unter How To: Print Using the GDI Print API (How [To: Drucken mithilfe der GDI-Druck-API).](how-to--print-using-the-gdi-print-api.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **OpenPrinterW** (Unicode) und **OpenPrinterA** (ANSI)<br/>                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**\_DRUCKEREINSTELLUNGEN**](printer-defaults.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

