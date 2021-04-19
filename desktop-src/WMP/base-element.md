---
title: Basis Element
description: Das Basiselement definiert eine URL-Zeichenfolge, die an den Anfang der an Windows Media Player gesendeten URLs angehängt ist.
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- Windows-Basis Element Media Player
topic_type:
- apiref
api_name:
- BASE Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44b62a24f73ed6cf78820efe1ca76e0eccd3fb59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372651"
---
# <a name="base-element"></a>Basis Element

Das **Basis** Element definiert eine URL-Zeichenfolge, die an den Anfang der an Windows Media Player gesendeten URLs angehängt ist.

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attribute

**Href** (erforderlich)

Die Zeichenfolge, die an den Anfang an die an Windows Media Player gesendeten URLs angehängt wird. Der Standardwert ist die NULL-Zeichenfolge ("").

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente           |
|-----------------|--------------------|
| Übergeordnete Elemente | **ASX**, **Eintrag** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element definiert eine URL-Zeichenfolge, die an den Anfang der URL-Flip-URLs angehängt wird, die an Windows Media Player gesendet werden Beim URL-Flipping handelt es sich um einen Skript Mechanismus, der bewirkt, dass Windows Media Player eine neue URL in einem Browser-oder Browser Rahmen öffnet, wenn ein Skript Befehl empfangen wird.

Das **Basis** Element ähnelt einem Basisverzeichnis für relative Links. Sie wirkt sich nur auf URLs aus, die mithilfe von Skript Befehlen als Teil des Inhaltsdaten Stroms gesendet werden, der in Windows Media Player abgespielt wird.

Ein **Basis** Element, das als untergeordnetes Element eines **ASX** -Elements definiert ist, wird zum Standardwert für die gesamte Metadatendatei. Ein **Basis** Element, das in einem **Entry** -Element definiert ist, überschreibt jedes **Basis** Element im übergeordneten **ASX** -Element (nur für dieses **Eintrags** Element).

> [!Note]  
> Wenn das **href** -Attribut nicht mit einem/-Zeichen endet, fügt Windows Media Player ein an das Ende der Zeichenfolge an.

 

## <a name="examples"></a>Beispiele


```XML
<BASE HREF="https://msdn.microsoft.com/" />

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





