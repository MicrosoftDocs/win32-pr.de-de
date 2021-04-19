---
description: Die DataSize-Eigenschaft des Datensatz-Objekts ist eine schreibgeschützte Eigenschaft, die die Größe der Daten für das angegebene Feld zurückgibt.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Record. DataSize-Eigenschaft
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
ms.openlocfilehash: 500ee0039f4bfe638f4eca3740669e821c97ca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361948"
---
# <a name="recorddatasize-property"></a>Record. DataSize-Eigenschaft

Die **DataSize** -Eigenschaft des [**Datensatz**](record-object.md) -Objekts ist eine schreibgeschützte Eigenschaft, die die Größe der Daten für das angegebene Feld zurückgibt. Wenn es sich bei den Daten um einen Datenstrom handelt, wird die Datenstrom Länge in Bytes zurückgegeben. Wenn es sich bei den Daten um eine Zeichenfolge handelt, wird die Zeichen folgen Länge ohne NULL zurückgegeben. Wenn es sich bei den Daten um eine ganze Zahl handelt, wird der Wert 4 zurückgegeben (was die Größe der ganzen Zahl angibt). Wenn die Daten NULL sind, wird 0 zurückgegeben.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a>Eigenschaftswert

Erforderliche Feldnummer des Werts im Datensatz, 1-basiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




