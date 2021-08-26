---
description: Die Item-Eigenschaft ist eine schreibgeschützte Eigenschaft, die einen Datensatz in einer RecordList-Objektsammlung zurückgibt.
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: RecordList.Item-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7df19a26fd4e8464963f09ffdf227ac88f4376624a88df84d6245efa3c5fd927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041810"
---
# <a name="recordlistitem-property"></a>RecordList.Item-Eigenschaft

Die **Item-Eigenschaft** ist eine schreibgeschützte Eigenschaft, die einen Datensatz in einer [**RecordList-Objektsammlung**](recordlist-object.md) zurückgibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a>Eigenschaftswert

Indexnummer des Elements mit der Auflistung von Zeichenfolgen. Der Index ist erforderlich.

## <a name="remarks"></a>Hinweise

Der Client muss vor dem Verweisen auf die Item-Eigenschaft überprüfen, ob das [**RecordList-Objekt**](recordlist-object.md) vorhanden und nicht leer ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecordList ist als 000C1096-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                          |



 

 




