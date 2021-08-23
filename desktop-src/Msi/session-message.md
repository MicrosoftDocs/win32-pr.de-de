---
description: Die Message-Methode des Session-Objekts führt alle aktivierten Protokollierungsvorgänge aus und verzieht die Ausführung auf das Benutzeroberflächenhandlerobjekt, das der Engine zugeordnet ist. Die Protokollierung kann für die verschiedenen Nachrichtentypen selektiv aktiviert werden. Weitere Informationen finden Sie unter EnableLog-Methode.
ms.assetid: 09053700-a641-4970-bf55-d7c81f345257
title: Session.Message-Methode
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
ms.openlocfilehash: 6d14d59e801afcdf69bec2f1169d5c5b14469e8b13ac3f4c593955c7e235c7b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629140"
---
# <a name="sessionmessage-method"></a>Session.Message-Methode

Die **Message-Methode** des [**Session-Objekts**](session-object.md) führt alle aktivierten Protokollierungsvorgänge aus und verzieht die Ausführung auf das Benutzeroberflächenhandlerobjekt, das der Engine zugeordnet ist. Die Protokollierung kann für die verschiedenen Nachrichtentypen selektiv aktiviert werden. Weitere Informationen finden Sie unter [**EnableLog-Methode.**](installer-enablelog.md)

Wenn Datensatzfeld 0 eine Formatierungszeichenfolge enthält, wird es verwendet, um die Daten in den anderen Feldern zu formatieren. Wenn es sich bei der Nachricht um eine Fehler-, Warnungs- oder Benutzermeldung handelt, wird versucht, eine Meldungsvorlage in der Fehlertabelle für die aktuelle Datenbank mithilfe der Fehlernummer im Feld 1 des Datensatzes für Meldungstypen und Rückgabewerte zu finden.

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

Der *kind-Parameter* muss einer der folgenden Werte sein. Um ein Meldungsfeld mit Pushschaltflächen und Symbolen anzuzeigen, berechnen Sie den Wert der *Art,* indem Sie **msiMessageTypeError,** **msiMessageTypeWarning** oder **msiMessageTypeUser** die standardmäßigen Nachrichtenfeldstile hinzufügen, die von [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) und [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) verwendet werden. Weitere Informationen finden Sie unten im Abschnitt "Hinweise".



| Konstante                                                                                                                                                                                                                                                                                                                 | Bedeutung                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiMessageTypeFatalExit"></span><span id="msimessagetypefatalexit"></span><span id="MSIMESSAGETYPEFATALEXIT"></span><dl> <dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt> </dl>                     | Vorzeitige Beendigung, möglicherweise schwerwiegender Speicherausbruch.<br/>                                                                              |
| <span id="msiMessageTypeError"></span><span id="msimessagetypeerror"></span><span id="MSIMESSAGETYPEERROR"></span><dl> <dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt> </dl>                                     | Formatierte Fehlermeldung, \[ 1 \] ist die Nachrichtennummer in der [Fehlertabelle](error-table.md).<br/>                                               |
| <span id="msiMessageTypeWarning"></span><span id="msimessagetypewarning"></span><span id="MSIMESSAGETYPEWARNING"></span><dl> <dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt> </dl>                             | Formatierte Warnmeldung, \[ 1 \] ist die Nachrichtennummer in der [Fehlertabelle](error-table.md).<br/>                                             |
| <span id="msiMessageTypeUser_"></span><span id="msimessagetypeuser_"></span><span id="MSIMESSAGETYPEUSER_"></span><dl> <dt> **msiMessageTypeUser**</dt> <dt>&H03000000</dt> </dl>                                     | Benutzeranforderungsmeldung, \[ 1 \] ist die Nachrichtennummer in [der Fehlertabelle](error-table.md).<br/>                                                  |
| <span id="msiMessageTypeInfo"></span><span id="msimessagetypeinfo"></span><span id="MSIMESSAGETYPEINFO"></span><dl> <dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt> </dl>                                         | Informative Meldung für das Protokoll, die nicht angezeigt werden soll.<br/>                                                                                 |
| <span id="msiMessageTypeFilesInUse"></span><span id="msimessagetypefilesinuse"></span><span id="MSIMESSAGETYPEFILESINUSE"></span><dl> <dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt> </dl>                 | Liste der verwendeten Dateien, die ersetzt werden müssen.<br/>                                                                                    |
| <span id="msiMessageTypeResolveSource"></span><span id="msimessagetyperesolvesource"></span><span id="MSIMESSAGETYPERESOLVESOURCE"></span><dl> <dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt> </dl>     | Anforderung zum Bestimmen eines gültigen Quellspeicherorts.<br/>                                                                                     |
| <span id="msiMessageTypeOutOfDiskSpace"></span><span id="msimessagetypeoutofdiskspace"></span><span id="MSIMESSAGETYPEOUTOFDISKSPACE"></span><dl> <dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt> </dl> | Meldung zu unzureichendem Speicherplatz.<br/>                                                                                                  |
| <span id="msiMessageTypeActionStart"></span><span id="msimessagetypeactionstart"></span><span id="MSIMESSAGETYPEACTIONSTART"></span><dl> <dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt> </dl>             | Start der Aktion, \[ 1 \] Aktionsname, \[ 2 \] Beschreibung, \[ 3 \] Vorlage für ACTIONDATA-Nachrichten.<br/>                                    |
| <span id="msiMessageTypeActionData"></span><span id="msimessagetypeactiondata"></span><span id="MSIMESSAGETYPEACTIONDATA"></span><dl> <dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt> </dl>                 | Aktionsdaten. Datensatzfelder entsprechen der Vorlage der ACTIONSTART-Nachricht.<br/>                                                     |
| <span id="msiMessageTypeProgress"></span><span id="msimessagetypeprogress"></span><span id="MSIMESSAGETYPEPROGRESS"></span><dl> <dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt> </dl>                         | Statusanzeigeinformationen. Weitere Informationen finden Sie unten in der Beschreibung der Datensatzfelder.<br/>                                                             |
| <span id="msiMessageTypeCommonData_"></span><span id="msimessagetypecommondata_"></span><span id="MSIMESSAGETYPECOMMONDATA_"></span><dl> <dt> **msiMessageTypeCommonData**</dt> <dt>&H0B000000</dt> </dl>             | Um die Schaltfläche Abbrechen zu aktivieren, legen Sie \[ 1 \] auf 2 und \[ 2 \] auf 1 fest. <br/> Um die Schaltfläche Abbrechen zu deaktivieren, legen Sie \[ 1 \] auf 2 und \[ 2 \] auf 0 fest.<br/> |



 

</dd> <dt>

*record* 
</dt> <dd>

Erforderliches [**Datensatzobjekt,**](record-object.md) das ein meldungsspezifisches Feld enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Konstante                                                                                              | Wert         |
|-------------------------------------------------------------------------------------------------------|---------------|
| <dl> <dt>**msiMessageStatusError**</dt> </dl>  | –1<br/> |
| <dl> <dt>**msiMessageStatusNone**</dt> </dl>   | 0<br/>  |
| <dl> <dt>**msiMessageStatusOk**</dt> </dl>     | 1<br/>  |
| <dl> <dt>**msiMessageStatusCancel**</dt> </dl> | 2<br/>  |
| <dl> <dt>**msiMessageStatusAbort**</dt> </dl>  | 3<br/>  |
| <dl> <dt>**msiMessageStatusRetry**</dt> </dl>  | 4<br/>  |
| <dl> <dt>**msiMessageStatusIgnore**</dt> </dl> | 5<br/>  |
| <dl> <dt>**msiMessageStatusYes**</dt> </dl>    | 6<br/>  |
| <dl> <dt>**msiMessageStatusNo**</dt> </dl>     | 7<br/>  |



 

## <a name="remarks"></a>Hinweise

**Felder für Nachrichtendatensatz**

Im Folgenden werden die Datensatzfelddefinitionen beschrieben, wenn msiMessageTypeProgress als Nachrichtentyp übergeben wird.

Feld 1 gibt den Typ der Statusmeldung an. Die Bedeutung der anderen Felder hängt vom Wert in diesem Feld ab. Die möglichen Werte, die in Feld 1 festgelegt werden können, sind wie folgt.



| Nachrichtenname     | Wert | Beschreibung von Feld 1                                                                                                 |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------|
| MasterReset      | 0     | Setzt die Statusanzeige zurück und legt die erwartete Gesamtanzahl von Ticks in der Leiste fest.                                         |
| ActionInfo       | 1     | Stellt Informationen zu Statusmeldungen bereit, die von der aktuellen Aktion gesendet werden sollen.                                 |
| ProgressReport   | 2     | Erhöht die Statusanzeige.                                                                                        |
| ProgressAddition | 3     | Aktiviert eine Aktion (z. B. CustomAction), um der erwarteten Gesamtanzahl des Fortschritts der Statusanzeige Ticks hinzuzufügen. |



 

Die Bedeutung von Feld 2 hängt wie folgt vom Wert in Feld 1 ab.



| Feld 1-Wert | Beschreibung von Feld 2                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------|
| 0             | Erwartete Gesamtanzahl von Ticks in der Statusanzeige.                                                        |
| 1             | Anzahl der Ticks, die die Statusanzeige für jede ActionData-Nachricht verschiebt. Dieses Feld wird ignoriert, wenn Feld 3 0 ist. |
| 2             | Anzahl der Ticks, die die Statusanzeige verschoben wurde.                                                                |
| 3             | Anzahl der Ticks, die dem erwarteten Gesamtfortschritt hinzugefügt werden sollen.                                                         |



 

Die Bedeutung von Feld 3 hängt wie folgt vom Wert in Feld 1 ab.



| Feld 1-Wert | Feld 3-Wert | Beschreibung von Feld 3                                                                                             |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------|
| 0             | 0             | Fortschrittsanzeige vorwärts (von links nach rechts)                                                                            |
|               | 1             | Statusanzeige rückwärts (von rechts nach links)                                                                           |
| 1             | 0             | Die aktuelle Aktion sendet explizite ProgressReport-Meldungen.                                                  |
|               | 1             | Erhöhen Sie die Statusanzeige jedes Mal um die Anzahl von Ticks, die in Feld 2 angegeben sind, wenn eine ActionData-Nachricht gesendet wird. |
| 2             | Nicht verwendet        |                                                                                                                 |
| 3             | Nicht verwendet        |                                                                                                                 |



 

Die Bedeutung von Feld 4 hängt wie folgt vom Wert in Feld 1 ab.



| Feld 1-Wert | Feld 4-Wert | Beschreibung von Feld 4                                                                                                                                 |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | 0             | Die Ausführung wird ausgeführt. In diesem Fall kann die Benutzeroberfläche die verbleibende Zeit berechnen und anzeigen.                                                      |
|               | 1             | Erstellen des Ausführungsskripts. In diesem Fall kann auf der Benutzeroberfläche eine Meldung angezeigt werden, dass Sie warten, bis das Installationsprogramm die Installation vorbereitet hat. |
| 1             | Nicht verwendet        |                                                                                                                                                     |
| 2             | Nicht verwendet        |                                                                                                                                                     |
| 3             | Nicht verwendet        |                                                                                                                                                     |



 

**Anzeigen von Meldungsfeldern**

Um ein Meldungsfeld mit Pushschaltflächen und Symbolen anzuzeigen, berechnen Sie den Wert der *Art,* indem Sie die standardmäßigen Nachrichtenfeldstile, die von **MessageBox** und **MessageBoxEx** verwendet werden, **msiMessageTypeError,** **msiMessageTypeWarning** oder **msiTypeUser** hinzufügen. Die verfügbaren Pushschaltflächenoptionen für VBScript sind vbOKOnly (MB \_ OK), vbOKCancel (MB \_ OKCANCEL), vbAbortRetryIgnore (MB \_ ABORTRETRYIGNORE), vbYesNoCancel (MB \_ YESNOCANCEL), vbYesNo (MB \_ YESNO) und vbRetryCancel (MB \_ RETRYCANCEL). Die verfügbaren Symboloptionen für VBScript sind vbCritical (MB \_ ICONERROR), vbQuestion (MB \_ ICONQUESTION), vbExclamation (MB \_ ICONWARNING) und vbInformation (MB \_ ICONINFORMATION).

Der folgende Aufruf sendet beispielsweise eine **msiMessageTypeError-Nachricht** mit dem Symbol vbExclamation und den Schaltflächen vbYesNo.


```VB
Session.Message &H01000034, record
```



Wenn eine benutzerdefinierte Aktion die **Message-Methode** aufruft, sollte die benutzerdefinierte Aktion einen Abbruch durch den Benutzer verarbeiten können und **msiDoActionStatusUserExit** zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist als 000C109E-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                             |



 

 
