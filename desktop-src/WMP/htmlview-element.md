---
title: HtmlView-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Das HtmlView-Element gibt die Basis-URL einer HtmlView-Webseite an.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- HtmlView-Element, Windows-Media Player
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f11a60e41b7f78be3440e16a7d2b3934f75e8ee3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372374"
---
# <a name="htmlview-element"></a>HtmlView-Element

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **HtmlView** -Element gibt die Basis-URL einer HtmlView-Webseite an.

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**Baseurl** (erforderlich)
</dt> <dd>

Basis-URL für die von Windows Media Player angezeigte HtmlView-Webseite.

</dd> </dl>

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Sie können dieses Element verwenden, um die HtmlView-Funktion in Ihren Online Store zu integrieren. Wenn die Domäne der URL, die im aktuellen Onlinespeicher angegeben ist, mit der Domäne der HtmlView-Webseite übereinstimmt, erfolgt die wieder **Gabe jetzt** ohne Benutzereingriff, und der HtmlView-Inhalt wird angezeigt. Andernfalls fordert Windows Media Player den Benutzer zur Eingabe der Berechtigung auf, den HtmlView-Inhalt anzuzeigen.

Wenn beispielsweise die URL für die HtmlView-Webseite lautet https://www.proseware.com/html/HTMLView.htm und die URL für das **baseurl** -Attribut als angegeben wird https://www.proseware.com , wird die HtmlView-Webseite angezeigt, ohne den Benutzer aufzufordern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Anzeigen von Webseiten in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Param-Element**](param-element.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





