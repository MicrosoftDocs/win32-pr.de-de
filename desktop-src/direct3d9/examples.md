---
description: Es folgen zwei Binärvorlagendefinitionen und ein Beispiel für ein binäres Datenobjekt.
ms.assetid: vs|directx_sdk|~\examples.htm
title: Beispiele (Direct3D 9-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8b8e2a9c500042e9b8d7c7fd911ab74b2f428d1ef814aca9e5fda1be7dcab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523097"
---
# <a name="examples-direct3d-9-graphics"></a>Beispiele (Direct3D 9-Grafiken)

Es folgen zwei Binärvorlagendefinitionen und ein Beispiel für ein binäres Datenobjekt.

> [!Note]  
> Daten werden im Little-Endian-Format gespeichert, was in diesen Beispielen nicht gezeigt wird.

 

Die geschlossene Rgb-Vorlage wird durch die UUID {55b6d780-37ec-11d0-ab39-0020af71e433} identifiziert und verfügt über drei Member : r, g und b – jeweils vom Typ float.


```
TOKEN_TEMPLATE, TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_OBRACE,
TOKEN_GUID, 55b6d780, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_FLOAT, TOKEN_NAME, 1, 'r', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'g', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'b', TOKEN_SEMICOLON,
TOKEN_CBRACE
```



Die geschlossene Vorlage Matrix4x4 wird durch die UUID {55b6d781-37ec-11d0-ab39-0020af71e433} identifiziert und verfügt über ein Element vom Typ float – ein zweidimensionales Array mit dem Namen matrix.


```
TOKEN_TEMPLATE, TOKEN_NAME, 9, 'M', 'a', 't', 'r', 'i', 'x', '4', 'x', '4', TOKEN_OBRACE,
TOKEN_GUID, 55b6d781, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_ARRAY, TOKEN_FLOAT, TOKEN_NAME, 6, 'm', 'a', 't', 'r', 'i', 'x',
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_CBRACE
```



Das folgende binäre Datenobjekt zeigt eine Instanz der zuvor definierten RGB-Vorlage. Das Beispielobjekt hat den Namen blue, und seine drei Member – r, g und b – haben die Werte 0.0, 0.0 bzw. 1.0.


```
TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_NAME, 4, 'b', 'l', 'u', 'e', TOKEN_OBRACE,
TOKEN_FLOAT_LIST, 3, 0.0, 0.0, 1.0, TOKEN_CBRACE
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Binärcodierung](binary-encoding.md)
</dt> </dl>

 

 



