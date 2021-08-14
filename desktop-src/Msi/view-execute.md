---
description: Die Execute-Methode des View-Objekts verwendet das Fragezeichentoken, um Parameter in einer SQL darstellen. Weitere Informationen finden Sie unter SQL Syntax. Die Werte dieser Parameter werden als entsprechende Felder eines Parameterdatensatz übergeben.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Execute-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Execute
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9bfd1120382ea06f6046f4435d0143024422ff6345959099326ab4a5428d26d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804028"
---
# <a name="viewexecute-method"></a>View.Execute-Methode

Die **Execute-Methode** des [**View-Objekts**](view-object.md) verwendet das Fragezeichentoken, um Parameter in einer SQL darstellen. Weitere Informationen finden Sie unter [SQL Syntax](sql-syntax.md). Die Werte dieser Parameter werden als entsprechende Felder eines Parameterdatensatz übergeben.

## <a name="syntax"></a>Syntax


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*record* 
</dt> <dd>

Optionale [**Datensatzobjekte,**](record-object.md) die die Werte enthalten, die die Parametertoken (?) in der SQL ersetzen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode muss aufgerufen werden, bevor die [**Fetch-Methode aufgerufen**](view-fetch.md) wird.

Wenn die SQL-Abfrage Werte mit Parametermarkierungen (?) angibt, muss ein Datensatz bereitgestellt werden, der alle Ersetzungswerte enthält, die in der gleichen Reihenfolge und vom gleichen Datentyp wie die Parametermarker sein müssen. Wenn diese Methode mit INSERT- und UPDATE-Abfragen verwendet wird, müssen die Fragezeichentoken allen nicht parametrisierten Werten voran stehen.

Diese Abfragen sind beispielsweise gültig:

UPDATE {table-list} SET {column}= ? , {column}= {constant}

INSERT INTO {table} ({column-list}) VALUES (?, {constant-list})

Diese Abfragen sind jedoch ungültig:

UPDATE {table-list} SET {column}= {constant}, {column}=?

INSERT INTO {table} ({column-list}) VALUES ({constant-list}, ? )

Wenn bei der Methode ein Fehler auftritt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView ist als \_ 000C109C-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                |



 

 




