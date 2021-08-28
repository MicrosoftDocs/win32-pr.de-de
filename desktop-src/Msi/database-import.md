---
description: Mit der Import-Methode des Database-Objekts wird eine Datenbanktabelle aus einer Textarchivdatei importiert, und vorhandene Tabellen werden gelöscht.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Database.Import-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Import
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 31bd306475460b03e9b4b5137cbd8fe214128dbec0dac516d2d9557de137a82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075030"
---
# <a name="databaseimport-method"></a>Database.Import-Methode

Die **Import-Methode** des [**Database-Objekts**](database-object.md) importiert eine Datenbanktabelle aus [Textarchivdateien](text-archive-files.md)und entfernt vorhandene Tabellen.

## <a name="syntax"></a>Syntax


```JScript
Database.Import(
  path,
  file
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*path* 
</dt> <dd>

Erforderlicher Ordner, in dem die Textdatei vorhanden ist.

</dd> <dt>

*datei* 
</dt> <dd>

Erforderlicher Name der zu importierenden Datei. Dies schließt den Ordner nicht ein, da dieser im Pfadobjekt festgelegt werden muss. Der Tabellenname wird in der Datei angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase ist als 000C109D-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Datenbank**](database-object.md)
</dt> <dt>

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




