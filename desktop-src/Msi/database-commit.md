---
description: Die Commit-Methode des Datenbankobjekts schließt die persistente Form der Datenbank ab.
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Database. Commit-Methode
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
ms.openlocfilehash: d62c998a70e0a4a036695be10b2bf1d983044241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371277"
---
# <a name="databasecommit-method"></a>Database. Commit-Methode

Die **Commit** -Methode des [**Daten Bank**](database-object.md) Objekts schließt die persistente Form der Datenbank ab. Alle persistenten Daten werden in die beschreibbare Datenbank geschrieben, und es werden keine temporären Spalten oder Zeilen geschrieben. Diese Methode hat keine Auswirkungen auf eine Datenbank, die als schreibgeschützt geöffnet ist. Diese Methode kann mehrmals aufgerufen werden, um den aktuellen Status von Tabellen zu speichern, die in den Arbeitsspeicher geladen werden. Wenn die Datenbank schließlich geschlossen wird, wird für alle Änderungen, die nach dem letzten **Commit** vorgenommen werden, ein Rollback ausgeführt. Diese Methode wird normalerweise vor dem Herunterfahren aufgerufen, wenn alle Daten Bank Änderungen abgeschlossen wurden.

## <a name="syntax"></a>Syntax


```JScript
Database.Commit()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




