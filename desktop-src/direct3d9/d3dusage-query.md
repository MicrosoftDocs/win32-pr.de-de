---
description: Diese Optionen identifizieren Abfrage Ressourcentypen.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f5dda7f84dfa36e4f3b7ece1b359a4841bbbf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126877"
---
# <a name="d3dusage_query"></a>D3DUSAGE- \_ Abfrage

Diese Optionen identifizieren Abfrage Ressourcentypen.



|                                            |                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definieren                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                         |
| D3DUSAGE- \_ Abfrage \_ Filter                    | Fragen Sie das Ressourcen Format ab, um festzustellen, ob es andere Textur Filtertypen als D3DTEXF Point unterstützt \_ (was immer unterstützt wird).                                                                                                                                                                                                                         |
| D3DUSAGE \_ Query \_ legacybumpmap             | Abfragen der Ressource über eine Legacy-Bump-Karte.                                                                                                                                                                                                                                                                                                         |
| D3DUSAGE \_ Query \_ postpixelshader- \_ BLENDING | Fragen Sie die Ressource ab, um die Unterstützung für die Unterstützung für die Unterstützung von Post Wenn [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit D3DUSAGE \_ Query \_ postpixelshader- \_ Blending fehlschlägt, werden Post Pixel Mischungs Vorgänge nicht unterstützt. Hierzu gehören Alpha Test, Pixel Nebel, Mischung aus Renderziel, Farb Schreib Aktivierung und Dithering. |
| D3DUSAGE \_ Abfrage \_ srgbread                  | Fragen Sie die Ressource ab, um zu überprüfen, ob eine Textur während eines Lesevorgangs Gammakorrektur unterstützt.                                                                                                                                                                                                                                                        |
| D3DUSAGE \_ Abfrage \_ srgbwrite                 | Fragen Sie die Ressource ab, um zu überprüfen, ob eine Textur während eines Schreibvorgangs Gammakorrektur unterstützt.                                                                                                                                                                                                                                                       |
| D3DUSAGE \_ Query \_ vertextexture             | Fragen Sie die Ressource ab, um die Unterstützung für die Vertexshader-Textur Stichproben                                                                                                                                                                                                                                                                            |
| D3DUSAGE \_ Query \_ wrapandmip                | Fragen Sie die Ressource ab, um Unterstützung für Textur Wrapping und MIP-Zuordnung zu überprüfen.                                                                                                                                                                                                                                                                          |



 

Verwenden Sie [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) , um die Hardwareunterstützung für diese Verwendungen und andere in [D3DUSAGE](d3dusage.md)aufgelistete Verwendungen abzufragen.

## <a name="constant-information"></a>Konstante Informationen



|                          |             |
|--------------------------|-------------|
| Header                   | d3d9types. h |
| Mindestens Betriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
