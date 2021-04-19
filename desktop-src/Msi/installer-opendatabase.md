---
description: Die OpenDatabase-Methode des Installer-Objekts öffnet eine vorhandene Datenbank oder erstellt eine neue Datenbank und gibt ein Database-Objekt zurück. Es wird ein Fehler generiert, wenn das Database-Objekt nicht erfolgreich erstellt und geöffnet werden kann.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Installer.OpenDatabase-Methode
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
ms.openlocfilehash: 897e683fd56ce3e7496dd945ee068a9e6f0c0f77
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492269"
---
# <a name="installeropendatabase-method"></a>Installer.OpenDatabase-Methode

Die **OpenDatabase-Methode** des [**Installer-Objekts**](installer-object.md) öffnet eine vorhandene Datenbank oder erstellt eine neue Datenbank und gibt ein [**Database-Objekt**](database-object.md) zurück. Es wird ein Fehler generiert, wenn das **Database-Objekt** nicht erfolgreich erstellt und geöffnet werden kann.

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

Erforderliche Zeichenfolge, die den Pfadnamen der Datenbank enthält. Wenn eine leere Zeichenfolge angegeben wird, wird eine temporäre Datenbank erstellt, die nicht beibehalten wird.

</dd> <dt>

*Openmode* 
</dt> <dd>

Ein Parameter aus der folgenden Liste oder eine Zeichenfolge, die den Pfadnamen der neuen Ausgabedatenbankdatei enthält, in die beim Commit geschrieben werden soll.



| Parameter                                                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt> </dl>                 | Öffnet eine schreibgeschützte Datenbank ohne permanente Änderungen.<br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt> </dl>                 | Öffnet eine Datenbank mit Lese-/Schreibzugriff im Transaktionsmodus.<br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt> </dl>                         | Öffnet eine Datenbank mit direktem Lese-/Schreibzugriff ohne Transaktion.<br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt> </dl>                         | Erstellt eine neue Datenbank im Transact-Modus mit Lese-/Schreibzugriff.<br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt> </dl> | Erstellt eine neue Datenbank mit Lese-/Schreibzugriff im direkten Modus.<br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt> </dl>         | Öffnet eine Datenbank zum Anzeigen von Ankündigen von Skriptdateien, z. B. die von der [**CreateAdvertiseScript-Methode**](installer-createadvertisescript.md) generierten Dateien.<br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt> </dl>            | Fügt dieses Flag hinzu, um eine Patchdatei anzugeben.<br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**Database-Objekt,**](database-object.md) das die vorhandene oder neue Installationsdatenbank darstellt, die geöffnet wurde.

## <a name="remarks"></a>Bemerkungen

Wenn eine Datenbank als Ausgabe einer anderen Datenbank geöffnet wird, ist der Zusammenfassungsinformationsdatenstrom der Ausgabedatenbank tatsächlich eine schreibgeschützte Spiegelung der ursprünglichen Datenbank und kann daher nicht geändert werden. Darüber hinaus wird sie nicht in der Datenbank beibehalten. Um die Zusammenfassungsinformationen für die Ausgabedatenbank zu erstellen oder zu ändern, müssen sie geschlossen und erneut geöffnet werden.

Um Änderungen an einer Datenbank vorzunehmen und zu speichern, öffnen Sie zuerst die Datenbank in der Transaktion (msiOpenDatabaseModeTransact), erstellen (msiOpenDatabaseModeCreate oder msiOpenDatabaseModeCreateDirect) oder den direkten Modus (msiOpenDatabaseModeDirect). Rufen Sie nach dem Vornehmen der Änderungen immer die [**Commit-Methode**](database-commit.md) auf, bevor Sie das Datenbankhandle schließen. Die **Commit-Methode** leert alle Puffer.

Rufen Sie immer die [**Commit-Methode**](database-commit.md) für eine Datenbank auf, die im direkten Modus geöffnet wurde (msiOpenDatabaseModeDirect oder msiOpenDatabaseModeCreateDirect), bevor Sie die Datenbank schließen. Wenn dies nicht geschieht, kann die Datenbank beschädigt werden.

Da die **OpenDatabase-Methode** den Datenbankzugriff initiiert, kann sie nicht mit einer ausgeführten Installation verwendet werden.

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



 

 




