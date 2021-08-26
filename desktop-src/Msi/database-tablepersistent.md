---
description: Die TablePersistent-Eigenschaft des Database-Objekts gibt den Persistenzzustand der Tabelle als einen der folgenden Parameter zurück.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Database.TablePersistent-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.TablePersistent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f5eaf32996adef39976ba9fbaf88834c339e27dbe13c4e7fbcd1928ac1973b9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129640"
---
# <a name="databasetablepersistent-property"></a>Database.TablePersistent-Eigenschaft

Die **TablePersistent-Eigenschaft** des [**Database-Objekts**](database-object.md) gibt den Persistenzzustand der Tabelle als einen der folgenden Parameter zurück.



| Tabellenzustand               | Wert | Beschreibung                    |
|---------------------------|-------|--------------------------------|
| msiEvaluateConditionFalse | 0     | Die Tabelle ist temporär.            |
| msiEvaluateConditionTrue  | 1     | Die Tabelle ist persistent.           |
| msiEvaluateConditionNone  | 2     | Die Tabelle befindet sich nicht in der Datenbank.  |
| msiEvaluateConditionError | 3     | Ungültiger oder fehlender Tabellenname. |



 

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase ist als 000C109D-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                            |



 

 




