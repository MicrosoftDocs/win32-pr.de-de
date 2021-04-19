---
description: Dies ist die IntegerData-Eigenschaft des Datensatz-Objekts. Diese Eigenschaft mit Lese-/Schreibzugriff überträgt ganzzahlige 32-Bit-Daten in ein oder aus einem angegebenen Feld innerhalb des Datensatzes. Wenn ein Feldwert nicht in eine ganze Zahl konvertiert werden kann, wird "msidatabasenullinteger" zurückgegeben.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Record. IntegerData (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ed816c75ab6adc98b3ac19984079d840a4a447b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370123"
---
# <a name="recordintegerdata-property"></a>Record. IntegerData (Eigenschaft)

Dies ist die **IntegerData** -Eigenschaft des [**Datensatz**](record-object.md) -Objekts. Diese Eigenschaft mit Lese-/Schreibzugriff überträgt ganzzahlige 32-Bit-Daten in ein oder aus einem angegebenen Feld innerhalb des Datensatzes. Wenn ein Feldwert nicht in eine ganze Zahl konvertiert werden kann, wird "msidatabasenullinteger" zurückgegeben.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

Erforderliche Feldnummer des Werts im Datensatz, 1-basiert.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie msidatabasenullinteger, um ein ganz Zahl Feld für Datensätze auf NULL festzulegen. Der zurückgegebene Wert eines nicht vorhandenen Felds ist msidatabasenullinteger. Der Versuch, einen Wert in einem nicht vorhandenen Feld zu speichern, verursacht einen Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




