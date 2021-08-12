---
title: InfoCenter-Element
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | InfoCenter-Element
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- InfoCenter-Windows Media Player
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1d89e7a35d0d9daacd87d3ac840f0ee87fa7c82b317afd54c9283344e204f8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576259"
---
# <a name="infocenter-element"></a>InfoCenter-Element

> [!Note]  
> In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **InfoCenter-Element** gibt die URL der Webseite an, die Windows Media Player im Infocenter-Ansichtsfeature von Now **Playing** angezeigt wird, wenn der Onlineshop aktiv ist.

``` syntax
<InfoCenter
    URL = "URL"
/>
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (erforderlich)
</dt> <dd>

URL für die Webseite, die Windows Media Player wird.

</dd> </dl>

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Der Benutzer steuert, wann die Infocenteransicht aktiv ist.

Um Informationen zum aktuell abspielten Medienelement abzurufen, müssen Sie eine Instanz des Windows Media Player-Steuerelements in Ihre Webseite einbetten und das Player-Objektmodell verwenden.

In der folgenden Tabelle sind die mit der URL-Anforderung gesendeten Parameter aufgeführt. Andere sind möglicherweise aus Gründen der Legacykompatibilität vorhanden.



| Name         | Wert                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | Windows geografische Standort-ID. Die Standort-ID wird vom Benutzer im Bereich **Standort** der Einstellungen für regionale Optionen und Sprachoptionen in Systemsteuerung. |
| *locale*     | Windows Media Player-ID.                                                                                                                                     |
| *userlocale* | Windows-ID. Das Gebiets anders wird vom Benutzer im Bereich **Standards und Formate** der Einstellungen für Regional- und Sprachoptionen in Systemsteuerung.        |
| *version*    | Windows Media Player Versionsnummer im folgenden Format: 10.0.x.xxxx oder 11.0.x.xxxx.                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





