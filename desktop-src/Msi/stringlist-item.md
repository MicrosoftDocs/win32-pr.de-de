---
description: Die Item-Eigenschaft ist eine schreibgeschützte Eigenschaft, die eine Zeichenfolge in der stringlist-Objekt Auflistung zurückgibt.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: Stringlist. Item-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ebd32af433fd932cb05d062fbc515a3245113343
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359694"
---
# <a name="stringlistitem-property"></a>Stringlist. Item-Eigenschaft

Die **Item** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die eine Zeichenfolge in der [**stringlist-Objekt Auflistung**](stringlist-object.md) zurückgibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a>Eigenschaftswert

Index Nummer des Elements mit der Auflistung von Zeichen folgen. Dieser Parameter ist erforderlich.

## <a name="remarks"></a>Bemerkungen

Der Client muss überprüfen, ob das [**stringlist-Objekt**](stringlist-object.md) vorhanden und nicht leer ist, bevor auf die **Item** -Eigenschaft verwiesen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ istringlist ist definiert als 000c1095-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




