---
description: Die SummaryInformation-Eigenschaft des Database-Objekts gibt ein SummaryInfo-Objekt zurück, das zum Untersuchen, Aktualisieren und Hinzufügen von Eigenschaften zum Zusammenfassungsinformationsstream verwendet werden kann.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Database.SummaryInformation (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cf181b35457b8f4be5737bfa31cf284d86ed21f48800dcab6044cef444a5b640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947577"
---
# <a name="databasesummaryinformation-property"></a>Database.SummaryInformation (Eigenschaft)

Die **SummaryInformation-Eigenschaft** des [**Database-Objekts**](database-object.md) gibt ein [**SummaryInfo-Objekt**](summaryinfo-object.md) zurück, das zum Untersuchen, Aktualisieren und Hinzufügen von Eigenschaften zum Zusammenfassungsinformationsstream [verwendet werden kann.](summary-information-stream.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a>Eigenschaftswert

Die maximale Anzahl von Eigenschaften, die hinzugefügt oder geändert werden sollen. Dieser Parameter ist erforderlich und wird verwendet, um während der Streamgenerierung ausreichend Arbeitsarbeitsspeicher zu reservieren. Diese Anzahl von Eigenschaften muss nicht gespeichert werden. Der Wert 0 muss verwendet werden, wenn die Datenbank schreibgeschützt geöffnet ist, um zu verhindern, dass der Stream aktualisiert wird.

## <a name="remarks"></a>Hinweise

Wenn ein Wert *von maxProperties* größer als 0 verwendet wird, um einen vorhandenen Zusammenfassungsinformationsstream zu öffnen, muss die [**Persist-Methode**](summaryinfo-persist.md) aufgerufen werden, bevor das Objekt geschlossen wird. Wenn dies nicht der Fall ist, gehen die vorhandenen Datenstrominformationen verloren.

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IDatabase der IID ist als \_ 000C109D-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                            |



 

 




