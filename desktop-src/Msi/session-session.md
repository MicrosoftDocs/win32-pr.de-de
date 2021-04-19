---
description: Die Property-Eigenschaft des Session-Objekts ist eine Lese-/Schreibeigenschaft, die den Zeichen folgen Wert einer benannten installereigenschaft darstellt, die vom Sitzungs Objekt verwaltet wird.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Session. Property (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9635d5b9ee093f270e4ee7993f78609d60caa13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367116"
---
# <a name="sessionproperty-property"></a>Session. Property (Eigenschaft)

Die **Property** -Eigenschaft des [**Session**](session-object.md) -Objekts ist eine Lese-/Schreibeigenschaft, die den Zeichen folgen Wert einer benannten installereigenschaft darstellt, die vom **Sitzungs** Objekt in der in-Memory-Eigenschaften Tabelle verwaltet wird, oder, wenn ein Prozentzeichen (%) als Präfix angegeben wird, der Wert einer System Umgebungsvariablen für den aktuellen Prozess. Es können entweder Zeichen folgen Werte oder ganzzahlige Werte angegeben werden. Eine nicht vorhandene Eigenschaft oder Umgebungsvariable entspricht dem Wert NULL.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

Der Unterscheidung nach Groß-/Kleinschreibung oder der Name einer Umgebungsvariablen mit dem Präfix "Prozentzeichen (%)" ist erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




