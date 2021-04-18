---
description: Normale Zuordnungs Konstanten für Zuordnungen.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37985456e81b20af9b3e4396d10045d5e58c9b7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338857"
---
# <a name="d3dx_normalmap"></a>D3DX \_ normalmap

Normale Zuordnungs Konstanten für Zuordnungen.



|                                     |                                                                                                                                                                                                    |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definieren                            | BESCHREIBUNG                                                                                                                                                                                        |
| D3DX \_ normalmap- \_ Spiegelung \_ U          | Gibt an, dass Pixel außerhalb des Kanten der Textur auf der u-Achse gespiegelt, nicht umschließt werden sollen.                                                                                                   |
| D3DX \_ normalmap- \_ Spiegelung \_ V          | Gibt an, dass die Pixel am Rand der Textur auf der v-Achse gespiegelt und nicht umschließt werden sollen.                                                                                                   |
| D3DX \_ normalmap- \_ Spiegelung             | Identisch mit der Angabe von D3DX \_ normalmap- \_ Spiegelung \_ U \| D3DX \_ normalmap- \_ Spiegel \_ V.                                                                                                                       |
| D3DX \_ normalmap \_ invertsign         | Kehrt die Richtung der einzelnen normalen um.                                                                                                                                                              |
| D3DX \_ normalmap \_ Compute- \_ oksion | Berechnet den pro-Pixel-Okklusions Begriff und codiert ihn in das Alpha. Ein Alpha von 1 bedeutet, dass das Pixel in keiner Weise verdeckt wird, und ein Alpha von 0 bedeutet, dass das Pixel vollständig verdeckt ist. |



 

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3dx9tex. h |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX-Konstanten](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[**D3DXComputeNormalMap**](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



