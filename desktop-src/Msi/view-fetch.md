---
description: Mit der FETCH-Methode des View-Objekts wird die nächste Zeile von Spaltendaten abgerufen, wenn im Resultset weitere Zeilen verfügbar sind; andernfalls ist es NULL. Rufen Sie die Execute-Methode vor der FETCH-Methode auf.
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: View. FETCH-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Fetch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16d3a14f3c4f54f64364488322007a99c0f7cd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365920"
---
# <a name="viewfetch-method"></a>View. FETCH-Methode

Mit der **Fetch** -Methode des [**View**](view-object.md) -Objekts wird die nächste Zeile von Spaltendaten abgerufen, wenn im Resultset weitere Zeilen verfügbar sind; andernfalls ist es NULL. Rufen Sie die [**Execute**](view-execute.md) -Methode vor der **Fetch** -Methode auf.

## <a name="syntax"></a>Syntax


```JScript
View.Fetch()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das gleiche [**Datensatz**](record-object.md) -Objekt sollte zum Abrufen der Daten in mehreren Zeilen verwendet werden. andernfalls sollte das Objekt freigegeben werden, indem der Gültigkeitsbereich verlassen wird. Der Datensatz kann für das Ende des Resultsets mithilfe der Syntax "if fetchrecord is Nothing" getestet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView ist definiert als 000c109c-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




