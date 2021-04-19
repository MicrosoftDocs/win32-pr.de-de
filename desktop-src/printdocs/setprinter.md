---
description: Die Funktion SetPrinter legt die Daten für einen angegebenen Drucker fest oder legt den Zustand des angegebenen Druckers fest, indem der Druckvorgang angehalten, der Druck fortgesetzt oder alle Druckaufträge gelöscht werden.
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
title: SetPrinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinter
- SetPrinterA
- SetPrinterW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-printer-WinSpool-l1-1-0.dll
- Ext-MS-Win-printer-WinSpool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 5f2c58d97315ff108c8f12bd029849993a307025
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349978"
---
# <a name="setprinter-function"></a>SetPrinter-Funktion

Die Funktion **SetPrinter** legt die Daten für einen angegebenen Drucker fest oder legt den Zustand des angegebenen Druckers fest, indem der Druckvorgang angehalten, der Druck fortgesetzt oder alle Druckaufträge gelöscht werden.

## <a name="syntax"></a>Syntax


```C++
BOOL SetPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker. Verwenden Sie die Funktion " [**OpenPrinter**](openprinter.md)", " [**OpenPrinter2**](openprinter2.md)" oder " [**addprinter**](addprinter.md) ", um ein Drucker Handle abzurufen.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Der Typ der Daten, die die Funktion in dem Puffer speichert, auf den *pprinter* zeigt. Wenn der *Befehls* Parameter ungleich 0 (null) ist, muss der *ebeneinameter* gleich 0 (null) sein.

Dieser Wert kann 0, 2, 3, 4, 5, 6, 7, 8 oder 9 sein.

</dd> <dt>

*pprinter* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der Daten enthält, die für den Drucker festgelegt werden sollen, oder die Informationen für den Befehl enthält, der vom *Befehls* Parameter angegeben wird. Der Typ der Daten im Puffer wird durch den Wert der *Ebene* bestimmt.



| Ebene                                                                                                | Struktur                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Wenn der *Befehls* Parameter der **\_ druckersteuerungsestatusstatus \_ \_** ist, muss *pprinter* einen **DWORD** -Wert enthalten, der den festzulegenden neuen Drucker Status angibt. Eine Liste der möglichen Statuswerte finden Sie unter dem **statusmember** der Struktur " [**Printer \_ Info \_ 2**](printer-info-2.md) ". Beachten Sie, dass der **Drucker \_ Status \_ angeh** alten wurde und der **Drucker \_ Status \_ ausstehende \_ Löschung** keine gültigen Status Werte ist.<br/> Wenn die *Ebene* 0 ist, der *Befehls* Parameter jedoch nicht der **Status der Drucker \_ Steuerungs \_ Sätze \_** ist, muss *pprinter* **null** sein.<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Eine " [**Printer \_ Info \_ 2**](printer-info-2.md) "-Struktur, die ausführliche Informationen über den Drucker enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Eine [**Drucker \_ Info \_ 3**](printer-info-3.md) -Struktur, die die Sicherheitsinformationen des Druckers enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Eine [**Drucker \_ Info \_ 4**](printer-info-4.md) -Struktur, die die minimalen Drucker Informationen enthält, einschließlich des Drucker namens, des Server namens und der Angabe, ob der Drucker Remote oder lokal ist.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Eine [**Drucker \_ Info \_ 5**](printer-info-5.md) -Struktur, die Drucker Informationen enthält, wie z. b. Drucker Attribute und Timeout Einstellungen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Eine [**Drucker \_ Info \_ 6**](printer-info-6.md) -Struktur, die den Statuswert eines Druckers angibt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Eine [**Drucker \_ Info \_ 7**](printer-info-7.md) -Struktur. Der *dwAction* -Member dieser Struktur gibt an, ob **SetPrinter** die Daten des Druckers im Verzeichnisdienst veröffentlichen, erneut veröffentlichen, erneut veröffentlichen oder aktualisieren soll.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | Eine [**Drucker \_ Info \_ 8**](printer-info-8.md) -Struktur, die die globalen Standarddrucker Einstellungen angibt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | Eine [**Drucker \_ Info \_ 9**](printer-info-9.md) -Struktur, die die Standarddrucker Einstellungen pro Benutzer angibt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*Befehl* \[ in\]
</dt> <dd>

Die auszuführende Aktion.

Wenn der *Level* -Parameter ungleich NULL ist, legen Sie den Wert dieses Parameters auf NULL fest. In diesem Fall behält der Drucker seinen aktuellen Zustand bei, und die Funktion konfiguriert die Druckerdaten gemäß den Parametern " *Level* " und " *pprinter* " neu.

Wenn der *Level* -Parameter 0 (null) ist, legen Sie den Wert dieses Parameters auf einen der folgenden Werte fest.



| Wert                                                                                                                                                                                                  | Bedeutung                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CONTROL_PAUSE"></span><span id="printer_control_pause"></span><dl> <dt>**Drucker \_ Steuerelement anhalten \_**</dt> </dl>                 | Halten Sie den Drucker an.<br/>                                                                                                                       |
| <span id="PRINTER_CONTROL_PURGE"></span><span id="printer_control_purge"></span><dl> <dt>**Löschen von Drucker \_ Steuerelementen \_**</dt> </dl>                 | Löschen Sie alle Druckaufträge im Drucker.<br/>                                                                                                    |
| <span id="PRINTER_CONTROL_RESUME"></span><span id="printer_control_resume"></span><dl> <dt>**Drucker Steuerelement fortsetzen \_ \_**</dt> </dl>              | Setzen Sie einen angehaltenen Drucker fort.<br/>                                                                                                                 |
| <span id="PRINTER_CONTROL_SET_STATUS"></span><span id="printer_control_set_status"></span><dl> <dt>**\_Status des druckersteuerungsets \_ \_**</dt> </dl> | Legen Sie den Druckerstatus fest.<br/> Legen Sie den Parameter " *pprinter* " auf einen Zeiger auf einen **DWORD** -Wert fest, der den neuen Druckerstatus angibt.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

Wenn *Level* 7 ist und bei der Veröffentlichungs Aktion ein Fehler aufgetreten ist, gibt **SetPrinter** eine **\_ \_ ausstehende Fehler** -e/a zurück und versucht, die Aktion im Hintergrund abzuschließen. Wenn *Level* 7 ist und die Aktualisierungs Aktion fehlgeschlagen ist, gibt **SetPrinter** die **Fehler \_ Datei \_ nicht \_ gefunden** zurück.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Sie können **SetPrinter** nicht verwenden, um den Standarddrucker zu ändern.

Um die aktuellen Druckereinstellungen zu ändern, rufen Sie die [**GetPrinter**](getprinter.md) -Funktion auf, um die aktuellen Einstellungen in eine [**Drucker \_ Info \_ 2**](printer-info-2.md) -Struktur abzurufen, die Elemente dieser Struktur nach Bedarf zu ändern und dann **SetPrinter** aufzurufen.

Die Funktion " **SetPrinter** " ignoriert die Member " **pservername**", " **AveragePPM**", " **Status**" und " **cjobs** " einer [**Drucker \_ Info \_ 2**](printer-info-2.md) -Struktur.

Durch das Anhalten eines Druckers wird die Planung aller Druckaufträge für diesen Drucker angehalten, mit Ausnahme eines Druckauftrags, der möglicherweise gerade gedruckt wird. Druckaufträge können an einen angehaltenen Drucker übermittelt werden, aber es ist nicht geplant, Aufträge auf diesem Drucker zu drucken, bis der Druckvorgang fortgesetzt wird. Wenn ein Drucker gelöscht wird, werden alle Druckaufträge für diesen Drucker gelöscht, mit Ausnahme des aktuellen Druckauftrags.

Wenn Sie **SetPrinter** verwenden, um die Standardstruktur [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) für einen Drucker zu ändern (Global Festlegen der Drucker Standardwerte), müssen Sie zuerst die [**DocumentProperties**](documentproperties.md) -Funktion aufrufen, um die **DEVMODE** -Struktur zu überprüfen.

Für die [**Drucker \_ Info \_ 2**](printer-info-2.md) -und [**Printer \_ Info \_ 3**](printer-info-3.md) -Strukturen, die einen Zeiger auf eine Sicherheits Beschreibung enthalten, kann die Funktion nur die Komponenten der Sicherheits Beschreibung festlegen, für die der Aufrufer über die Berechtigung zum Ändern verfügt. Um bestimmte sicherheitsbeschreibungkomponenten festzulegen, müssen Sie die erforderlichen Zugriffsrechte angeben, wenn Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**OpenPrinter2**](openprinter2.md) aufrufen, um ein Handle für den Drucker abzurufen. In der folgenden Tabelle sind die zum Ändern der verschiedenen sicherheitsbeschreibungkomponenten erforderlichen Zugriffsrechte aufgeführt.



| Zugriffsberechtigung            | Sicherheitsbeschreibungerkomponente             |
|------------------------------|-------------------------------------------|
| **\_Besitzer schreiben**             | Besitzer<br/> Primäre Gruppe<br/> |
| **\_DAC schreiben**               | Freigegebene Zugriffs Steuerungs Liste (DACL)  |
| **Zugreifen auf die \_ System \_ Sicherheit** | System Zugriffs Steuerungs Liste (SACL)         |



 

Wenn die Sicherheits Beschreibung eine Komponente enthält, für die der Aufrufer nicht über das zu ändernde Zugriffsrecht verfügt, kann **SetPrinter** nicht ausgeführt werden. Die Komponenten einer Sicherheits Beschreibung, die Sie nicht ändern möchten, sollten nach Bedarf **null** sein oder nicht vorhanden sein. Wenn Sie die Sicherheits Beschreibung nicht ändern möchten und **SetPrinter** mit einer [**\_ Druckerinfo- \_ 2**](printer-info-2.md) -Struktur aufrufen, legen Sie den **psecuritydescriptor** -Member dieser Struktur auf **null** fest.

Die Internetverbindungs Firewall (ICF) blockiert standardmäßig Drucker Anschlüsse, eine Ausnahme für die Datei-und Druckfreigabe kann jedoch aktiviert werden. Wenn **SetPrinter** von einem Computer Administrator aufgerufen wird, wird die Ausnahme aktiviert. Wenn Sie von einem nicht-Administrator aufgerufen wird und die Ausnahme nicht bereits aktiviert wurde, schlägt der Aufruf fehl.

Sie können Ebene 7 mit der [**Drucker \_ Info \_ 7**](printer-info-7.md) -Struktur verwenden, um Verzeichnisdienst Daten für den Drucker zu veröffentlichen, zu veröffentlichen oder zu aktualisieren. Die Verzeichnisdienst Daten für einen Drucker enthalten alle Daten, die unter den splds-Schlüsseln gespeichert sind \_ \* , durch Aufrufe der [**setprinterdataex**](setprinterdataex.md) -Funktion für den Drucker. Legen Sie vor dem Aufrufen von **SetPrinter** den **pszobjectguid** -Member der **Drucker \_ Info \_ 7** auf **null** fest, und legen Sie den *dwAction* -Member auf einen der folgenden Werte fest.



| Wert                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dsprint- \_ Veröffentlichung**<br/>   | Veröffentlicht die Verzeichnisdienst Daten.<br/>                                                                                                                                                                                                                                                                                                                                        |
| **dsprint \_ erneut veröffentlichen**<br/> | Die Verzeichnisdienst Daten für den Drucker werden nicht veröffentlicht und dann erneut veröffentlicht, sodass alle Eigenschaften im veröffentlichten Drucker aktualisiert werden. Bei der erneuten Veröffentlichung wird auch die GUID des veröffentlichten Druckers geändert. Verwenden Sie diesen Wert, wenn Sie vermuten, dass die veröffentlichten Daten des Druckers beschädigt wurden.<br/>                                                                                         |
| **dsprint- \_ Veröffentlichung aufheben**<br/> | Veröffentlicht die Veröffentlichung der Verzeichnisdienst Daten.<br/>                                                                                                                                                                                                                                                                                                                                      |
| **dsprint- \_ Update**<br/>    | Aktualisiert die Verzeichnisdienst Daten. Dies entspricht der **dsprint- \_ Veröffentlichung**, mit dem Unterschied, dass **SetPrinter** fehlschlägt, wenn die **Fehler \_ Datei \_ nicht \_ gefunden** wurde, wenn der Drucker nicht bereits veröffentlicht wurde.<br/> Verwenden Sie das **dsprint- \_ Update** zum Aktualisieren veröffentlichter Eigenschaften, aber nicht das veröffentlichen. Druckertreiber sollten immer das **dsprint- \_ Update** anstelle der **dsprint- \_ Veröffentlichung** verwenden.<br/> |



 

**Dsprint \_ Pending** ist kein gültiger *dwAction* -Wert für **SetPrinter**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Setprinterw** (Unicode) und **setprintera** (ANSI)<br/>                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 2**](printer-info-2.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 3**](printer-info-3.md)
</dt> <dt>

[**Drucker \_ Info \_ 4**](printer-info-4.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 5**](printer-info-5.md)
</dt> <dt>

[**Drucker \_ Info \_ 6**](printer-info-6.md)
</dt> <dt>

[**Drucker \_ Info \_ 7**](printer-info-7.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 8**](printer-info-8.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 9**](printer-info-9.md)
</dt> <dt>

[**Setprinterdataex**](setprinterdataex.md)
</dt> </dl>

 

 




