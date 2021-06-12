---
description: Erfahren Sie mehr über eine Kombination aus einem oder mehreren Flags, die das Geräteerstellungsverhalten in der D3DVTXPCAPS-Konstante steuern.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b544f3e4a69de23607366832aca110e42c61d6d
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011083"
---
# <a name="d3dvtxpcaps"></a>D3DVTXPCAPS

Eine Kombination aus einem oder mehreren Flags, die das Erstellungsverhalten des Geräts steuern.



| \#Definieren                                | Beschreibung                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DVTXPCAPS \_ DIRECTIONALLIGHTS          | Das Gerät kann gerichtete Beleuchtungen durchführen.                                                                                                                                                                  |
| D3DVTXPCAPS \_ LOCALVIEWER                | Das Gerät kann den lokalen Viewer verwenden.                                                                                                                                                                        |
| D3DVTXPCAPS \_ MATERIALSOURCE7            | Wenn diese Obergrenze festgelegt ist, unterstützt das Gerät die Farbmaterialzustände D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE und D3DRS \_ SPECULARMATERIALSOURCE. |
| D3DVTXPCAPS \_ NO \_ TEXGEN \_ NONLOCALVIEWER | Das Gerät unterstützt keine Texturgenerierung im nicht lokalen Viewermodus.                                                                                                                               |
| D3DVTXPCAPS \_ POSITIONALLIGHTS           | Das Gerät kann Positionslichter (einschließlich Punkt und Punkt) durchführen.                                                                                                                                         |
| D3DVTXPCAPS \_ TEXGEN                     | Das Gerät kann texgen.                                                                                                                                                                              |
| D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP          | Das Gerät unterstützt D3DTSS \_ TCI \_ SPHEREMAP.                                                                                                                                                            |
| D3DVTXPCAPS-TWEENING \_                   | Das Gerät kann Scheitelpunkt-Tweening durchführen.                                                                                                                                                                     |



 

## <a name="constant-information"></a>Konstanteninformationen



| Anforderung                         | Wert           |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



