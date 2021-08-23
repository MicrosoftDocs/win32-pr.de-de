---
description: Das View-Objekt stellt ein Resultset dar, das beim Verarbeiten einer Abfrage mithilfe der OpenView-Methode des Database-Objekts abgerufen wird.
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: View-Objekt
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
ms.openlocfilehash: f5025df952ce6e3c5ce43bf3dcb93748a241702b8c4e2f52cd9d0fd00103dc49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145273"
---
# <a name="view-object"></a>View-Objekt

Das **View-Objekt** stellt ein Resultset dar, das beim Verarbeiten einer Abfrage mithilfe der [**OpenView-Methode**](database-openview.md) des [**Database-Objekts**](database-object.md) abgerufen wird. Bevor Daten übertragen werden können, muss die Abfrage mit der [**Execute-Methode**](view-execute.md) ausgeführt werden, wobei alle ersetzbaren Parameter übergeben werden, die in der SQL Abfragezeichenfolge angegeben sind. Die Abfrage kann bei Bedarf erneut mit unterschiedlichen Parametern ausgeführt werden, aber erst nach dem Freigeben des Resultset, indem entweder alle Datensätze abgerufen oder die [**Close-Methode**](view-close.md) aufgerufen wird.

## <a name="members"></a>Member

Das **View-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **View-Objekt** verfügt über diese Methoden.



| Methode                            | Beschreibung                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Schließen**](view-close.md)       | Beendet die Abfrageausführung und gibt Datenbankressourcen frei.<br/>                                                                                                          |
| [**Ausführen**](view-execute.md)   | Verwendet das Fragezeichentoken, um Parameter in einer SQL Abfrage darzustellen. Die Werte dieser Parameter werden als die entsprechenden Felder eines Parameterdatensatzes übergeben.<br/> |
| [**Holen**](view-fetch.md)       | Gibt ein [**Record-Objekt**](record-object.md) zurück, das die angeforderten Spaltendaten enthält, wenn mehr Zeilen im Resultset verfügbar sind, andernfalls WIRD NULL zurückgegeben.<br/>      |
| [**GetError**](view-geterror.md) | Gibt den Validierungsfehler und den Spaltennamen zurück, für die der Fehler aufgetreten ist.<br/>                                                                                           |
| [**Ändern**](view-modify.md)     | Ändert eine Datenbankzeile mit einem geänderten [**Record-Objekt,**](record-object.md) das von der [**Fetch-Methode**](view-fetch.md) abgerufen wurde.<br/>                                   |



 

### <a name="properties"></a>Eigenschaften

Das **View-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                         | Beschreibung                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**Columninfo**](view-columninfo.md)<br/> | Gibt ein [**Record-Objekt**](record-object.md) zurück, das die angeforderten Informationen zu jeder Spalte im Resultset enthält.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView ist als 000C109C-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Windows Beispiele für Skripterstellung für Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




