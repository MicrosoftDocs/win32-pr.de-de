---
title: EQUALIZERSETTINGS.normalization
description: Das Normalisierungsattribut gibt einen Wert an, der angibt, ob die Normalisierung aktiviert ist, oder ruft einen Wert ab.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS.normalization Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f2befdd62f0508822d5547cb3b894b93ea095f52db4cf9bbdb4a444d99251c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578166"
---
# <a name="equalizersettingsnormalization"></a>EQUALIZERSETTINGS.normalization

Das  Normalisierungsattribut gibt einen Wert an, der angibt, ob die Normalisierung aktiviert ist, oder ruft einen Wert ab.

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Lese-/Schreib-Wert.



| Wert | BESCHREIBUNG                         |
|-------|-------------------------------------|
| true  | Die Normalisierung ist aktiviert.           |
| false | Standard. Die Normalisierung ist deaktiviert. |



 

## <a name="remarks"></a>Hinweise

Wenn die Normalisierung aktiviert ist, wird das Audiosignal für eine gesamte digitale Mediendatei auf den maximal zulässigen Wert hochskaliert. Dadurch können mehrere Dateien auf ungefähr demselben Volume wiedergegeben werden, ohne dass Volumeanpassungen erforderlich sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EQUALIZERSETTINGS-Element**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationAverage**](equalizersettings-normalizationaverage.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationPeak**](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





