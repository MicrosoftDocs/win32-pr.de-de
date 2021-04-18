---
title: Image-Element (WMP-SDK)
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Image-Element (WMP-SDK)
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- Bild Element Windows-Media Player
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c10b62365453f395c1aaf373e355c21260900f8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360959"
---
# <a name="image-element-wmp-sdk"></a>Image-Element (WMP-SDK)

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **Image** -Element gibt die Bilder an, die von Windows Media Player dem Benutzer angezeigt werden, um den Online Store darzustellen.

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

<span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**Eulaurl** (erforderlich für den Speicher vom Typ 1, wird für Typ 2 ignoriert)
</dt> <dd>

Die URL für das Logo, das von Windows Media Player im Dialogfeld Endbenutzer-Lizenzvertrag (EULA) angezeigt wird. Dabei muss es sich um ein PNG-Bild handeln, das 80 x 80 Pixel ist.

</dd> <dt>

<span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**Menuurl** (optional)
</dt> <dd>

Die URL für das Bild, das von Windows Media Player im Menü Dienste angezeigt wird. Dieses Bild muss 15 x 15 Pixel betragen.

</dd> <dt>

<span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**Servicelargeurl** (optional)
</dt> <dd>

Bei einem Online Store vom Typ 1 ist dies die URL für das Image, das in Windows Media Player auf der Registerkarte " **Online Stores** " angezeigt wird. Für Windows Media Player 11 muss dieses Bild 45 Pixel breit und 13 Pixel hoch sein. Bei Windows Media Player 12 muss dieses Bild 45 Pixel breit und 30 Pixel hoch sein. Um sowohl die Versionen 11 als auch 12 von Windows Media Player zu unterstützen, müssen Sie zwei separate ServiceInfo.xml Dokumente bereitstellen, von denen jedes auf das Bild der passenden Größe für servicelargeurl zeigt.

Bei einem Online Store vom Typ 2 ist dies die URL für das Image, das in Windows Media Player neben der Registerkarte **Online Stores** oder neben den Schaltflächen für den Aufgabenbereich angezeigt wird. Dieses Bild muss 30 x 30 Pixel betragen.

</dd> <dt>

<span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**Servicesmallurl** (optional)
</dt> <dd>

Die URL für das Logo, das zusammen mit der im **Description** -Element angegebenen Marketing Beschreibung angezeigt wird. Wenn Sie nicht bereitgestellt wird, ist sie leer. (Alle Typen, optional) Dabei muss es sich um ein PNG-Bild handeln, das 45 Pixel breit und 13 Pixel hoch ist.

</dd> </dl>

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Die unterstützten Bildformate sind GIF, JPG, BMP und PNG (das empfohlene Format). Die Verwendung von Webtransparenz wird unterstützt und empfohlen. Animierte GIF-Dateien werden nicht unterstützt.

Wenn Sie keinen Wert für **menuurl** angeben, zeigt Windows Media Player im Menü für den Online Shop keine Grafik an.

Sie können ein animiertes Bild für servicelargeurl bereitstellen. In Windows Media Player 10 oder 11 ist das Bild animiert. In Windows Media Player 12 wird nur der erste Frame des Bilds angezeigt. Zum Bereitstellen eines animierten Bilds erstellen Sie eine einzelne Bilddatei, die aufeinander folgende Rahmen der Animation enthält. Beispielsweise können Sie für ein Bild, das 30 Pixel breit und 30 Pixel hoch ist, 20 aufeinander folgende Bilder nebeneinander in einem Bild bereitstellen, das 600 Pixel breit und 30 Pixel hoch ist. Ein solches Bild wird von Windows Media Player automatisch animiert, indem die 20 einzelnen Bilder nacheinander angezeigt werden. Diese Animation tritt nur einmal auf, wenn der Online Shop geöffnet wird. der Vorgang wird nicht wiederholt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





