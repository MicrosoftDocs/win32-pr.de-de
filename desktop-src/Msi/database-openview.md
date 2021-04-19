---
description: Die OpenView-Methode des Database-Objekts gibt ein Ansichts Objekt zurück, das die durch eine SQL-Zeichenfolge angegebene Abfrage darstellt.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Database. OpenView-Methode (certview. h)
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
ms.openlocfilehash: 8dc62ca38bfe28980da71ecf63eda8e6c39aaf0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359810"
---
# <a name="databaseopenview-method"></a>Database. OpenView-Methode

Die **OpenView** -Methode des [**Database**](database-object.md) -Objekts gibt ein [**Ansichts**](view-object.md) Objekt zurück, das die durch eine SQL-Zeichenfolge angegebene Abfrage darstellt.

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

Erforderliche SQL-Abfrage Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Informationen zur SQL-Syntax, die im Installer implementiert ist, finden Sie unter [SQL-Syntax](sql-syntax.md).

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| Header<br/>  | <dl> <dt>Certview. h</dt> </dl>                                                                                                                                                                   |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verbindung**](database-object.md)
</dt> <dt>

[SQL-Syntax](sql-syntax.md)
</dt> </dl>

 

 




