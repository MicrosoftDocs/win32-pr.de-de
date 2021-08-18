---
description: Anwendungen müssen keine Texturfilterung verwenden.
ms.assetid: bba0e485-ac5a-4e43-9eb7-25cd0c90d316
title: Nearest-Point Sampling (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee8146ce8cfc2d5852cf3847233b431352d69b8bc1f0a52f41da5ac3c9a7c89d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119458758"
---
# <a name="nearest-point-sampling-direct3d-9"></a>Nearest-Point Sampling (Direct3D 9)

Anwendungen müssen keine Texturfilterung verwenden. Direct3D kann so festgelegt werden, dass die Texeladresse berechnet wird, die häufig nicht als ganze Zahlen ausgewertet wird, und kopiert die Farbe des Texels mit der nächstgelegenen ganzzahligen Adresse. Dieser Prozess wird als Nearest Point Sampling (Stichprobenentnahme am nächsten Punkt) bezeichnet. Dies kann eine schnelle und effiziente Methode zum Verarbeiten von Texturen sein, wenn die Größe der Textur der Größe des Bilds des Primitivs auf dem Bildschirm ähnelt. Andernfalls muss die Textur vergrößert oder verknöpft werden. Das Ergebnis kann ein segmentiertes, gealiastes oder unscharfes Bild sein.

Ihre C++-Anwendung kann die Stichprobenentnahme am nächsten Punkt auswählen, indem sie die [**IDirect3DDevice9::SetSamplerState-Methode aufruft.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) Legen Sie den Wert des ersten Parameters auf die ganzzahlige Indexnummer (0-7) der Textur fest, für die Sie eine Texturfilterungsmethode auswählen. Übergeben Sie D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER oder D3DSAMP \_ MIPFILTER für den zweiten Parameter, um den Filter für Vergrößerung, Vergrößerung oder Mipmapping festzulegen. Übergeben Sie D3DTEXF \_ POINT im dritten Parameter.

Sie sollten die Stichprobenentnahme am nächsten Punkt sorgfältig verwenden, da dies manchmal zu grafischen Artefakten führen kann, wenn die Textur an der Grenze zwischen zwei Texeln entnommen wird. Diese Grenze ist die Position entlang der Textur (u oder v), an der das zusammengestellte Texel von einem Texel zum nächsten übergeht. Wenn Punktstichproben verwendet werden, wählt das System ein Beispiel-Texel oder das andere aus, und das Ergebnis kann sich plötzlich von einem Texel zum nächsten texel ändern, wenn die Grenze überschritten wird. Dieser Effekt kann als unerwünschte Grafikartefakte in der angezeigten Textur angezeigt werden. Wenn die lineare Filterung verwendet wird, wird das resultierende Texel sowohl aus benachbarten Texeln berechnet als auch reibungslos kombiniert, wenn sich der Texturindex durch die Grenze bewegt.

Dieser Effekt kann beim Zuordnen einer sehr kleinen Textur zu einem sehr großen Polygon beobachtet werden: ein Vorgang, der häufig als Vergrößerung bezeichnet wird. Wenn Sie beispielsweise eine Textur verwenden, die wie ein Checkerboard aussieht, führt die Stichprobenentnahme am nächsten Punkt zu einem größeren Checkerboard, das unterschiedliche Kanten anzeigt. Im Gegensatz dazu führt die lineare Texturfilterung zu einem Bild, bei dem die Farben des Checkerboards gleichmäßig über das Polygon variieren.

In den meisten Fällen erhalten Anwendungen die besten Ergebnisse, indem sie nach Möglichkeit die nächstgelegene Punktstichprobe vermeiden. Der Großteil der Hardware ist derzeit für die lineare Filterung optimiert, sodass die Leistung Ihrer Anwendung nicht beeinträchtigt werden sollte. Wenn für den gewünschten Effekt unbedingt die Verwendung der Stichprobenentnahme am nächsten Punkt erforderlich ist , z. B. wenn Texturen verwendet werden, um lesbare Textzeichen anzuzeigen, sollte Ihre Anwendung äußerst vorsichtig sein, um die Stichprobenentnahme an den Texelgrenzen zu vermeiden, was zu unerwünschten Effekten führen kann. Die folgende Abbildung zeigt, wie diese Artefakte aussehen können.

![Abbildung eines sechsteiligen Felds mit nicht zusammenhängenden horizontalen Linien in den beiden oberen rechten Quadraten](images/ptrtfct.png)

Beachten Sie, dass die beiden Quadrate in der oberen rechten Seite der Gruppe anders erscheinen als ihre Nachbarn, wobei diagonale Offsets durch sie verlaufen. Um grafische Artefakte wie diese zu vermeiden, müssen Sie mit Direct3D-Textursamplingregeln für die Filterung des nächstgelegenen Punkts vertraut sein. Direct3D ordnet eine Gleitkommatexturkoordinate im Bereich von \[ 0,0, 1,0 \] (0,0 bis 1,0, einschließlich) einem ganzzahligen Texelbereichswert im Bereich von \[ - 0,5, n bis 0,5 zu, \] wobei n die Anzahl der Texel in einer bestimmten Dimension in der Textur ist. Der resultierende Texturindex wird auf die nächste ganze Zahl gerundet. Diese Zuordnung kann Samplingungenauigkeiten an Texelgrenzen einführen.

Stellen Sie sich für ein einfaches Beispiel eine Anwendung vor, die Polygone mit dem Texturadressierungsmodus D3DTADDRESS \_ WRAP rendert. Mithilfe der von Direct3D verwendeten Zuordnung wird der u-Texturindex wie im folgenden Diagramm für eine Textur mit einer Breite von 4 Texeln dargestellt.

![Diagramm der Texturkoordinaten 0,0 und 1,0 an der Grenze zwischen Texel](images/ptsmpprb.png)

Beachten Sie, dass sich die Texturkoordinaten 0,0 und 1,0 für diese Abbildung genau an der Grenze zwischen texels befinden. Mit der Methode, mit der Direct3D Werte zuordnt, liegen die Texturkoordinaten zwischen \[ - 0,5, 4 und 0,5, \] wobei 4 die Breite der Textur ist. In diesem Fall ist das texel als Stichprobe das 0-Texel für einen Texturindex von 1,0. Wenn die Texturkoordinate jedoch nur etwas kleiner als 1,0 wäre, wäre das n-Texel anstelle des 0-Texels das n-Texel.

Dies hat zur Folge, dass das Vergrößern einer kleinen Textur mithilfe von Texturkoordinaten von genau 0,0 und 1,0 mit der Filterung des nächstgelegenen Punkts auf einem am Bildschirmbereich ausgerichteten Dreieck zu Pixeln führt, für die die Texturkarte an der Grenze zwischen Texel entnommen wird. Alle Ungenauigkeiten bei der Berechnung von Texturkoordinaten, wenn auch klein, ergeben Artefakte entlang der Bereiche im gerenderten Bild, die den Texelrändern der Texturkarte entsprechen.

Diese Zuordnung von Gleitkommatexturkoordinaten zu ganzzahligen Texel mit perfekter Genauigkeit ist schwierig, rechenintensiv und im Allgemeinen nicht erforderlich. Die meisten Hardwareimplementierungen verwenden einen iterativen Ansatz zum Berechnen von Texturkoordinaten an jeder Pixelposition innerhalb eines Dreiecks. Iterative Ansätze neigen dazu, diese Ungenauigkeiten auszublenden, da die Fehler während der Iteration gleichmäßig angesammelt werden.

Der Direct3D-Referenzrasterizer verwendet einen direkten Auswertungsansatz zum Berechnen von Texturindizes an jeder Pixelposition. Die direkte Auswertung unterscheidet sich vom iterativen Ansatz darin, dass jede Ungenauigkeit im Vorgang eine eher zufällige Fehlerverteilung aufweist. Dies führt dazu, dass die Samplingfehler, die an den Grenzen auftreten, deutlicher erkennbar sind, da der Verweisrasterizer diesen Vorgang nicht mit perfekter Genauigkeit ausführt.

Der beste Ansatz besteht darin, die Nächstgelegene Punktfilterung nur bei Bedarf zu verwenden. Wenn Sie sie verwenden müssen, wird empfohlen, Texturkoordinaten leicht von den Begrenzungspositionen zu verdrücken, um Artefakte zu vermeiden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturfilterung](texture-filtering.md)
</dt> </dl>

 

 
