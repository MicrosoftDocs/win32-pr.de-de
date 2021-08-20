---
description: Parameter für Denkparameter werden über Renderzustände des Geräts gesteuert.
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: Parameter von "Parameters" (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36c7883905e59c7147b94a2f803e7b5b74baeccf9383885fe49c69f2e1eeac87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094798"
---
# <a name="fog-parameters-direct3d-9"></a>Parameter von "Parameters" (Direct3D 9)

Parameter für Denkparameter werden über Renderzustände des Geräts gesteuert. Sowohl der Pixel- als auch der Scheitelpunkt-Typ unterstützen alle Formeln, die in [Formulas (Direct3D 9)](fog-formulas.md)eingeführt wurden. Der [**aufzählte D3DFOGMODE-Typ**](./d3dfogmode.md) definiert Konstanten, mit denen Sie die Formel identifizieren können, die Microsoft Direct3D verwenden soll. Der Renderzustand D3DRSTABLEMODE steuert den Modus, den Direct3D für Pixelpixel verwendet, und der \_ D3DRS-RenderzustandVERTEXMODE steuert den Modus für Scheitelpunkt-Ziehpunkte. \_

Wenn Sie die lineare Formel formula (Lineare Formel für Gleichung) verwenden, legen Sie die Anfangs- und Endentfernungen durch die Renderzustände D3DRS \_ REGRESSIONSTART und D3DRS \_ REGRESSIONEND fest. Wie das System diese Werte interpretiert, hängt von der Art des von Ihrer Anwendung verwendeten Typs ab – Pixel- oder Scheitelpunkt-Scheitelpunkt – und bei Verwendung von Pixelpixeln, wenn z- oder w-basierte Tiefe verwendet wird. In der folgenden Tabelle sind die Typen und deren Start- und Endeinheiten zusammengefasst.



| Typ "2012"  | Start-/End-Einheiten      |
|-----------|--------------------------|
| Pixel (Z) | Gerätebereich \[ 0.0,1.0\] |
| Pixel (W) | Kameraraum             |
| Scheitelpunkt    | Kameraraum             |



 

Der D3DRS-Renderzustand VORDENSITY steuert die Dichte, die angewendet \_ wird, wenn eine exponentiale Formel aktiviert wird. Die Dichte der Luft ist im Wesentlichen ein Gewichtungsfaktor im Bereich von 0,0 bis 1,0 (einschließlich), der den Entfernungswert im Exponenten skaliert.

Die Farbe, die das System für das Blending von Blending verwendet, wird über den Renderzustand des D3DRS-GERÄTS \_ (COLOR COLOR) gesteuert. Weitere Informationen finden Sie unter [Color Color (Direct3D 9)](fog-color.md) und [Blending von Blending (Direct3D 9).](fog-blending.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Typen von Typen](fog-types.md)
</dt> </dl>

 

 
