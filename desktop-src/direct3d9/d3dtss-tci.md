---
description: Treibertexturkoordinatenfunktionsflags.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f954020f80a8c980316e71f22f75ad47616e071d460d1c4a6c13e762ab3df462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750600"
---
# <a name="d3dtss_tci"></a>D3DTSS \_ TCI

Treibertexturkoordinatenfunktionsflags.



| \#Definieren                                 | Wert       | Beschreibung                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DTSS \_ TCI \_ PASSTHRU                    | 0x00000000L | Verwenden Sie die angegebenen Texturkoordinaten, die im Scheitelpunktformat enthalten sind. Dieser Wert wird in 0 (null) gelöst.                                                                                                               |
| D3DTSS \_ TCI \_ CAMERASPACENORMAL           | 0x00010000L | Verwenden Sie den Scheitelpunkt normal, transformiert in den Kameraraum, als Eingabetexturkoordinaten für die Texturtransformation dieser Phase.                                                                                        |
| D3DTSS \_ TCI \_ CAMERASPACEPOSITION         | 0x00020000L | Verwenden Sie die Scheitelpunktposition, transformiert in den Kameraraum, als Eingabetexturkoordinaten für die Texturtransformation dieser Stufe.                                                                                      |
| D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR | 0x00030000L | Verwenden Sie den Reflektionsvektor, der in den Kameraraum transformiert wird, als Eingabetexturkoordinate für die Texturtransformation dieser Phase. Der Reflektionsvektor wird aus der Position des Eingabe-Scheitelpunkts und dem normalen Vektor berechnet. |
| D3DTSS \_ TCI \_ SPHEREMAP                   | 0x00040000L | Verwenden Sie die angegebenen Texturkoordinaten für die Kugelzuordnung.                                                                                                                                                            |



 

Diese Konstanten werden von D3DTSS \_ TEXCOORDINDEX verwendet.

## <a name="constant-information"></a>Konstante Informationen



|  Anforderung                        | Wert           |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



