---
title: Equalizersettings. Normalisierung
description: Das normalisierungs Attribut gibt einen Wert an, der angibt, ob Normalisierung aktiviert ist, oder ruft diesen ab.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- Equalizersettings. Normalisierung Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9714359e5d5e2af0c82a0d687555f7cfcbf1cf70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359284"
---
# <a name="equalizersettingsnormalization"></a>Equalizersettings. Normalisierung

Das **normalisierungs** Attribut gibt einen Wert an, der angibt, ob Normalisierung aktiviert ist, oder ruft diesen ab.

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                         |
|-------|-------------------------------------|
| true  | Normalisierung ist aktiviert.           |
| false | Standard. Die Normalisierung ist deaktiviert. |



 

## <a name="remarks"></a>Bemerkungen

Wenn die Normalisierung aktiviert ist, wird das Audiosignal für eine gesamte digitale Mediendatei auf den maximalen Wert hochskaliert. Auf diese Weise können mehrere Dateien auf ungefähr demselben Volume abgespielt werden, ohne dass die volumeanpassungen erforderlich sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Equalizersettings-Element**](equalizersettings-element.md)
</dt> <dt>

[**Equalizersettings. normalizationaverage**](equalizersettings-normalizationaverage.md)
</dt> <dt>

[**Equalizersettings. normalizationpeak**](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





