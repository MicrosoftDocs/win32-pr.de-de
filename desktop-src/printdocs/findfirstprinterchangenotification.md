---
description: Die findfirstprinterchangenotifi-Funktion erstellt ein Änderungs Benachrichtigungs Objekt und gibt ein Handle für das-Objekt zurück. Anschließend können Sie dieses Handle in einem Rückruf einer der Wait-Funktionen verwenden, um Änderungen am Drucker oder Druckserver zu überwachen.
ms.assetid: 4155ef5c-cd96-4960-919b-d9a495bb73a5
title: Findfirstprinterchangenotifi-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindFirstPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2da6a2ae73aa5b987ea3b8f8789f81ed0b4cdf06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215977"
---
# <a name="findfirstprinterchangenotification-function"></a>Findfirstprinterchangenotifi-Funktion

Die **findfirstprinterchangenotifi-** Funktion erstellt ein Änderungs Benachrichtigungs Objekt und gibt ein Handle für das-Objekt zurück. Anschließend können Sie dieses Handle in einem Rückruf einer der Wait-Funktionen verwenden, um Änderungen am Drucker oder Druckserver zu überwachen.

Der **findfirstprinterchangenotifizierungsbefehl** gibt den Typ der zu überwachenden Änderungen an. Sie können eine Reihe von Bedingungen angeben, die auf Änderungen überwacht werden sollen, einen Satz von zu überwachenden Drucker Informationsfeldern oder beides.

Ein warte Vorgang für das Änderungs Benachrichtigungs Handle ist erfolgreich, wenn eine der angegebenen Änderungen auf dem angegebenen Drucker oder Druckserver auftritt. Anschließend rufen Sie die Funktion " [**findnextprinterchangenotifitifitifitifitifitifitifitifitifitifitifitifitifitifitifitifitifitifi"**](findnextprinterchangenotification.md) auf, um Informationen über die Änderung abzurufen und das Änderungs Benachrichtigungs Objekt

## <a name="syntax"></a>Syntax


```C++
HANDLE FindFirstPrinterChangeNotification(
  _In_     HANDLE hPrinter,
           DWORD  fdwFilter,
           DWORD  fdwOptions,
  _In_opt_ LPVOID pPrinterNotifyOptions
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker oder Druckserver, den Sie überwachen möchten. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*"f" Filtern* 
</dt> <dd>

Die Bedingungen, die bewirken, dass das Änderungs Benachrichtigungs Objekt in den signalisierten Zustand versetzt wird. Eine Änderungs Benachrichtigung tritt auf, wenn eine oder mehrere der angegebenen Bedingungen erfüllt sind. Der *Parameter* "Parameter" kann NULL sein, wenn " *pprinternotifyoptions* " nicht **null** ist.

Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CHANGE_FORM"></span><span id="printer_change_form"></span><dl> <dt>**Formular für Drucker \_ Änderung \_**</dt> </dl>                                   | Benachrichtigen von Änderungen an einem Formular. Sie können dieses allgemeine Flag oder eines oder mehrere der folgenden spezifischen Flags festlegen:<br/> <dl> <dd>Formular "Drucker \_ Änderung \_ Hinzufügen" \_</dd> <dd>Formular für den Drucker \_ Änderungs \_ Satz \_</dd> <dd>Formular für das Löschen von Drucker \_ Änderungen \_ \_</dd> </dl>                                                                              |
| <span id="PRINTER_CHANGE_JOB"></span><span id="printer_change_job"></span><dl> <dt>**Auftrag zur Drucker \_ Änderung \_**</dt> </dl>                                      | Benachrichtigen von Änderungen an einem Auftrag. Sie können dieses allgemeine Flag oder eines oder mehrere der folgenden spezifischen Flags festlegen:<br/> <dl> <dd>Drucker \_ Änderung \_ Auftrag hinzufügen \_</dd> <dd>Auftrag für Drucker \_ Änderungs \_ Satz \_</dd> <dd>Auftrag zum Löschen der Drucker \_ Änderung \_ \_</dd> <dd>\_ \_ Schreib \_ Auftrag für Drucker Änderung</dd> </dl>                                  |
| <span id="PRINTER_CHANGE_PORT"></span><span id="printer_change_port"></span><dl> <dt>**Drucker \_ \_ änderungsport**</dt> </dl>                                   | Benachrichtigen von Änderungen an einem Port. Sie können dieses allgemeine Flag oder eines oder mehrere der folgenden spezifischen Flags festlegen:<br/> <dl> <dd>Drucker \_ Änderung \_ " \_ Port hinzufügen"</dd> <dd>Port für die Drucker \_ Änderung \_ konfigurieren \_ </dd> <dd>\_druckeränderungsport \_ Löschen \_</dd> </dl>                                                                       |
| <span id="PRINTER_CHANGE_PRINT_PROCESSOR"></span><span id="printer_change_print_processor"></span><dl> <dt>**Drucker \_ Änderungs \_ Druck \_ Prozessor**</dt> </dl> | Benachrichtigen von Änderungen an einem Druck Prozessor. Sie können dieses allgemeine Flag oder eines oder mehrere der folgenden spezifischen Flags festlegen: <br/> <dl> <dd>Drucker \_ Änderung \_ Hinzufügen eines \_ Druck \_ Prozessors </dd> <dd>Drucker \_ Änderung \_ Delete- \_ Druck \_ Prozessor</dd> </dl>                                                                                        |
| <span id="PRINTER_CHANGE_PRINTER"></span><span id="printer_change_printer"></span><dl> <dt>**Drucker \_ Änderungs \_ Drucker**</dt> </dl>                          | Benachrichtigen von Änderungen an einem Drucker. Sie können dieses allgemeine Flag oder eines oder mehrere der folgenden spezifischen Flags festlegen:<br/> <dl> <dd>Drucker \_ Änderung \_ Drucker hinzufügen \_</dd> <dd>Drucker \_ Änderungs \_ Satz- \_ Drucker</dd> <dd>Drucker \_ Änderung Drucker \_ Löschen \_</dd> <dd>Fehler beim Drucker \_ Änderungs \_ \_ Verbindungs \_ Drucker.</dd> </dl> |
| <span id="PRINTER_CHANGE_PRINTER_DRIVER"></span><span id="printer_change_printer_driver"></span><dl> <dt>**Drucker \_ Treiber für Drucker Änderung \_ \_**</dt> </dl>    | Benachrichtigen von Änderungen an einem Druckertreiber Sie können dieses allgemeine Flag oder eines oder mehrere der folgenden spezifischen Flags festlegen:<br/> <dl> <dd>Drucker \_ Änderung \_ Drucker \_ Treiber hinzufügen \_</dd> <dd>Drucker \_ \_ Treiber- \_ Drucker \_ Treiber</dd> <dd>Drucker \_ Änderung zum \_ Löschen des \_ Drucker \_ Treibers</dd> </dl>                                   |
| <span id="PRINTER_CHANGE_ALL"></span><span id="printer_change_all"></span><dl> <dt>**\_alle Drucker Änderungen \_**</dt> </dl>                                      | Benachrichtigen, wenn eine der obigen Änderungen auftritt.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**Drucker \_ Änderungs \_ Server**</dt> </dl>                             | Windows 7: Benachrichtigen von Änderungen am Server.<br/> Dieses Flag ist nicht in den überwachten Änderungen enthalten, indem der Wert für den **\_ \_ gesamten Drucker Änderungs** Wert festgelegt wird.<br/>                                                                                                                                                                                                      |



 

Beschreibungen der spezifischeren Flags in der vorangehenden Tabelle finden Sie unter der [**findnextprinterchangenotifi-**](findnextprinterchangenotification.md) Funktion.

</dd> <dt>

*"f"-Optionen* 
</dt> <dd>

Das Flag, das die Kategorie der Drucker bestimmt, für die Benachrichtigungen verwendet werden.



| Wert                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_NOTIFY_CATEGORY_ALL"></span><span id="printer_notify_category_all"></span><dl> <dt>**Drucker \_ \_Kategorie \_ alle**</dt> <dt>0x001000</dt> Benachrichtigen </dl> | [**Findnextprinterchangenotifigibt**](findnextprinterchangenotification.md) Benachrichtigungen für 2D-und 3D-Drucker zurück.<br/> |
| <span id="PRINTER_NOTIFY_CATEGORY_3D"></span><span id="printer_notify_category_3d"></span><dl> <dt>**Drucker \_ \_Kategorie \_ 3D**</dt> <dt>0x002000</dt> Benachrichtigen </dl>    | [**Findnextprinterchangenotifigibt**](findnextprinterchangenotification.md) nur bei 3D-Druckern Benachrichtigungen zurück.<br/>        |



 

Wenn dieses Flag auf NULL (0) festgelegt ist, funktioniert **findfirstprinterchangenotifiken** nur für 2D-Drucker. Dies ist der Standardwert.

</dd> <dt>

*pprinternotifyoptions* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf die Struktur der [**Drucker \_ Benachrichtigungs \_ Optionen**](printer-notify-options.md) . Der **ptypes** -Member dieser Struktur ist ein Array aus mindestens einer [**Art von Drucker \_ Benachrichtigungs \_ Optionen \_**](printer-notify-options-type.md) , von dem jedes ein zu überwachende Drucker Informationsfeld angibt. Eine Änderungs Benachrichtigung tritt auf, wenn ein oder mehrere der angegebenen Felder geändert werden. Wenn eine Änderung auftritt, kann die Funktion [**findnextprinterchangenotifidie**](findnextprinterchangenotification.md) neuen Drucker Informationen abrufen. Dieser Parameter kann **null** sein, wenn " *f-Filter* " ungleich 0 (null) ist.

Eine Liste der Felder, die überwacht werden können, finden Sie unter [**Art der Drucker \_ Benachrichtigungs \_ Optionen \_**](printer-notify-options-type.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Handle für ein Änderungs Benachrichtigungs Objekt, das dem angegebenen Drucker oder Druckserver zugeordnet ist.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein ungültiger \_ handle- \_ Wert.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Um einen Drucker oder Druckserver zu überwachen, rufen Sie die **findfirstprinterchangenotifizierungsfunktion** auf, und verwenden Sie dann das zurückgegebene Änderungs Benachrichtigungs Objekt Handle in einem Rückruf einer der [Wait-Funktionen](/windows/desktop/Sync/wait-functions). Ein warte Vorgang für ein Änderungs Benachrichtigungs Objekt wird erfüllt, wenn das Änderungs Benachrichtigungs Objekt in den signalisierten Zustand wechselt. Das System signalisiert dem Objekt, wenn eine oder mehrere der durch " *bdwfilter* " oder " *pprinternotifyoptions* " angegebenen Änderungen auf dem überwachten Drucker oder Druckserver auftreten.

Beim Abrufen von **findfirstprinterchangenotifiziken** muss entweder *fdwfilter* ungleich NULL sein, oder *pprinternotifyoptions* darf nicht **null** sein. Wenn beide angegeben werden, werden Benachrichtigungen für beide angezeigt.

Wenn ein warte Vorgang für ein Drucker Änderungs Benachrichtigungs Objekt erfüllt ist, rufen Sie die [**findnextprinterchangenotifitifi-**](findnextprinterchangenotification.md) Funktion auf, um die Ursache der Benachrichtigung zu bestimmen. Für eine von " *sdwfilter*" angegebene Bedingung meldet **findnextprinterchangenotifidie** Bedingungen, die sich geändert haben. Bei einem von *pprinternotifyoptions* angegebenen Drucker Informationsfeld meldet **findnextprinterchangenotifidas** geänderte Feld bzw. die geänderten Felder sowie die neuen Informationen für diese Felder. **Findnextprinterchangenotifisetzt** das Änderungs Benachrichtigungs Objekt auch auf den nicht signalisierten Zustand zurück, damit Sie es in einem anderen warte Vorgang verwenden können, um die Überwachung des Druckers oder des Druck Servers fortzusetzen.

Rufen Sie die [**findnextprinterchangenotifi-**](findnextprinterchangenotification.md) Funktion mit einer Ausnahme nicht auf, wenn sich das Änderungs Benachrichtigungs Objekt nicht im signalisierten Zustand befindet. Wenn die wait-Funktion den Timeout Wert der Wartezeit zurückgibt \_ , befindet sich das Änderungs Objekt nicht im signalisierten Zustand. Rufen Sie die Funktion " **findnextprinterchangenotifitifitifitifitifitifitifitifitifitifitifitifitifitifi"** nur auf Eine Ausnahme bildet die Verwendung von **findnextprinterchangenotifizierung** mit dem \_ \_ \_ im Parameter *pprinternotifyoptions* festgelegten Refresh-Bit für die Drucker Benachrichtigung.

Wenn das Änderungs Benachrichtigungs Objekt nicht mehr benötigt wird, schließen Sie es, indem Sie die [**findcloseprinterchangenotifi-**](findcloseprinterchangenotification.md) Funktion aufrufen.

Aufrufer von **findfirstprinterchangenotifiken** müssen sicherstellen, dass das an **findfirstprinterchangenotifiübergebenen** Drucker Handle gültig bleibt, bis [**findcloseprinterchangenotifiaufgerufen**](findcloseprinterchangenotification.md) wird. Wenn das Drucker handle vor dem Benachrichtigungs Handle für Drucker Änderungen geschlossen wird, können weitere Benachrichtigungen nicht übermittelt werden.

Von **findfirstprinterchangenotifizierung** werden keine Änderungs Benachrichtigungen für 3D-Drucker an Server Handles gesendet.

> [!Note]  
> In Windows XP mit Service Pack 2 (SP2) und höher blockiert die Internetverbindungs Firewall (ICF) standardmäßig Drucker Anschlüsse, eine Ausnahme für die Datei-und Druckfreigabe kann jedoch aktiviert werden. Wenn ein Benutzer eine Druckerverbindung mit einem anderen Computer herstellt und die Ausnahme nicht aktiviert ist, empfängt der Benutzer keine Drucker Änderungs Benachrichtigungen vom Server. Ein Computer Administrator muss die Ausnahme aktivieren.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Findcloseprinterchangenotifizierung**](findcloseprinterchangenotification.md)
</dt> <dt>

[**Findnextprinterchangenotifizierung**](findnextprinterchangenotification.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Drucker \_ Benachrichtigungs \_ Optionen**](printer-notify-options.md)
</dt> <dt>

[**Typ der Drucker \_ Benachrichtigungs \_ Optionen \_**](printer-notify-options-type.md)
</dt> </dl>

 

