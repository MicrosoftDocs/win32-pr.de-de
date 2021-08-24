---
title: Intervallsyntax
description: Stellt einen Zeitintervallwert dar.
ms.assetid: e41b71da-cd05-4a4a-8b97-9210dbe314de
ms.tgt_platform: multiple
keywords:
- Intervallsyntax AD-Schema
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e088c8347ff12172cb87c521e049e2646a0711e1eaedf805887b6988af1e284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580290"
---
# <a name="interval-syntax"></a>Intervallsyntax

Stellt einen Zeitintervallwert dar. Die tatsächlichen Zeiteinheiten hängen davon ab, welches Attribut diese Syntax verwendet. Diese Syntax ist mit der [**LargeInteger-Syntax**](s-largeinteger.md) identisch, mit der Ausnahme, dass die hohen und niedrigen Werte ganze Zahlen ohne Vorzeichen sind.



| Eingabe | Wert |
|--------------|------------------------------------------------------------------------------------|
| Name         | Intervall                                                                           |
| Syntax-ID    | 2.5.5.16                                                                           |
| OM-ID        | 65                                                                                 |
| MAPI-Typ    | \-                                                                                 |
| ADS-Typ     | ADSTYPE \_ LARGE \_ INTEGER                                                            |
| Variant-Typ | VT \_ DISPATCH                                                                       |
| SDS-Typ     | Ein COM-Objekt, das in ein [**IADsLargeInteger-Objekt castiert werden kann.**](/windows/desktop/api/iads/nn-iads-iadslargeinteger) |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger)
</dt> <dt>

[**LargeInteger**](s-largeinteger.md)
</dt> </dl>

 

 
