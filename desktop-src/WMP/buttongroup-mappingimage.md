---
title: BUTTONGROUP.mappingImage
description: Das mappingImage-Attribut gibt den Namen des Bilds an, das die Schaltflächenzuordnung der BUTTONGROUP darstellt, oder ruft sie ab.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- BUTTONGROUP.mappingImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c26a920042aae4ba144f194845f350030f5675c1b9cc3fcfed552346904add1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119899"
---
# <a name="buttongroupmappingimage"></a>BUTTONGROUP.mappingImage

Das **mappingImage-Attribut** gibt den Namen des Bilds an, das die Schaltflächenzuordnung der BUTTONGROUP darstellt, **oder ruft sie ab.**

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**

## <a name="remarks"></a>Hinweise

Dies ist ein obligatorisches Attribut, das angegeben werden muss.

Das Zuordnungsbild sollte die gleichen Dimensionen wie das Hauptbild **haben.** Es handelt sich um eine Karte der klickbaren Bereiche des Hauptbilds. Erstellen Sie die Karte, indem Sie jeden klickbaren Bereich mit einer anderen Farbe füllen.

Wenn Sie jedes **BUTTONELEMENT definieren,** bestimmen Sie seine Farbe über die Karte mithilfe des **mappingColor-Attributs.** Wenn das Hauptbild z. B. eine Schaltflächengrafik mit Stoppzeichen ist, können Sie eine Karte mit dem Rotbereich des Vorzeichens erstellen. Das **BUTTONELEMENT-Attribut** muss dann rot angegeben werden, damit auf das Stoppzeichenbild geklickt werden kann.

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF (ohne animierte GIFs). Da JPGs verlustbeendet sind und daher unerwarteten Farbwechseln unterliegen, werden sie für die Zuordnung von Bildern nicht empfohlen.

## <a name="examples"></a>Beispiele

Die folgende Abbildung ist ein Beispiel für ein **mappingImage und** das sichtbare Bild, dem es entspricht. Diese Bilder sind Teil der Skin im Tiny-Ordner, der im SDK enthalten ist.

![Beispielzuordnungsbild](images/absam01m.png)![Beispielhintergrundbild](images/absam01f.png)

Weitere Informationen finden Sie *unter BUTTONELEMENT*. [mappingColor-Attribut](buttonelement-mappingcolor.md) für ein Codebeispiel, das die Verwendung dieses Attributs veranschaulicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BUTTONELEMENT.mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**BUTTONGROUP-Element**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.transparencyColor**](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





