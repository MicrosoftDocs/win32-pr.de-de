---
description: Die Export-Methode des Database-Objekts kopiert die Struktur und die Daten aus einer angegebenen Tabelle in eine Textarchivdatei.
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Database.Export-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Export
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: faa5e2459eb0fe4ba04fd548bc478c9a0e2c85267e1df8e3d318f4a3f6a082ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745610"
---
# <a name="databaseexport-method"></a>Database.Export-Methode

Die **Export-Methode** des [**Database-Objekts**](database-object.md) kopiert die Struktur und die Daten aus einer angegebenen Tabelle in eine [Textarchivdatei.](text-archive-files.md)

## <a name="syntax"></a>Syntax


```JScript
Database.Export(
  table,
  path,
  file
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tabelle* 
</dt> <dd>

Erforderlicher Name der Datenbanktabelle. Bei Verwendung der Installer-Datenbank wird die Groß-/Kleinschreibung beachtet.

</dd> <dt>

*path* 
</dt> <dd>

Erforderliche Zeichenfolge, die der Pfad zum Ordner ist, in dem die Textdatei gespeichert wird.

</dd> <dt>

*datei* 
</dt> <dd>

Erforderlicher Name der zu erstellenden Datei. Dies schließt den Ordner nicht ein, da dieser im Pfadobjekt festgelegt werden muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase ist als 000C109D-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                            |



 

 




