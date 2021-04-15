---
description: Anwendungen müssen die Textur Filterung nicht verwenden.
ms.assetid: bba0e485-ac5a-4e43-9eb7-25cd0c90d316
title: Nearest-Point Sampling (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11cf98ee917b124b35f3c30ff263365ec3c46e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392589"
---
# <a name="nearest-point-sampling-direct3d-9"></a>Nearest-Point Sampling (Direct3D 9)

Anwendungen müssen die Textur Filterung nicht verwenden. Direct3D kann so festgelegt werden, dass die textabzahl berechnet wird, die häufig nicht Ganzzahlen ergibt, und die Farbe des texms mit der nächstgelegenen ganzzahligen Adresse kopiert. Dieser Vorgang wird als "nächster Punkt Sampling" bezeichnet. Dies kann eine schnelle und effiziente Methode zum Verarbeiten von Texturen sein, wenn die Größe der Textur der Größe des primitiven Bilds auf dem Bildschirm ähnelt. Andernfalls muss die Textur vergrößert oder minimiert werden. Das Ergebnis kann ein segmentierte, Alias-oder unscharfe Bild sein.

Ihre C++-Anwendung kann die Stichprobenentnahme am nächsten Punkt durch Aufrufen der Methode [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) auswählen. Legen Sie den Wert des ersten Parameters auf die ganzzahlige Indexnummer (0-7) der Textur fest, für die Sie eine Textur Filterungs Methode auswählen. Übergeben \_ Sie D3DSAMP MagFilter, D3DSAMP \_ MinFilter oder D3DSAMP \_ MipFilter für den zweiten Parameter, um den Filter für die Vergrößerung, minifizierung oder den Mipmapping-Filter festzulegen. Pass D3DTEXF \_ Punkt im dritten Parameter.

Sie sollten die Stichprobenentnahme für das nächste Punkt sorgfältig verwenden, da es mitunter grafische Artefakte verursachen kann, wenn die Textur an der Grenze zwischen zwei texeln gemessen wird. Diese Grenze ist die Position entlang der Textur (u oder v), an der der abgetastete Texturtyp von einem texturdown zum nächsten übergeht. Wenn die Punkt Stichproben Erstellung verwendet wird, wählt das System ein Beispiel textexaus, und das Ergebnis kann sich bei Überschreitung der Grenze plötzlich von einem texseto den nächsten texsetyp ändern. Dieser Effekt kann in der angezeigten Textur als unerwünschte grafische Artefakte angezeigt werden. Wenn eine lineare Filterung verwendet wird, wird das resultierende Texel aus benachbarten texeln berechnet und nahtlos zwischen Ihnen gemischt, wenn der Textur Index durch die Grenze bewegt wird.

Dieser Effekt kann bei der Zuordnung einer sehr kleinen Textur zu einem sehr großen Polygon angezeigt werden: ein Vorgang, der häufig als Vergrößerungs Vorgang bezeichnet wird. Wenn Sie z. b. eine Textur verwenden, die wie ein checkboard aussieht, führt die Stichprobenentnahme am nächsten Punkt zu einem größeren checkboard, das unterschiedliche Ränder anzeigt. Im Gegensatz dazu führt die lineare Textur Filterung zu einem Bild, bei dem die Farben des Prüf Boards über das gesamte Polygon hinweg reibungslos abweichen.

In den meisten Fällen erhalten Anwendungen die besten Ergebnisse, indem Sie nach Möglichkeit das nächste Punkt Beispiel vermeiden. Der Großteil der Hardware ist heute für die lineare Filterung optimiert, sodass Ihre Anwendung nicht beeinträchtigt wird. Wenn die gewünschte Auswirkung wirklich die Verwendung der nächsten Punkt Stichprobe erfordert, z. b. bei der Verwendung von Texturen zum Anzeigen lesbarer Textzeichen, sollte Ihre Anwendung sehr vorsichtig sein, um die Stichprobenentnahme an den Textzeile zu vermeiden, was zu unerwünschten Effekten führen kann. In der folgenden Abbildung wird gezeigt, wie diese Artefakte aussehen können.

![Abbildung eines sechsstufigen Felds mit nicht kontinuierlichen horizontalen Linien in den beiden oberen rechten Quadraten](images/ptrtfct.png)

Beachten Sie, dass die beiden Quadrate in der oberen rechten Ecke der Gruppe sich von den Nachbarn unterscheiden, wobei diagonal Offsets durch Sie ausgeführt werden. Um Grafik Artefakte wie diese zu vermeiden, müssen Sie mit den Direct3D-Textur-Samplings-Regeln für die Next-Point-Filterung vertraut sein. Direct3D ordnet eine Gleit Komma-Textur Koordinate im \[ Bereich von 0,0, 1,0 \] (0,0 bis 1,0, inklusiv) einem ganzzahligen Texel-Leerraum zu, \[ der von-0,5, n-0,5 \] , wobei n die Anzahl der texeln in einer gegebenen Dimension in der Textur ist. Der resultierende Textur Index wird auf die nächste ganze Zahl gerundet. Diese Zuordnung kann zu Stichproben Ungenauigkeiten bei Texel-Grenzen führen.

Stellen Sie sich bei einem einfachen Beispiel eine Anwendung vor, die Polygone mit dem D3DTADDRESS \_ Wrap-Textur Adressierungs Modus rendert. Mit der von Direct3D verwendeten Zuordnung wird der u-Textur Index wie im folgenden Diagramm dargestellt für eine Textur mit einer Breite von 4 texeln zugeordnet.

![Diagramm der Texturkoordinaten 0,0 und 1,0 an der Grenze zwischen texeln](images/ptsmpprb.png)

Beachten Sie, dass sich die Texturkoordinaten 0,0 und 1,0 für diese Abbildung genau von der Grenze zwischen Texels unterliegen. Mithilfe der Methode, mit der Direct3D-Werte zuordnet, reichen die Texturkoordinaten von \[ -0,5, 4-0,5 \] , wobei 4 die Breite der Textur ist. In diesem Fall handelt es sich bei dem abgetasteten textext um den 0 textext für einen Textur Index von 1,0. Wenn die Textur Koordinate jedoch nur geringfügig kleiner als 1,0 ist, wäre der abgetastete textext der n Texel anstelle des 0-Texels.

Dies impliziert, dass eine kleine Textur mit Texturkoordinaten von exakt 0,0 und 1,0 mit der nächstgelegenen Filterung auf einem auf einem Bildschirmrand ausgerichteten Dreieck in Pixel vergrößert wird, für die die Textur Map an der Grenze zwischen Texels gemessen wird. Alle Ungenauigkeiten bei der Berechnung von Texturkoordinaten, die jedoch klein sind, führen zu Artefakten in den Bereichen im gerenderten Bild, die den texrändern der Textur Karte entsprechen.

Die Durchführung dieser Zuordnung von Gleit Komma Texturkoordinaten zu ganzzahligen texeln mit perfekter Genauigkeit ist schwierig, Rechenzeit aufwändig und in der Regel nicht erforderlich. Die meisten Hardware Implementierungen verwenden einen iterativen Ansatz zum Berechnen von Texturkoordinaten an jeder Pixelposition innerhalb eines Dreiecks. Iterative Ansätze Blenden tendenziell diese Ungenauigkeiten aus, da die Fehler gleichmäßig während der Iteration kumuliert werden.

Der Direct3D Reference Raster verwendet einen direkt Auswertungs Ansatz zum Berechnen von Textur Indizes an jedem Pixel Speicherort. Die direkte Auswertung unterscheidet sich vom iterativen Ansatz dahin, dass jede Ungenauigkeit im Vorgang eine eher zufällige Fehlerverteilung aufweist. Das Ergebnis ist, dass die an den Grenzen auftretenden Stichprobenfehler deutlicher erkennbar sein können, da der Verweis Raster diesen Vorgang nicht mit der perfekten Genauigkeit ausführt.

Der beste Ansatz besteht darin, die nächstgelegene Punkt Filterung nur bei Bedarf zu verwenden. Wenn Sie es verwenden müssen, empfiehlt es sich, die Texturkoordinaten leicht von den Begrenzungs Positionen zu versetzen, um Artefakte zu vermeiden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Filterung](texture-filtering.md)
</dt> </dl>

 

 
