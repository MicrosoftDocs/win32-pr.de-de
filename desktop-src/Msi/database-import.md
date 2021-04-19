---
description: Mit der Import-Methode des Datenbankobjekts wird eine Datenbanktabelle aus einer Textarchiv Datei importiert, wobei alle vorhandenen Tabellen gelöscht werden.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Database. Import-Methode
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
ms.openlocfilehash: b931b77e6cf736bc291079532d20d9c6b48dd243
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370070"
---
# <a name="databaseimport-method"></a>Database. Import-Methode

Mit der **Import** -Methode des [**Daten Bank**](database-object.md) Objekts wird eine Datenbanktabelle aus einer [Textarchiv Datei](text-archive-files.md)importiert, wobei alle vorhandenen Tabellen gelöscht werden.

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

Der erforderliche Name der zu importierenden Datei. Dies schließt den Ordner nicht ein, da dieser im Path-Objekt festgelegt werden muss. Der Tabellenname wird in der Datei angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verbindung**](database-object.md)
</dt> <dt>

[**Msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




