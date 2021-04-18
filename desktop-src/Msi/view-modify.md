---
description: Die Modify-Methode des View-Objekts ändert eine Datenbankzeile mit einem geänderten Daten Satz Objekt, das von der FETCH-Methode abgerufen wird.
ms.assetid: c3c500aa-070f-41d7-90f7-db979452d24f
title: View. Modify-Methode
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
ms.openlocfilehash: b4dc97f2e3b5f85d472cfcbfad6017ce4e051e4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371189"
---
# <a name="viewmodify-method"></a>View. Modify-Methode

Die **Modify** -Methode des [**View**](view-object.md) -Objekts ändert eine Datenbankzeile mit einem geänderten [**Daten Satz**](record-object.md) Objekt, das von der [**Fetch**](view-fetch.md) -Methode abgerufen wird.

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

Erforderliche Aktion, die für die Datenbankzeile ausgeführt werden soll. Diese Aktion ist einer der in der folgenden Tabelle dargestellten.



| Name der Aktion                                                                                                                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiViewModifySeek"></span><span id="msiviewmodifyseek"></span><span id="MSIVIEWMODIFYSEEK"></span><dl> <dt>**msiviewmodifyseek**</dt> <dt>– 1</dt> </dl>                                            | Aktualisiert die Informationen im angegebenen Datensatz, ohne die Position im Resultset zu ändern, ohne dass nachfolgende Abruf Vorgänge beeinträchtigt werden. Der Datensatz kann dann für nachfolgende Updates, Lösch-und Aktualisierungs Vorgang verwendet werden. Alle Primärschlüssel Spalten der Tabelle müssen in der Abfrage enthalten sein, und der Datensatz muss mindestens so viele Felder enthalten wie die Abfrage. Seek kann nicht mit Multitable-Abfragen verwendet werden. Siehe Hinweise. Dieser Modus kann nicht mit einer Sicht verwendet werden, die Joins enthält.<br/>                                                                             |
| <span id="msiViewModifyRefresh"></span><span id="msiviewmodifyrefresh"></span><span id="MSIVIEWMODIFYREFRESH"></span><dl> <dt>**msiviewmodifyrefresh**</dt> <dt>0</dt> </dl>                                 | Aktualisiert die Informationen im Datensatz. Muss zuerst die [**Fetch**](view-fetch.md) -Methode mit demselben Datensatz aufzurufen. Schlägt für eine gelöschte Zeile fehl. Funktioniert sowohl mit Lese-als auch mit schreibgeschützten Datensätzen.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyInsert"></span><span id="msiviewmodifyinsert"></span><span id="MSIVIEWMODIFYINSERT"></span><dl> <dt>**msiviewmodifyinsert**</dt> <dt>1</dt> </dl>                                     | Fügt einen Datensatz ein. Schlägt fehl, wenn eine Zeile mit denselben primär Schlüsseln vorhanden ist. Schlägt mit einer schreibgeschützten Datenbank fehl. Dieser Modus kann nicht mit einer Sicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="msiViewModifyUpdate"></span><span id="msiviewmodifyupdate"></span><span id="MSIVIEWMODIFYUPDATE"></span><dl> <dt>**msiviewmodifyupdate**</dt> <dt>2</dt> </dl>                                     | Aktualisiert einen vorhandenen Datensatz. Nur nicht-Primärschlüssel. Muss zuerst die [**Fetch**](view-fetch.md) -Methode mit demselben Datensatz aufzurufen. Schlägt mit einem gelöschten Datensatz fehl. Funktioniert nur mit Lese-/Schreibdaten Sätzen.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyAssign"></span><span id="msiviewmodifyassign"></span><span id="MSIVIEWMODIFYASSIGN"></span><dl> <dt>**msiviewmodif yassign**</dt> <dt>3</dt> </dl>                                     | Schreibt aktuelle Daten im Cursor in eine Tabellenzeile. Aktualisiert einen Datensatz, wenn die Primärschlüssel einer vorhandenen Zeile entsprechen und eingefügt werden, wenn Sie nicht identisch sind. Schlägt mit einer schreibgeschützten Datenbank fehl. Dieser Modus kann nicht mit einer Sicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiViewModifyReplace"></span><span id="msiviewmodifyreplace"></span><span id="MSIVIEWMODIFYREPLACE"></span><dl> <dt>**msiviewmodifyreplace**</dt> <dt>4</dt> </dl>                                 | Aktualisiert oder löscht einen Datensatz und fügt ihn in eine Tabelle ein. Muss zuerst die [**Fetch**](view-fetch.md) -Methode mit demselben Datensatz aufzurufen. Aktualisiert einen Datensatz, wenn die Primärschlüssel unverändert sind. Löscht die alte Zeile und fügt neu ein, wenn die Primärschlüssel geändert wurden. Schlägt mit einer schreibgeschützten Datenbank fehl. Dieser Modus kann nicht mit einer Sicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                           |
| <span id="msiViewModifyMerge"></span><span id="msiviewmodifymerge"></span><span id="MSIVIEWMODIFYMERGE"></span><dl> <dt>**msiviewmodifymerge**</dt> <dt>5</dt> </dl>                                         | Fügt einen Datensatz in einer Tabelle ein oder überprüft diesen. Wird eingefügt, wenn Primärschlüssel keiner Zeile entsprechen und überprüft wird, ob eine Entsprechung vorliegt. Schlägt fehl, wenn der Datensatz nicht mit den Daten in der Tabelle identisch ist. Schlägt fehl, wenn ein Datensatz mit einem doppelten Schlüssel vorhanden ist, der nicht identisch ist. Funktioniert nur mit Lese-/Schreibdaten Sätzen. Dieser Modus kann nicht mit einer Sicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                |
| <span id="msiViewModifyDelete"></span><span id="msiviewmodifydelete"></span><span id="MSIVIEWMODIFYDELETE"></span><dl> <dt>**msiviewmodifydelete**</dt> <dt>6</dt> </dl>                                     | Entfernt eine Zeile aus der Tabelle. Muss zuerst die [**Fetch**](view-fetch.md) -Methode mit demselben Datensatz aufzurufen. Schlägt fehl, wenn die Zeile gelöscht wurde. Funktioniert nur mit Lese-/Schreibdaten Sätzen. Dieser Modus kann nicht mit einer Sicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyInsertTemporary"></span><span id="msiviewmodifyinserttemporary"></span><span id="MSIVIEWMODIFYINSERTTEMPORARY"></span><dl> <dt>**msiviewmodifyinserttemporary**</dt> <dt>7</dt> </dl> | Fügt einen temporären Datensatz ein. Die Informationen sind nicht persistent. Schlägt fehl, wenn eine Zeile mit demselben Primärschlüssel vorhanden ist. Funktioniert nur mit Lese-/Schreibdaten Sätzen. Dieser Modus kann nicht mit einer Sicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                                                                                                                                                           |
| <span id="msiViewModifyValidate"></span><span id="msiviewmodifyvalidate"></span><span id="MSIVIEWMODIFYVALIDATE"></span><dl> <dt>**msiviewmodifyvalidate**</dt> <dt>8</dt> </dl>                             | Überprüft einen Datensatz. Wird nicht zwischen Joins überprüft. Muss zuerst die [**Fetch**](view-fetch.md) -Methode mit demselben Datensatz aufzurufen. Abrufen von Validierungs Fehlern mit der [**getError**](view-geterror.md) -Methode. Funktioniert mit Lese-/Schreib-und schreibgeschützten Datensätzen. Dieser Modus kann nicht mit einer Sicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                                                         |
| <span id="msiViewModifyValidateNew"></span><span id="msiviewmodifyvalidatenew"></span><span id="MSIVIEWMODIFYVALIDATENEW"></span><dl> <dt>**msiviewmodifyvalidatenew**</dt> <dt>9</dt> </dl>                 | Überprüft einen neuen Datensatz. Wird nicht zwischen Joins überprüft. Prüft, ob doppelte Schlüssel vorhanden sind. Ruft Validierungs Fehler durch Aufrufen der [**getError**](view-geterror.md) -Methode ab. Erfordert den Aufruf der [**msidatabase. OpenView**](database-openview.md) -Methode mit einem Modify-Wert. Funktioniert mit Lese-/Schreib-und schreibgeschützten Datensätzen. Dieser Modus kann nicht mit einer Sicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                 |
| <span id="msiViewModifyValidateField"></span><span id="msiviewmodifyvalidatefield"></span><span id="MSIVIEWMODIFYVALIDATEFIELD"></span><dl> <dt>**msiviewmodifyvalidatefield**</dt> <dt>10</dt> </dl>        | Überprüft Felder eines abgerufenen oder neuen Datensatzes. Kann ein oder mehrere Felder eines unvollständigen Datensatzes überprüfen. Ruft Validierungs Fehler durch Aufrufen der [**getError**](view-geterror.md) -Methode ab. Funktioniert mit Lese-/Schreib-und schreibgeschützten Datensätzen. Dieser Modus kann nicht mit einer Sicht verwendet werden, die Joins enthält.<br/>                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyValidateDelete"></span><span id="msiviewmodifyvalidatedelete"></span><span id="MSIVIEWMODIFYVALIDATEDELETE"></span><dl> <dt>**msiviewmodifyvalidatedelete**</dt> <dt>11</dt> </dl>    | Überprüft einen Datensatz, der später gelöscht wird. Muss zuerst die [**Fetch**](view-fetch.md) -Methode mit demselben Datensatz aufzurufen. Schlägt fehl, wenn eine andere Zeile auf die Primärschlüssel dieser Zeile verweist. Bei der Überprüfung wird nicht überprüft, ob die Primärschlüssel dieser Zeile in Eigenschaften oder Zeichen folgen vorhanden sind. Überprüft nicht, ob es sich bei einer Spalte um einen Fremdschlüssel für mehrere Tabellen handelt. Abrufen von Validierungs Fehlern durch Aufrufen der [**getError**](view-geterror.md) -Methode. Funktioniert mit Lese-/Schreib-und schreibgeschützten Datensätzen. Dieser Modus kann nicht mit einer Sicht verwendet werden, die Joins enthält.<br/> |



 

</dd> <dt>

*record* 
</dt> <dd>

Erforderlich. Daten [**Satz**](record-object.md) Objekt, das von der [**Fetch**](view-fetch.md) -Methode mit geänderten Felddaten abgerufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode muss nach der [**Execute**](view-execute.md) -Methode aufgerufen werden.

Zum Ausführen einer SQL-Anweisung muss eine Sicht erstellt werden. Eine Sicht, die kein Resultset erstellt (z. b. CREATE TABLE oder INSERT INTO), kann jedoch nicht mit der **Modify** -Methode verwendet werden, um Tabellen in der Sicht zu aktualisieren.

Die Werte "msiviewmodifyvalidate", "msiviewmodifyvalidatenew", "msiviewmodifyvalidatefield" und "msiviewmodifyvalidatedelete" der **Modify** -Methode führen keine tatsächlichen Updates aus. Sie stellen sicher, dass die Daten im Datensatz gültig sind. Die Verwendung dieser Aktionen erfordert, dass die Datenbank eine [ \_ Validierungs Tabelle](-validation-table.md) enthält.

Sie können einen Datensatz, der Binärdaten enthält, nicht aus einer Datenbank abrufen und diesen Datensatz dann verwenden, um die Daten in eine vollständig andere Datenbank einzufügen. Wenn Sie Binärdaten aus einer Datenbank in eine andere verschieben möchten, sollten Sie die Daten in eine Datei exportieren und dann mithilfe der [**setStream**](record-setstream.md) -Methode des [**Datensatz**](record-object.md) -Objekts in die neue Datenbank importieren. Dadurch wird sichergestellt, dass jede Datenbank über eine eigene Kopie der Binärdaten verfügt.

> [!Note]  
> Benutzerdefinierte Aktionen können nur temporäre Zeilen, Spalten oder Tabellen aus einer Datenbank hinzufügen, ändern oder entfernen. Benutzerdefinierte Aktionen können keine persistenten Daten in einer Datenbank ändern, z. b. Daten, die Teil der auf dem Datenträger gespeicherten Datenbank sind. Weitere Informationen finden Sie unter [zugreifen auf die aktuelle Installer-Sitzung von innerhalb einer benutzerdefinierten Aktion](accessing-the-current-installer-session-from-inside-a-custom-action.md).

 

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView ist definiert als 000c109c-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




