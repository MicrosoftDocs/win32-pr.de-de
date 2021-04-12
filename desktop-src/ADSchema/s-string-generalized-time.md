---
title: Syntax für Zeichen folgen (generalisierte Zeit)
description: Ein Zeit Zeichen folgen Format, das von ASN. 1-Standards definiert wird. | Syntax für Zeichen folgen (generalisierte Zeit)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Zeichenfolge (generalisierte Zeit) Syntax AD-Schema
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e754fe622d3ff6f010521b7bc9b9e4ff7a5f34
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219201"
---
# <a name="stringgeneralized-time-syntax"></a>Syntax für Zeichen folgen (generalisierte Zeit)

Ein Zeit Zeichen folgen Format, das von ASN. 1-Standards definiert wird. Verwenden Sie diese Syntax zum Speichern von Zeitwerten in Generalized-Time Format.

Das Format für die Generalized-Time-Syntax lautet "YYYYMMDDHHMMSS. 0z". Ein Beispiel für einen zulässigen Wert ist "20010928060000.0 z". "Z" weist auf keine Zeit differenzielle Abweichung hin. Active Directory speichert Datum/Uhrzeit als Greenwich Mean Time (GMT). Wenn keine Zeit differenzielle Angabe angegeben ist, ist GMT die Standardeinstellung.

Wenn die Uhrzeit in einer anderen Zeitzone als GMT angegeben wird, wird die Differenz zwischen der Zeitzone und der GMT an die Zeichenfolge angefügt, nicht an "Z" in der Form "YYYYMMDDHHMMSS. 0 \[ +/- \] hhmm". Ein Beispiel für einen zulässigen Wert ist "20010928060000.0 + 0200". Die differenzielle Abhängigkeit basiert auf der Formel: GMT = local + Differential.

Weitere Informationen finden Sie unter ISO 8601 und X680.



| Eingabe | Wert |
|--------------|----------------------------------------------------------------------------|
| Name         | String(Generalized-Time)                                                   |
| Syntax-ID    | 2.5.5.11                                                                   |
| OM-ID        | 24                                                                         |
| MAPI-Typ    | SYSTIME                                                                    |
| ADS-Typ     | adstype- \_ UTC- \_ Zeit                                                         |
| Varianttyp | VT- \_ Datum                                                                   |
| SDS-Typ     | [System.DateTime](/dotnet/api/system.datetime) |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[System.DateTime](/dotnet/api/system.datetime)
</dt> </dl>

 

 
