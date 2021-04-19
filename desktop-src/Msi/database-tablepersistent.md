---
description: Die tablepersistent-Eigenschaft des Database-Objekts gibt den persistenzstatus der Tabelle als einen der folgenden Parameter zurück.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Database. tablepersistent (Eigenschaft)
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
ms.openlocfilehash: 1a1e91e1c01ca3fe2efc45855583031e84dc2b47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372737"
---
# <a name="databasetablepersistent-property"></a>Database. tablepersistent (Eigenschaft)

Die **tablepersistent** -Eigenschaft des [**Database**](database-object.md) -Objekts gibt den persistenzstatus der Tabelle als einen der folgenden Parameter zurück.



| Tabellen Status               | Wert | BESCHREIBUNG                    |
|---------------------------|-------|--------------------------------|
| msievaluateconditionfalse | 0     | Die Tabelle ist temporär.            |
| msievaluateconditiontrue  | 1     | Die Tabelle ist persistent.           |
| msievaluateconditionnone  | 2     | Die Tabelle befindet sich nicht in der Datenbank.  |
| msievaluateconditionerror | 3     | Ungültiger oder fehlender Tabellenname. |



 

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




