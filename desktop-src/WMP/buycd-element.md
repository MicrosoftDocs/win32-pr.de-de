---
title: BuyCD-Element
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | BuyCD-Element
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- BuyCD-Element Windows Media Player
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0b2af0f12b06c7d5701db3fcc073d7b7c330e8798408206b64a8b9811f27d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135843"
---
# <a name="buycd-element"></a>BuyCD-Element

> [!Note]  
> In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **BuyCD-Element** gibt die URLs für Webseiten an, Windows Media Player angezeigt werden, wenn sich der Benutzer für einen Kauf entscheidet.

``` syntax
<BuyCD
    MediaPlayerURL = "URL"
    MediaCenterURL = "URL"
    BrowserURL = "URL"
/>
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (erforderlich)
</dt> <dd>

URL für die Webseite, die der Onlineshop anzeigt, um eine CD oder DVD für den Kauf in Windows Media Player.

</dd> <dt>

<span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**
</dt> <dd>

URL für die Webseite, die der Onlineshop anzeigt, um eine CD oder DVD zum Kauf in Windows XP Media Center Edition 2004 Update anbieten.

</dd> <dt>

<span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**
</dt> <dd>

URL für die Webseite, die der Onlineshop anzeigt, um eine CD oder DVD für den Kauf in einem separaten Browserfenster anbieten zu können. Diese URL wird auch von Windows XP Service Pack 2 oder höher für das **Onlinefeature Shop for music** verwendet.

</dd> </dl>

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Benutzer in Windows Media Player auf eine Schaltfläche oder einen Link klickt, um eine CD oder DVD zu erwerben, sendet der Player die URL-Anforderung an ServiceTask1 mit Parametern, die mithilfe eines Fragezeichens (?) als Trennzeichen für Abfragezeichenfolgen angefügt werden. In der folgenden Tabelle sind die mit der URL-Anforderung gesendeten Parameter aufgeführt. Andere sind möglicherweise aus Gründen der Legacykompatibilität vorhanden.



| Name         | Wert                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Album*      | Der Wert des **WM/AlbumTitle-Attributs** für das Medienelement.                                                                                                        |
| *Künstler*     | Der Wert des **WM/AlbumArtist-Attributs,** sofern vorhanden, oder der Wert des **Author-Attributs** für das Medienelement.                                         |
| *Geoid*      | Windows geografische Standort-ID. Die Standort-ID wird vom Benutzer im Bereich **Standort** der Einstellungen für regionale Optionen und Sprachoptionen in Systemsteuerung. |
| *locale*     | Windows Media Player-ID.                                                                                                                                     |
| *Titel*      | Der Wert des **Title-Attributs** für das Medienelement.                                                                                                                |
| *UFID*       | Der Wert des **WM/UniqueFileIdentifier-Attributs** für das Medienelement.                                                                                              |
| *userlocale* | Windows-ID. Das Gebiets anders wird vom Benutzer im Bereich **Standards und Formate** der Einstellungen für Regional- und Sprachoptionen in Systemsteuerung.        |
| *version*    | Windows Media Player Versionsnummer im folgenden Format: 10.0.x.xxxx oder 11.0.x.xxxx.                                                                         |



 

Windows XP Media Center Edition 2004 bietet Benutzern eine Benutzeroberfläche, die so konzipiert ist, dass sie aus der Entfernung angezeigt werden kann. Sie sollten Webseiten für den *MediaCenterURL-Parameter* erstellen, um auf großen Displays angezeigt zu werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ServiceInfo-Beispieldokument für einen Typ 1 online Store**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





