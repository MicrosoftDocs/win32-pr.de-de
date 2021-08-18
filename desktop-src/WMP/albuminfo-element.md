---
title: AlbumInfo-Element
description: Das AlbumInfo-Element gibt die URL für die Webseite an, die Windows Media Player, wenn der Benutzer sich für die Anzeige weiterer Informationen zu einem bestimmten Medienelement entscheidet.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- Element "AlbumInfo Windows Media Player
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a5f8fab7da8f61ce6ee5451ebcef4dc33517aae2396f0817fac19222713db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055378"
---
# <a name="albuminfo-element"></a>AlbumInfo-Element

> [!Note]  
> In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **AlbumInfo-Element** gibt die URL für die Webseite an, die Windows Media Player, wenn der Benutzer sich für die Anzeige weiterer Informationen zu einem bestimmten Medienelement entscheidet.

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (erforderlich)
</dt> <dd>

URL für die Webseite, die Windows Media Player wird.

</dd> </dl>

## <a name="parentchild-elements"></a>Über- und untergeordnete Elemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Benutzer in Windows Media Player auf eine Schaltfläche klickt, um zusätzliche Informationen zu einem bestimmten Medienelement anzeigen zu können, sendet der Player die URL-Anforderung mit angefügten Parametern unter Verwendung eines Fragezeichens (?) als Trennzeichen für Abfragezeichenfolgen. In der folgenden Tabelle sind die mit der URL-Anforderung gesendeten Parameter aufgeführt. Andere sind möglicherweise aus Gründen der Legacykompatibilität vorhanden.



| Name         | Wert                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Album*      | Der Wert des **WM/AlbumTitle-Attributs** für das Medienelement.                                                                                                        |
| *Künstler*     | Der Wert des **WM/AlbumArtist-Attributs,** sofern vorhanden, oder der Wert des **Author-Attributs** für das Medienelement.                                         |
| *Geoid*      | Windows geografische Standort-ID. Die Standort-ID wird vom Benutzer im Bereich **Standort** der Einstellungen für regionale Optionen und Sprachoptionen in Systemsteuerung. |
| *locale*     | Windows Media Player-ID.                                                                                                                                     |
| *Titel*      | Der Wert des **Title-Attributs** für das Medienelement.                                                                                                                |
| *UFID*       | Der Wert des **WM/UniqueFileIdentifier-Attributs** für das Medienelement.                                                                                              |
| *userlocale* | Windows-ID. Das Gebiets anders wird vom Benutzer im Bereich **Standards und Formate** der Einstellungen "Regionale Optionen" und "Sprachoptionen" in Systemsteuerung.        |
| *version*    | Windows Media Player Versionsnummer im folgenden Format: 10.0.x.xxxx oder 11.0.x.xxxx.                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





