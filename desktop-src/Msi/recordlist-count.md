---
description: Die Count-Eigenschaft ist eine schreibgeschützte Eigenschaft, die die Anzahl der Elemente im RecordList-Objekt zurückgibt.
ms.assetid: df384d5c-931f-4a31-af55-d013f010e100
title: RecordList. Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Count
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 01d1ee815140b86acefd6d8fee10ca7827eba9ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360960"
---
# <a name="recordlistcount-property"></a>RecordList. Count-Eigenschaft

Die **count** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die die Anzahl der Elemente im [**RecordList**](recordlist-object.md) -Objekt zurückgibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = RecordList.Count
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Der Client muss überprüfen, ob das [**RecordList**](recordlist-object.md) -Objekt vorhanden und nicht leer ist, bevor auf die Count-Eigenschaft verwiesen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ irecordlist ist definiert als 000c1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




