---
description: Besteht aus einem Index Parameter und einer RGBA-Farbe und wird zum Definieren von Gitter Scheitelpunkt Farben verwendet. Der Index definiert den Scheitelpunkt, auf den die Farbe angewendet wird.
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: Indexedcolor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895cf56efedfa7214bcfa6acafd32ab9324bbe8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341708"
---
# <a name="indexedcolor"></a>Indexedcolor

Besteht aus einem Index Parameter und einer RGBA-Farbe und wird zum Definieren von Gitter Scheitelpunkt Farben verwendet. Der Index definiert den Scheitelpunkt, auf den die Farbe angewendet wird.

``` syntax
template IndexedColor
{
    < 1630B820-7842-11cf-8F52-0040333594A3 >
    DWORD index;
    ColorRGBA indexColor;
} 
```

Hierbei gilt:

-   Index-A DWORD. Siehe oben genannte Beschreibung.
-   indexcolor: eine colorrgba-Vorlage. Siehe [**colorrgba**](colorrgba.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



