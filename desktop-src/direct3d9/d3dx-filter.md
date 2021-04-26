---
description: Die folgenden Flags werden verwendet, um anzugeben, welche Kanäle in einer Textur verwendet werden sollen.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6e1ab3ab51a73277da685b7ac562e84d1b94a9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997327"
---
# <a name="d3dx_filter"></a>\_D3DX-FILTER

Die folgenden Flags werden verwendet, um anzugeben, welche Kanäle in einer Textur verwendet werden sollen.



| \#Definieren                | BESCHREIBUNG                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX \_ FILTER \_ NONE      | Es erfolgt keine Skalierung oder Filterung. Pixel außerhalb der Grenzen des Quellbilds werden als transparent schwarz angenommen.                                                                                 |
| D3DX-FILTERPUNKT \_ \_     | Jedes Zielpixel wird durch Sampling des nächstgelegenen Pixels aus dem Quellbild berechnet.                                                                                                                     |
| D3DX-FILTER \_ \_ LINEAR    | Jedes Zielpixel wird durch Sampling der vier nächstgelegenen Pixel aus dem Quellbild berechnet. Dieser Filter funktioniert am besten, wenn die Skalierung auf beiden Achsen kleiner als zwei ist.                                          |
| \_D3DX-FILTERDREIECK \_  | Jedes Pixel im Quellbild trägt gleichermaßen zum Zielbild bei. Dies ist die langsamste der Filter.                                                                                           |
| D3DX-FILTERFELD \_ \_       | Jedes Pixel wird berechnet, indem ein 2x2(x2)-Feld aus Pixeln aus dem Quellbild durchschnittlich berechnet wird. Dieser Filter funktioniert nur, wenn die Dimensionen des Ziels die Hälfte der Quelldimensionen sind, wie dies bei Mipmaps der Fall ist. |
| D3DX-FILTERSPIEGELUNG \_ \_ \_ U | Pixel am Rand der Textur auf der U-Achse sollten gespiegelt und nicht umschlossen werden.                                                                                                                           |
| \_D3DX-FILTERSPIEGELUNG \_ \_ V | Pixel am Rand der Textur auf der V-Achse sollten gespiegelt und nicht umschlossen werden.                                                                                                                           |
| \_D3DX-FILTERSPIEGELUNG \_ \_ W | Pixel am Rand der Textur auf der W-Achse sollten gespiegelt und nicht umschlossen werden.                                                                                                                           |
| \_D3DX-FILTERSPIEGELUNG \_    | Die Angabe dieses Flags entspricht der Angabe der W-Flags D3DX \_ FILTER \_ MIRROR \_ U, D3DX FILTER MIRROR V und \_ \_ \_ D3DX \_ FILTER \_ \_ MIRROR.                                                                     |
| D3DX \_ FILTER \_ DITHER    | Das resultierende Bild muss mithilfe eines 4x4-geordneten Ditheralgorithmus geblendet werden.                                                                                                                                  |
| D3DX \_ FILTER \_ SRGB \_ IN  | Die Eingabedaten sind im Farbraum sRGB (gamma 2.2) enthalten.                                                                                                                                                              |
| D3DX \_ FILTER \_ SRGB \_ OUT | Die Ausgabedaten sind im Farbraum sRGB (Gamma 2,2) enthalten.                                                                                                                                                         |
| D3DX \_ FILTER \_ SRGB      | Entspricht der Angabe von D3DX \_ FILTER \_ SRGB \_ IN \| D3DX \_ FILTER \_ SRGB \_ OUT.                                                                                                                                       |



 

Jeder gültige Filter muss genau eines der folgenden Flags enthalten: D3DX \_ FILTER \_ NONE, D3DX \_ FILTER \_ POINT, D3DX \_ FILTER \_ LINEAR, D3DX \_ FILTER TRIANGLE oder \_ D3DX \_ FILTER \_ BOX. Darüber hinaus können Sie den OR-Operator verwenden, um null oder mehr der folgenden optionalen Flags mit einem gültigen Filter anzugeben: D3DX \_ FILTER \_ MIRROR \_ U, D3DX \_ FILTER MIRROR \_ \_ V, D3DX \_ FILTER MIRROR \_ \_ W, D3DX \_ FILTER \_ MIRROR, D3DX \_ FILTER \_ DITHER, D3DX \_ FILTER \_ SRGB \_ IN, D3DX \_ FILTER \_ SRGB OUT oder \_ D3DX \_ FILTER \_ SRGB.

Die Angabe von D3DX \_ DEFAULT für diesen Parameter entspricht in der Regel der Angabe von D3DX FILTER TRIANGLE \_ \_ \| D3DX \_ FILTER \_ DITHER. D3DX DEFAULT kann jedoch \_ unterschiedliche Bedeutungen haben, je nachdem, welche Methode den Filter verwendet. Beispiel:

-   Bei Verwendung von [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)wird D3DX \_ DEFAULT D3DX \_ FILTER TRIANGLE \_ \| D3DX \_ FILTER \_ DITHER zugeordnet.
-   Bei Verwendung von [**D3DXFilterTexture**](d3dxfiltertexture.md)wird D3DX DEFAULT D3DX FILTER BOX zugestellt, wenn die Texturgröße eine Zweierleistung hat, andernfalls \_ \_ \_ D3DX \_ FILTER BOX \_ \| D3DX \_ FILTER \_ DITHER.

Verweisen Sie auf jede Methode, um nach Informationen zur Zuordnung des D3DX \_ DEFAULT-Filters zu prüfen.

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3dx9tex.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX-Konstanten](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



