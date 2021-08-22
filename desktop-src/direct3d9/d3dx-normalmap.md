---
description: Normal ordnet Generierungskonstanten zu.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d3a3d2f35fa409e4432dd7600cb544df25110d10aa9af7f5ee18fd622ea1309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374950"
---
# <a name="d3dx_normalmap"></a>D3DX \_ NORMALMAP

Normal ordnet Generierungskonstanten zu.



| \#Definieren                            | Beschreibung                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX \_ NORMALMAP \_ MIRROR \_ U          | Gibt an, dass Pixel außerhalb des Texturrands auf der U-Achse gespiegelt und nicht umschlossen werden sollen.                                                                                                   |
| D3DX \_ NORMALMAP \_ MIRROR \_ V          | Gibt an, dass Pixel außerhalb des Texturrands auf der V-Achse gespiegelt und nicht umschlossen werden sollen.                                                                                                   |
| D3DX \_ NORMALMAP \_ MIRROR             | Entspricht der Angabe von D3DX \_ NORMALMAP \_ MIRROR U \_ \| D3DX \_ NORMALMAP MIRROR \_ \_ V.                                                                                                                       |
| D3DX \_ NORMALMAP \_ INVERTSIGN         | Umkehrt die Richtung der einzelnen Normalitäten.                                                                                                                                                              |
| D3DX \_ NORMALMAP \_ COMPUTE \_ OCCLUSION | Berechnet den Verdeckungsbegriff pro Pixel und codiert ihn in das Alpha. Ein Alpha von 1 bedeutet, dass das Pixel in keiner Weise verdeckt wird, und ein Alpha von 0 bedeutet, dass das Pixel vollständig verdeckt ist. |



 

## <a name="constant-information"></a>Konstanteninformationen



| Anforderung                         | Wert           |
|--------------------------|------------|
| Header                   | d3dx9tex.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX-Konstanten](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[**D3DXComputeNormalMap**](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



