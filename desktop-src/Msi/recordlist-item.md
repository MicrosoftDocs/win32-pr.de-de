---
description: Die Item-Eigenschaft ist eine schreibgeschützte Eigenschaft, die einen Datensatz in einer RecordList-Objekt Auflistung zurückgibt.
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: RecordList. Item-Eigenschaft
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
ms.openlocfilehash: 4c7b9332393c4055cb8052b2b759b93781c0fd73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364739"
---
# <a name="recordlistitem-property"></a>RecordList. Item-Eigenschaft

Die **Item** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die einen Datensatz in einer [**RecordList**](recordlist-object.md) -Objekt Auflistung zurückgibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a>Eigenschaftswert

Index Nummer des Elements mit der Auflistung von Zeichen folgen. Der Index ist erforderlich.

## <a name="remarks"></a>Bemerkungen

Der Client muss überprüfen, ob das [**RecordList**](recordlist-object.md) -Objekt vorhanden und nicht leer ist, bevor auf die Item-Eigenschaft verwiesen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ irecordlist ist definiert als 000c1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




