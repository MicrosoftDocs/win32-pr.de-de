---
title: Object(DS-DN)-Syntax
description: Eine Zeichenfolge, die einen Distinguished Name (DN) enthält.
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- Objektsyntax (DS-DN) AD-Schema
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0c9adf4138de56d90ac89743c3b428a1f25b45027bc19f0b5dccc2e005b143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835683"
---
# <a name="objectds-dn-syntax"></a>Object(DS-DN)-Syntax

Eine Zeichenfolge, die einen Distinguished Name (DN) enthält. Bei Attributen mit dieser Syntax behandelt Active Directory Attributwerte als Verweise auf das vom DN identifizierte Objekt und aktualisiert den Wert automatisch, wenn das Objekt verschoben oder umbenannt wird. Geben Sie für Abfragen, die Attribute der DN-Syntax in einem Filter enthalten, vollständige Distinguished Names an. Platzhalter (z. B. cn=John \* ) werden nicht unterstützt.



| Eingabe | Wert |
|--------------|------------------------------------------------------------------------|
| Name         | Object(DS-DN)                                                          |
| Syntax-ID    | 2.5.5.1                                                                |
| OM-ID        | 127                                                                    |
| MAPI-Typ    | OBJECT                                                                 |
| ADS-Typ     | ADSTYPE \_ DN \_ STRING                                                    |
| Variant-Typ | VT \_ BSTR                                                               |
| SDS-Typ     | [System.String](/dotnet/api/system.string) |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[System.String](/dotnet/api/system.string)
</dt> </dl>

 

 
