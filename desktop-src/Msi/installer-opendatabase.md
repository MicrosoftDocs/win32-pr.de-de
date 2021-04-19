---
description: Die OpenDatabase-Methode des Installer-Objekts öffnet eine vorhandene Datenbank oder erstellt eine neue Datenbank, die ein Datenbankobjekt zurückgibt. Es wird ein Fehler generiert, wenn das Datenbankobjekt nicht erfolgreich erstellt und geöffnet werden kann.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Installer. OpenDatabase-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenDatabase
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 13256f0bbe2d5adad61c46ea091e8207f1a9351b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358226"
---
# <a name="installeropendatabase-method"></a>Installer. OpenDatabase-Methode

Die **OpenDatabase** -Methode des [**Installer**](installer-object.md) -Objekts öffnet eine vorhandene Datenbank oder erstellt eine neue Datenbank, die ein [**Daten Bank**](database-object.md) Objekt zurückgibt. Es wird ein Fehler generiert, wenn das **Daten Bank** Objekt nicht erfolgreich erstellt und geöffnet werden kann.

## <a name="syntax"></a>Syntax


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*name* 
</dt> <dd>

Erforderliche Zeichenfolge, die den Pfadnamen der Datenbank enthält. Wenn eine leere Zeichenfolge angegeben wird, wird eine temporäre Datenbank erstellt, die nicht persistent gespeichert wird.

</dd> <dt>

*openMode* 
</dt> <dd>

Ein Parameter aus der folgenden Liste oder eine Zeichenfolge, die den Pfadnamen der neuen Ausgabedaten Bank Datei enthält, in die nach dem Commit geschrieben werden soll.



| Parameter                                                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <dt>**msiopendatabasemodereadonly**</dt> <dt>0</dt> </dl>                 | Öffnet eine schreibgeschützte Datenbank, keine persistenten Änderungen.<br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <dt>**msiopendatabasemodebug**</dt> <dt>1</dt> </dl>                 | Öffnet einen Lese-/Schreibmodus für die Datenbank im Transaktionsmodus.<br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <dt>**msiopendatabasemodebug**</dt> <dt>2</dt> </dl>                         | Öffnet einen direkten Lese-/Schreibzugriff für die Datenbank ohne Transaktion.<br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <dt>**msiopendatabasemode Create**</dt> <dt>3</dt> </dl>                         | Erstellt eine neue Datenbank mit Lese-/Schreibzugriff im Transact-Modus.<br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <dt>**msiopendatabasemodekreatedirect**</dt> <dt>4</dt> </dl> | Erstellt eine neue Datenbank mit Lese-/Schreibzugriff im direkten Modus.<br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <dt>**msiopendatabasemodelistscript**</dt> <dt>5</dt> </dl>         | Öffnet eine Datenbank, um Ankündigungs Skriptdateien anzuzeigen, wie z. b. die Dateien [**, die von der Methode**](installer-createadvertisescript.md) "Methode" generiert wurden.<br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <dt>**msiopendatabasemodepatchfile**</dt> <dt>32</dt> </dl>            | Fügt dieses Flag hinzu, um eine Patchdatei anzugeben.<br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn eine Datenbank als Ausgabe einer anderen Datenbank geöffnet wird, ist der Zusammenfassungs Datenstrom der Ausgabedatenbank tatsächlich eine schreibgeschützte Spiegelung der ursprünglichen Datenbank und kann daher nicht geändert werden. Außerdem wird Sie nicht in der Datenbank gespeichert. Um die zusammenfassenden Informationen für die Ausgabedatenbank zu erstellen oder zu ändern, muss sie geschlossen und erneut geöffnet werden.

Zum Erstellen und Speichern von Änderungen an einer Datenbank öffnen Sie zunächst die Datenbank in der Transaktion (msiopendatabasemodetransact), Create (msiopendatabasemodecreate oder msiopendatabasemodekreatedirect) oder Direct (msiopendatabasemodedirect)-Modus. Nachdem Sie die Änderungen vorgenommen haben, sollten Sie vor dem Schließen des Daten Bank Handles immer die [**Commit**](database-commit.md) -Methode aufruft. Die **Commit** -Methode leert alle Puffer.

Aufrufen Sie immer die [**Commit**](database-commit.md) -Methode für eine Datenbank, die im direkten Modus (msiopendatabasemodedirect oder msiopendatabasemodecreatedirect) geöffnet wurde, bevor Sie die Datenbank schließen. Wenn dies nicht möglich ist, kann die Datenbank beschädigt werden.

Da die **OpenDatabase** -Methode den Datenbankzugriff initiiert, kann Sie nicht mit einer laufenden Installation verwendet werden.

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




