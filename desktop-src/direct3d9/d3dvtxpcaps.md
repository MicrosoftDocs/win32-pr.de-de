---
description: Erfahren Sie mehr über eine Kombination aus einem oder mehrere Flags, die das Verhalten beim Erstellen von Geräten in der D3DVTXPCAPS-Konstante steuern.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a230b7eeba5f10ec24e4a33f9fe85b90b67e6b55502250ec1df18af0e5fff15f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988850"
---
# <a name="d3dvtxpcaps"></a>D3DVTXPCAPS

Eine Kombination aus einem oder mehrere Flags, die das Verhalten beim Erstellen des Geräts steuern.



| \#Definieren                                | Beschreibung                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DVTXPCAPS \_ DIRECTIONALLIGHTS          | Das Gerät kann direktionale Beleuchtungen verwenden.                                                                                                                                                                  |
| D3DVTXPCAPS \_ LOCALVIEWER                | Das Gerät kann einen lokalen Viewer verwenden.                                                                                                                                                                        |
| D3DVTXPCAPS \_ MATERIALSOURCE7            | Wenn diese Obergrenze festgelegt ist, unterstützt das Gerät die Farbmaterialzustände: D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, \_ D3DRSMESSGERÄTSSIVEMATERIALSOURCE und D3DRS \_ SPECULARMATERIALSOURCE. |
| D3DVTXPCAPS \_ NO \_ TEXGEN \_ NONLOCALVIEWER | Das Gerät unterstützt keine Texturgenerierung im nicht lokalen Viewermodus.                                                                                                                               |
| D3DVTXPCAPS \_ POSITIONALLIGHTS           | Das Gerät kann Positionslichter (einschließlich Punkt und Spot) verwenden.                                                                                                                                         |
| D3DVTXPCAPS \_ TEXGEN                     | Gerät kann texgen.                                                                                                                                                                              |
| D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP          | Das Gerät unterstützt D3DTSS \_ TCI \_ SPHEREMAP.                                                                                                                                                            |
| D3DVTXPCAPS-OPTIMIERUNG \_                   | Das Gerät kann Scheitelpunkt-Tweening verwenden.                                                                                                                                                                     |



 

## <a name="constant-information"></a>Konstante Informationen



| Anforderung                         | Wert           |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



