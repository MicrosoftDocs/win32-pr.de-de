---
description: Lichteigenschaften beschreiben den Typ und die Farbe einer Lichtquelle.
ms.assetid: b39f1287-c67b-4cbb-b599-4a1b2f4981ac
title: Lichteigenschaften (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14c3e815401fe0b35c7409dec783515de5c3422ac92d6aed6fd4adebf09f8c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747000"
---
# <a name="light-properties-direct3d-9"></a>Lichteigenschaften (Direct3D 9)

Lichteigenschaften beschreiben den Typ und die Farbe einer Lichtquelle. Abhängig vom verwendeten Lichttyp kann ein Licht Eigenschaften für Dämpfung und Bereich oder für Spotlighteffekte aufweisen. Aber nicht alle Arten von Beleuchtung verwenden alle Eigenschaften. Direct3D verwendet die [**D3DLIGHT9-Struktur,**](d3dlight9.md) um Informationen zu Lichteigenschaften für alle Arten von Datenquellen zu übertragen. Dieser Abschnitt enthält Informationen zu allen lichten Eigenschaften. Die Informationen sind in die folgenden Gruppen unterteilt.

Die Position, der Bereich und die Dämpfungseigenschaften definieren die Position eines Lichts im Weltraum und das Verhalten des Lichts, das es über die Entfernung ausgibt. Wie alle lichten Eigenschaften, die Sie in C++ verwenden, sind diese in der [**D3DLIGHT9-Struktur**](d3dlight9.md) eines Lichts enthalten.

-   [Lichtdämpfung](#light-attenuation)
-   [Helle Farbe](#light-color)
-   [Lichtrichtung](#light-direction)
-   [Lichtposition](#light-position)
-   [Lichtbereich](#light-range)

## <a name="light-attenuation"></a>Lichtdämpfung

Die Dämpfung steuert, wie sich die Intensität eines Lichts in Richtung des durch die Bereichseigenschaft angegebenen maximalen Abstands verringert. Drei [**D3DLIGHT9-Strukturmember**](d3dlight9.md) stellen die lichte Dämpfung dar: Attenuation0, Attenuation1 und Attenuation2. Diese Member enthalten Gleitkommawerte im Bereich von 0,0 bis unendlich, um die Dämpfung eines Lichts zu steuern. Einige Anwendungen legen den Member Attenuation1 auf 1,0 und die anderen auf 0,0 fest. Dies führt zu einer Lichtstärke, die sich in 1/D ändert, wobei D der Abstand von der Lichtquelle zum Scheitelpunkt ist. Die maximale Lichtdichte liegt an der Quelle, wobei sie auf 1 / (Lichtbereich) im Bereich des Lichts abnimmt. In der Regel legt eine Anwendung Attenuation0 auf 0,0, Attenuation1 auf einen konstanten Wert und Attenuation2 auf 0,0 fest.

Sie können Dämpfungswerte kombinieren, um komplexere Dämpfungseffekte zu erzielen. Oder Sie können sie auf Werte außerhalb des normalen Bereichs festlegen, um gleichmäßige Dämpfungseffekte zu erzeugen. Negative Dämpfungswerte sind jedoch nicht zulässig. Weitere Informationen finden Sie [unter Dämpfung und Spotlight-Faktor (Direct3D 9).](attenuation-and-spotlight-factor.md)

## <a name="light-color"></a>Helle Farbe

Beleuchtung in Direct3D gibt drei Farben aus, die unabhängig in den Beleuchtungsberechnungen des Systems verwendet werden: eine diffuse Farbe, eine Umgebungsfarbe und eine Glanzfarbe. Jede wird vom Direct3D-Beleuchtungsmodul integriert und interagiert mit einer Entsprechung aus dem aktuellen Material, um eine endgültige Farbe zu erzeugen, die beim Rendern verwendet wird. Die diffuse Farbe interagiert mit der diffusen Reflektionseigenschaft des aktuellen Materials, der Glanzfarbe mit der Spiegelungseigenschaft des Materials usw. Informationen dazu, wie Direct3D diese Farben anwendet, finden Sie unter [Mathematik der Beleuchtung (Direct3D 9).](mathematics-of-lighting.md)

In einer C++-Anwendung enthält die [**D3DLIGHT9-Struktur**](d3dlight9.md) drei Member für diese Farben: Diffuse, Ambient und Specular. Jedes ist eine [**D3DCOLORVALUE-Struktur,**](d3dcolorvalue.md) die die ausgegebene Farbe definiert.

Der Farbtyp, der am stärksten auf die Berechnungen des Systems angewendet wird, ist die diffuse Farbe. Die gängigste diffuse Farbe ist Weiß (R:1.0 G:1.0 B:1.0), aber Sie können Farben nach Bedarf erstellen, um gewünschte Effekte zu erzielen. Beispielsweise könnten Sie rotes Licht für ein Lichtmittel verwenden, oder Sie könnten grünes Licht für ein Verkehrssignal verwenden, das auf "Go" festgelegt ist.

Im Allgemeinen legen Sie die Komponenten für helle Farben auf Werte zwischen 0,0 und 1,0 (einschließlich) fest, dies ist jedoch keine Voraussetzung. Beispielsweise können Sie alle Komponenten auf 2.0 festlegen, wodurch ein Licht entsteht, das "hell als weiß" ist. Diese Art von Einstellung kann besonders nützlich sein, wenn Sie andere Dämpfungseinstellungen als constant verwenden.

Beachten Sie, dass direct3D zwar RGBA-Werte für Beleuchtung verwendet, die Alphafarbkomponente jedoch nicht verwendet wird.

Normalerweise werden Materialfarben für die Beleuchtung verwendet. Sie können jedoch angeben, dass material colors-emissive, ambient, diffuse und specular-durch diffuse oder specular vertex colors überschrieben werden sollen. Dazu rufen [**Sie SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) auf und legen die in der folgenden Tabelle aufgeführten Gerätezustandsvariablen fest.



| Gerätezustandsvariable         | Bedeutung                                       | type                   | Standard          |
|-------------------------------|-----------------------------------------------|------------------------|------------------|
| D3DRS \_ AMBIENTMATERIALSOURCE  | Definiert, wo Umgebungsmaterialfarbe erhalten werden soll.  | D3DMATERIALCOLORSOURCE | D3DMCS \_ MATERIAL |
| D3DRS \_ DIFFUSEMATERIALSOURCE  | Definiert, wo diffuse Materialfarbe erhalten werden soll.  | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR1   |
| D3DRS \_ SPECULARMATERIALSOURCE | Definiert, wo die Farbe des Glanzmaterials erhalten werden soll. | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR2   |
| D3DRS \_ EMISSIVEMATERIALSOURCE | Definiert, wo eine freizügige Materialfarbe angezeigt werden soll. | D3DMATERIALCOLORSOURCE | D3DMCS \_ MATERIAL |
| D3DRS \_ COLORVERTEX            | Deaktiviert oder aktiviert die Verwendung von Scheitelpunktfarben.     | BOOL                   | TRUE             |



 

Der Alpha-/Transparenzwert stammt immer nur aus dem Alphakanal der diffusen Farbe.

Der Farbwert stammt immer nur aus dem Alphakanal der Glanzfarbe.

D3DMATERIALCOLORSOURCE kann die folgenden Werte aufweisen.

-   D3DMCS \_ MATERIAL – Materialfarbe wird als Quelle verwendet.
-   D3DMCS COLOR1 : \_ Diffuse Vertexfarbe wird als Quelle verwendet.
-   D3DMCS COLOR2 : \_ Die Specular Vertex-Farbe wird als Quelle verwendet.

## <a name="light-direction"></a>Lichtrichtung

Die Richtungseigenschaft eines Lichts bestimmt die Richtung, in der das vom Objekt ausgegebene Licht im Weltraum bewegt wird. Die Richtung wird nur von gerichteten Beleuchtungen und Spotlights verwendet und mit einem Vektor beschrieben.

Legen Sie die Lichtrichtung im Direction-Member der [**D3DLIGHT9-Struktur**](d3dlight9.md) des Lichts fest. Der Richtungsmember ist vom Typ [**D3DVECTOR.**](d3dvector.md) Richtungsvektoren werden unabhängig von der Position des Lichts in einer Szene als Entfernungen von einem logischen Ursprung beschrieben. Daher weist ein Blickpunkt, der direkt auf eine Szene zeigt – entlang der positiven Z-Achse – einen Richtungsvektor von <0,0,1>, unabhängig davon, wo seine Position definiert ist. Auf ähnliche Weise können Sie das direkt auf einer Szene geschaltete Strahllicht simulieren, indem Sie ein direktionales Licht verwenden, dessen Richtung <0,-1,0> ist. Natürlich müssen Sie keine Beleuchtung erstellen, die entlang der Koordinatenachsen leuchtet. Sie können Werte mischen und abgleichen, um Licht zu erzeugen, das in interessanteren Winkeln leuchtet.

> [!Note]  
> Obwohl Sie den Richtungsvektor eines Lichts nicht normalisieren müssen, stellen Sie immer sicher, dass er eine Größe hat. Verwenden Sie also keinen <0,0,0> Richtungsvektor.

 

## <a name="light-position"></a>Lichtposition

Die Lichtposition wird mithilfe einer [**D3DVECTOR-Struktur**](d3dvector.md) im Position-Member der [**D3DLIGHT9-Struktur**](d3dlight9.md) beschrieben. Es wird davon ausgegangen, dass sich die x-, y- und z-Koordinaten im Weltraum befinden. Direktionale Beleuchtung ist die einzige Art von Licht, die nicht die Position-Eigenschaft verwendet.

## <a name="light-range"></a>Lichtbereich

Die Bereichseigenschaft eines Lichts bestimmt den Abstand im Weltraum, bei dem Gitternetze in einer Szene kein von diesem Objekt ausgegebenes Licht mehr empfangen. Das Range-Element enthält einen Gleitkommawert, der den maximalen Bereich des Lichts im Weltraum darstellt. Richtungslichter verwenden nicht die Bereichseigenschaft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beleuchtung und Materialien](lights-and-materials.md)
</dt> </dl>

 

 
