---
description: Das View-Objekt stellt ein Resultset dar, das bei der Verarbeitung einer Abfrage mit der OpenView-Methode des Datenbankobjekts abgerufen wurde.
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: Objekt anzeigen
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c26cfa3c4873913d70fca63537f1d25532648a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371164"
---
# <a name="view-object"></a>Objekt anzeigen

Das **View** -Objekt stellt ein Resultset dar, das bei der Verarbeitung einer Abfrage mit der [**OpenView**](database-openview.md) -Methode des [**Daten Bank**](database-object.md) Objekts abgerufen wurde. Bevor Daten übertragen werden können, muss die Abfrage mit der [**Execute**](view-execute.md) -Methode ausgeführt werden, wobei alle ersetzbaren Parameter, die in der SQL-Abfrage Zeichenfolge festgelegt sind, übergeben werden. Die Abfrage wird möglicherweise erneut ausgeführt, mit unterschiedlichen Parametern, wenn erforderlich, aber erst nach der Freigabe des Resultsets, indem alle Datensätze abgerufen oder die [**Close**](view-close.md) -Methode aufgerufen wird.

## <a name="members"></a>Member

Das **Ansichts** Objekt enthält die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **View** -Objekt verfügt über diese Methoden.



| Methode                            | BESCHREIBUNG                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Schließen**](view-close.md)       | Beendet die Abfrage Ausführung und gibt Datenbankressourcen frei.<br/>                                                                                                          |
| [**Auszuführen**](view-execute.md)   | Verwendet das Fragezeichen Token, um Parameter in einer SQL-Abfrage darzustellen. Die Werte dieser Parameter werden als die entsprechenden Felder eines Parameterdaten Satzes übergeben.<br/> |
| [**Fetti**](view-fetch.md)       | Gibt ein Daten Satz Objekt zurück, das die angeforderten Spaltendaten enthält, wenn weitere Zeilen im Resultset verfügbar sind. andernfalls wird NULL zurück [**gegeben**](record-object.md) .<br/>      |
| [**GetError**](view-geterror.md) | Gibt den Validierungs Fehler und den Spaltennamen zurück, für den der Fehler aufgetreten ist.<br/>                                                                                           |
| [**Ändern**](view-modify.md)     | Ändert eine Datenbankzeile mit einem geänderten [**Daten Satz**](record-object.md) Objekt, das von der [**Fetch**](view-fetch.md) -Methode abgerufen wird.<br/>                                   |



 

### <a name="properties"></a>Eigenschaften

Das **Ansichts** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                         | BESCHREIBUNG                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**ColumnInfo**](view-columninfo.md)<br/> | Gibt ein [**Daten Satz**](record-object.md) Objekt zurück, das die angeforderten Informationen zu jeder Spalte im Resultset enthält.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView ist definiert als 000c109c-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




