---
description: Die Count-Eigenschaft ist eine schreibgeschützte Eigenschaft, die die Anzahl der Elemente im RecordList-Objekt zurückgibt.
ms.assetid: df384d5c-931f-4a31-af55-d013f010e100
title: RecordList.Count-Eigenschaft
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
ms.openlocfilehash: 06ee66668fc22ef8888c3be3bdccfff404b9c8bf0a2eb0498919de6c934a005c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519400"
---
# <a name="recordlistcount-property"></a>RecordList.Count-Eigenschaft

Die **Count-Eigenschaft** ist eine schreibgeschützte Eigenschaft, die die Anzahl der Elemente im [**RecordList-Objekt**](recordlist-object.md) zurückgibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = RecordList.Count
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Der Client muss überprüfen, ob das [**RecordList-Objekt**](recordlist-object.md) vorhanden und nicht leer ist, bevor er auf die Count-Eigenschaft verweist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecordList ist als 000C1096-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                          |



 

 




