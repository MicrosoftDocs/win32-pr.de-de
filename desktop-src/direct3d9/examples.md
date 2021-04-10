---
description: Es folgen zwei Beispiele für binäre Vorlagen Definitionen und ein Beispiel für ein binäres Datenobjekt.
ms.assetid: vs|directx_sdk|~\examples.htm
title: Beispiele (Direct3D 9-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fbb8cbe45881243e17f80fd302c0fb4640685
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124490"
---
# <a name="examples-direct3d-9-graphics"></a>Beispiele (Direct3D 9-Grafiken)

Es folgen zwei Beispiele für binäre Vorlagen Definitionen und ein Beispiel für ein binäres Datenobjekt.

> [!Note]  
> Die Daten werden im Little-Endian-Format gespeichert, das in diesen Beispielen nicht angezeigt wird.

 

Die geschlossene Vorlage RGB wird durch die UUID {55b6d780-37ec-11D0-ab39-0020af71e433} identifiziert und verfügt über die drei Member-r, g und b-jeweils den Typ float.


```
TOKEN_TEMPLATE, TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_OBRACE,
TOKEN_GUID, 55b6d780, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_FLOAT, TOKEN_NAME, 1, 'r', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'g', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'b', TOKEN_SEMICOLON,
TOKEN_CBRACE
```



Die geschlossene Vorlage Matrix4x4 wird von der UUID {55b6d781-37ec-11D0-ab39-0020af71e433} identifiziert und verfügt über einen Member, d. h. ein zweidimensionales Array mit dem Namen "Matrix" vom Typ "float".


```
TOKEN_TEMPLATE, TOKEN_NAME, 9, 'M', 'a', 't', 'r', 'i', 'x', '4', 'x', '4', TOKEN_OBRACE,
TOKEN_GUID, 55b6d781, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_ARRAY, TOKEN_FLOAT, TOKEN_NAME, 6, 'm', 'a', 't', 'r', 'i', 'x',
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_CBRACE
```



Das folgende binäre Datenobjekt zeigt eine Instanz der RGB-Vorlage an, die zuvor definiert wurde. Das Beispiel Objekt hat den Namen Blue und seine drei Member-r, g und b-besitzen die Werte 0,0, 0,0 und 1,0.


```
TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_NAME, 4, 'b', 'l', 'u', 'e', TOKEN_OBRACE,
TOKEN_FLOAT_LIST, 3, 0.0, 0.0, 1.0, TOKEN_CBRACE
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Binärcodierung](binary-encoding.md)
</dt> </dl>

 

 



