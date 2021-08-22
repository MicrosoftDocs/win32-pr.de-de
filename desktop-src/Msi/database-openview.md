---
description: Die OpenView-Methode des Database-Objekts gibt ein View-Objekt zurück, das die von einer Zeichenfolge angegebene SQL darstellt.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Database.OpenView-Methode (Certview.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.OpenView
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ccc37b72dd44064172672d1067dae293da30048853f3ca83f82fb50b0a90cfaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947523"
---
# <a name="databaseopenview-method"></a>Database.OpenView-Methode

Die **OpenView-Methode** des [**Database-Objekts**](database-object.md) gibt ein [**View-Objekt**](view-object.md) zurück, das die von einer Zeichenfolge angegebene SQL darstellt.

## <a name="syntax"></a>Syntax


```JScript
Database.OpenView(
  sql
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sql* 
</dt> <dd>

Erforderlich SQL Abfragezeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Weitere Informationen zur SQL im Installationsprogramm implementierten Syntax finden Sie unter [SQL Syntax](sql-syntax.md).

Wenn bei der Methode ein Fehler auftritt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| Header<br/>  | <dl> <dt>Certview.h</dt> </dl>                                                                                                                                                                   |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IDatabase der IID ist als \_ 000C109D-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Datenbank**](database-object.md)
</dt> <dt>

[SQL-Syntax](sql-syntax.md)
</dt> </dl>

 

 




