---
description: Die Close-Methode des View-Objekts beendet die Abfrage Ausführung und gibt Datenbankressourcen frei.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: View. Close-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Close
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d0a0afbf078879f579eae15a9636a4a270799fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357703"
---
# <a name="viewclose-method"></a>View. Close-Methode

Die **Close** -Methode des [**View**](view-object.md) -Objekts beendet die Abfrage Ausführung und gibt Datenbankressourcen frei.

## <a name="syntax"></a>Syntax


```JScript
View.Close()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode muss aufgerufen werden, bevor die [**Execute**](view-execute.md) -Methode erneut für das [**View**](view-object.md) -Objekt aufgerufen wird, es sei denn, alle Zeilen des Resultsets wurden mit der [**Fetch**](view-fetch.md) -Methode abgerufen. Sie wird intern aufgerufen, wenn die Ansicht zerstört wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView ist definiert als 000c109c-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




