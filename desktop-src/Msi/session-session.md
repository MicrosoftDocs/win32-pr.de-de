---
description: Die Property-Eigenschaft des Session-Objekts ist eine Lese-/Schreibeigenschaft, die den Zeichenfolgenwert einer benannten Installereigenschaft darstellt, wie er vom Session-Objekt verwaltet wird.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Session.Property-Eigenschaft
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
ms.openlocfilehash: 7f47efd603f10378e6cf5b09144d57776a42cd515f3bd6194174d94bc2583514
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628830"
---
# <a name="sessionproperty-property"></a>Session.Property-Eigenschaft

Die **Property-Eigenschaft** des [**Session-Objekts**](session-object.md) ist eine Eigenschaft mit Lese-/Schreibzugriff, die den Zeichenfolgenwert einer benannten Installereigenschaft darstellt, wie er vom **Session-Objekt** in der Eigenschaftstabelle im Arbeitsspeicher verwaltet wird, oder, wenn ihm ein Prozentzeichen (%) vorangestellt ist, der Wert einer Systemumgebungsvariablen für den aktuellen Prozess. Es können entweder Zeichenfolgen- oder ganzzahlige Werte angegeben werden. Eine nicht vorhandene Eigenschaft oder Umgebungsvariable entspricht dem Wert NULL.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

Erforderlicher Name einer Eigenschaft, bei dem die Groß-/Kleinschreibung beachtet wird, oder ein Name, bei dem die Groß-/Kleinschreibung nicht beachtet wird, einer Umgebungsvariablen mit einem Prozentzeichen (%) vorangestellt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession ist als \_ 000C109E-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                             |



 

 




