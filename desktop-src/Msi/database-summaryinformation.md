---
description: Die SummaryInformation-Eigenschaft des Database-Objekts gibt ein SummaryInfo-Objekt zurück, das zum Überprüfen, aktualisieren und Hinzufügen von Eigenschaften zum Zusammenfassungs Informationsdaten Strom verwendet werden kann.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Database. SummaryInformation (Eigenschaft)
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
ms.openlocfilehash: 524c4fa2fe5014436f122f0a5460aced820e30ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367183"
---
# <a name="databasesummaryinformation-property"></a>Database. SummaryInformation (Eigenschaft)

Die **SummaryInformation** -Eigenschaft des [**Database**](database-object.md) -Objekts gibt ein [**SummaryInfo**](summaryinfo-object.md) -Objekt zurück, das zum Überprüfen, aktualisieren und Hinzufügen von Eigenschaften zum [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md)verwendet werden kann.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a>Eigenschaftswert

Die maximale Anzahl von Eigenschaften, die hinzugefügt oder geändert werden sollen. Dieser Parameter ist erforderlich und wird verwendet, um während der Datenstrom Generierung ausreichend Arbeitsspeicher zuzuordnen. Es ist nicht erforderlich, diese Anzahl von Eigenschaften zu speichern. Wenn die Datenbank schreibgeschützt geöffnet ist, muss der Wert 0 (null) verwendet werden, um zu verhindern, dass der Stream aktualisiert wird.

## <a name="remarks"></a>Bemerkungen

Wenn ein Wert von *maxproperties* größer als 0 verwendet wird, um einen vorhandenen Zusammenfassungs Informationsdaten Strom zu öffnen, muss die persistente [**Methode vor dem Schließen**](summaryinfo-persist.md) des Objekts aufgerufen werden. Wenn dies nicht der Fall ist, gehen die vorhandenen Datenstrom Informationen verloren.

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




