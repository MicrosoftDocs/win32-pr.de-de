---
title: Object (DN-Binary)-Syntax
description: Eine Oktett-Zeichenfolge, die einen binären Wert und einen Distinguished Name (DN) enthält.
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Objekt Syntax (DN-Binary) AD-Schema
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e96f640ad729f203362df906bcc6afe6b82e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104106701"
---
# <a name="objectdn-binary-syntax"></a>Object (DN-Binary)-Syntax

Eine Oktett-Zeichenfolge, die einen binären Wert und einen Distinguished Name (DN) enthält.



| Eingabe | Wert |
|--------------|------------------------------------------------------------------------------------|
| Name         | Object(DN-Binary)                                                                  |
| Syntax-ID    | 2.5.5.7                                                                            |
| OM-ID        | 127                                                                                |
| MAPI-Typ    | TString                                                                            |
| ADS-Typ     | adstype \_ DN \_ mit \_ Binär                                                          |
| Varianttyp | VT \_ -Verteilung                                                                       |
| SDS-Typ     | Ein COM-Objekt, das in [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)umgewandelt werden kann. |



## <a name="remarks"></a>Bemerkungen

Ein Wert mit dieser Syntax weist das folgende Format auf:

``` syntax
B:<char count>:<binary value>:<object DN>
```

Dabei ist " &lt; char Count &gt; " die Anzahl von hexadezimalen Ziffern im " &lt; binären Wert &gt; ", " &lt; Binärwert &gt; " ist die hexadezimale Darstellung des binären Werts, und " &lt; Object DN &gt; " ist ein definierter Name. Active Directory aktualisiert den DN automatisch, wenn das Objekt, auf das es verweist, verschoben oder umbenannt wird. Weitere Informationen und ein Codebeispiel, in dem diese Syntax verwendet wird, finden Sie unter [Aktivieren der Umbenennungs sicheren Bindung mit der otherWellKnownObjects-Eigenschaft](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
