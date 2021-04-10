---
description: Schlüssel Übergang
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Schlüssel Übergang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e4f83bbe26f49989d612efe718c2d838ce7f1d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860095"
---
# <a name="key-transition"></a>Schlüssel Übergang

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Der Schlüssel Übergang führt die Schlüssel Erstellung basierend auf RGB-Wert, Alpha-Wert, Farbton oder Leuchtkraft durch.

Die folgende Abbildung zeigt den Schlüssel Übergang:

![Schlüssel Übergang](images/trans-key.png)

Klassen-ID (CLSID): {C5B19592-145E-11d3-9F04-006008039E37}

CLSID-Variablen Name: CLSID \_ dxtkey

Anzeige Name: "dxtkey"

Eigenschaften



| Eigenschaft   | type  | Gültiger Bereich           | BESCHREIBUNG                                                                                                                                                                                                                                                | Gilt für                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Farbton        | INT   | 0 – 360                 | Der Farbton Wert, für den der Schlüssel angezeigt werden soll.                                                                                                                                                                                                                             | Farbton                            |
| Invertierung     | BOOL  | **False** oder **true** | Boolescher Wert, der angibt, ob die Standardoperation des Schlüssels umgekehrt werden soll. Wenn der Wert **false** ist, werden die Pixel im überliegenden Bild standardmäßig transparent gemacht. Wenn **true**, kehrt der Vorgang um.                                                   | Chroma, Hue, Leuchtkraft, nicht rot |
| KeyType    | INT   | Siehe Hinweise           | Gibt den Typ des Schlüssels an. Weitere Informationen finden Sie in den Hinweisen.                                                                                                                                                                                              | Alle                            |
| Luminance  | INT   | 0 – 100                 | Der Wert für die Leuchtkraft, auf den der Schlüssel fest.                                                                                                                                                                                                                       | Luminance                      |
| RGB        | DWORD | 0x0 – 0xffffff        | Die Farbe, in der der Schlüssel angezeigt werden soll. Der Wert ist eine hexadezimale Zahl mit dem Format 0x *RRGGBB*, wobei *RR* der rote Wert, *GG* der grüne Wert und *BB* der blaue Wert ist. (Rein rot, grün und blau sind 0xFF0000, 0x00FF00 bzw. 0x0000FF.) | Chroma                         |
| Ähnlichkeit | INT   | 0 – 100                 | Der Bereich der Farbdaten, der transparent wird. Bei höheren Werten ist eine größere Anzahl ähnlicher Farben transparent.                                                                                                                                        | Chroma, nicht rot                 |



 

## <a name="remarks"></a>Bemerkungen

Der Typ des Schlüssels, der ausgeführt wird, hängt vom Wert der **KeyType** -Eigenschaft ab, die einen der folgenden Werte aufweisen muss:



| Wert | Enumeration       | Beschreibung                                           |
|-------|-------------------|-------------------------------------------------------|
| 0     | dxtkey \_ RGB       | Chroma-Schlüssel (Schlüssel nach RGB-Wert).                        |
| 1     | dxtkey \_ nicht rot    | Nicht-rote Taste. (Macht blaue und grüne Bereiche transparent.) |
| 2     | dxtkey- \_ Leuchtkraft | Der Schlüssel für die Leuchtkraft.                                        |
| 3     | dxtkey \_ Alpha     | Schlüssel nach Alpha Wert.                                   |
| 4     | dxtkey- \_ Farbton       | Schlüssel nach Farbton.                                           |



 

Der Schlüsseltyp ist standardmäßig dxtkey \_ alpha.

 

 



