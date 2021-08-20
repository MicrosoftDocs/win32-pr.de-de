---
title: Image-Element (WMP SDK)
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | Image-Element (WMP SDK)
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- Image-Element Windows Media Player
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9815844833c8068fb89589368f29b15787ad8fb18a21c9f9c6867d202e3095a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862640"
---
# <a name="image-element-wmp-sdk"></a>Image-Element (WMP SDK)

> [!Note]  
> In diesem Abschnitt werden funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **Image-Element** gibt die Bilder an, die dem Benutzer Windows Media Player angezeigt werden, um den Onlineshop darzustellen.

``` syntax
<Image
    EulaURL = "URL"
    MenuURL = "URL"
    ServiceLargeURL = "URL"
    ServiceSmallURL = "URL"
/>
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (erforderlich für Speicher vom Typ 1, für Typ 2 ignoriert)
</dt> <dd>

URL für das Logo, das Windows Media Player im Dialogfeld Endbenutzer-Lizenzvertrag (EULA) angezeigt wird. Dabei muss es sich um ein PNG-Bild mit 80 x 80 Pixeln handelt.

</dd> <dt>

<span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (optional)
</dt> <dd>

URL für das Bild, das Windows Media Player im Menü "Dienste" angezeigt wird. Dieses Bild muss 15 x 15 Pixel groß sein.

</dd> <dt>

<span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (optional)
</dt> <dd>

Bei einem Onlineshop vom Typ 1 ist dies die URL für das Bild, das Windows Media Player auf der Registerkarte **Onlineshops** angezeigt wird. Für Windows Media Player 11 muss dieses Bild 45 x 13 Pixel breit sein. Für Windows Media Player 12 muss dieses Bild 45 x 30 Pixel breit sein. Um die Versionen 11 und 12 von Windows Media Player zu unterstützen, müssen Sie zwei separate ServiceInfo.xml Dokumente bereitstellen, von denen jedes auf das entsprechend dimensionierte Image für ServiceLargeURL verweist.

Bei einem Onlineshop vom Typ 2 ist dies die URL für das Bild, das Windows Media Player neben der Registerkarte **Onlineshops** oder neben den Schaltflächen des Aufgabenbereichs angezeigt wird. Dieses Bild muss 30 x 30 Pixel groß sein.

</dd> <dt>

<span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (optional)
</dt> <dd>

URL für das Logo, das zusammen mit der Marketingbeschreibung angezeigt wird, die im **Description-Element** angegeben ist. Wenn sie nicht angegeben wird, ist sie leer. (Alle Typen, optional) Dies muss ein PNG-Bild sein, das 45 Pixel breit und 13 Pixel hoch ist.

</dd> </dl>

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Die unterstützten Bildformate sind .gif, .jpg, .bmp und .png (das empfohlene Format). Die Verwendung von Webtransparenz wird sowohl unterstützt als auch empfohlen. Animierte GIF-Dateien werden nicht unterstützt.

Wenn Sie keinen Wert für **MenuURL** bereitstellen, zeigt Windows Media Player keine Grafik im Menü für Ihren Onlineshop an.

Sie können ein animiertes Bild für ServiceLargeURL bereitstellen. In Windows Media Player 10 oder 11 wird das Bild animiert. In Windows Media Player 12 wird nur der erste Frame des Bilds angezeigt. Um ein animiertes Bild bereitzustellen, erstellen Sie eine einzelne Bilddatei, die aufeinander folgende Frames Ihrer Animation enthält. Für ein Bild, das 30 Pixel breit und 30 Pixel hoch ist, können Sie beispielsweise 20 aufeinander folgende Bilder nebeneinander in einem Bild bereitstellen, das 600 Pixel breit und 30 Pixel hoch ist. Windows Media Player würde ein solches Bild automatisch animieren, indem die 20 einzelnen Bilder nacheinander angezeigt werden. Diese Animation tritt nur einmal auf, wenn der Onlineshop geöffnet wird. wird nicht wiederholt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ServiceInfo-Beispieldokument für ein Online-Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für ein Online-Store vom Typ 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





