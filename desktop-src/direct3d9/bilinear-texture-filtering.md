---
description: Texturen werden in der unteren rechten Ecke immer linear von (0,0, 0,0) an der oberen linken Ecke bis (1,0, 1,0) adressiert, wie in der folgenden Abbildung dargestellt.
ms.assetid: 16fb04b9-4476-4dbe-a24f-51c0813a7917
title: Bilineare Textur Filterung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51213e5187c775963de2fa740847d55084c5be2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393186"
---
# <a name="bilinear-texture-filtering-direct3d-9"></a>Bilineare Textur Filterung (Direct3D 9)

Texturen werden in der unteren rechten Ecke immer linear von (0,0, 0,0) an der oberen linken Ecke bis (1,0, 1,0) adressiert, wie in der folgenden Abbildung dargestellt.

![Abbildung der 4X4-Textur mit voll Tonfarben](images/bilinear-fig7a.png)

Texturen werden in der Regel so dargestellt, als würden Sie aus voll Tonfarben bestehen, aber es ist eigentlich korrekter, dass Sie sich auf die gleiche Weise wie die Raster Darstellung vorstellen können: jede Textzelle wird in der Mitte einer Raster Zelle definiert, wie in der folgenden Abbildung dargestellt.

![Abbildung der 4X4-Textur mit texeln, die in der Mitte der Rasterzellen definiert sind](images/bilinear-fig7b.png)

Wenn Sie den Textur Sampler bei UV-Koordinaten (0,375, 0,375) für die Farbe der Textur Anfragen, erhalten Sie rot (255, 0,0). Das ist ideal, da der exakte Mittelpunkt der roten Textzelle sich bei UV (0,375, 0,375) befindet. Was geschieht, wenn Sie den Sampler um die Farbe der Textur bei UV (0,25, 0,25) bitten? Das ist nicht ganz einfach, da der Punkt bei UV (0,25, 0,25) in der exakten Ecke von vier texeln liegt.

Das einfachste Schema besteht darin, dass der Sampler einfach die Farbe des nächsten Texten zurückgibt. Dies wird als Punkt Filterung bezeichnet (siehe [Sampling des nächsten Punkts (Direct3D 9)](nearest-point-sampling.md)) und ist in der Regel aufgrund von grainen-oder grobe-Ergebnissen nicht erwünscht. Point-Sampling unsere Textur bei UV (0,25, 0,25) zeigt ein weiteres Problem mit dem nächstgelegenen filtern: Es gibt vier texeln, die vom Stichproben Punkt entfernt werden, sodass es keine einzelnen nächsten texellen gibt. Eines dieser vier texeln wird als die zurückgegebene Farbe ausgewählt. die Auswahl hängt jedoch davon ab, wie die Koordinate gerundet wird. Dies kann zu Tränen enden Artefakten führen (Weitere Informationen finden Sie im Nearest-Point Sampling-Artikel im SDK).

Ein etwas genaueres und allgemeineres Filter Schema besteht darin, den gewichteten Durchschnitt der 4 texeln zu berechnen, die dem Stichproben Punkt am nächsten sind. Dies wird als bilineare Filterung bezeichnet, und die zusätzlichen berechnungskosten sind normalerweise unerheblich, da diese Routine in moderner Grafikhardware implementiert ist. Im folgenden finden Sie die Farben, die wir mit der bilinearen Filterung für einige verschiedene Beispiel Punkte erhalten:


```
UV: (0.5, 0.5)
```



Dieser Punkt befindet sich an der exakten Grenze zwischen rot, grün, blau und weißen texeln. Die Farbe, die der Sampler zurückgibt, ist grau:


```
  0.25 * (255, 0, 0)
  0.25 * (0, 255, 0) 
  0.25 * (0, 0, 255) 
## + 0.25 * (255, 255, 255) 
------------------------
= (128, 128, 128)
```




```
UV: (0.5, 0.375)
```



Dieser Punkt befindet sich im Mittelpunkt des Rahmens zwischen roten und grünen texeln. Die Farbe, die der Sampler zurückgibt, ist gelb grau (Beachten Sie, dass die Beiträge der blauen und weißen texeln auf 0 skaliert werden):


```
  0.5 * (255, 0, 0)
  0.5 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (128, 128, 0)
```




```
UV: (0.375, 0.375)
```



Dies ist die Adresse des roten texms, bei dem es sich um die zurückgegebene Farbe handelt (alle anderen texeln in der Filter Berechnung werden auf 0 gewichtet):


```
  1.0 * (255, 0, 0)
  0.0 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (255, 0, 0)
```



Vergleichen Sie diese Berechnungen mit der folgenden Abbildung, die zeigt, was geschieht, wenn die Berechnung der bilinearen Filterung an jeder Textur Adresse in der 4 x 4-Textur ausgeführt wird.

![Abbildung der 4X4-Textur mit bilinearer Filterung, die bei jeder Textur Adresse ausgeführt wird](images/bilinear-fig7c.jpg)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Filterung](texture-filtering.md)
</dt> </dl>

 

 



