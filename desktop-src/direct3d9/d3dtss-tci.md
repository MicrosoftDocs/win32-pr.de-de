---
description: Treibertexturkoordinatenfunktionsflags.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58746f17eb18b679a4dfe4957ac46236baeec35d
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342975"
---
# <a name="d3dtss_tci"></a>D3DTSS \_ TCI

Treibertexturkoordinatenfunktionsflags.



| \#Definieren                                 | Wert       | BESCHREIBUNG                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DTSS \_ TCI \_ PASSTHRU                    | 0x00000000L | Verwenden Sie die angegebenen Texturkoordinaten, die im Scheitelpunktformat enthalten sind. Dieser Wert wird in 0 (null) gelöst.                                                                                                               |
| D3DTSS \_ TCI \_ CAMERASPACENORMAL           | 0x00010000L | Verwenden Sie den Scheitelpunkt normal, transformiert in den Kameraraum, als Eingabetexturkoordinaten für die Texturtransformation dieser Phase.                                                                                        |
| D3DTSS \_ TCI \_ CAMERASPACEPOSITION         | 0x00020000L | Verwenden Sie die Scheitelpunktposition, transformiert in den Kameraraum, als Eingabetexturkoordinaten für die Texturtransformation dieser Stufe.                                                                                      |
| D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR | 0x00030000L | Verwenden Sie den Reflektionsvektor, der in den Kameraraum transformiert wird, als Eingabetexturkoordinate für die Texturtransformation dieser Stufe. Der Reflektionsvektor wird aus der Position des Eingabe-Scheitelpunkts und dem normalen Vektor berechnet. |
| D3DTSS \_ TCI \_ SPHEREMAP                   | 0x00040000L | Verwenden Sie die angegebenen Texturkoordinaten für die Kugelzuordnung.                                                                                                                                                            |



 

Diese Konstanten werden von D3DTSS \_ TEXCOORDINDEX verwendet.

## <a name="constant-information"></a>Konstanteninformationen



|  Anforderung                        | Wert           |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



