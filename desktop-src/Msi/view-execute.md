---
description: Die Execute-Methode des View-Objekts verwendet das Fragezeichen Token zum Darstellen von Parametern in einer SQL-Anweisung. Weitere Informationen finden Sie unter SQL-Syntax. Die Werte dieser Parameter werden als die entsprechenden Felder eines Parameterdaten Satzes übergeben.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Exeniedliche Methode
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
ms.openlocfilehash: 939d1aa5216085d701fb728ad5e5e9aa9e07e702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359223"
---
# <a name="viewexecute-method"></a>View.Exeniedliche Methode

Die **Execute** -Methode des [**View**](view-object.md) -Objekts verwendet das Fragezeichen Token zum Darstellen von Parametern in einer SQL-Anweisung. Weitere Informationen finden Sie unter [SQL-Syntax](sql-syntax.md). Die Werte dieser Parameter werden als die entsprechenden Felder eines Parameterdaten Satzes übergeben.

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

Optionale [**Datensatz**](record-object.md) -Objekte, die die Werte enthalten, die die Parameter Token (?) in der SQL-Abfrage ersetzen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode muss vor allen Aufrufen der [**Fetch**](view-fetch.md) -Methode aufgerufen werden.

Wenn die SQL-Abfrage Werte mit Parameter Markierungen (?) angibt, muss ein Datensatz angegeben werden, der alle Ersetzungs Werte enthält, die sich in der gleichen Reihenfolge und dem gleichen Datentyp wie die Parameter Markierungen befinden müssen. Wenn diese Methode mit INSERT-und Update-Abfragen verwendet wird, müssen die Fragezeichen Token allen nicht parametrisierten Werten vorangestellt sein.

Diese Abfragen sind z. b. gültig:

Aktualisieren von {Table-List} Set {Column} =? , {Column} = {Constant}

INSERT INTO {TABLE} ({Column-List})-Werte (?, {Constant-List})

Diese Abfragen sind jedoch ungültig:

Aktualisieren von {Table-List} Set {Column} = {Constant}, {Column} =?

INSERT INTO {TABLE} ({Column-List})-Werte ({Constant-List},? )

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView ist definiert als 000c109c-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




