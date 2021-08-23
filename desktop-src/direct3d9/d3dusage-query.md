---
description: Diese Optionen identifizieren Abfrageressourcentypen.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d681b093b8dacbd78e42ff2d8fa700954b3efb02b571d0b33097d29152e1d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988860"
---
# <a name="d3dusage_query"></a>D3DUSAGE-ABFRAGE \_

Diese Optionen identifizieren Abfrageressourcentypen.



| \#Definieren                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_D3DUSAGE-ABFRAGEFILTER \_                    | Fragen Sie das Ressourcenformat ab, um festzustellen, ob es andere Texturfiltertypen als D3DTEXF POINT unterstützt \_ (was immer unterstützt wird).                                                                                                                                                                                                                         |
| D3DUSAGE \_ QUERY \_ LEGACYBUMPMAP             | Fragen Sie die Ressource nach einer Legacy-Bump map ab.                                                                                                                                                                                                                                                                                                         |
| D3DUSAGE \_ QUERY \_ POSTPIXELSHADER \_ BLENDING | Fragen Sie die Ressource ab, um die Unterstützung für Die-Pixel-Shaderblending-Unterstützung zu überprüfen. Wenn [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit D3DUSAGE \_ QUERY \_ POSTPIXELSHADER \_ BLENDING fehlschlägt, werden Postpixelmischungsvorgänge nicht unterstützt. Dazu gehören Alphatest, Pixelzeil, Render-Ziel-Blending, Aktivieren von Farbschreib- und Dithering. |
| D3DUSAGE \_ QUERY \_ SRGBREAD                  | Fragen Sie die Ressource ab, um zu überprüfen, ob eine Textur die Gammakorrektur während eines Lesevorgangs unterstützt.                                                                                                                                                                                                                                                        |
| D3DUSAGE \_ QUERY \_ SRGBWRITE                 | Fragen Sie die Ressource ab, um zu überprüfen, ob eine Textur die Gammakorrektur während eines Schreibvorgangs unterstützt.                                                                                                                                                                                                                                                       |
| D3DUSAGE \_ QUERY \_ VERTEXTEXTURE             | Fragen Sie die Ressource ab, um die Unterstützung für die Textursampling des Vertex-Shaders zu überprüfen.                                                                                                                                                                                                                                                                            |
| D3DUSAGE \_ QUERY \_ WRAPANDMIP                | Fragen Sie die Ressource ab, um die Unterstützung für Texturumbruch und MIP-Zuordnung zu überprüfen.                                                                                                                                                                                                                                                                          |



 

Verwenden Sie [**CheckDeviceFormat,**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) um die Hardwareunterstützung für diese Und einige andere Verwendungen abzufragen, die in [D3DUSAGE](d3dusage.md)aufgeführt sind.

## <a name="constant-information"></a>Konstanteninformationen



| Anforderung                         | Wert            |
|--------------------------|-------------|
| Header                   | d3d9types.h |
| Mindestbetriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
