---
description: Das Datenbankobjekt greift auf eine Installerdatenbank zu.
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
ms.openlocfilehash: 5b47e4678d9475abe90c4b55d6adb514314dcc0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364468"
---
# <a name="database-object"></a>Datenbankobjekt

Das **Daten Bank** Objekt greift auf eine Installerdatenbank zu.

Das **Daten Bank** Objekt wird freigegeben, wenn es entweder außerhalb des gültigen Bereichs liegt oder wenn die zugeordnete Objekt Variable auf NULL festgelegt ist. Die [**Commit**](database-commit.md) -Methode muss aufgerufen werden, bevor das **Database** -Objekt freigegeben wird, um alle persistenten Änderungen zu schreiben. Wenn die **Commit** -Methode nicht aufgerufen wird, führt das Installationsprogramm bei der Objekt Zerstörung ein implizites ROLLBACK durch.

Der-Client kann das folgende Verfahren für den Datenzugriff verwenden.

**Abfragen der API-Sequenzierung**

1.  Rufen Sie ein **Daten Bank** Objekt ab, indem Sie [**OpenDatabase**](installer-opendatabase.md) oder das [**Installer**](installer-object.md) -Objekt aufrufen.
2.  Initiieren Sie eine Abfrage mithilfe einer SQL-Zeichenfolge, indem Sie die [**OpenView**](database-openview.md) -Methode des **Daten Bank** Objekts aufrufen.
3.  Legen Sie Abfrage Parameter in einem [**Datensatz**](record-object.md) -Objekt fest, und führen Sie die Datenbankabfrage durch Aufrufen der [**Execute**](view-execute.md) -Methode des [**View**](view-object.md) -Objekts aus. Dies erzeugt ein Ergebnis, das abgerufen oder aktualisiert werden kann.
4.  Rufen Sie die [**Fetch**](view-fetch.md) -Methode des [**View**](view-object.md) -Objekts wiederholt auf, um [**Daten Satz**](record-object.md) Objekte zurückzugeben
5.  Aktualisieren von Daten Bank Zeilen eines [**Datensatz**](record-object.md) -Objekts, das von der [**Fetch**](view-fetch.md) -Methode abgerufen wurde, mithilfe der [**Modify**](view-modify.md) -Methode des [**View**](view-object.md) -Objekts.
6.  Geben Sie die Abfrage und alle nicht abgerufenen Datensätze durch Aufrufen der [**Close**](view-close.md) -Methode des [**View**](view-object.md) -Objekts frei.
7.  Speichern Sie alle Datenbankupdates, indem Sie die [**Commit**](database-commit.md) -Methode des **Daten Bank** Objekts aufrufen.

## <a name="members"></a>Member

Das **Daten Bank** Objekt verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Daten Bank** Objekt verfügt über diese Methoden.



| Methode                                                                    | BESCHREIBUNG                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Applytransform**](database-applytransform.md)                         | Wendet die Transformation auf diese Datenbank an.<br/>                                                                                                                        |
| [**Einzusetzen**](database-commit.md)                                         | Schließt die persistente Form der Datenbank ab.<br/>                                                                                                                 |
| [**"Kreatetransformsummaryinfo"**](database-createtransformsummaryinfo.md) | Erstellt den Zusammenfassungs Informationsdaten Strom einer vorhandenen Transformations Datei und füllt ihn auf.<br/>                                                                            |
| [**Enableuipreview**](database-enableuipreview.md)                       | Erleichtert das Erstellen von Dialogfeldern und-Plakaten durch Bereitstellen der Unterstützung, die zum Anzeigen der in der Installer-Datenbank gespeicherten Dialogfelder für Benutzeroberflächen erforderlich ist.<br/> |
| [**Exportieren**](database-export.md)                                         | Kopiert die Struktur und die Daten aus einer angegebenen Tabelle in eine Textarchiv Datei.<br/>                                                                                   |
| [**Gene Rate Transform**](database-generatetransform.md)                   | Erstellt eine Transformation.<br/>                                                                                                                                           |
| [**Importieren**](database-import.md)                                         | Importiert eine Datenbanktabelle aus einer Textarchiv Datei.<br/>                                                                                                             |
| [**Merge**](database-merge.md)                                           | Führt die Verweis Datenbank mit der Basisdatenbank zusammen.<br/>                                                                                                          |
| [**OpenView –**](database-openview.md)                                     | Gibt ein [**Ansichts**](view-object.md) Objekt zurück, das die von einer SQL-Zeichenfolge angegebene Abfrage darstellt.<br/>                                                                 |



 

### <a name="properties"></a>Eigenschaften

Das **Daten Bank** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                               | BESCHREIBUNG                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Databasestate**](database-databasestate.md)<br/>                             | Gibt den persistenzstatus der Datenbank zurück.<br/>                                                                                                        |
| [**PrimaryKeys**](database-primarykeys.md)<br/>                                 | Gibt ein [**Daten Satz**](record-object.md) Objekt zurück, das den Tabellennamen und die Spaltennamen (die die Primärschlüssel umfasst) enthält.<br/>                        |
| [**SummaryInformation (Datenbankobjekt)**](database-summaryinformation.md)<br/> | Gibt ein [**SummaryInfo**](summaryinfo-object.md) -Objekt zurück, das zum Überprüfen, aktualisieren und Hinzufügen von Eigenschaften zum Zusammenfassungs Informationsdaten Strom verwendet werden kann.<br/> |
| [**Tablepersistent**](database-tablepersistent.md)<br/>                         | Gibt den persistenzstatus der Tabelle zurück.<br/>                                                                                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




