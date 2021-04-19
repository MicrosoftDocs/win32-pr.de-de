---
title: ButtonGroup. mappingImage
description: Das mappingImage-Attribut gibt den Namen des Bilds an, das die Schaltflächen Zuordnung der ButtonGroup darstellt, oder ruft ihn ab.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- ButtonGroup. mappingImage-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4afc44a00d5ce9b15ee01d4a0dc1aff52c555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367694"
---
# <a name="buttongroupmappingimage"></a>ButtonGroup. mappingImage

Das **mappingImage** -Attribut gibt den Namen des Bilds an, das die Schaltflächen Zuordnung der **ButtonGroup** darstellt, oder ruft ihn ab.

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Dies ist ein obligatorisches Attribut, das angegeben werden muss.

Das Zuordnungsbild sollte die gleichen Dimensionen wie das Haupt **Bild** sein. Dabei handelt es sich um eine Karte der durch Klicken aktivierbaren Bereiche des Haupt Bilds. Erstellen Sie die Zuordnung, indem Sie jeden klickbaren Bereich mit einer anderen Farbe ausfüllen.

Wenn Sie die einzelnen **ButtonElement-Elemente** definieren, legen Sie Ihre Farbe mithilfe des **mappingColor** -Attributs aus der Zuordnung fest. Wenn Sie z. b. im Hauptbild eine Schaltflächen Grafik mit der Schaltfläche "mit Vorzeichen" haben, können Sie eine Karte mit dem Bereich der roten Farbe erstellen. Das **ButtonElement** -Attribut muss dann als rot angegeben werden, damit das Bild für das Abbrechen des signierten Zeichens geklickt werden kann.

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF (keine animierten GIFs). Da es sich bei den JPGs um Verlust Verluste handelt, werden Sie daher nicht für die Zuordnung von Bildern empfohlen.

## <a name="examples"></a>Beispiele

Die folgende Abbildung ist ein Beispiel für ein **mappingImage** und das sichtbare Bild, dem es entspricht. Diese Images sind Teil der Skin im kleinen Ordner, der im SDK enthalten ist.

![Bild der Beispiel Zuordnung](images/absam01m.png)![Beispiel Hintergrundbild](images/absam01f.png)

Siehe *ButtonElement*. [mappingColor](buttonelement-mappingcolor.md) -Attribut für ein Codebeispiel zur Veranschaulichung der Verwendung dieses Attributs.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ButtonElement. mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**ButtonGroup-Element**](buttongroup-element.md)
</dt> <dt>

[**ButtonGroup. Image**](buttongroup-image.md)
</dt> <dt>

[**ButtonGroup. TransparencyColor**](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





