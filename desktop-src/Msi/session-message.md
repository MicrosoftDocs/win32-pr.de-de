---
description: Die Message-Methode des Session-Objekts führt alle aktivierten Protokollierungs Vorgänge aus und führt die Ausführung für das UI-Handlerobjekt aus, das der Engine zugeordnet ist. Die Protokollierung kann selektiv für verschiedene Nachrichten Typen aktiviert werden. Siehe EnableLog-Methode.
ms.assetid: 09053700-a641-4970-bf55-d7c81f345257
title: Session. Message-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Message
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e20cfebe0a3359a99770cbd242501649bf93f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371773"
---
# <a name="sessionmessage-method"></a>Session. Message-Methode

Die **Message** -Methode des [**Session**](session-object.md) -Objekts führt alle aktivierten Protokollierungs Vorgänge aus und führt die Ausführung für das UI-Handlerobjekt aus, das der Engine zugeordnet ist. Die Protokollierung kann selektiv für verschiedene Nachrichten Typen aktiviert werden. Siehe [**EnableLog**](installer-enablelog.md) -Methode.

Wenn das Daten Satz Feld 0 eine Formatierungs Zeichenfolge enthält, wird es verwendet, um die Daten in den anderen Feldern zu formatieren. Wenn es sich bei der Nachricht um einen Fehler, eine Warnung oder eine Benutzer Meldung handelt, wird versucht, eine Nachrichten Vorlage in der Fehler Tabelle für die aktuelle Datenbank mithilfe der Fehlernummer zu suchen, die in Feld 1 des Datensatzes für Nachrichten Typen und Rückgabewerte gefunden wurde.

## <a name="syntax"></a>Syntax


```JScript
Session.Message(
  kind,
  record
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Art* 
</dt> <dd>

Der *Kind* -Parameter muss einer der folgenden Werte sein. Wenn Sie ein Meldungs Feld mit pushschaltflächen und Symbolen anzeigen möchten, berechnen Sie den Wert der *Art* , indem Sie die von [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) und [**messageboxex**](/windows/win32/api/winuser/nf-winuser-messageboxexa) verwendeten Standardformate für Meldungs Felder zu **msimessagetypeerror**, **msimessagetypewarning** oder **msimessagetypeuser** hinzufügen. Weitere Informationen finden Sie im Abschnitt "Hinweise" weiter unten.



| Konstante                                                                                                                                                                                                                                                                                                                 | Bedeutung                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiMessageTypeFatalExit"></span><span id="msimessagetypefatalexit"></span><span id="MSIMESSAGETYPEFATALEXIT"></span><dl> <dt>**msimessagetypefatalexit**</dt> - <dt>&H00000000</dt> </dl>                     | Vorzeitige Beendigung, möglicherweise schwerwiegender Arbeitsspeicher.<br/>                                                                              |
| <span id="msiMessageTypeError"></span><span id="msimessagetypeerror"></span><span id="MSIMESSAGETYPEERROR"></span><dl> <dt>**msimessagetypeerror**</dt> - <dt>&H01000000</dt> </dl>                                     | Formatierte Fehlermeldung, \[ 1 \] ist Nachrichtennummer in der [Fehler Tabelle](error-table.md).<br/>                                               |
| <span id="msiMessageTypeWarning"></span><span id="msimessagetypewarning"></span><span id="MSIMESSAGETYPEWARNING"></span><dl> <dt>**msimessagetypewarning**</dt> - <dt>&H02000000</dt> </dl>                             | Formatierte Warnmeldung, \[ 1 \] ist Nachrichtennummer in der [Fehler Tabelle](error-table.md).<br/>                                             |
| <span id="msiMessageTypeUser_"></span><span id="msimessagetypeuser_"></span><span id="MSIMESSAGETYPEUSER_"></span><dl> <dt> **msimessagetypeuser**</dt> - <dt>&H03000000</dt> </dl>                                     | Benutzer Anforderungs Nachricht, \[ 1 \] ist Nachrichtennummer in der [Fehler Tabelle](error-table.md).<br/>                                                  |
| <span id="msiMessageTypeInfo"></span><span id="msimessagetypeinfo"></span><span id="MSIMESSAGETYPEINFO"></span><dl> <dt>**msimessagetypeingefo**</dt> - <dt>&H04000000</dt> </dl>                                         | Informative Meldung für das Protokoll, die nicht angezeigt werden soll.<br/>                                                                                 |
| <span id="msiMessageTypeFilesInUse"></span><span id="msimessagetypefilesinuse"></span><span id="MSIMESSAGETYPEFILESINUSE"></span><dl> <dt>**msimessagetypefilesinuse**</dt> <dt>&H05000000</dt> </dl>                 | Die Liste der zu verwendenden Dateien, die ersetzt werden müssen.<br/>                                                                                    |
| <span id="msiMessageTypeResolveSource"></span><span id="msimessagetyperesolvesource"></span><span id="MSIMESSAGETYPERESOLVESOURCE"></span><dl> <dt>**msimessagetyperesolvesource**</dt> <dt>&H06000000</dt> </dl>     | Anforderung zum Ermitteln eines gültigen Quell Speicher Orts.<br/>                                                                                     |
| <span id="msiMessageTypeOutOfDiskSpace"></span><span id="msimessagetypeoutofdiskspace"></span><span id="MSIMESSAGETYPEOUTOFDISKSPACE"></span><dl> <dt>**msimessagetypeouesf Disk Space**</dt> <dt>&H07000000</dt> </dl> | Nicht genügend Speicherplatz Nachricht.<br/>                                                                                                  |
| <span id="msiMessageTypeActionStart"></span><span id="msimessagetypeactionstart"></span><span id="MSIMESSAGETYPEACTIONSTART"></span><dl> <dt>**msimessagetypeactionstart**</dt> <dt>&H08000000</dt> </dl>             | Start der Aktion, \[ 1 \] Aktionsname, \[ 2 \] Beschreibung, \[ 3 \] Vorlage für Action Data Messages.<br/>                                    |
| <span id="msiMessageTypeActionData"></span><span id="msimessagetypeactiondata"></span><span id="MSIMESSAGETYPEACTIONDATA"></span><dl> <dt>**msimessagetypeactiondata**</dt> <dt>&H09000000</dt> </dl>                 | Aktions Daten. Daten Satz Felder entsprechen der Vorlage der Aktions Start Nachricht.<br/>                                                     |
| <span id="msiMessageTypeProgress"></span><span id="msimessagetypeprogress"></span><span id="MSIMESSAGETYPEPROGRESS"></span><dl> <dt>**msimessagetypeprogress**</dt> <dt>&H0A000000</dt> </dl>                         | Informationen zur Statusanzeige. Weitere Informationen finden Sie unter Beschreibung der Daten Satz Felder unten.<br/>                                                             |
| <span id="msiMessageTypeCommonData_"></span><span id="msimessagetypecommondata_"></span><span id="MSIMESSAGETYPECOMMONDATA_"></span><dl> <dt> **msimessagetypecommondata**</dt> <dt>&H0B000000</dt> </dl>             | Um die Schaltfläche Abbrechen zu aktivieren, legen Sie \[ 1 \] bis 2 und \[ 2 \] auf 1 fest. <br/> So deaktivieren Sie die Schaltfläche "Abbrechen" für \[ 1 \] bis 2 und \[ 2 \] bis 0<br/> |



 

</dd> <dt>

*record* 
</dt> <dd>

Erforderliches [**Daten Satz**](record-object.md) Objekt, das ein Nachrichten spezifisches Feld enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Konstante                                                                                              | Wert         |
|-------------------------------------------------------------------------------------------------------|---------------|
| <dl> <dt>**msimessagestatus userror**</dt> </dl>  | -1<br/> |
| <dl> <dt>**msimessagestatus-None**</dt> </dl>   | 0<br/>  |
| <dl> <dt>**msimessagestatuusok**</dt> </dl>     | 1<br/>  |
| <dl> <dt>**msimessagestatus Cancel**</dt> </dl> | 2<br/>  |
| <dl> <dt>**msimessagestatus-Abort**</dt> </dl>  | 3<br/>  |
| <dl> <dt>**msimessagestatus-Wiederholungsversuch**</dt> </dl>  | 4<br/>  |
| <dl> <dt>**msimessagestatusignore**</dt> </dl> | 5<br/>  |
| <dl> <dt>**msimessagestatusyes**</dt> </dl>    | 6<br/>  |
| <dl> <dt>**msimessagestatus-Nr**</dt> </dl>     | 7<br/>  |



 

## <a name="remarks"></a>Bemerkungen

**Nachrichten Daten Satz Felder**

Im folgenden werden die Definitionen der Daten Satz Felder beschrieben, wenn msimessagetypeprogress als Nachrichtentyp übergeben wird.

Feld 1 gibt den Typ der Statusmeldung an. Die Bedeutung der anderen Felder hängt von dem Wert in diesem Feld ab. Die möglichen Werte, die in Feld 1 festgelegt werden können, lauten wie folgt.



| Nachrichtenname     | Wert | Beschreibung von Feld 1                                                                                                 |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------|
| Masterreset      | 0     | Setzt die Statusanzeige zurück und legt die erwartete Gesamtzahl der Ticks in der Leiste fest.                                         |
| ActionInfo       | 1     | Stellt Informationen im Zusammenhang mit Fortschrittsmeldungen bereit, die von der aktuellen Aktion gesendet werden sollen.                                 |
| Progressreport   | 2     | Erhöht die Statusanzeige.                                                                                        |
| Progressaddition | 3     | Ermöglicht einer Aktion (z. b. CustomAction), Ticks zur erwarteten Gesamtzahl der Statusanzeige hinzuzufügen. |



 

Die Bedeutung von Feld 2 hängt wie folgt von dem Wert in Feld 1 ab.



| Wert für Feld 1 | Beschreibung von Feld 2                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------|
| 0             | Erwartete Gesamtzahl der Ticks in der Statusanzeige.                                                        |
| 1             | Anzahl der Ticks, die die Statusanzeige für jede Aktions Daten Nachricht verschiebt. Dieses Feld wird ignoriert, wenn Feld 3 den Wert 0 hat. |
| 2             | Anzahl der Ticks, die die Statusanzeige verschoben hat.                                                                |
| 3             | Anzahl der Ticks, die dem erwarteten Gesamtfortschritt hinzugefügt werden sollen.                                                         |



 

Die Bedeutung von Feld 3 hängt wie folgt von dem Wert in Feld 1 ab.



| Wert für Feld 1 | Feld 3-Wert | Beschreibung von Feld 3                                                                                             |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------|
| 0             | 0             | Fortschrittsleiste weiterleiten (von links nach rechts)                                                                            |
|               | 1             | Rückwärts Statusanzeige (von rechts nach links)                                                                           |
| 1             | 0             | Mit der aktuellen Aktion werden explizite progressreport-Meldungen gesendet.                                                  |
|               | 1             | Erhöhen Sie die Statusanzeige um die Anzahl der Ticks, die in Feld 2 jedes Mal angegeben werden, wenn eine Aktions Daten Nachricht gesendet wird. |
| 2             | Nicht verwendet        |                                                                                                                 |
| 3             | Nicht verwendet        |                                                                                                                 |



 

Die Bedeutung von Feld 4 hängt wie folgt von dem Wert in Feld 1 ab.



| Wert für Feld 1 | Wert für Feld 4 | Beschreibung von Feld 4                                                                                                                                 |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | 0             | Die Ausführung wird ausgeführt. In diesem Fall kann die Benutzeroberfläche die verbleibende Zeit berechnen und anzeigen.                                                      |
|               | 1             | Erstellen des Ausführungs Skripts. In diesem Fall könnte die Benutzeroberfläche eine Meldung anzeigen, die gewartet werden soll, während das Installationsprogramm die Installation vorbereitet. |
| 1             | Nicht verwendet        |                                                                                                                                                     |
| 2             | Nicht verwendet        |                                                                                                                                                     |
| 3             | Nicht verwendet        |                                                                                                                                                     |



 

**Anzeigen von Meldungs Feldern**

Wenn Sie ein Meldungs Feld mit pushschaltflächen und Symbolen anzeigen möchten, berechnen Sie den Wert der *Art* , indem Sie die von **MessageBox** und **messageboxex** verwendeten Standardformate für Meldungs Felder zu **msimessagetypeerror**, **msimessagetypewarning** oder **msitypeuser** hinzufügen. Die verfügbaren Optionen für pushschaltflächen für VBScript sind vbOKOnly (MB \_ OK), vbOKCancel (MB \_ okabbrechen), vbAbortRetryIgnore (MB \_ AbortRetryIgnore), vbYesNoCancel (MB \_ YesNoCancel), vbYesNo (MB \_ YesNo) und vbRetryCancel (MB \_ RetryCancel). Die verfügbaren Symbol Optionen für VBScript sind vbCritical (MB \_ iconerror), vbQuestion (MB \_ iconquestion), vbExclamation (MB \_ iconwarning) und vbInformation (MB \_ iconinformation).

Der folgende-Befehl sendet z. b. eine **msimessagetypeerror** -Meldung mit dem vbExclamation-Symbol und den vbYesNo-Schaltflächen.


```VB
Session.Message &H01000034, record
```



Wenn eine benutzerdefinierte Aktion die **Message** -Methode aufruft, sollte die benutzerdefinierte Aktion in der Lage sein, einen Abbruch durch den Benutzer zu verarbeiten und muss **msidoaction statususerexit** zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 
