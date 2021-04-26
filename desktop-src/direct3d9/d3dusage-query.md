---
description: Diese Optionen identifizieren Abfrageressourcentypen.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eac450ed722da26fe4885d41707483adf401f89
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994107"
---
# <a name="d3dusage_query"></a>D3DUSAGE-ABFRAGE \_

Diese Optionen identifizieren Abfrageressourcentypen.



| \#Definieren                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DUSAGE-ABFRAGEFILTER \_ \_                    | Fragen Sie das Ressourcenformat ab, um zu sehen, ob es andere Texturfiltertypen als D3DTEXF \_ POINT unterstützt (was immer unterstützt wird).                                                                                                                                                                                                                         |
| D3DUSAGE \_ QUERY \_ LEGACYBUMPMAP             | Fragen Sie die Ressource nach einer Legacy-Bumpmap ab.                                                                                                                                                                                                                                                                                                         |
| D3DUSAGE \_ QUERY \_ POSTPIXELSHADER \_ BLENDING | Fragen Sie die Ressource ab, um die Unterstützung für Shaderblending nach Pixel zu überprüfen. Wenn [**CheckDeviceFormat mit**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) D3DUSAGE \_ QUERY \_ POSTPIXELSHADER BLENDING fehlschlägt, werden Vorgänge nach dem Mischen von \_ Pixeln nicht unterstützt. Dazu gehören Alphatest, Pixelverblendung, Renderzielblending, Aktivieren des Farbschreibens und Dithering. |
| D3DUSAGE \_ QUERY \_ SRGBREAD                  | Fragen Sie die Ressource ab, um zu überprüfen, ob eine Textur die Gammakorrektur während eines Lesevorgang unterstützt.                                                                                                                                                                                                                                                        |
| D3DUSAGE \_ QUERY \_ SRGBWRITE                 | Fragen Sie die Ressource ab, um zu überprüfen, ob eine Textur die Gammakorrektur während eines Schreibvorgang unterstützt.                                                                                                                                                                                                                                                       |
| D3DUSAGE \_ QUERY \_ VERTEXTEXTURE             | Fragen Sie die Ressource ab, um die Unterstützung für vertex shader texture sampling zu überprüfen.                                                                                                                                                                                                                                                                            |
| D3DUSAGE \_ QUERY \_ WRAPANDMIP                | Fragen Sie die Ressource ab, um die Unterstützung für Texturumbruch und Mipzuordnung zu überprüfen.                                                                                                                                                                                                                                                                          |



 

Verwenden Sie [**CheckDeviceFormat,**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) um die Hardwareunterstützung für diese Und einige andere Verwendungen abzufragen, die in [D3DUSAGE](d3dusage.md)aufgeführt sind.

## <a name="constant-information"></a>Konstanteninformationen



|                          |             |
|--------------------------|-------------|
| Header                   | d3d9types.h |
| Mindestbetriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
