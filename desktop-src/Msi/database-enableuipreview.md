---
description: Die EnableUIPreview-Methode des Database-Objekts erleichtert die Erstellung von Dialogfeldern und Feldern, indem sie die Unterstützung bietet, die zum Anzeigen von In der Installer-Datenbank gespeicherten Benutzeroberflächendialogfeldern erforderlich ist.
ms.assetid: c4687de7-8ab4-4377-ac5c-1fed7c915519
title: Database.EnableUIPreview-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.EnableUIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7631b1d2d6becffcfcec7078c58dbe9469827beefea07b80dbb04a1295119fe6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745720"
---
# <a name="databaseenableuipreview-method"></a>Database.EnableUIPreview-Methode

Die **EnableUIPreview-Methode** des [**Database-Objekts**](database-object.md) erleichtert die Erstellung von Dialogfeldern und Feldern, indem sie die Unterstützung bietet, die zum Anzeigen von In der Installer-Datenbank gespeicherten Benutzeroberflächendialogfeldern erforderlich ist. Die -Methode startet den Vorschaumodus, indem sie ein **Datenbank-Vorschauobjekt** zurücksendet. Der Vorschaumodus endet, wenn das Vorschauobjekt freigegeben wird.

## <a name="syntax"></a>Syntax


```JScript
Database.EnableUIPreview()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IDatabase der IID ist als \_ 000C109D-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                            |



 

 




