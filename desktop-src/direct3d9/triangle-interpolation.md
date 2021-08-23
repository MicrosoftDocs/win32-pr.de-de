---
description: Während des Renderings interpoliert die Pipeline Scheitelpunktdaten über jedes Dreieck.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Dreiecksinterpolation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a411f53351ccd5d3407b358b03e705677e9bf5a96a57b162016afe09332bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746260"
---
# <a name="triangle-interpolation-direct3d-9"></a>Dreiecksinterpolation (Direct3D 9)

Während des Renderings interpoliert die Pipeline Scheitelpunktdaten über jedes Dreieck. Vertexdaten können eine Vielzahl von Daten sein und umfassen (aber nicht beschränkt auf): diffuse Farbe, Specular Color, diffuses Alpha (Dreiecksdurchlässigkeit), Specular Alpha und einen Fixfaktor (aus specular alpha für die Vertexpipeline fester Funktion und aus dem Register für programmierbare Vertexpipeline). Die Scheitelpunktdaten werden durch die [Scheitelpunktdeklaration (Direct3D 9) definiert.](vertex-declaration.md)

Bei einigen Scheitelpunktdaten ist die Interpolation vom aktuellen Schattierungsmodus abhängig, wie in der folgenden Tabelle gezeigt.



| Schattierungsmodus | Beschreibung                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flach         | Nur der Füschfaktor wird im flachen Schattierungsmodus interpoliert. Für alle anderen interpolierten Werte wird die Farbe des ersten Scheitelpunkts im Dreieck auf das gesamte Gesicht angewendet. |
| Gouraud      | Die lineare Interpolation wird zwischen allen drei Scheitelzeichen ausgeführt.                                                                                                               |



 

Die diffuse Farbe und die Winkelfarbe werden je nach Farbmodell unterschiedlich behandelt. Im RGB-Farbmodell verwendet das System die Rot-, Grün- und Blaufarbenkomponenten in der Interpolation.

Die Alphakomponente einer Farbe wird als separater interpolierter Wert behandelt, da Gerätetreiber Transparenz auf zwei unterschiedliche Arten implementieren können: durch Texturmischung oder durch Ausschnitt.

Verwenden Sie den ShadeCaps-Member der [**D3DCAPS9-Struktur,**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) um zu bestimmen, welche Interpolationsformen der aktuelle Gerätetreiber unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Koordinatensysteme und Geometrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



