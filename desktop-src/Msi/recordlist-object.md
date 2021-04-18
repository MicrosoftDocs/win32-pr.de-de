---
description: Das RecordList-Objekt ist eine Sammlung von Datensatz-Objekten. Sie müssen überprüfen, ob das RecordList-Objekt vorhanden und nicht leer ist, bevor Sie auf seine Eigenschaften verweisen.
ms.assetid: 7f5ac153-8da1-4dc8-9bb7-defd4e821142
title: RecordList-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3f09887333d8ddbf83de4bea2b2e654411883e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371674"
---
# <a name="recordlist-object"></a>RecordList-Objekt

Das **RecordList** -Objekt ist eine Sammlung von [**Datensatz**](record-object.md) -Objekten. Sie müssen überprüfen, ob das **RecordList** -Objekt vorhanden und nicht leer ist, bevor Sie auf seine Eigenschaften verweisen.

## <a name="members"></a>Member

Das **RecordList** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **RecordList** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                     | BESCHREIBUNG                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [**Countdown**](recordlist-count.md)<br/> | Gibt die Anzahl der Elemente im **RecordList** -Objekt zurück.<br/> |
| [**Element**](recordlist-item.md)<br/>   | Gibt einen Datensatz in einer **RecordList** -Objekt Auflistung zurück.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ irecordlist ist definiert als 000c1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Datensatz**](record-object.md)
</dt> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




