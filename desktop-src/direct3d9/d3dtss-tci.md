---
description: Funktionsflags für die Treibertexturkoordinaten.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da9ca23ebc4dd121527721a9d10a2db55a4d555
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995257"
---
# <a name="d3dtss_tci"></a>D3DTSS \_ TCI

Funktionsflags für die Treibertexturkoordinaten.



| \#Definieren                                 | Wert       | BESCHREIBUNG                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DTSS \_ TCI \_ PASSTHRU                    | 0x00000000L | Verwenden Sie die angegebenen Texturkoordinaten, die im Scheitelpunktformat enthalten sind. Dieser Wert wird in 0 (null) aufgelöst.                                                                                                               |
| D3DTSS \_ TCI \_ CAMERASPACENORMAL           | 0x00010000L | Verwenden Sie die Vertexnorm, die in den Kameraraum transformiert ist, als Eingabetexturkoordinaten für die Texturtransformation dieser Phase.                                                                                        |
| D3DTSS \_ TCI \_ CAMERASPACEPOSITION         | 0x00020000L | Verwenden Sie die in den Kameraraum transformierte Scheitelpunktposition als Eingabetexturkoordinaten für die Texturtransformation dieser Phase.                                                                                      |
| D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR | 0x00030000L | Verwenden Sie den in den Kameraraum transformierten Reflektionsvektor als Eingabetexturkoordinate für die Texturtransformation dieser Phase. Der Reflektionsvektor wird aus der Eingabevertexposition und dem normalen Vektor berechnet. |
| D3DTSS \_ TCI \_ SPHEREMAP                   | 0x00040000L | Verwenden Sie die angegebenen Texturkoordinaten für die Kugelzuordnung.                                                                                                                                                            |



 

Diese Konstanten werden von D3DTSS \_ TEXCOORDINDEX verwendet.

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



