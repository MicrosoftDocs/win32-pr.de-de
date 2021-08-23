---
description: Die Funktion AddPrinter fügt der Liste der unterstützten Drucker für einen angegebenen Server einen Drucker hinzu.
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: AddPrinter-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinter
- AddPrinterA
- AddPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6034c330da19f5982e9bbacbf75cc16f0a7d10dd65f9c8bded2efa5cbda70835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601140"
---
# <a name="addprinter-function"></a>AddPrinter-Funktion

Die **Funktion AddPrinter** fügt der Liste der unterstützten Drucker für einen angegebenen Server einen Drucker hinzu.

## <a name="syntax"></a>Syntax


```C++
HANDLE AddPrinter(
  _In_ LPTSTR *pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem der Drucker installiert werden soll. Wenn diese Zeichenfolge **NULL** ist, wird der Drucker lokal installiert.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Die Version der -Struktur, auf die *pPrinter* verweist. Dieser Wert muss 2 sein.

</dd> <dt>

*pPrinter* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**PRINTER \_ INFO \_ 2-Struktur,**](printer-info-2.md) die Informationen zum Drucker enthält. Sie müssen werte ungleich **NULL** für die **Member pPrinterName,** **pPortName,** **pDriverName** und **pPrintProcessor** dieser Struktur angeben, bevor **Sie AddPrinter** aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Handle (nicht threadsicher) für ein neues Druckerobjekt. Wenn Sie mit dem Handle fertig sind, übergeben Sie es an die [**ClosePrinter-Funktion,**](closeprinter.md) um es zu schließen.

Wenn die Funktion fehlschlägt, ist der Rückgabewert **NULL.**

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode nicht in [**DllMain**](/windows/desktop/Dlls/dllmain)auf.

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Der Aufrufer muss über [seLoadDriverPrivilege verfügen.](/windows/desktop/SecAuthZ/authorization-constants)

Das zurückgegebene Handle ist nicht threadsicher. Wenn Aufrufer sie gleichzeitig in mehreren Threads verwenden müssen, müssen sie mithilfe der [Synchronisierungsfunktionen](/windows/desktop/Sync/synchronization-functions)benutzerdefinierten Synchronisierungszugriff auf das Druckerhandle bereitstellen. Um das Schreiben von benutzerdefiniertem Code zu vermeiden, kann die Anwendung bei Bedarf ein Druckerhandle für jeden Thread öffnen.

Es folgen die Member der [**PRINTER \_ INFO \_ 2-Struktur,**](printer-info-2.md) die festgelegt werden können, bevor die **AddPrinter-Funktion** aufgerufen wird:

-   **Attribute**
-   **pPrintProcessor**
-   **DefaultPriority**
-   **Priority**
-   **pComment**
-   **pSecurityDescriptor**
-   **pDatatype**
-   **pSepFile**
-   **pDevMode**
-   **pShareName**
-   **pLocation**
-   **StartTime**
-   **pParameters**
-   **UntilTime**

Die Member **Status,** **cJobs** und **AveragePPM** der [**PRINTER INFO \_ \_ 2-Struktur**](printer-info-2.md) sind für die Verwendung durch die [**GetPrinter-Funktion**](getprinter.md) reserviert. Sie dürfen nicht festgelegt werden, bevor **AddPrinter** aufgerufen wird.

Wenn **pSecurityDescriptor** **NULL** ist, weist das System dem Drucker einen Standardsicherheitsdeskriptor zu. Der Standardsicherheitsdeskriptor verfügt über die folgenden Berechtigungen.



| Wert                          | Beschreibung                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Administratoren und Hauptbenutzer | Vollsteuerung für die Druckwarteschlange. Dies bedeutet, dass Mitglieder dieser Gruppen die Warteschlange drucken, verwalten (die Warteschlange löschen, eine beliebige Einstellung der Warteschlange ändern können, einschließlich der Sicherheitsbeschreibung), und die Druckaufträge aller Benutzer verwalten können (Löschen, Anhalten, Fortsetzen, Neustarten von Aufträgen). Beachten Sie, dass Power Users nicht vorhanden ist, bevor Windows XP Professional.<br/> |
| Ersteller/Besitzer                  | Kann eigene Aufträge verwalten. Dies bedeutet, dass Benutzer, die Aufträge übermitteln, ihre eigenen Aufträge verwalten (löschen, anhalten, fortsetzen, neu starten).                                                                                                                                                                                                                                  |
| allen Beteiligten                       | Ausführen und Standardlesesteuerelement. Dies bedeutet, dass Mitglieder der Gruppe "Jeder" Eigenschaften der Druckwarteschlange drucken und lesen können.                                                                                                                                                                                                                     |



 

Nachdem eine Anwendung ein Druckerobjekt mit der **AddPrinter-Funktion** erstellt hat, muss sie die [**PrinterProperties-Funktion**](printerproperties.md) verwenden, um die richtigen Einstellungen für den Druckertreiber anzugeben, der dem Druckerobjekt zugeordnet ist.

Die **AddPrinter-Funktion** gibt einen Fehler zurück, wenn bereits ein Druckerobjekt mit dem gleichen Namen vorhanden ist, es sei denn, dieses Objekt ist als Löschvorgang ausstehend gekennzeichnet. In diesem Fall wird der vorhandene Drucker nicht gelöscht, und die **AddPrinter-Erstellungsparameter** werden verwendet, um die vorhandenen Druckereinstellungen zu ändern (als ob die Anwendung die [**SetPrinter-Funktion**](setprinter.md) verwendet hätte).

Verwenden Sie die [**EnumPrintProcessors-Funktion,**](enumprintprocessors.md) um die auf einem Server installierten Druckprozessoren aufzuzählen. Verwenden Sie die [**EnumPrintProcessorDatatypes-Funktion,**](enumprintprocessordatatypes.md) um den Von einem Druckprozessor unterstützten Satz von Datentypen aufzuzählen. Verwenden Sie die [**EnumPorts-Funktion,**](enumports.md) um den Satz verfügbarer Ports aufzuzählen. Verwenden Sie die [**EnumPrinterDrivers-Funktion,**](enumprinterdrivers.md) um die installierten Druckertreiber aufzuzählen.

Der Aufrufer der **AddPrinter-Funktion** muss \_ über SERVER ACCESS \_ ADMINISTER-Zugriff auf den Server verfügen, auf dem der Drucker erstellt werden soll. Das von der Funktion zurückgegebene Handle verfügt über die \_ PRINTER ALL \_ ACCESS-Berechtigung und kann zum Ausführen von Verwaltungsvorgängen auf dem Drucker verwendet werden.

Wenn der **DrvPrinterEvent-Funktion** das FLAG PRINTER EVENT FLAG NO UI übergeben \_ \_ \_ \_ wird, sollte der Treiber während **drvPrinterEvent** keinen UI-Aufruf verwenden. To do UI-related jobs, the installer should either use the **VendorSetup** entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer. Weitere Informationen zu **VendorSetup** finden Sie im Microsoft Windows Driver Development Kit (DDK).

Die Internet Connection Firewall (ICF) blockiert standardmäßig Druckerports, aber eine Ausnahme für Datei- und Druckfreigabe ist aktiviert, wenn Sie **AddPrinter** ausführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **AddPrinterW** (Unicode) und **AddPrinterA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**PrinterProperties**](printerproperties.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

