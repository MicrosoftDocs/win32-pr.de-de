---
description: Der Microsoft DirectX Graphic Infrastructure (DXGI) verwaltet Aufgaben auf niedriger Ebene, die unabhängig von der Direct3D-Grafikruntime sein können. DXGI bietet ein allgemeines Framework für mehrere Direct3D-Versionen.
ms.assetid: bcbeb4bc-3bd1-40ed-b176-a8091cc6ee9f
title: Programmierhandbuch für DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0ac41155557c14ca41f8e0ea9f1836247bd3b78da213c1fbbed521499eae7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518383"
---
# <a name="programming-guide-for-dxgi"></a>Programmierhandbuch für DXGI

Der Microsoft DirectX Graphic Infrastructure (DXGI) verwaltet Aufgaben auf niedriger Ebene, die unabhängig von der Direct3D-Grafikruntime sein können. DXGI bietet ein allgemeines Framework für mehrere Direct3D-Versionen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                              | BESCHREIBUNG                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DXGI – Übersicht](d3d10-graphics-programming-guide-dxgi.md)<br/>                                                              | Dieses Thema enthält folgende Abschnitte:<br/>                                                                                                                   |
| [DXGI 1.2-Verbesserungen](dxgi-1-2-improvements.md)<br/>                                                                      | Die folgende Funktionalität wurde in DXGI 1.2 hinzugefügt.<br/>                                                                                                       |
| [DXGI 1.3-Verbesserungen](dxgi-1-3-improvements.md)<br/>                                                                      | Die folgende Funktionalität wurde in DXGI 1.3 hinzugefügt, die ab Windows 8.1 enthalten ist.<br/>                                                            |
| [DXGI 1.4-Verbesserungen](dxgi-1-4-improvements.md)<br/>                                                                      | Die folgende Funktionalität wurde in DXGI 1.4 hinzugefügt oder geändert, hauptsächlich zur Unterstützung von Direct3D 12. <br/>                                                           |
| [DXGI 1.5-Verbesserungen](dxgi-1-5-improvements.md)<br/>                                                                      | DXGI 1.5 wurde um die folgende Funktionalität erweitert, um eine flexiblere Angabe und Duplizierung von Ausgabeformaten zu unterstützen.<br/>                                |
| [DXGI 1.6-Verbesserungen](dxgi-1-6-improvements.md)<br/>                                                                      | Dxgi 1.6 wurde die folgende Funktionalität hinzugefügt, um HDR-Anzeigen zu erkennen.<br/>                                                                       |
| [Verwenden von DirectX mit High Dynamic Range-Displays und erweiterter Farbe](../direct3darticles/high-dynamic-range.md)     | Dieses Thema bietet eine technische Übersicht über das Rendern von Direct3D 11- und Direct3D 12-Inhalten mit hohem dynamischen Bereich auf eine HDR10-Anzeige mithilfe Windows 10 erweiterten Farbunterstützung.<br/> |
| [Variable Aktualisierungsrate wird angezeigt](variable-refresh-rate-displays.md)<br/>                                                    | Variable Aktualisierungsrate zeigt an, dass *das Löschen* aktiviert werden muss. Dies wird auch als "vsync-off"-Unterstützung bezeichnet.<br/>                                                    |
| [Verwenden der Gammakorrektur](using-gamma-correction.md)<br/>                                                                    | Die Gammakorrektur oder kurz Gamma ist der Name eines nicht linearen Vorgangs, den Systeme verwenden, um Pixelwerte in Bildern zu codieren und zu decodieren.<br/>                        |
| [Formatunterstützung für Direct3D-Feature 10Level9 9.1-Hardware](format-support-for-direct3d-feature-level-9-1-hardware.md)<br/> | In diesem Abschnitt werden die Formate [**(DXGI \_ FORMAT-Werte)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) angegeben, die in Direct3D Feature 10Level9 9.1-Hardware unterstützt werden.<br/>        |
| [Formatunterstützung für Direct3D-Feature 10Level9 9.3-Hardware](format-support-for-direct3d-feature-level-9-3-hardware.md)<br/> | In diesem Abschnitt werden die Formate [**(DXGI \_ FORMAT-Werte)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) angegeben, die in Direct3D Feature 10Level9 9.3-Hardware unterstützt werden.<br/>        |
| [Formatunterstützung für Direct3D Feature Level 10.0-Hardware](format-support-for-direct3d-feature-level-10-0-hardware.md)<br/>  | In diesem Abschnitt werden die Formate [**(DXGI \_ FORMAT-Werte)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) angegeben, die in Direct3D 10.0-Hardware unterstützt werden.<br/>                        |
| [Formatunterstützung für Direct3D Feature Level 10.1-Hardware](format-support-for-direct3d-feature-level-10-1-hardware.md)<br/>  | In diesem Abschnitt werden die Formate [**(DXGI \_ FORMAT-Werte)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) angegeben, die in Direct3D 10.1-Hardware unterstützt werden.<br/>                        |
| [Formatunterstützung für Direct3D-Featureebene 11.0-Hardware](format-support-for-direct3d-11-0-feature-level-hardware.md)<br/>  | In diesem Abschnitt werden die Formate [**(DXGI \_ FORMAT-Werte)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) angegeben, die in Direct3D Feature Level 11.0-Hardware unterstützt werden.<br/>          |
| [Formatunterstützung für Direct3D-Featureebene 11.1-Hardware](format-support-for-direct3d-11-1-feature-level-hardware.md)<br/>  | In diesem Abschnitt werden die Formate [**(DXGI \_ FORMAT-Werte)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) angegeben, die in Direct3D Feature Level 11.1-Hardware unterstützt werden.<br/>          |
| [Formatunterstützung für Direct3D-Featureebene 12.0-Hardware](hardware-support-for-direct3d-12-0-formats.md)<br/>               | In diesem Abschnitt werden die Formate [**(DXGI \_ FORMAT-Werte)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) angegeben, die in Direct3D Feature Level 12.0-Hardware unterstützt werden.<br/>          |
| [Formatunterstützung für Direct3D Feature Level 12.1-Hardware](hardware-support-for-direct3d-12-1-formats.md)<br/>               | In diesem Abschnitt werden die Formate [**(DXGI \_ FORMAT-Werte)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) angegeben, die in Direct3D 12.1-Hardware unterstützt werden.<br/>                        |
| [Überprüfen der Hardwarefeatureunterstützung](checking-hardware-feature-support.md)<br/>                                              | In diesem Abschnitt wird beschrieben, wie Sie die Formatunterstützung für Direct3D-Hardware auf Featureebene mithilfe von API-Aufrufen überprüfen.<br/>                                                       |
| [Verwenden Sie das DXGI-Flip-Modell, um eine optimale Leistung zu erzielen.](for-best-performance--use-dxgi-flip-model.md)<br/>                              | Dieses Thema enthält Entwicklerleitfäden zum Maximieren von Leistung und Effizienz im Präsentationsstapel für moderne Versionen von Windows.<br/>                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXGI](dx-graphics-dxgi.md)
</dt> <dt>

[DXGI-Referenz](d3d10-graphics-reference-dxgi.md)
</dt> <dt>

[DirectX Graphic Infrastructure (DXGI): Bewährte Methoden](../direct3darticles/dxgi-best-practices.md)
</dt> </dl>

 

 
