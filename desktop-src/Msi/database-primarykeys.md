---
description: Die primarykeys-Eigenschaft des Database-Objekts gibt ein Datensatz-Objekt zurück, das den Tabellennamen in Feld 0 und die Spaltennamen (bestehend aus den primär Schlüsseln) in nachfolgenden Feldern enthält, die ihren Spalten Nummern entsprechen.
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: Database. primarykeys (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.PrimaryKeys
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dc266bc2e563e6f32b7ff9b8c7c8cb0df69b723d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364531"
---
# <a name="databaseprimarykeys-property"></a>Database. primarykeys (Eigenschaft)

Die **primarykeys** -Eigenschaft des [**Database**](database-object.md) -Objekts gibt ein [**Datensatz**](record-object.md) -Objekt zurück, das den Tabellennamen in Feld 0 und die Spaltennamen (bestehend aus den primär Schlüsseln) in nachfolgenden Feldern enthält, die ihren Spalten Nummern entsprechen. Die Feld Anzahl des Datensatzes entspricht der Anzahl von Primärschlüssel Spalten.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a>Eigenschaftswert

Erforderlicher Name einer vorhandenen Tabelle. Wenn die Tabelle nicht vorhanden ist, wird ein Fehler generiert.

## <a name="remarks"></a>Bemerkungen

Die **primarykeys** -Eigenschaft kann nicht mit der Tabellen [ \_ Tabelle](-tables-table.md) oder der [ \_ Spalten Tabelle](-columns-table.md)verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




