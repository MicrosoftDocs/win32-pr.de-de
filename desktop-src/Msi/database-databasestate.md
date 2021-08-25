---
description: Die DatabaseState-Eigenschaft des Database-Objekts ist eine schreibgeschützte Eigenschaft.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Database.DatabaseState-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.DatabaseState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a44fcc9e082878077533edafcd44c9f5a5f26e76bddd3ddb5619fb2842ec0d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745640"
---
# <a name="databasedatabasestate-property"></a>Database.DatabaseState-Eigenschaft

Die **DatabaseState-Eigenschaft** des [**Database-Objekts**](database-object.md) ist eine schreibgeschützte Eigenschaft.

Diese Eigenschaft gibt den Persistenzzustand der Datenbank als einen der folgenden Parameter zurück.



| Datenbankstatus        | Wert | Beschreibung                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| msiDatabaseStateRead  | 0     | Die Datenbank wird als schreibgeschützt geöffnet. Änderungen an persistenten Daten sind nicht zulässig, und temporäre Daten werden nicht gespeichert. |
| msiDatabaseStateWrite | 1     | Die Datenbank ist für Lese- und Schreibzugriff vollständig funktionsfähig.                                                          |



 

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Database.DatabaseState
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase ist als 000C109D-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                            |



 

 




