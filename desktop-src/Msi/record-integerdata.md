---
description: Dies ist die IntegerData-Eigenschaft des Record-Objekts. Diese Lese-/Schreibeigenschaft überträgt 32-Bit-Ganzzahldaten in ein oder aus einem angegebenen Feld innerhalb des Datensatzes. Wenn ein Feldwert nicht in eine ganze Zahl konvertiert werden kann, wird msiDatabaseNullInteger zurückgegeben.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Record.IntegerData(Eigenschaft)
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
ms.openlocfilehash: b3593f31d8f8cea6278346e8c99bb9c9b880aed273ae7ab70614ade112cd8c8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912920"
---
# <a name="recordintegerdata-property"></a>Record.IntegerData(Eigenschaft)

Dies ist die **IntegerData-Eigenschaft** des [**Record-Objekts.**](record-object.md) Diese Lese-/Schreibeigenschaft überträgt 32-Bit-Ganzzahldaten in ein oder aus einem angegebenen Feld innerhalb des Datensatzes. Wenn ein Feldwert nicht in eine ganze Zahl konvertiert werden kann, wird msiDatabaseNullInteger zurückgegeben.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

Erforderliche Feldnummer des Werts innerhalb des Datensatzes, 1-basiert.

## <a name="remarks"></a>Hinweise

Verwenden Sie msiDatabaseNullInteger, um ein Datensatz-Ganzzahlfeld auf NULL zu setzen. Der zurückgegebene Wert eines nicht vorhandenen Felds ist msiDatabaseNullInteger. Der Versuch, einen Wert in einem nicht vorhandenen Feld zu speichern, verursacht einen Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord ist als 000C1093-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                              |



 

 




