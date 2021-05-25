---
description: Die folgenden Flags werden verwendet, um anzugeben, welche Kanäle in einer Textur verwendet werden sollen.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c83fd0b3e12d6b5bccb13f9c5fab5e078587dbd4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342865"
---
# <a name="d3dx_filter"></a>\_D3DX-FILTER

Die folgenden Flags werden verwendet, um anzugeben, welche Kanäle in einer Textur verwendet werden sollen.



| \#Definieren                | BESCHREIBUNG                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX \_ FILTER \_ NONE      | Es erfolgt keine Skalierung oder Filterung. Pixel außerhalb der Grenzen des Quellbilds werden als transparent schwarz angenommen.                                                                                 |
| \_D3DX-FILTERPUNKT \_     | Jedes Zielpixel wird berechnet, indem das nächste Pixel aus dem Quellbild entnommen wird.                                                                                                                     |
| D3DX \_ FILTER \_ LINEAR    | Jedes Zielpixel wird berechnet, indem die vier nächsten Pixel aus dem Quellbild entnommen werden. Dieser Filter funktioniert am besten, wenn die Skala auf beiden Achsen kleiner als zwei ist.                                          |
| \_D3DX-FILTERDREIECK \_  | Jedes Pixel im Quellbild trägt gleichermaßen zum Zielbild bei. Dies ist der langsamste Filter.                                                                                           |
| \_D3DX-FILTERFELD \_       | Jedes Pixel wird berechnet, indem der Mittelwert eines 2x2(x2)-Felds von Pixeln aus dem Quellbild berechnet wird. Dieser Filter funktioniert nur, wenn die Abmessungen des Ziels halb so sind wie bei Mipmaps. |
| \_D3DX-FILTERSPIEGELUNG \_ \_ U | Pixel vom Rand der Textur auf der U-Achse sollten gespiegelt und nicht umschlossen werden.                                                                                                                           |
| \_D3DX-FILTERSPIEGELUNG \_ \_ V | Pixel vom Rand der Textur auf der V-Achse sollten gespiegelt und nicht umschlossen werden.                                                                                                                           |
| \_D3DX-FILTERSPIEGELUNG \_ \_ W | Pixel vom Rand der Textur auf der W-Achse sollten gespiegelt und nicht umschlossen werden.                                                                                                                           |
| \_D3DX-FILTERSPIEGELUNG \_    | Die Angabe dieses Flags ist identisch mit der Angabe der Flags D3DX \_ FILTER \_ MIRROR \_ U, D3DX FILTER MIRROR V und \_ \_ \_ D3DX \_ FILTER MIRROR \_ \_ W.                                                                     |
| D3DX \_ FILTER \_ DITHER    | Das resultierende Bild muss mithilfe eines 4x4-geordneten Ditheralgorithmus gedithert werden.                                                                                                                                  |
| D3DX \_ FILTER \_ SRGB \_ IN  | Die Eingabedaten sind im sRGB-Farbraum (Gamma 2,2) gespeichert.                                                                                                                                                              |
| D3DX \_ FILTER \_ SRGB \_ OUT | Die Ausgabedaten werden im sRGB-Farbraum (Gamma 2.2) angezeigt.                                                                                                                                                         |
| D3DX \_ FILTER \_ SRGB      | Identisch mit der Angabe von D3DX \_ FILTER \_ SRGB \_ IN \| D3DX \_ FILTER \_ SRGB \_ OUT.                                                                                                                                       |



 

Jeder gültige Filter muss genau eines der folgenden Flags enthalten: D3DX \_ FILTER \_ NONE, D3DX \_ FILTER \_ POINT, D3DX \_ FILTER \_ LINEAR, D3DX \_ FILTER TRIANGLE oder \_ D3DX \_ FILTER \_ BOX. Darüber hinaus können Sie den OR-Operator verwenden, um null oder mehr der folgenden optionalen Flags mit einem gültigen Filter anzugeben: D3DX \_ FILTER \_ MIRROR \_ U, D3DX \_ FILTER MIRROR \_ \_ V, D3DX \_ FILTER MIRROR \_ \_ W, D3DX \_ FILTER \_ MIRROR, D3DX \_ FILTER \_ DITHER, D3DX \_ FILTER \_ SRGB \_ IN, D3DX FILTER SRGB OUT oder \_ \_ \_ D3DX \_ FILTER \_ SRGB.

Die Angabe von D3DX DEFAULT für diesen Parameter entspricht normalerweise der Angabe von \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER. D3DX DEFAULT kann jedoch unterschiedliche Bedeutungen haben, je \_ nachdem, welche Methode den Filter verwendet. Beispiel:

-   Bei Verwendung [**von D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)wird D3DX \_ DEFAULT D3DX \_ FILTER TRIANGLE \_ \| D3DX \_ FILTER \_ DITHERzugestellt.
-   Bei Verwendung von [**D3DXFilterTexture**](d3dxfiltertexture.md)wird D3DX \_ DEFAULT D3DX \_ FILTER BOX \_ zugeordnet, wenn die Texturgröße eine Potenz von zwei hat, und D3DX \_ FILTER BOX \_ \| D3DX \_ FILTER \_ DITHER andernfalls .

Verweisen Sie auf jede Methode, um nach Informationen zur Zuordnung des D3DX \_ DEFAULT-Filters zu suchen.

## <a name="constant-information"></a>Konstanteninformationen



| Anforderung                         | Wert           |
|--------------------------|------------|
| Header                   | d3dx9tex.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX-Konstanten](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



