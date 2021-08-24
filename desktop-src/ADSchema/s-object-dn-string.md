---
title: Object(DN-String)-Syntax
description: Eine Oktettzeichenfolge, die einen Zeichenfolgenwert und einen DN enthält.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- Object(DN-String) syntax AD Schema
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18222343a5c10b7231d174021c8d4238ba075b66b648d99a704f4e1d1d651e2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580250"
---
# <a name="objectdn-string-syntax"></a>Object(DN-String)-Syntax

Eine Oktettzeichenfolge, die einen Zeichenfolgenwert und einen DN enthält.



| Eingabe | Wert |
|--------------|------------------------------------------------------------------------------------|
| Name         | Object(DN-String)                                                                  |
| Syntax-ID    | 2.5.5.14                                                                           |
| OM-ID        | 127                                                                                |
| MAPI-Typ    | \-                                                                                 |
| ADS-Typ     | ADSTYPE \_ DN \_ MIT \_ ZEICHENFOLGE                                                          |
| Variant-Typ | VT \_ DISPATCH                                                                       |
| SDS-Typ     | Ein COM-Objekt, das in ein [**IADsDNWithString-Objekt**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)umgecastet werden kann. |



## <a name="remarks"></a>Hinweise

Ein Wert mit dieser Syntax hat das folgende Format:

``` syntax
S:<char count>:<string value>:<object DN>
```

wobei " &lt; char count " die Anzahl der Zeichen in der Zeichenfolge &gt; &lt; &gt; "String Value" und &lt; "Object &gt; DN" ein Distinguished Name eines Objekts in Active Directory ist. Active Directory aktualisiert den DN, wenn das Objekt, auf das es verweist, verschoben oder umbenannt wird.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
