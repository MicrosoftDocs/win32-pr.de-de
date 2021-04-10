---
description: Die addprinter-Funktion fügt der Liste der unterstützten Drucker für einen angegebenen Server einen Drucker hinzu.
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: Addprinter-Funktion (winspool. h)
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
ms.openlocfilehash: 51416ed59bc1c6df1d2c69de87d61bdecab522f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215866"
---
# <a name="addprinter-function"></a>Addprinter-Funktion

Die **addprinter** -Funktion fügt der Liste der unterstützten Drucker für einen angegebenen Server einen Drucker hinzu.

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

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem der Drucker installiert werden soll. Wenn diese Zeichenfolge **null** ist, wird der Drucker lokal installiert.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Die Version der-Struktur, auf die *pprinter* zeigt. Dieser Wert muss 2 sein.

</dd> <dt>

*pprinter* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**\_ Druckerinfo- \_ 2**](printer-info-2.md) -Struktur, die Informationen über den Drucker enthält. Sie müssen Werte ungleich **null** für die Member **pprintername**, **pportname**, **pdrivername** und **pprintprocessor** dieser Struktur angeben, bevor Sie **addprinter** aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Handle (nicht Thread sicher) für ein neues Drucker Objekt. Wenn Sie mit dem Handle fertig sind, übergeben Sie es an die [**closeprinter**](closeprinter.md) -Funktion, um es zu schließen.

Wenn die Funktion fehlschlägt, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Diese Methode darf nicht in [**DllMain**](/windows/desktop/Dlls/dllmain)aufgerufen werden.

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Der [Aufrufer muss über die SeLoadDriverPrivilege-Berechtigung](/windows/desktop/SecAuthZ/authorization-constants)verfügen.

Das zurückgegebene Handle ist nicht Thread sicher. Wenn Aufrufer Sie gleichzeitig für mehrere Threads verwenden müssen, müssen Sie den benutzerdefinierten Synchronisierungs Zugriff auf das Drucker Handle mithilfe der [Synchronisierungs Funktionen](/windows/desktop/Sync/synchronization-functions)bereitstellen. Um das Schreiben von benutzerdefiniertem Code zu vermeiden, kann die Anwendung bei Bedarf ein Drucker Handle für jeden Thread öffnen.

Im folgenden sind die Elemente der [**\_ Druckerinfo- \_ 2**](printer-info-2.md) -Struktur aufgeführt, die vor dem Aufrufen der **addprinter** -Funktion festgelegt werden können:

-   **Attribute**
-   **pprintprocessor**
-   **DefaultPriority**
-   **Priority**
-   **pcomment**
-   **psecuritydescriptor**
-   **pdatatype**
-   **psepfile**
-   **pdevmode**
-   **psharename**
-   **pLocation**
-   **StartTime**
-   **pParameters**
-   **UntilTime**

Die Member " **Status**", " **cjobs**" und " **AveragePPM** " der Struktur " [**Printer \_ Info \_ 2**](printer-info-2.md) " sind für die Verwendung durch die Funktion " [**GetPrinter**](getprinter.md) " reserviert. Sie dürfen nicht vor dem Aufrufen von **addprinter** festgelegt werden.

Wenn **psecuritydescriptor** den Wert **null** hat, weist das System dem Drucker eine Standard Sicherheits Beschreibung zu. Die Standard Sicherheits Beschreibung verfügt über die folgenden Berechtigungen.



| Wert                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Administratoren und Hauptbenutzer | Vollständige Steuerung der Druck Warteschlange. Dies bedeutet, dass Mitglieder dieser Gruppen die Warteschlange drucken, verwalten können (kann die Warteschlange löschen, beliebige Einstellungen der Warteschlange ändern, einschließlich der Sicherheits Beschreibung) und die Druckaufträge aller Benutzer verwalten (löschen, anhalten, fortsetzen, Aufträge neu starten). Beachten Sie, dass Hauptbenutzer nicht vor Windows XP Professional vorhanden sind.<br/> |
| Ersteller/Besitzer                  | Kann eigene Aufträge verwalten. Dies bedeutet, dass Benutzer, die Aufträge übermitteln, ihre eigenen Aufträge verwalten (löschen, anhalten, fortsetzen, neu starten) können.                                                                                                                                                                                                                                  |
| Jeder                       | Execute-und Standard-Lese Steuerelement. Dies bedeutet, dass Mitglieder der Gruppe "jeder" die Eigenschaften der Druck Warteschlange drucken und lesen können.                                                                                                                                                                                                                     |



 

Nachdem eine Anwendung ein Drucker Objekt mit der **addprinter** -Funktion erstellt hat, muss Sie die [**printerproperties**](printerproperties.md) -Funktion verwenden, um die korrekten Einstellungen für den Druckertreiber anzugeben, der dem Drucker Objekt zugeordnet ist.

Die **addprinter** -Funktion gibt einen Fehler zurück, wenn bereits ein Drucker Objekt mit demselben Namen vorhanden ist, es sei denn, das Objekt ist als ausstehende Löschung markiert. In diesem Fall wird der vorhandene Drucker nicht gelöscht, und die **addprinter** -Erstellungs Parameter werden verwendet, um die vorhandenen Druckereinstellungen zu ändern (als ob die Anwendung die [**SetPrinter**](setprinter.md) -Funktion verwendet hätte).

Verwenden Sie die [**enumprintprocessor**](enumprintprocessors.md) -Funktion, um den Satz von Druck Prozessoren aufzulisten, die auf einem Server installiert sind. Verwenden Sie die [**enumprintprocessordatatypes**](enumprintprocessordatatypes.md) -Funktion, um den Satz von Datentypen aufzulisten, den ein Druck Prozessor unterstützt. Verwenden Sie die [**enumports**](enumports.md) -Funktion, um den Satz verfügbarer Ports aufzulisten. Verwenden Sie die [**enumprinterdrivers**](enumprinterdrivers.md) -Funktion, um die installierten Druckertreiber aufzuzählen.

Der Aufrufer der **addprinter** -Funktion muss über Server \_ Zugriffsberechtigungen \_ für den Server verfügen, auf dem der Drucker erstellt werden soll. Das Handle, das von der Funktion zurückgegeben wird, verfügt über die \_ \_ Berechtigung für den Drucker Zugriff und kann verwendet werden, um administrative Vorgänge auf dem Drucker auszuführen.

Wenn der **drvprinterevent** -Funktion das \_ druckerereignisflag kein UI-Flag übermittelt wird \_ \_ \_ , sollte der Treiber während **drvprinterevent** keinen UI-Befehl verwenden. Zum Ausführen von UI-bezogenen Aufträgen sollte das Installationsprogramm entweder den **vendorsetup** -Eintrag in der INF-Datei des Druckers verwenden, oder für Plug & Play Geräte kann das Installationsprogramm einen gerätespezifischen Co-Installer verwenden. Weitere Informationen zu **vendorsetup** finden Sie im Microsoft Windows Driver Development Kit (DDK).

Die Internetverbindungs Firewall (ICF) blockiert standardmäßig die Druckerports, aber eine Ausnahme für die Datei-und Druckfreigabe ist aktiviert, wenn Sie **addprinter** ausführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Addprinterw** (Unicode) und **addprintera** (ANSI)<br/>                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Closeprinter**](closeprinter.md)
</dt> <dt>

[**Deleteprinter**](deleteprinter.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> <dt>

[**Enumprinterdrivers**](enumprinterdrivers.md)
</dt> <dt>

[**Enumprintprozessoren**](enumprintprocessors.md)
</dt> <dt>

[**Enumprintprocessordatatypes**](enumprintprocessordatatypes.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 2**](printer-info-2.md)
</dt> <dt>

[**Printerproperties**](printerproperties.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

