---
description: Funktionsflags für die Treiber Textur Koordinate.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4973e045decd393be2f8a6d340f369761a411a44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958563"
---
# <a name="d3dtss_tci"></a>D3DTSS- \_ TCI

Funktionsflags für die Treiber Textur Koordinate.



|                                          |             |                                                                                                                                                                                                                      |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definieren                                 | Wert       | BESCHREIBUNG                                                                                                                                                                                                          |
| D3DTSS \_ TCI- \_ passthru                    | 0x00000000L | Verwenden Sie die angegebenen Texturkoordinaten, die im Scheitelpunkt Format enthalten sind. Dieser Wert wird in NULL aufgelöst.                                                                                                               |
| D3DTSS \_ TCI \_ cameraspacenormal           | 0x00010000l | Verwenden Sie den Vertex normal, transformiert in den Kamera Raum, als Eingabe Texturkoordinaten für die Textur Transformation dieses Stufen.                                                                                        |
| D3DTSS \_ TCI \_ cameraspaceposition         | 0x00020000l | Verwenden Sie die Vertex-Position, die in den Kamerabereich transformiert wird, als Eingabe Texturkoordinaten für die Textur Transformation dieser Stufe.                                                                                      |
| D3DTSS \_ TCI \_ cameraspacereflectionvector | 0x00030000l | Verwenden Sie den reflektionvektor, transformiert in den Kamera Raum, als Eingabe Textur Koordinate für die Textur Transformation dieses Stufen. Der reflektionvektor wird aus der eintexposition der Eingabe und dem normalen Vektor berechnet. |
| D3DTSS \_ TCI- \_ spheremap                   | 0x00040000l | Verwenden Sie die angegebenen Texturkoordinaten für die Kugel Zuordnung.                                                                                                                                                            |



 

Diese Konstanten werden von D3DTSS \_ texcoordindex verwendet.

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps. h |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



