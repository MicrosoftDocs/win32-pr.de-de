---
description: Die Commit-Methode des Database-Objekts finalisiert die persistente Form der Datenbank.
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Database.Commit-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Commit
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 049dec8c4d0531240d1244efb5bb7e1f0a3a337f51498d39ae09bcd6cf31c374
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044870"
---
# <a name="databasecommit-method"></a>Database.Commit-Methode

Die **Commit-Methode** des [**Database-Objekts**](database-object.md) finalisiert die persistente Form der Datenbank. Alle persistenten Daten werden in die beschreibbare Datenbank geschrieben, und es werden keine temporären Spalten oder Zeilen geschrieben. Diese Methode hat keine Auswirkungen auf eine Datenbank, die als schreibgeschützt geöffnet ist. Diese Methode kann mehrmals aufgerufen werden, um den aktuellen Zustand von Tabellen zu speichern, die in den Arbeitsspeicher geladen werden. Wenn die Datenbank schließlich geschlossen wird, wird für alle Änderungen, die nach dem letzten **Commit** vorgenommen wurden, ein Rollback ausgeführt. Diese Methode wird normalerweise vor dem Herunterfahren aufgerufen, wenn alle Datenbankänderungen abgeschlossen wurden.

## <a name="syntax"></a>Syntax


```JScript
Database.Commit()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase ist als 000C109D-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                            |



 

 




