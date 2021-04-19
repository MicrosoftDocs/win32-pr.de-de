---
description: Die StringData-Eigenschaft des Datensatz-Objekts ist eine Lese-/Schreibeigenschaft, die Zeichen folgen Daten in ein oder aus einem angegebenen Feld im Datensatz überträgt. Wenn eine ganze Zahl oder ein Objekt gespeichert wurde, wird der zugehörige Zeichen folgen Wert zurückgegeben.
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: Record. StringData (Eigenschaft)
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
ms.openlocfilehash: 21f72c35795696875aa55f2d5d791564c6f1fee5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361947"
---
# <a name="recordstringdata-property"></a>Record. StringData (Eigenschaft)

Die **StringData** -Eigenschaft des [**Datensatz**](record-object.md) -Objekts ist eine Lese-/Schreibeigenschaft, die Zeichen folgen Daten in ein oder aus einem angegebenen Feld im Datensatz überträgt. Wenn eine ganze Zahl oder ein Objekt gespeichert wurde, wird der zugehörige Zeichen folgen Wert zurückgegeben.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

Erforderliche Feldnummer des Werts im Datensatz, 1-basiert.

## <a name="remarks"></a>Bemerkungen

Der zurückgegebene Wert eines nicht vorhandenen Felds ist eine leere Zeichenfolge. Verwenden Sie entweder eine leere Variante oder eine leere Zeichenfolge, um ein Feld für die Daten Satz Zeichenfolge auf NULL festzulegen. Der Versuch, einen Wert in einem nicht vorhandenen Feld zu speichern, verursacht einen Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




