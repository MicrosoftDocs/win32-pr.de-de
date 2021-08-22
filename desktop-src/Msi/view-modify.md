---
description: Die Modify-Methode des View-Objekts ändert eine Datenbankzeile mit einem geänderten Record-Objekt, das von der Fetch-Methode abgerufen wird.
ms.assetid: c3c500aa-070f-41d7-90f7-db979452d24f
title: View.Modify-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Modify
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e4149afb638c01b31d51c45f5d55c6f43fe50b4a85b77c25b4f6a5e0ed5993fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498860"
---
# <a name="viewmodify-method"></a>View.Modify-Methode

Die **Modify-Methode** des [**View-Objekts**](view-object.md) ändert eine Datenbankzeile mit einem geänderten [**Record-Objekt,**](record-object.md) das von der [**Fetch-Methode**](view-fetch.md) abgerufen wird.

## <a name="syntax"></a>Syntax


```JScript
View.Modify(
  action,
  record
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*action* 
</dt> <dd>

Erforderliche Aktion, die für die Datenbankzeile ausgeführt werden muss. Diese Aktion ist eine der in der folgenden Tabelle aufgeführten Aktionen.



| Name der Aktion                                                                                                                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiViewModifySeek"></span><span id="msiviewmodifyseek"></span><span id="MSIVIEWMODIFYSEEK"></span><dl> <dt>**msiViewModifySeek**</dt> <dt>–1</dt> </dl>                                            | Aktualisiert die Informationen im angegebenen Datensatz, ohne die Position im Resultset zu ändern und ohne auswirkungen auf nachfolgende Abrufvorgänge. Der Datensatz kann dann für nachfolgende Updates, Löschungen und Aktualisierungen verwendet werden. Alle Primärschlüsselspalten der Tabelle müssen sich in der Abfrage befinden, und der Datensatz muss mindestens so viele Felder wie die Abfrage enthalten. Seek kann nicht mit mehrtabellen Abfragen verwendet werden. Weitere Informationen finden Sie in den Hinweisen. Dieser Modus kann nicht mit einer Ansicht verwendet werden, die Joins enthält.<br/>                                                                             |
| <span id="msiViewModifyRefresh"></span><span id="msiviewmodifyrefresh"></span><span id="MSIVIEWMODIFYREFRESH"></span><dl> <dt>**msiViewModifyRefresh**</dt> <dt>0</dt> </dl>                                 | Aktualisiert die Informationen im Datensatz. Zuerst muss die [**Fetch-Methode**](view-fetch.md) mit demselben Datensatz aufgerufen werden. Fehler bei einer gelöschten Zeile. Funktioniert sowohl mit Lese-/Schreib- als auch mit schreibgeschützten Datensätzen.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyInsert"></span><span id="msiviewmodifyinsert"></span><span id="MSIVIEWMODIFYINSERT"></span><dl> <dt>**msiViewModifyInsert**</dt> <dt>1</dt> </dl>                                     | Fügt einen Datensatz ein. Schlägt fehl, wenn eine Zeile mit denselben Primärschlüsseln vorhanden ist. Fehler bei einer schreibgeschützten Datenbank. Dieser Modus kann nicht mit einer Ansicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="msiViewModifyUpdate"></span><span id="msiviewmodifyupdate"></span><span id="MSIVIEWMODIFYUPDATE"></span><dl> <dt>**msiViewModifyUpdate**</dt> <dt>2</dt> </dl>                                     | Aktualisiert einen vorhandenen Datensatz. Nur Nicht-Primärschlüssel. Zuerst muss die [**Fetch-Methode**](view-fetch.md) mit demselben Datensatz aufgerufen werden. Fehler bei einem gelöschten Datensatz. Funktioniert nur mit Datensätzen mit Lese-/Schreibzugriff.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyAssign"></span><span id="msiviewmodifyassign"></span><span id="MSIVIEWMODIFYASSIGN"></span><dl> <dt>**msiViewModifyAssign**</dt> <dt>3</dt> </dl>                                     | Schreibt aktuelle Daten im Cursor in eine Tabellenzeile. Aktualisiert den Datensatz, wenn die Primärschlüssel mit einer vorhandenen Zeile übereinstimmen, und fügt ein, wenn sie nicht übereinstimmen. Fehler bei einer schreibgeschützten Datenbank. Dieser Modus kann nicht mit einer Ansicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiViewModifyReplace"></span><span id="msiviewmodifyreplace"></span><span id="MSIVIEWMODIFYREPLACE"></span><dl> <dt>**msiViewModifyReplace**</dt> <dt>4</dt> </dl>                                 | Aktualisiert oder löscht einen Datensatz und fügt diesen in eine Tabelle ein. Zuerst muss die [**Fetch-Methode**](view-fetch.md) mit demselben Datensatz aufgerufen werden. Aktualisiert den Datensatz, wenn die Primärschlüssel unverändert sind. Löscht die alte Zeile und fügt neue ein, wenn sich Primärschlüssel geändert haben. Fehler bei einer schreibgeschützten Datenbank. Dieser Modus kann nicht mit einer Ansicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                           |
| <span id="msiViewModifyMerge"></span><span id="msiviewmodifymerge"></span><span id="MSIVIEWMODIFYMERGE"></span><dl> <dt>**msiViewModifyMerge**</dt> <dt>5</dt> </dl>                                         | Fügt einen Datensatz in eine Tabelle ein oder überprüft sie. Fügt ein, wenn Primärschlüssel keiner Zeile entsprechen, und überprüft, ob eine Übereinstimmung vorliegt. Schlägt fehl, wenn der Datensatz nicht mit den Daten in der Tabelle übereinstimmt. Schlägt fehl, wenn ein Datensatz mit einem doppelten Schlüssel vorhanden ist, der nicht identisch ist. Funktioniert nur mit Datensätzen mit Lese-/Schreibzugriff. Dieser Modus kann nicht mit einer Ansicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                |
| <span id="msiViewModifyDelete"></span><span id="msiviewmodifydelete"></span><span id="MSIVIEWMODIFYDELETE"></span><dl> <dt>**msiViewModifyDelete**</dt> <dt>6</dt> </dl>                                     | Entfernt eine Zeile aus der Tabelle. Zuerst muss die [**Fetch-Methode**](view-fetch.md) mit demselben Datensatz aufgerufen werden. Schlägt fehl, wenn die Zeile gelöscht wurde. Funktioniert nur mit Datensätzen mit Lese-/Schreibzugriff. Dieser Modus kann nicht mit einer Ansicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyInsertTemporary"></span><span id="msiviewmodifyinserttemporary"></span><span id="MSIVIEWMODIFYINSERTTEMPORARY"></span><dl> <dt>**msiViewModifyInsertTemporary**</dt> <dt>7</dt> </dl> | Fügt einen temporären Datensatz ein. Die Informationen sind nicht persistent. Schlägt fehl, wenn eine Zeile mit demselben Primärschlüssel vorhanden ist. Funktioniert nur mit Datensätzen mit Lese-/Schreibzugriff. Dieser Modus kann nicht mit einer Ansicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                                                                                                                                                           |
| <span id="msiViewModifyValidate"></span><span id="msiviewmodifyvalidate"></span><span id="MSIVIEWMODIFYVALIDATE"></span><dl> <dt>**msiViewModifyValidate**</dt> <dt>8</dt> </dl>                             | Überprüft einen Datensatz. Überprüft nicht joinübergreifend. Zuerst muss die [**Fetch-Methode**](view-fetch.md) mit demselben Datensatz aufgerufen werden. Abrufen von Validierungsfehlern mit der [**GetError-Methode.**](view-geterror.md) Funktioniert mit Lese-/Schreib- und schreibgeschützten Datensätzen. Dieser Modus kann nicht mit einer Ansicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                                                         |
| <span id="msiViewModifyValidateNew"></span><span id="msiviewmodifyvalidatenew"></span><span id="MSIVIEWMODIFYVALIDATENEW"></span><dl> <dt>**msiViewModifyValidateNew**</dt> <dt>9</dt> </dl>                 | Überprüft einen neuen Datensatz. Überprüft nicht joinübergreifend. Sucht nach doppelten Schlüsseln. Ruft Validierungsfehler ab, indem die [**GetError-Methode**](view-geterror.md) aufgerufen wird. Erfordert das Aufrufen [**der MsiDatabase.OpenView-Methode**](database-openview.md) mit einem Modify-Wert. Funktioniert mit Lese-/Schreib- und schreibgeschützten Datensätzen. Dieser Modus kann nicht mit einer Ansicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                 |
| <span id="msiViewModifyValidateField"></span><span id="msiviewmodifyvalidatefield"></span><span id="MSIVIEWMODIFYVALIDATEFIELD"></span><dl> <dt>**msiViewModifyValidateField**</dt> <dt>10</dt> </dl>        | Überprüft Felder eines abgerufenen oder neuen Datensatzes. Kann ein oder mehrere Felder eines unvollständigen Datensatzes überprüfen. Ruft Validierungsfehler ab, indem die [**GetError-Methode**](view-geterror.md) aufgerufen wird. Funktioniert mit Lese-/Schreib- und schreibgeschützten Datensätzen. Dieser Modus kann nicht mit einer Ansicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyValidateDelete"></span><span id="msiviewmodifyvalidatedelete"></span><span id="MSIVIEWMODIFYVALIDATEDELETE"></span><dl> <dt>**msiViewModifyValidateDelete**</dt> <dt>11</dt> </dl>    | Überprüft einen Datensatz, der später gelöscht wird. Zuerst muss die [**Fetch-Methode**](view-fetch.md) mit demselben Datensatz aufgerufen werden. Schlägt fehl, wenn eine andere Zeile auf die Primärschlüssel dieser Zeile verweist. Bei der Überprüfung wird nicht überprüft, ob die Primärschlüssel dieser Zeile in Eigenschaften oder Zeichenfolgen vorhanden sind. Überprüft nicht, ob eine Spalte ein Fremdschlüssel für mehrere Tabellen ist. Rufen Sie Validierungsfehler ab, indem Sie die [**GetError-Methode**](view-geterror.md) aufrufen. Funktioniert mit Lese-/Schreib- und schreibgeschützten Datensätzen. Dieser Modus kann nicht mit einer Ansicht verwendet werden, die Joins enthält.<br/> |



 

</dd> <dt>

*record* 
</dt> <dd>

Erforderlich. [**Datensatzobjekt,**](record-object.md) das von der [**Fetch-Methode**](view-fetch.md) mit geänderten Felddaten abgerufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode muss nach der [**Execute-Methode aufgerufen**](view-execute.md) werden.

Zum Ausführen einer SQL-Anweisung muss eine Sicht erstellt werden. Eine Sicht, die kein ResultSet erstellt, z. B. CREATE TABLE oder INSERT INTO, kann jedoch nicht mit der **Modify-Methode** verwendet werden, um Tabellen über die Sicht zu aktualisieren.

Die Werte msiViewModifyValidate, msiViewModifyValidateNew, msiViewModifyValidateField und msiViewModifyValidateDelete der **Modify-Methode** führen keine tatsächlichen Updates durch. Sie stellen sicher, dass die Daten im Datensatz gültig sind. Die Verwendung dieser Aktionen erfordert, dass die Datenbank eine [ \_ Validierungstabelle enthält.](-validation-table.md)

Sie können keinen Datensatz mit Binärdaten aus einer Datenbank abrufen und dann mit diesem Datensatz die Daten in eine völlig andere Datenbank einfügen. Um Binärdaten aus einer Datenbank in eine andere zu verschieben, sollten Sie die Daten in eine Datei exportieren und sie dann mithilfe der [**SetStream-Methode**](record-setstream.md) des [**Record-Objekts**](record-object.md) in die neue Datenbank importieren. Dadurch wird sichergestellt, dass jede Datenbank über eine eigene Kopie der Binärdaten verfügt.

> [!Note]  
> Benutzerdefinierte Aktionen können einer Datenbank nur temporäre Zeilen, Spalten oder Tabellen hinzufügen, ändern oder daraus entfernen. Benutzerdefinierte Aktionen können keine persistenten Daten in einer Datenbank ändern, z. B. Daten, die Teil der auf dem Datenträger gespeicherten Datenbank sind. Weitere Informationen finden Sie unter [Zugreifen auf die aktuelle Installersitzung aus einer benutzerdefinierten Aktion.](accessing-the-current-installer-session-from-inside-a-custom-action.md)

 

Wenn bei der Methode ein Fehler auftritt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView ist als \_ 000C109C-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                |



 

 




