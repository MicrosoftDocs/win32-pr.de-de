---
description: Das Database-Objekt greift auf eine Installationsdatenbank zu.
ms.assetid: 97765884-3e1c-486a-932c-6430b113fac8
title: Datenbankobjekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3dcdb2c4098905d7e6a410e786d4af254732bc80cee4b760870a7c1c44a8ec26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086200"
---
# <a name="database-object"></a>Datenbankobjekt

Das **Database-Objekt** greift auf eine Installationsdatenbank zu.

Das **Database-Objekt** wird freigegeben, wenn es entweder aus dem Gültigkeitsbereich entfernt wird oder wenn die zugeordnete Objektvariable auf NULL festgelegt ist. Die [**Commit-Methode**](database-commit.md) muss aufgerufen werden, bevor das **Database-Objekt** freigegeben wird, um alle persistenten Änderungen zu schreiben. Wenn die **Commit-Methode** nicht aufgerufen wird, führt das Installationsprogramm ein implizites Rollback nach der Objektvernichtung aus.

Der Client kann das folgende Verfahren für den Datenzugriff verwenden.

**So fragen Sie die API-Sequenzierung ab**

1.  Rufen Sie ein **Database-Objekt** ab, indem Sie [**openDatabase**](installer-opendatabase.md) oder das [**Installer-Objekt**](installer-object.md) aufrufen.
2.  Initiieren Sie eine Abfrage mithilfe einer SQL Zeichenfolge, indem Sie die [**OpenView-Methode**](database-openview.md) des **Database-Objekts** aufrufen.
3.  Legen Sie Abfrageparameter in einem [**Record-Objekt**](record-object.md) fest, und führen Sie die Datenbankabfrage durch Aufrufen der [**Execute-Methode**](view-execute.md) des [**View-Objekts**](view-object.md) aus. Dies führt zu einem Ergebnis, das abgerufen oder aktualisiert werden kann.
4.  Rufen Sie die [**Fetch-Methode**](view-fetch.md) des [**View-Objekts**](view-object.md) wiederholt auf, um [**Record-Objekte**](record-object.md) zurückzugeben.
5.  Aktualisieren Sie die Datenbankzeilen eines [**Record-Objekts,**](record-object.md) das von der [**Fetch-Methode**](view-fetch.md) mithilfe der [**Modify-Methode**](view-modify.md) des [**View-Objekts**](view-object.md) abgerufen wurde.
6.  Geben Sie die Abfrage und alle nicht abgerufenen Datensätze frei, indem Sie die [**Close-Methode**](view-close.md) des [**View-Objekts aufrufen.**](view-object.md)
7.  Speichern Sie alle Datenbankupdates, indem Sie die [**Commit-Methode**](database-commit.md) des **Database-Objekts** aufrufen.

## <a name="members"></a>Member

Das **Database-Objekt** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Database-Objekt** verfügt über diese Methoden.



| Methode                                                                    | BESCHREIBUNG                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyTransform**](database-applytransform.md)                         | Wendet die Transformation auf diese Datenbank an.<br/>                                                                                                                        |
| [**Commit**](database-commit.md)                                         | Finalisiert die persistente Form der Datenbank.<br/>                                                                                                                 |
| [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) | Erstellt und füllt den Zusammenfassungsinformationsdatenstrom einer vorhandenen Transformationsdatei.<br/>                                                                            |
| [**EnableUIPreview**](database-enableuipreview.md)                       | Erleichtert die Erstellung von Dialogfeldern und Werbern, indem die erforderliche Unterstützung zum Anzeigen der in der Installer-Datenbank gespeicherten Dialogfelder für die Benutzeroberfläche geboten wird.<br/> |
| [**Exportieren**](database-export.md)                                         | Kopiert die Struktur und die Daten aus einer angegebenen Tabelle in eine Textarchivdatei.<br/>                                                                                   |
| [**GenerateTransform**](database-generatetransform.md)                   | Erstellt eine Transformation.<br/>                                                                                                                                           |
| [**Importieren**](database-import.md)                                         | Importiert eine Datenbanktabelle aus einer Textarchivdatei.<br/>                                                                                                             |
| [**Zusammenführen**](database-merge.md)                                           | Führt die Verweisdatenbank mit der Basisdatenbank zusammen.<br/>                                                                                                          |
| [**Openview**](database-openview.md)                                     | Gibt ein [**View-Objekt**](view-object.md) zurück, das die durch eine SQL Zeichenfolge angegebene Abfrage darstellt.<br/>                                                                 |



 

### <a name="properties"></a>Eigenschaften

Das **Database-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                               | BESCHREIBUNG                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DatabaseState**](database-databasestate.md)<br/>                             | Gibt den Persistenzzustand der Datenbank zurück.<br/>                                                                                                        |
| [**PrimaryKeys**](database-primarykeys.md)<br/>                                 | Gibt ein [**Record-Objekt**](record-object.md) zurück, das den Tabellennamen und die Spaltennamen (bestehend aus den Primärschlüsseln) enthält.<br/>                        |
| [**SummaryInformation (Datenbankobjekt)**](database-summaryinformation.md)<br/> | Gibt ein [**SummaryInfo-Objekt**](summaryinfo-object.md) zurück, das zum Untersuchen, Aktualisieren und Hinzufügen von Eigenschaften zum Zusammenfassungsinformationsdatenstrom verwendet werden kann.<br/> |
| [**TablePersistent**](database-tablepersistent.md)<br/>                         | Gibt den Persistenzzustand der Tabelle zurück.<br/>                                                                                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase ist als 000C109D-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Windows Beispiele für Skripterstellung für Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




