---
description: Besteht aus einem Indexparameter und einer RGBA-Farbe und wird zum Definieren von Gittervertexfarben verwendet. Der Index definiert den Scheitelpunkt, auf den die Farbe angewendet wird.
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: IndexedColor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b0dcaf850786a18e5fc317276939436b93c3a49765d520aa40f88cd53707d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563730"
---
# <a name="indexedcolor"></a>IndexedColor

Besteht aus einem Indexparameter und einer RGBA-Farbe und wird zum Definieren von Gittervertexfarben verwendet. Der Index definiert den Scheitelpunkt, auf den die Farbe angewendet wird.

``` syntax
template IndexedColor
{
    < 1630B820-7842-11cf-8F52-0040333594A3 >
    DWORD index;
    ColorRGBA indexColor;
} 
```

Hierbei gilt:

-   index: Ein DWORD. Weitere Informationen finden Sie in der obigen Beschreibung.
-   indexColor: Eine ColorRGBA-Vorlage. Weitere Informationen finden Sie unter [**ColorRGBA**](colorrgba.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



