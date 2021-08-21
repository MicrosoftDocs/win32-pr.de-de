---
description: Die Close-Methode des View-Objekts beendet die Abfrageausführung und gibt Datenbankressourcen frei.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: View.Close-Methode
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
ms.openlocfilehash: edbf2dd30902fa437fdd67d21efb86bb2edeabbd499f0f022501f166ad1b92a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498850"
---
# <a name="viewclose-method"></a>View.Close-Methode

Die **Close-Methode** des [**View-Objekts**](view-object.md) beendet die Abfrageausführung und gibt Datenbankressourcen frei.

## <a name="syntax"></a>Syntax


```JScript
View.Close()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode muss aufgerufen werden, bevor die [**Execute-Methode**](view-execute.md) erneut für das [**View-Objekt**](view-object.md) aufgerufen wird, es sei denn, alle Zeilen des ResultSets wurden mit der [**Fetch-Methode**](view-fetch.md) abgerufen. Sie wird intern aufgerufen, wenn die Ansicht zerstört wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView ist als \_ 000C109C-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                |



 

 




