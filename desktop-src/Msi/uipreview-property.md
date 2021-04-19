---
description: Die Property-Eigenschaft des uipreview-Objekts ist eine Lese-/Schreibeigenschaft, die den Zeichen folgen Wert einer benannten installereigenschaft darstellt, oder, wenn ein Prozentzeichen (%) als Präfix angegeben ist, der Wert einer System Umgebungsvariablen für den aktuellen Prozess.
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: Uipreview. Property (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 430c6f75b03fe69f8054bb2b0a61bab59dcc4d58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358079"
---
# <a name="uipreviewproperty-property"></a>Uipreview. Property (Eigenschaft)

Die **Property** -Eigenschaft des [**uipreview**](uipreview-object.md) -Objekts ist eine Lese-/Schreibeigenschaft, die den Zeichen folgen Wert einer benannten installereigenschaft darstellt, oder, wenn ein Prozentzeichen (%) als Präfix angegeben ist, der Wert einer System Umgebungsvariablen für den aktuellen Prozess. Dies ist verfügbar, um eine ordnungsgemäße Anzeige von Dialogfeldern zu ermöglichen, die von Eigenschafts Werten abhängig sind. Es können entweder Zeichen folgen Werte oder ganzzahlige Werte angegeben werden. Eine nicht vorhandene Eigenschaft oder Umgebungsvariable entspricht dem Wert NULL.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

Der Unterscheidung nach Groß-/Kleinschreibung oder der Name einer Umgebungsvariablen mit dem Präfix "Prozentzeichen (%)" ist erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iuipreview ist definiert als 000c109a-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




