---
title: Object(DN-Binary)-Syntax
description: Eine Oktettzeichenfolge, die einen Binärwert und einen Distinguished Name (DN) enthält.
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Objektsyntax (DN-Binary) AD-Schema
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15172a8577cf8ccec71053c3d374b389d71d3264fcc1934b19440a3f9efc4904
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702570"
---
# <a name="objectdn-binary-syntax"></a>Object(DN-Binary)-Syntax

Eine Oktettzeichenfolge, die einen Binärwert und einen Distinguished Name (DN) enthält.



| Eingabe | Wert |
|--------------|------------------------------------------------------------------------------------|
| Name         | Object(DN-Binary)                                                                  |
| Syntax-ID    | 2.5.5.7                                                                            |
| OM-ID        | 127                                                                                |
| MAPI-Typ    | TSTRING                                                                            |
| ADS-Typ     | \_ADSTYPE-DN \_ MIT \_ BINÄRDATEI                                                          |
| Variant-Typ | VT \_ DISPATCH                                                                       |
| SDS-Typ     | Ein COM-Objekt, das in ein [**IADsDNWithBinary -Objekt castiert werden kann.**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary) |



## <a name="remarks"></a>Hinweise

Ein Wert mit dieser Syntax hat das folgende Format:

``` syntax
B:<char count>:<binary value>:<object DN>
```

wobei " char count " die Anzahl der &lt; &gt; Hexadezimalziffern in " binärer Wert &lt; &gt; ", " binärer Wert " die &lt; &gt; hexadezimale Darstellung des Binärwerts und " &lt; Objekt-DN &gt; " ein Distinguished Name ist. Active Directory aktualisiert den DN automatisch, wenn das Objekt, auf das es verweist, verschoben oder umbenannt wird. Weitere Informationen und ein Codebeispiel, in dem diese Syntax verwendet wird, finden Sie unter Aktivieren der umbenennungssicheren Bindung mit der [otherWellKnownObjects-Eigenschaft.](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
