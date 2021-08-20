---
description: Die Item-Eigenschaft ist eine schreibgeschützte Eigenschaft, die eine Zeichenfolge in der StringList-Objektauflistung zurückgibt.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: StringList.Item-Eigenschaft
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
ms.openlocfilehash: 85962aac5e841c929518a7a37fdada647ce4c74baa69be23048f26f5470c91fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142018"
---
# <a name="stringlistitem-property"></a>StringList.Item-Eigenschaft

Die **Item-Eigenschaft** ist eine schreibgeschützte Eigenschaft, die eine Zeichenfolge in der [**StringList Object-Auflistung**](stringlist-object.md) zurückgibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a>Eigenschaftswert

Indexnummer des Elements mit der Auflistung von Zeichenfolgen. Dieser Parameter ist erforderlich.

## <a name="remarks"></a>Hinweise

Der Client muss überprüfen, ob das [**StringList-Objekt**](stringlist-object.md) vorhanden und nicht leer ist, bevor er auf die **Item-Eigenschaft** verweist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IStringList ist als 000C1095-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                          |



 

 




