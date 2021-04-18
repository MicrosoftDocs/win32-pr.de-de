---
description: Die Count-Eigenschaft ist eine schreibgeschützte Eigenschaft, die die Anzahl der Elemente im stringlist-Objekt zurückgibt.
ms.assetid: aa85b8d9-344d-4f31-aa86-9e6497c07751
title: Stringlist. Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Count
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b880b6d6c7c995c2aff1a40e7e4fcc6908eb7c58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354701"
---
# <a name="stringlistcount-property"></a>Stringlist. Count-Eigenschaft

Die **count** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die die Anzahl der Elemente im [**stringlist-Objekt**](stringlist-object.md)zurückgibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = StringList.Count
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Der Client muss überprüfen, ob das [**stringlist**](stringlist-object.md) -Objekt vorhanden und nicht leer ist, bevor auf die **count** -Eigenschaft verwiesen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ istringlist ist definiert als 000c1095-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




