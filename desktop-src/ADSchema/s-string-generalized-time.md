---
title: String(Generalized-Time)-Syntax
description: Ein durch ASN.1-Standards definiertes Zeitzeichenfolgenformat. | String(Generalized-Time)-Syntax
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- String(Generalized-Time)-Syntax AD-Schema
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bf7d965b03b75f4186b807098a5262c402d0c19104a4c09357958b38a77a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580210"
---
# <a name="stringgeneralized-time-syntax"></a>String(Generalized-Time)-Syntax

Ein durch ASN.1-Standards definiertes Zeitzeichenfolgenformat. Verwenden Sie diese Syntax zum Speichern von Zeitwerten im Generalized-Time Format.

Das Format für Generalized-Time Syntax ist "YYYYMMDDHHMMSS.0Z". Ein Beispiel für einen zulässigen Wert ist "20010928060000.0Z". Das "Z" gibt an, dass es keine differenzielle Zeit gibt. Active Directory speichert Datum/Uhrzeit als Greenwich Mean Time (GMT). Wenn kein zeitdifferenzieller Wert angegeben wird, ist GMT der Standardwert.

Wenn die Zeit in einer anderen Zeitzone als GMT angegeben wird, wird die Differenz zwischen der Zeitzone und GMT an die Zeichenfolge anstelle von "Z" in der Form "YYYYMMDDHHMMSS.0 \[ +/- \] HHMM" angefügt. Ein Beispiel für einen zulässigen Wert ist "20010928060000.0+0200". Das differenzielle -Wert basiert auf der Formel GMT=Local+differential.

Weitere Informationen finden Sie unter ISO 8601 und X680.



| Eingabe | Wert |
|--------------|----------------------------------------------------------------------------|
| Name         | String(Generalized-Time)                                                   |
| Syntax-ID    | 2.5.5.11                                                                   |
| OM-ID        | 24                                                                         |
| MAPI-Typ    | Systime                                                                    |
| ADS-Typ     | ADSTYPE \_ UTC \_ TIME                                                         |
| Variant-Typ | VT \_ DATE                                                                   |
| SDS-Typ     | [System.DateTime](/dotnet/api/system.datetime) |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[System.DateTime](/dotnet/api/system.datetime)
</dt> </dl>

 

 
