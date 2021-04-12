---
description: Die folgenden Flags werden verwendet, um anzugeben, auf welchen Kanälen in einer Textur gearbeitet werden soll.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 128525de2e403c11239c300372b79bd8ee8c1277
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481307"
---
# <a name="d3dx_filter"></a>D3DX- \_ Filter

Die folgenden Flags werden verwendet, um anzugeben, auf welchen Kanälen in einer Textur gearbeitet werden soll.



|                         |                                                                                                                                                                                                             |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definieren                | BESCHREIBUNG                                                                                                                                                                                                 |
| D3DX \_ Filter \_ None      | Es findet keine Skalierung oder Filterung statt. Es wird davon ausgegangen, dass Pixel außerhalb der Begrenzungen des Quell Bilds transparent schwarz sind.                                                                                 |
| D3DX- \_ Filter \_ Punkt     | Jedes Zielpixel wird berechnet, indem das nächste Pixel aus dem Quell Image entnommen wird.                                                                                                                     |
| D3DX- \_ Filter \_ linear    | Jedes Zielpixel wird berechnet, indem die vier nächsten Pixel aus dem Quell Image entnommen werden. Dieser Filter funktioniert am besten, wenn die Skala auf beiden Achsen kleiner als zwei ist.                                          |
| D3DX \_ Filter \_ Dreieck  | Jedes Pixel im Quell Image trägt gleichermaßen dem Ziel Image bei. Dies ist der langsamste der Filter.                                                                                           |
| D3DX \_ Filter \_ Feld       | Jedes Pixel wird berechnet, indem das Feld 2 x 2 (x2) aus dem Quell Abbild durchläuft. Dieser Filter kann nur verwendet werden, wenn die Abmessungen des Ziels die Hälfte der der Quelle sind, wie es bei MipMaps der Fall ist. |
| D3DX \_ Filter \_ Spiegelung \_ U | Pixel am Rand der Textur auf der u-Achse sollten gespiegelt, nicht umschließt werden.                                                                                                                           |
| D3DX \_ Filter \_ Spiegelung \_ V | Pixel am Rand der Textur auf der v-Achse sollten gespiegelt und nicht umschließt werden.                                                                                                                           |
| D3DX \_ Filter \_ Spiegelung \_ | Pixel am Rand der Textur auf der w-Achse sollten gespiegelt, nicht umschließt werden.                                                                                                                           |
| D3DX- \_ Filter \_ Spiegelung    | Die Angabe dieses Flags ist identisch mit dem Angeben der D3DX \_ Filter \_ Mirror \_ U, D3DX \_ Filter \_ Spiegel \_ V und D3DX \_ Filter \_ Mirror \_ W-Flags.                                                                     |
| D3DX \_ Filter \_ Dither    | Das resultierende Bild muss mit einem 4 x 4-geordneten Dithering-Algorithmus ausgeblendet werden.                                                                                                                                  |
| D3DX \_ \_ sRGB Filtern \_ in  | Die Eingabedaten befinden sich im sRGB-Farbraum (Gamma 2,2).                                                                                                                                                              |
| D3DX \_ filtert \_ sRGB \_ out | Die Ausgabedaten befinden sich im sRGB-Farbraum (Gamma 2,2).                                                                                                                                                         |
| D3DX \_ \_ sRGB Filtern      | Identisch \_ \_ mit der Angabe von D3DX Filter sRGB \_ in \| D3DX \_ Filter \_ sRGB \_ out.                                                                                                                                       |



 

Jeder gültige Filter muss genau eines der folgenden Flags enthalten: D3DX \_ Filter \_ None, D3DX \_ Filter \_ Point, D3DX \_ Filter \_ linear, D3DX \_ Filter \_ Dreieck oder D3DX \_ Filter \_ Box. Außerdem können Sie mit dem-Operator oder dem-Operator NULL oder mehr der folgenden optionalen Flags mit einem gültigen Filter angeben: D3DX \_ Filter \_ Mirror \_ U, D3DX \_ Filter \_ Mirror \_ V, D3DX \_ Filter \_ Mirror \_ W, D3DX \_ Filter \_ Mirror, D3DX \_ Filter \_ Dither, D3DX \_ Filter \_ sRGB \_ in, D3DX \_ Filter \_ sRGB \_ out oder D3DX \_ Filter \_ sRGB.

Das angeben \_ von D3DX default für diesen Parameter entspricht in der Regel der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither. D3DX \_ Default kann jedoch unterschiedliche Bedeutungen haben, je nachdem, welche Methode den Filter verwendet. Beispiel:

-   Bei Verwendung von [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)wird D3DX \_ standardmäßig D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither zugeordnet.
-   Wenn Sie [**D3DXFilterTexture**](d3dxfiltertexture.md)verwenden, \_ wird D3DX standardmäßig D3DX \_ Filter Box zugeordnet, \_ Wenn die Textur Größe eine Potenz von zwei ist, und D3DX \_ Filter \_ Box \| D3DX \_ Filter \_ anderenfalls.

Verweisen Sie auf jede Methode, um Informationen dazu zu finden, wie D3DX \_ default Filter zugeordnet ist.

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3dx9tex. h |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX-Konstanten](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



