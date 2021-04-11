---
description: Direct3D wendet die folgenden Formeln auf die du-und DV-Komponenten in jedem Bump Map-Pixel an.
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: Bump-mappinenformeln (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436aee9689d78b8b706bb98d908f2e3fbc05ca6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127780"
---
# <a name="bump-mapping-formulas-direct3d-9"></a>Bump-mappinenformeln (Direct3D 9)

Direct3D wendet die folgenden Formeln auf die Komponenten "D<sub>U</sub> " und "d<sub>V</sub> " in jedem Bump Map-Pixel an.

![Formeln für die Transformationen der Bump-mappingmatrix](images/dudv-transform.png)

In diesen Formeln werden die Variablen d<sub>u</sub> und d<sub>v</sub> direkt von einem Bump-Karten Pixel entnommen und durch eine 2 x 2-Matrix transformiert, um die Ausgabe Delta Werte d<sub>u</sub>' und d<sub>v</sub>' zu erhalten. Das System verwendet die Ausgabewerte, um die Texturkoordinaten zu ändern, die die Umgebungs Zuordnung in der nächsten Textur Phase adressieren. Die Koeffizienten der Transformationsmatrix werden auch in den \_ Zuständen D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT10, D3DTSS \_ BUMPENVMAT01 und D3DTSS \_ BUMPENVMAT11 Texture festgelegt.

Zusätzlich zu den Delta Werten von "You" und "v" kann das System einen leuchtwert berechnen, der zum modulieren der Farbe der Umgebungs Zuordnung in der nächsten Mischungs Stufe verwendet wird, wie in der folgenden Formel dargestellt.

![Formel für Ausgabe Beleuchtung, berechnet von Skalierungsfaktor und Offset](images/l-transform.png)

In dieser Formel ist L ' die Ausgabe Helligkeit, die berechnet wird. Die L-Variable ist der von einem Bump-Karten Pixel ergriffene Glanz Wert, der mit dem Skalierungsfaktor multipliziert wird und dem Wert in der Variablen O entspricht. In den \_ Textur Phasen "D3DTSS bumpenvlscale" und "D3DTSS \_ bumpenvloffset" werden die Werte für die e-und O-Variablen in der Formel gesteuert. Diese Formel wird nur angewendet, wenn der Textur Mischungs Vorgang für die Stufe, die die Bump Map enthält, auf D3DTOP \_ bumpenvmapluminance festgelegt ist. Bei Verwendung \_ von D3DTOP bumpenvmap verwendet das System den Wert 1,0 für L '.

Nach dem Berechnen der Ausgabe Delta Werte D<sub>U</sub>' and d<sub>V</sub>' werden diese in der nächsten Textur Phase den Texturkoordinaten hinzugefügt, und die ausgewählte Farbe wird von der Leuchtkraft zur Erstellung der auf das Polygon angewendeten Farbe modusiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bump-Zuordnung](bump-mapping.md)
</dt> </dl>

 

 



