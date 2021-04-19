---
description: Die SummaryInformation-Eigenschaft des Installer-Objekts gibt ein SummaryInfo-Objekt zurück, das zum Überprüfen, aktualisieren und Hinzufügen von Eigenschaften zum Zusammenfassungs Informationsdaten Strom eines Pakets oder einer Transformation verwendet werden kann.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Installer. SummaryInformation (Eigenschaft)
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
ms.openlocfilehash: 1ee593ca2ffebf3ca5574a8e2a6547b9cd81be40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368307"
---
# <a name="installersummaryinformation-property"></a>Installer. SummaryInformation (Eigenschaft)

Die **SummaryInformation** -Eigenschaft des [**Installer**](installer-object.md) -Objekts gibt ein [**SummaryInfo**](summaryinfo-object.md) -Objekt zurück, das zum Überprüfen, aktualisieren und Hinzufügen von Eigenschaften zum Zusammenfassungs Informationsdaten Strom eines Pakets oder einer Transformation verwendet werden kann.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Wenn ein Wert von *maxproperties* größer als 0 verwendet wird, um einen vorhandenen Zusammenfassungs Informationsdaten Strom zu öffnen, muss die persistente [**Methode vor dem Schließen**](summaryinfo-persist.md) des Objekts aufgerufen werden. Wenn dies nicht der Fall ist, verlieren Sie die vorhandenen Datenstrom Informationen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




