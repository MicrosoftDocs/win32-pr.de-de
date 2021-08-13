---
description: Schlüsselübergang
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Schlüsselübergang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fc5b905b1650b6db6bb98b542193160825b8bd6dd74626ef9bddc91b118118
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397276"
---
# <a name="key-transition"></a>Schlüsselübergang

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Der Schlüsselübergang führt die Tastenbetonung basierend auf RGB-Wert, Alphawert, Farbton oder Leuchtdichte aus.

Die folgende Abbildung zeigt den Schlüsselübergang:

![Schlüsselübergang](images/trans-key.png)

Klassen-ID (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}

CLSID-Variablenname: CLSID \_ DxtKey

Anzeigename: "DxtKey"

Eigenschaften



| Eigenschaft   | type  | Gültiger Bereich           | Beschreibung                                                                                                                                                                                                                                                | Gilt für                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Farbton        | INT   | 0–360                 | Der Farbtonwert, für den die Taste geschaltet werden soll.                                                                                                                                                                                                                             | Farbton                            |
| Invertierung     | BOOL  | **FALSE** oder **TRUE** | Boolescher Wert, der angibt, ob der Standardvorgang des Schlüssels umgekehrt werden soll. False gibt an, dass Pixel im übermäßigen Bild standardmäßig transparent gemacht werden. True gibt an, dass der Vorgang umgekehrt wird.                                                   | Chroma, Hue, Luminance, Nonred |
| KeyType    | INT   | Siehe Hinweise           | Gibt den Typ des Schlüssels an. Weitere Informationen finden Sie in den Hinweisen.                                                                                                                                                                                              | Alle                            |
| Luminance  | INT   | 0–100                 | Der Leuchtdichtewert, für den die Taste aktiviert werden soll.                                                                                                                                                                                                                       | Luminance                      |
| RGB        | DWORD | 0x0 – 0xFFFFFF        | Die Farbe, für die die Taste angezeigt werden soll. Der Wert ist eine Hexadezimalzahl im Format 0x *RRGGBB,* wobei *RR* der rote Wert, *GG* der grüne Wert und *BB* der blaue Wert ist. (Reines Rot, Grün und Blau sind 0xFF0000, 0x00FF00 bzw. 0x0000FF.) | Chroma                         |
| Ähnlichkeit | INT   | 0–100                 | Der Bereich von Farbdaten, der transparent wird. Bei höheren Werten ist ein größerer Bereich ähnlicher Farben transparent.                                                                                                                                        | Aus, Nicht 10                 |



 

## <a name="remarks"></a>Hinweise

Der Typ des ausgeführten Schlüssels hängt vom Wert der **KeyType-Eigenschaft** ab, der einer der folgenden sein muss:



| Wert | Enumeration       | Beschreibung                                           |
|-------|-------------------|-------------------------------------------------------|
| 0     | DXTKEY \_ RGB       | Schlüssel des Schlüssels (Schlüssel nach RGB-Wert).                        |
| 1     | DXTKEY \_ NONRED    | Nicht beredter Schlüssel. (Macht blaue und grüne Bereiche transparent.) |
| 2     | DXTKEY \_ LUMINANCE | Luminance-Schlüssel.                                        |
| 3     | DXTKEY \_ ALPHA     | Schlüssel nach Alphawert.                                   |
| 4     | DXTKEY \_ HUE       | Schlüssel nach Farbton.                                           |



 

Der Schlüsseltyp ist standardmäßig DXTKEY \_ ALPHA.

 

 



