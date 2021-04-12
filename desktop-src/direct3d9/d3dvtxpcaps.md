---
description: Eine Kombination aus einem oder mehreren Flags, die das Erstellungs Verhalten des Geräts steuern.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2ffff3d1dcc1f68912847b9ce1677c2031189c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393206"
---
# <a name="d3dvtxpcaps"></a>D3DVTXPCAPS

Eine Kombination aus einem oder mehreren Flags, die das Erstellungs Verhalten des Geräts steuern.



|                                         |                                                                                                                                                                                                    |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definieren                                | BESCHREIBUNG                                                                                                                                                                                        |
| D3DVTXPCAPS \_ DirectionalLights          | Das Gerät kann direktionale Lichter ausführen.                                                                                                                                                                  |
| D3DVTXPCAPS \_ localviewer                | Das Gerät kann den lokalen Viewer ausführen.                                                                                                                                                                        |
| D3DVTXPCAPS \_ MATERIALSOURCE7            | Wenn diese Obergrenze festgelegt ist, unterstützt das Gerät die Farb Materialzustände: D3DRS \_ AmbientMaterialSource, D3DRS \_ DiffuseMaterialSource, D3DRS \_ emissivematerialsource und D3DRS \_ SpecularMaterialSource. |
| D3DVTXPCAPS \_ keine \_ TEXGEN- \_ nonlocalviewer | Das Gerät unterstützt keine Textur Generierung im nicht lokalen Viewer-Modus.                                                                                                                               |
| D3DVTXPCAPS \_ positionallights           | Das Gerät kann Positionsleuchten (einschließlich Punkt und Punkt) verwenden.                                                                                                                                         |
| D3DVTXPCAPS \_ TEXGEN                     | Das Gerät kann TEXGEN ausführen.                                                                                                                                                                              |
| D3DVTXPCAPS \_ TEXGEN- \_ spheremap          | Das Gerät unterstützt D3DTSS \_ TCI \_ sphiermap.                                                                                                                                                            |
| D3DVTXPCAPS- \_ twiening                   | Das Gerät kann Vertex-twiening durchführen.                                                                                                                                                                     |



 

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps. h |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



