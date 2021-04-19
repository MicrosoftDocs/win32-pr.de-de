---
title: Object (DN-String)-Syntax
description: Eine Oktett-Zeichenfolge, die einen Zeichen folgen Wert und einen DN enthält.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- AD-Schema der Object (DN-String)-Syntax
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823da21325abdc426d5f58df4cdf04de19fc68b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342678"
---
# <a name="objectdn-string-syntax"></a>Object (DN-String)-Syntax

Eine Oktett-Zeichenfolge, die einen Zeichen folgen Wert und einen DN enthält.



| Eingabe | Wert |
|--------------|------------------------------------------------------------------------------------|
| Name         | Object(DN-String)                                                                  |
| Syntax-ID    | 2.5.5.14                                                                           |
| OM-ID        | 127                                                                                |
| MAPI-Typ    | \-                                                                                 |
| ADS-Typ     | adstype \_ DN \_ mit \_ Zeichenfolge                                                          |
| Varianttyp | VT \_ -Verteilung                                                                       |
| SDS-Typ     | Ein COM-Objekt, das in ein [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)-Objekt umgewandelt werden kann. |



## <a name="remarks"></a>Bemerkungen

Ein Wert mit dieser Syntax weist das folgende Format auf:

``` syntax
S:<char count>:<string value>:<object DN>
```

&lt;dabei ist "char Count &gt; " die Anzahl von Zeichen in der Zeichen &lt; Folge "String value &gt; " und " &lt; Object DN &gt; " ein definierter Name eines Objekts in Active Directory. Active Directory aktualisiert den DN, wenn das Objekt, auf das verwiesen wird, verschoben oder umbenannt wird.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
