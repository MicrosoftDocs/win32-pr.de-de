---
title: Object (DS-DN)-Syntax
description: Eine Zeichenfolge, die einen Distinguished Name (DN) enthält.
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- AD-Schema der Object (DS-DN)-Syntax
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45154985fa7fbfc4d95d563196357d43eac2ea72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519351"
---
# <a name="objectds-dn-syntax"></a>Object (DS-DN)-Syntax

Eine Zeichenfolge, die einen Distinguished Name (DN) enthält. Für Attribute mit dieser Syntax verarbeitet Active Directory Attributwerte als Verweise auf das Objekt, das durch den DN identifiziert wird, und aktualisiert den Wert automatisch, wenn das Objekt verschoben oder umbenannt wird. Geben Sie für Abfragen, die Attribute der DN-Syntax in einem Filter enthalten, vollständige Distinguished Names an. Platzhalter (z. b. CN = John \* ) werden nicht unterstützt.



| Eingabe | Wert |
|--------------|------------------------------------------------------------------------|
| Name         | Object(DS-DN)                                                          |
| Syntax-ID    | 2.5.5.1                                                                |
| OM-ID        | 127                                                                    |
| MAPI-Typ    | OBJECT                                                                 |
| ADS-Typ     | adstype- \_ DN- \_ Zeichenfolge                                                    |
| Varianttyp | VT \_ BSTR                                                               |
| SDS-Typ     | [System.String](/dotnet/api/system.string) |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[System.String](/dotnet/api/system.string)
</dt> </dl>

 

 
