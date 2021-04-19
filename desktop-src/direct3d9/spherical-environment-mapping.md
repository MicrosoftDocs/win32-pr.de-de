---
description: Kugelförmige Umgebungs Zuordnungen oder Kugel Karten sind spezielle Texturen, die ein Bild der Szene in Bezug auf ein Objekt enthalten, oder die Beleuchtungseffekte um das Objekt.
ms.assetid: b4a8defc-876f-4a23-a12e-e7423a1e8f89
title: Sphärischen Umgebungs Zuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b0e7aaa123478ecc7cc327dca0b13a8aae3d0c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346607"
---
# <a name="spherical-environment-mapping-direct3d-9"></a>Sphärischen Umgebungs Zuordnung (Direct3D 9)

Kugelförmige Umgebungs Zuordnungen oder Kugel Karten sind spezielle Texturen, die ein Bild der Szene in Bezug auf ein Objekt enthalten, oder die Beleuchtungseffekte um das Objekt. Im Gegensatz zu kubischen Umgebungs Zuordnungen stellen Kugel Karten nicht direkt die Umgebung eines Objekts dar. Das Teekanne-Bild im Thema [Umgebungs Zuordnung (Direct3D 9)](environment-mapping.md) zeigt die reflektionseffekte, die Sie mit der Kugel Zuordnung erreichen können. Eine Kugel Karte ist eine 2D-Darstellung der vollständigen 360-Grad-Ansicht der Szene, die ein Objekt umschließt, wie in der folgenden Abbildung dargestellt.

![Darstellung eines Kugel Bilds von innerhalb eines Gebäudes](images/spheremap.png)

## <a name="texture-coordinates-for-spherical-environment-maps"></a>Texturkoordinaten für kugelförmige Umgebungs Zuordnungen

Die Texturkoordinaten, die Sie für jeden Scheitelpunkt angeben, der eine Umgebungs Zuordnung empfängt, sollten die Textur als eine Funktion der reflektierenden Verzerrung adressieren, die von der Krümmung der Oberfläche erstellt wird. Anwendungen müssen diese Texturkoordinaten für jeden Scheitelpunkt berechnen, um den gewünschten Effekt zu erzielen. Eine einfache und effektive Methode zum Generieren von Texturkoordinaten verwendet den Scheitelpunkt normal als Eingabe. Obwohl mehrere Methoden vorhanden sind, ist die folgende Gleichung bei Anwendungen üblich, die eine Umgebungs Zuordnung mit Kugel Karten durchführen.

![Gleichung der Berechnung von Texturkoordinaten für eine Kugel Karte](images/spheremap-formula.png)

In diesen Formeln sind Sie und v die berechneten Texturkoordinaten, und n<sub>x</sub> und n<sub>y</sub> sind die X-und y-Komponenten des Scheitelpunkt Scheitel Punkts in der Kamera. Die Formel ist einfach, aber effektiv. Wenn der normale eine positive x-Komponente aufweist, zeigt die normale auf der rechten Seite an, und die u-Koordinate wird so angepasst, dass die Textur entsprechend adressiert wird. Gleiches gilt für die v-Koordinate: positiv y gibt an, dass die normale Punkte angezeigt werden. Das Gegenteil gilt für negative Werte in jeder Komponente.

Wenn der normale Punkt direkt auf der Kamera steht, sollten die resultierenden Koordinaten keine Verzerrung erhalten. Die + 0,5-Abweichung an beide Koordinaten legt den Punkt der null-Verzerrung in der Mitte der Kugel Karte und eine Scheitelpunkt normale von (0, 0, z) auf diesen Punkt. Diese Formel berücksichtigt nicht die z-Komponente der normalen, aber Anwendungen, die die Formel verwenden, können Berechnungen optimieren, indem Sie Scheitel Punkte mit einem normalen Element überspringen, das ein positives z-Element aufweist. Dies funktioniert bei flatschattierten Objekten, da der Scheitelpunkt beim Rendern des-Objekts in der Kamera, wenn er von der Kamera entfernt wird (positiver z), beim Rendern des-Objekts ein Zeichen ist. Bei von Gouraud schattierten Objekten kann ein normaler Weg von der Kamera (positives x) und das Dreieck, das den Scheitelpunkt enthält, weiterhin sichtbar sein. Wenn Sie für diesen Scheitelpunkt nicht COMPUTE und v verwenden, kann das Gesicht weiterhin verwendet werden. Dies führt zu unerwartetem Verhalten.

## <a name="applying-spherical-environment-maps"></a>Anwenden von kugelförmigen Umgebungs Zuordnungen

Sie wenden eine Umgebungs Zuordnung auf Objekte auf die gleiche Weise wie für jede andere Textur an, indem Sie die Textur auf die passende Textur Phase mit der [**IDirect3DDevice9:: SetTexture**](/windows/desktop/api) -Methode festlegen. Legen Sie den ersten Parameter auf den Index der gewünschten Textur Phase fest, und legen Sie den zweiten Parameter auf die Adresse der [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle fest, die beim Erstellen der Textur für die Umgebungs Zuordnung zurückgegeben wurde. Sie können die Farb-und Alpha Mischungs Vorgänge und Argumente nach Bedarf festlegen, um die gewünschten Textur Mischungs Effekte zu erzielen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Umgebungs Zuordnung](environment-mapping.md)
</dt> </dl>

 

 
