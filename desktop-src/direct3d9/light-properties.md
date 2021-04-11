---
description: Helle Eigenschaften beschreiben den Typ und die Farbe einer Lichtquelle.
ms.assetid: b39f1287-c67b-4cbb-b599-4a1b2f4981ac
title: Light-Eigenschaften (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63239024109327e483ff93c2ee29fe42fc22c922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124010"
---
# <a name="light-properties-direct3d-9"></a>Light-Eigenschaften (Direct3D 9)

Helle Eigenschaften beschreiben den Typ und die Farbe einer Lichtquelle. Abhängig von der Art des verwendeten Lichts kann ein Lichteigenschaften für die Dämpfung und den Bereich oder für Spotlight-Effekte aufweisen. Allerdings verwenden nicht alle Arten von Lichtern alle Eigenschaften. Direct3D verwendet die [**D3DLIGHT9**](d3dlight9.md) -Struktur, um Informationen über helle Eigenschaften für alle Typen von Lichtquellen zu übertragen. Dieser Abschnitt enthält Informationen zu allen hellen Eigenschaften. Die Informationen sind in die folgenden Gruppen unterteilt:

Die Eigenschaften Position, Bereich und Dämpfung definieren die Position eines Lichts im Raum, und wie sich das Licht ausgibt, verhält sich über die Entfernung. Wie bei allen hellen Eigenschaften, die Sie in C++ verwenden, sind diese in der [**D3DLIGHT9**](d3dlight9.md) -Struktur eines Lichts enthalten.

-   [Licht Dämpfung](#light-attenuation)
-   [Helle Farbe](#light-color)
-   [Lichtrichtung](#light-direction)
-   [Helle Position](#light-position)
-   [Heller Bereich](#light-range)

## <a name="light-attenuation"></a>Licht Dämpfung

Durch die Dämpfung wird gesteuert, wie sich die Intensität eines Lichts auf den maximalen Abstand verringert, der in der Range-Eigenschaft angegeben ist. Drei [**D3DLIGHT9**](d3dlight9.md) -Strukturmember stellen eine leichte Dämpfung dar: Attenuation0, Attenuation1 und Attenuation2. Diese Member enthalten Gleit Komma Werte im Bereich von 0,0 bis unendlich und steuern die Dämpfung eines Lichts. Einige Anwendungen legen das Attenuation1-Element auf 1,0 und die anderen auf 0,0 fest, was zu einer leichten Intensität führt, die sich als 1/D ändert, wobei D der Abstand von der Lichtquelle zum Scheitelpunkt ist. Die maximale Lichtintensität befindet sich an der Quelle, die auf 1/(heller Bereich) im hellen Bereich reduziert wird. In der Regel legt eine Anwendung Attenuation0 auf 0,0, Attenuation1 auf einen konstanten Wert und Attenuation2 auf 0,0 fest.

Sie können Dämpfungswerte kombinieren, um komplexere Dämpfungseffekte zu erzielen. Sie können diese Werte auch auf Werte außerhalb des normalen Bereichs festlegen, um sogar die Auswirkungen auf eine andere Dämpfung zu erzeugen. Negative Dämpfungswerte sind jedoch nicht zulässig. Siehe [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md).

## <a name="light-color"></a>Helle Farbe

In Direct3D werden drei Farben ausgegeben, die unabhängig in den Beleuchtungsberechnungen des Systems verwendet werden: eine diffuse Farbe, eine Umgebungs Farbe und eine Glanz Farbe. Jede wird durch das Direct3D-Beleuchtungs Modul integriert, das mit einem Gegenstück aus dem aktuellen Material interagiert, um eine endgültige, beim Rendering verwendete Farbe zu schaffen. Die diffuse Farbe interagiert mit der diffctance-Eigenschaft der diffctance-Eigenschaft des aktuellen Materials, der Glanz Farbe mit der Glanz Wert Eigenschaft des Materials und so weiter. Einzelheiten dazu, wie Direct3D diese Farben anwendet, finden Sie unter [Mathematik der Beleuchtung (Direct3D 9)](mathematics-of-lighting.md).

In einer C++-Anwendung enthält die [**D3DLIGHT9**](d3dlight9.md) -Struktur drei Member für diese Farben (diffuses, Ambient und specatyp). jede ist eine [**D3DCOLORVALUE**](d3dcolorvalue.md) -Struktur, die die ausgegebene Farbe definiert.

Der Typ der Farbe, der sich am stärksten auf die Berechnungen des Systems anwendet, ist die diffuse Farbe. Die häufigste diffuse Farbe ist weiß (r:1.0 g:1.0 b:1.0), Sie können jedoch Farben nach Bedarf erstellen, um gewünschte Effekte zu erzielen. Beispielsweise können Sie rotes Licht für einen Kamin verwenden, oder Sie können grünes Licht für ein Verkehrssignal verwenden, das auf "Go" festgelegt ist.

Im Allgemeinen legen Sie die Komponenten für helle Farben auf Werte zwischen 0,0 und 1,0 (einschließlich) fest, dies ist jedoch nicht zwingend erforderlich. Beispielsweise können Sie alle Komponenten auf 2,0 festlegen, um ein Licht zu schaffen, das "heller als weiß" ist. Diese Art von Einstellung kann besonders nützlich sein, wenn Sie andere Einstellungen als Konstante verwenden.

Obwohl Direct3D RGBA-Werte für Lights verwendet, wird die Alpha Farbkomponente nicht verwendet.

In der Regel werden Material Farben für die Beleuchtung verwendet. Sie können jedoch angeben, dass die Material Farben (emissive, Ambient, diffuses und Glanz) durch diffuse oder Glanz Ende Scheitelpunkt Farben überschrieben werden sollen. Dies erfolgt durch Aufrufen von " [**strenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) " und durch Festlegen der in der folgenden Tabelle aufgeführten Gerätestatus Variablen.



| Gerätestatus Variable         | Bedeutung                                       | type                   | Standard          |
|-------------------------------|-----------------------------------------------|------------------------|------------------|
| D3DRS \_ AmbientMaterialSource  | Definiert, wo die Umgebungs Material Farbe zu erhalten ist.  | D3DMATERIALCOLORSOURCE | D3DMCS \_ Material |
| D3DRS \_ DiffuseMaterialSource  | Definiert, wo eine diffuse Material Farbe zu finden ist.  | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR1   |
| D3DRS \_ SpecularMaterialSource | Definiert den Ort, an dem eine Glanz Material Farbe zu finden ist. | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR2   |
| D3DRS \_ emissivematerialsource | Definiert den Speicherort für die selbst leuchtendes-Material Farbe. | D3DMATERIALCOLORSOURCE | D3DMCS \_ Material |
| D3DRS \_ ColorVertex            | Deaktiviert oder aktiviert die Verwendung von Scheitelpunkt Farben.     | BOOL                   | TRUE             |



 

Der Alpha/Transparenz-Wert ergibt sich immer nur aus dem Alphakanal der diffusen Farbe.

Der Nebelwert wird immer nur aus dem Alphakanal der Glanz Farbe abgeleitet.

D3DMATERIALCOLORSOURCE kann die folgenden Werte aufweisen.

-   D3DMCS \_ Material-Material Color wird als Quelle verwendet.
-   D3DMCS \_ COLOR1-diffuse Scheitelpunkt Farbe wird als Quelle verwendet.
-   D3DMCS \_ COLOR2-Glanz-Scheitelpunkt Farbe wird als Quelle verwendet.

## <a name="light-direction"></a>Lichtrichtung

Die Direction-Eigenschaft eines Lichts bestimmt die Richtung, in der das durch das Objekt ausgegebene Licht in Welt Raum verläuft. Die Richtung wird nur von direktionalen Lichtern und Schein Lichtern verwendet und wird mit einem Vektor beschrieben.

Legen Sie die helle Richtung im Direction-Member der [**D3DLIGHT9**](d3dlight9.md) -Struktur des Lichts fest. Direction-Member ist vom Typ [**D3DVECTOR**](d3dvector.md). Richtungs Vektoren werden als Abstände von einem logischen Ursprung, unabhängig von der Position des Lichts in einer Szene, beschrieben. Daher hat ein Spotlight, das direkt auf eine Szene entlang der positiven z-Achse zeigt, einen Richtungsvektor <0, 0, 1> unabhängig davon, wo seine Position als festgelegt ist. Auf ähnliche Weise können Sie das Licht direkt in einer Szene simulieren, indem Sie ein Direktionales Licht verwenden, dessen Richtung <0,-1, 0> ist. Natürlich müssen Sie keine Leuchten erstellen, die entlang der Koordinatenachsen Leuchten. Sie können Werte mischen und abgleichen, um Beleuchtung zu erstellen, die in interessanteren Winkeln angezeigt werden.

> [!Note]  
> Obwohl Sie den Richtungsvektor eines Lichts nicht normalisieren müssen, stellen Sie immer sicher, dass er die Größe hat. Verwenden Sie also keinen <0, 0, 0> Richtungsvektor.

 

## <a name="light-position"></a>Helle Position

Die helle Position wird mithilfe einer [**D3DVECTOR**](d3dvector.md) -Struktur im Positions Element der [**D3DLIGHT9**](d3dlight9.md) -Struktur beschrieben. Es wird davon ausgegangen, dass die x-, y-und z-Koordinaten sich im Raum der Welt befinden. Direktionale Lichter sind der einzige Typ von Licht, der die Positions Eigenschaft nicht verwendet.

## <a name="light-range"></a>Heller Bereich

Die Range-Eigenschaft eines Lichts bestimmt den Abstand im Raum, bei dem Meshs in einer Szene nicht mehr von diesem Objekt ausgegebene Licht empfangen. Der Bereichs Member enthält einen Gleit Komma Wert, der den maximalen Bereich des Lichts im Raum darstellt. Direktionale Lichter verwenden nicht die Range-Eigenschaft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beleuchtung und Materialien](lights-and-materials.md)
</dt> </dl>

 

 
