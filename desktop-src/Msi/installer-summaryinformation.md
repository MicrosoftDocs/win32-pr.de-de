---
description: Die SummaryInformation-Eigenschaft des Installer-Objekts gibt ein SummaryInfo-Objekt zurück, das zum Untersuchen, Aktualisieren und Hinzufügen von Eigenschaften zum Zusammenfassungsinformationsstream eines Pakets oder einer Transformation verwendet werden kann.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Installer.SummaryInformation (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f671a5424e1008787443a13f2b72e75cb931da2f0783681c360a1b03ad640aff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043620"
---
# <a name="installersummaryinformation-property"></a>Installer.SummaryInformation (Eigenschaft)

Die **SummaryInformation-Eigenschaft** des [**Installer-Objekts**](installer-object.md) gibt ein [**SummaryInfo-Objekt**](summaryinfo-object.md) zurück, das zum Untersuchen, Aktualisieren und Hinzufügen von Eigenschaften zum Zusammenfassungsinformationsstream eines Pakets oder einer Transformation verwendet werden kann.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Wenn ein Wert *von maxProperties* größer als 0 verwendet wird, um einen vorhandenen Zusammenfassungsinformationsstream zu öffnen, muss die [**Persist-Methode**](summaryinfo-persist.md) aufgerufen werden, bevor das Objekt geschlossen wird. Wenn dies nicht der Fall ist, gehen die vorhandenen Datenstrominformationen verloren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



 

 




