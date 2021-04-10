---
description: Die Microsoft DirectX Graphics Infrastructure (DXGI) verwaltet Low-Level-Aufgaben, die unabhängig von der Direct3D-Grafik Laufzeit sein können. DXGI bietet ein gemeinsames Framework für eine Reihe von Direct3D-Versionen.
ms.assetid: bcbeb4bc-3bd1-40ed-b176-a8091cc6ee9f
title: Programmier Handbuch für DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7834b2fc68019dccfb8ab8b2e62698465ff1ea2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213835"
---
# <a name="programming-guide-for-dxgi"></a>Programmier Handbuch für DXGI

Die Microsoft DirectX Graphics Infrastructure (DXGI) verwaltet Low-Level-Aufgaben, die unabhängig von der Direct3D-Grafik Laufzeit sein können. DXGI bietet ein gemeinsames Framework für eine Reihe von Direct3D-Versionen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                              | BESCHREIBUNG                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Übersicht über DXGI](d3d10-graphics-programming-guide-dxgi.md)<br/>                                                              | Dieses Thema enthält folgende Abschnitte:<br/>                                                                                                                   |
| [DXGI 1,2-Verbesserungen](dxgi-1-2-improvements.md)<br/>                                                                      | Die folgende Funktionalität wurde in DXGI 1,2 hinzugefügt.<br/>                                                                                                       |
| [DXGI 1,3-Verbesserungen](dxgi-1-3-improvements.md)<br/>                                                                      | Die folgende Funktionalität wurde in DXGI 1,3 hinzugefügt, die in Windows 8.1 enthalten ist.<br/>                                                            |
| [DXGI 1,4-Verbesserungen](dxgi-1-4-improvements.md)<br/>                                                                      | Die folgende Funktionalität wurde in DXGI 1,4 hinzugefügt oder geändert, größtenteils zur Unterstützung von Direct3D 12. <br/>                                                           |
| [DXGI 1,5-Verbesserungen](dxgi-1-5-improvements.md)<br/>                                                                      | Die folgende Funktionalität wurde DXGI 1,5 hinzugefügt, um eine flexiblere Angabe und Duplizierung von Ausgabeformaten zu unterstützen.<br/>                                |
| [DXGI 1,6-Verbesserungen](dxgi-1-6-improvements.md)<br/>                                                                      | Die folgende Funktionalität wurde DXGI 1,6 hinzugefügt, um HDR-anzeigen zu erkennen.<br/>                                                                       |
| [Verwenden von DirectX mit High Dynamic Range-Displays und erweiterter Farbe](../direct3darticles/high-dynamic-range.md)     | Dieses Thema bietet eine technische Übersicht über das Rendern von Inhalten mit hoher dynamischer Breite Direct3D 11 und Direct3D 12 in eine HDR10-Anzeige mithilfe von Unterstützung für erweiterte Farben in Windows 10.<br/> |
| [Variable Aktualisierungsrate anzeigen](variable-refresh-rate-displays.md)<br/>                                                    | Die Anzeige der Variablen Aktualisierungsrate erfordert, dass das *zerreißen* aktiviert wird. Dies wird auch als "VSYNC-Off"-Unterstützung bezeichnet.<br/>                                                    |
| [Verwenden von Gammakorrektur](using-gamma-correction.md)<br/>                                                                    | Gammakorrektur (oder Gamma) ist der Name eines nichtlinearen Vorgangs, den Systeme zum Codieren und Decodieren von Pixelwerten in Bildern verwenden.<br/>                        |
| [Format Unterstützung für das Direct3D-Feature 10level9 9,1 Hardware](format-support-for-direct3d-feature-level-9-1-hardware.md)<br/> | In diesem Abschnitt werden die Formate ([**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Werte) angegeben, die in der Direct3D-Funktion 10level9 9,1-Hardware unterstützt werden.<br/>        |
| [Format Unterstützung für das Direct3D-Feature 10level9 9,3 Hardware](format-support-for-direct3d-feature-level-9-3-hardware.md)<br/> | In diesem Abschnitt werden die Formate ([**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Werte) angegeben, die in der Direct3D-Funktion 10level9 9,3-Hardware unterstützt werden.<br/>        |
| [Format Unterstützung für Direct3D Feature Level 10,0 Hardware](format-support-for-direct3d-feature-level-10-0-hardware.md)<br/>  | In diesem Abschnitt werden die Formate ([**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Werte) angegeben, die in Direct3D 10,0-Hardware unterstützt werden.<br/>                        |
| [Format Unterstützung für Direct3D Feature Level 10,1 Hardware](format-support-for-direct3d-feature-level-10-1-hardware.md)<br/>  | In diesem Abschnitt werden die Formate ([**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Werte) angegeben, die in Direct3D 10,1-Hardware unterstützt werden.<br/>                        |
| [Format Unterstützung für Direct3D Feature Level 11,0 Hardware](format-support-for-direct3d-11-0-feature-level-hardware.md)<br/>  | In diesem Abschnitt werden die Formate ([**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Werte) angegeben, die auf Direct3D Feature Level 11,0-Hardware unterstützt werden.<br/>          |
| [Format Unterstützung für Direct3D Feature Level 11,1 Hardware](format-support-for-direct3d-11-1-feature-level-hardware.md)<br/>  | In diesem Abschnitt werden die Formate ([**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Werte) angegeben, die auf Direct3D Feature Level 11,1-Hardware unterstützt werden.<br/>          |
| [Format Unterstützung für Direct3D Feature Level 12,0 Hardware](hardware-support-for-direct3d-12-0-formats.md)<br/>               | In diesem Abschnitt werden die Formate ([**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Werte) angegeben, die auf Direct3D Feature Level 12,0-Hardware unterstützt werden.<br/>          |
| [Format Unterstützung für Direct3D Feature Level 12,1 Hardware](hardware-support-for-direct3d-12-1-formats.md)<br/>               | In diesem Abschnitt werden die Formate ([**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Werte) angegeben, die in Direct3D 12,1-Hardware unterstützt werden.<br/>                        |
| [Überprüfen der Hardware Funktions Unterstützung](checking-hardware-feature-support.md)<br/>                                              | In diesem Abschnitt wird erläutert, wie Sie mithilfe von API-aufrufen die Format Unterstützung für Hardware auf Featureebene Direct3D.<br/>                                                       |
| [Verwenden Sie zum erzielen der optimalen Leistung DXGI-Flip-Modell.](for-best-performance--use-dxgi-flip-model.md)<br/>                              | Dieses Thema enthält Anleitungen für Entwickler zur Maximierung der Leistung und Effizienz im Präsentations Stapel auf modernen Versionen von Windows.<br/>                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXGI](dx-graphics-dxgi.md)
</dt> <dt>

[DXGI-Referenz](d3d10-graphics-reference-dxgi.md)
</dt> <dt>

[DirectX-Grafik Infrastruktur (DXGI): bewährte Methoden](../direct3darticles/dxgi-best-practices.md)
</dt> </dl>

 

 
