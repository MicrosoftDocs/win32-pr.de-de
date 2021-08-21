---
title: HTMLView-Element
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Das HTMLView-Element gibt die Basis-URL einer HTMLView-Webseite an.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- HTMLView-Element Windows Media Player
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 703668427757df19675734e1503296a8a7144517801d0e8fdc0fadb25a16b0a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054888"
---
# <a name="htmlview-element"></a>HTMLView-Element

> [!Note]  
> In diesem Abschnitt werden funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **HTMLView-Element** gibt die Basis-URL einer HTMLView-Webseite an.

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (erforderlich)
</dt> <dd>

Basis-URL für die HTMLView-Webseite, die Windows Media Player angezeigt wird.

</dd> </dl>

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Sie können dieses Element verwenden, um das HTMLView-Feature in Ihren Onlineshop zu integrieren. Wenn die Domäne der vom aktuellen Onlineshop angegebenen URL mit der Domäne für die HTMLView-Webseite übereinstimmt, erfolgt der Wechsel zu **Jetzt wiedergeben** ohne Benutzereingriff, und der HTMLView-Inhalt wird angezeigt. Andernfalls fordert Windows Media Player den Benutzer zur Eingabe der Berechtigung zum Anzeigen des HTMLView-Inhalts auf.

Wenn beispielsweise die URL für die HTMLView-Webseite https://www.proseware.com/html/HTMLView.htm lautet und die URL für das **BaseURL-Attribut** als angegeben https://www.proseware.com ist, wird die HTMLView-Webseite ohne Aufforderung des Benutzers angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Anzeigen von Webseiten in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für ein Online-Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für ein Online-Store vom Typ 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**PARAM-Element**](param-element.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





