---
description: Während des Renderings interpoliert die Pipeline Scheitelpunkt Daten in jedem Dreieck.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Dreiecks interpolung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 405cbecd6123145d412a3e7f58f727bdf5b5a3e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346834"
---
# <a name="triangle-interpolation-direct3d-9"></a>Dreiecks interpolung (Direct3D 9)

Während des Renderings interpoliert die Pipeline Scheitelpunkt Daten in jedem Dreieck. Bei Scheitelpunkt Daten kann es sich um eine große Bandbreite von Daten handeln, die Sie einschließen können (aber nicht beschränkt auf): diffuse Farbe, Glanz Farbe, diffuse Alpha (Dreiecks Deckkraft), Glanz Alpha und einen Nebel Faktor (von Glanz Alpha für die Vertex-Pipeline mit fester Funktion und aus dem Nebel Register für eine programmierbare vertexpipeline entnommen). Die Vertex-Daten werden durch die [Vertexdeklaration (Direct3D 9)](vertex-declaration.md)definiert.

Bei einigen Scheitelpunkt Daten ist die Interpolation vom aktuellen Schattierungs Modus abhängig, wie in der folgenden Tabelle dargestellt.



| Schattierungs Modus | BESCHREIBUNG                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flach         | Nur der Nebel Faktor wird im flatschatmodus interpoliert. Für alle anderen interinterpolierten Werte wird die Farbe des ersten Scheitel Punkts im Dreieck auf die gesamte Oberfläche angewendet. |
| Gouraud      | Lineare Interpolationen werden zwischen allen drei Scheitel Punkten ausgeführt.                                                                                                               |



 

Die diffuse Farbe und die Glanz Farbe werden je nach Farbmodell anders behandelt. Im RGB-Farbmodell verwendet das System die roten, grünen und blauen Farbkomponenten in der interpolung.

Die Alpha Komponente einer Farbe wird als separater interinterintererter Wert behandelt, da Gerätetreiber Transparenz auf zwei verschiedene Arten implementieren können: mithilfe von Textur Mischungen oder mithilfe von stippling.

Verwenden Sie den ShadeCaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur, um zu bestimmen, welche Formen der Interpolationen der aktuelle Gerätetreiber unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Koordinatensysteme und Geometrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



