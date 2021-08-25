---
description: Die DataSize-Eigenschaft des Record-Objekts ist eine schreibgeschützte Eigenschaft, die die Größe der Daten für das designierte Feld zurückgibt.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Record.DataSize (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.DataSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 067fc09e65d644413e75ccd8a9c0173e30df8060dff0f772ae5d12705ab610aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912960"
---
# <a name="recorddatasize-property"></a>Record.DataSize (Eigenschaft)

Die **DataSize-Eigenschaft** des [**Record-Objekts**](record-object.md) ist eine schreibgeschützte Eigenschaft, die die Größe der Daten für das designierte Feld zurückgibt. Wenn es sich bei den Daten um einen Stream handelt, wird die Streamlänge in Bytes zurückgegeben. Wenn die Daten eine Zeichenfolge sind, wird die Zeichenfolgenlänge ohne NULL zurückgegeben. Wenn die Daten eine ganze Zahl sind, wird der Wert 4 zurückgegeben (gibt die Größe der ganzen Zahl an). Wenn die Daten NULL sind, wird 0 zurückgegeben.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a>Eigenschaftswert

Erforderliche Feldnummer des Werts innerhalb des Datensatzes, 1-basiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord ist als 000C1093-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                              |



 

 




