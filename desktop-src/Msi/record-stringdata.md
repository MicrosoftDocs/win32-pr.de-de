---
description: Die StringData-Eigenschaft des Record-Objekts ist eine Lese-/Schreibeigenschaft, die Zeichenfolgendaten in ein oder aus einem angegebenen Feld innerhalb des Datensatzes überträgt. Wenn eine ganze Zahl oder ein Objekt gespeichert wurde, wird der zugehörige Zeichenfolgenwert zurückgegeben.
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: Record.StringData-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.StringData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3b789d8f4d8c6bf26c63c5313c61d95035bb130e4a57b63fbe9c12cdc141bb42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327770"
---
# <a name="recordstringdata-property"></a>Record.StringData-Eigenschaft

Die **StringData-Eigenschaft** des [**Record-Objekts**](record-object.md) ist eine Lese-/Schreibeigenschaft, die Zeichenfolgendaten in ein oder aus einem angegebenen Feld innerhalb des Datensatzes überträgt. Wenn eine ganze Zahl oder ein Objekt gespeichert wurde, wird der zugehörige Zeichenfolgenwert zurückgegeben.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

Erforderliche Feldnummer des Werts innerhalb des Datensatzes, 1-basiert.

## <a name="remarks"></a>Hinweise

Der zurückgegebene Wert eines nicht vorhandenen Felds ist eine leere Zeichenfolge. Um ein Datensatzzeichenfolgenfeld auf NULL festzulegen, verwenden Sie entweder eine leere Variante oder eine leere Zeichenfolge. Der Versuch, einen Wert in einem nicht vorhandenen Feld zu speichern, verursacht einen Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord ist als 000C1093-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                              |



 

 




