---
description: Pherical Environment Maps (Kugelumgebungszuordnungen) sind spezielle Texturen, die ein Bild der Szene um ein Objekt oder die Beleuchtungseffekte um das Objekt enthalten.
ms.assetid: b4a8defc-876f-4a23-a12e-e7423a1e8f89
title: Pherical Environment Mapping (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be4347b71a041aaa8d7057ac2bb7523bfa235fe59f84fe1ba54c54283cd2159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746388"
---
# <a name="spherical-environment-mapping-direct3d-9"></a>Pherical Environment Mapping (Direct3D 9)

Pherical Environment Maps (Kugelumgebungszuordnungen) sind spezielle Texturen, die ein Bild der Szene um ein Objekt oder die Beleuchtungseffekte um das Objekt enthalten. Im Gegensatz zu kubischen Umgebungszuordnungen stellen Kugelkarten nicht direkt die Umgebung eines Objekts dar. Das Thema "Teepotentbild im Thema Umgebungszuordnung [(Direct3D 9)"](environment-mapping.md) zeigt die Reflektionseffekte, die Sie mit der Kugelzuordnung erreichen können. Eine Kugelkarte ist eine 2D-Darstellung der vollständigen 360-Grad-Ansicht der Szene um ein Objekt, wie es in der folgenden Abbildung dargestellt ist.

![Abbildung einer Kugelkarte des Inneren eines Gebäudes](images/spheremap.png)

## <a name="texture-coordinates-for-spherical-environment-maps"></a>Texturkoordinaten für pherische Karten

Die Texturkoordinaten, die Sie für jeden Scheitelpunkt angeben, der eine Umgebungszuordnung empfängt, sollten die Textur als Funktion der reflektierenden Verzerrung adressieren, die durch die Krümmung der Oberfläche erzeugt wird. Anwendungen müssen diese Texturkoordinaten für jeden Scheitelpunkt berechnen, um den gewünschten Effekt zu erzielen. Eine einfache und effektive Möglichkeit zum Generieren von Texturkoordinaten verwendet den Scheitelpunkt normal als Eingabe. Obwohl mehrere Methoden vorhanden sind, ist die folgende Gleichung bei Anwendungen üblich, die eine Umgebungszuordnung mit Kugelzuordnungen durchführen.

![Gleichung der Berechnung von Texturkoordinaten für eine Kugelkarte](images/spheremap-formula.png)

In diesen Formeln sind Sie und v die Texturkoordinaten, die berechnet werden, und N<sub>X</sub> und N<sub>Y</sub> sind die x- und y-Komponenten des Normalen des Scheitelpunkts des Kameraraums. Die Formel ist einfach, aber effektiv. Wenn der Normalwert über eine positive x-Komponente verfügt, zeigt der Normalwert nach rechts, und die u-Koordinate wird angepasst, um die Textur entsprechend zu adressieren. Ebenso für die v-Koordinate: Positives y gibt an, dass der Normalwert nach oben zeigt. Das Gegenteil gilt für negative Werte in jeder Komponente.

Wenn der Normalwert direkt auf die Kamera zeigt, sollten die resultierenden Koordinaten keine Verzerrung erhalten. Die +0,5-Verzerrung an beiden Koordinaten platziert den Punkt der Nullverzerrung in der Mitte der Kugelkarte, und ein Scheitelpunkt normal von (0, 0, z) adressiert diesen Punkt. Diese Formel berücksichtigt nicht die z-Komponente des Normalen, aber Anwendungen, die die Formel verwenden, können Berechnungen optimieren, indem Scheitelungen mit einem Normalwert übersprungen werden, der ein positives z-Element hat. Dies funktioniert bei flach schattierten Objekten, da der Scheitelpunkt beim Rendern des Objekts im Kameraraum gecullt wird, wenn der normale Punkt von der Kamera abwedelt (positive z). Bei Gouraud-schattierten Objekten kann ein Normalwert von der Kamera wegzeige (positives x), und das Dreieck, das den Scheitelpunkt enthält, kann weiterhin sichtbar sein. Wenn Sie sie und v für diesen Scheitelpunkt nicht berechnen, kann das Gesicht weiterhin verwendet werden, was zu unerwartetem Verhalten führt.

## <a name="applying-spherical-environment-maps"></a>Anwenden von pherical Environment Karten

Sie wenden eine Umgebungszuordnung auf Objekte auf die gleiche Weise wie für jede andere Textur an, indem Sie die Textur mit der [**IDirect3DDevice9::SetTexture-Methode**](/windows/desktop/api) auf die entsprechende Texturstufe festlegen. Legen Sie den ersten Parameter auf den Index für die gewünschte Texturphase und den zweiten Parameter auf die Adresse der [**IDirect3DDevice9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) fest, die zurückgegeben wurde, als Sie die Textur für die Umgebungszuordnung erstellt haben. Sie können die Farb- und Alphamischungsvorgänge und Argumente nach Bedarf festlegen, um die gewünschten Texturmischungseffekte zu erzielen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Umgebungszuordnung](environment-mapping.md)
</dt> </dl>

 

 
