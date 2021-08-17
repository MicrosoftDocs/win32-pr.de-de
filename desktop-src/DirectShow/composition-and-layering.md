---
description: Komposition und Ebenen
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Komposition und Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b173ed0727869d3630a2241d7237cf74fb5143a907a95fcc53901a7b85f285c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954229"
---
# <a name="composition-and-layering"></a>Komposition und Ebenen

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

In einer Sammlung von Spuren hat die erste Spur die niedrigste Priorität (Priorität 0), und jede nachfolgende Spur hat eine Priorität um eine Ebene höher. Auf jeder Prioritätsebene blenden die Quellclips in diesem Track die Quellclips in den darunter stehenden Spuren aus, es sei denn, diese Ebene enthält auch einen Übergang. Daher können Sie sich vorstellen, dass DES beim Rendern mehrere Durchläufe macht.

Zuerst wird track 0 gerendert. Es gibt nichts "unter" Track 0, sodass leere Bereiche als ein schwarzes Vollbild gerendert werden. Übergänge in dieser Schicht erfolgen zwischen dem schwarzen Bild und Track 0 oder umgekehrt. DES legt Track 1 über Track 0 ab und generiert alle Übergänge zwischen den beiden Spuren. Das Ergebnis ist die Zusammengesetzte der beiden Spuren. Als Nächstes platziert sie Track 2 auf dieser Zusammengesetzten. Übergänge auf dieser Ebene erfolgen zwischen dem zusammengesetzten und dem Track 2. Der Prozess wird fortgesetzt, bis die letzte Spur (mit der höchsten Priorität) heruntergefahren ist.

Wenn mehrere Spuren zusammengesetzt werden, verhalten sie sich wie eine einzelne Spur (als virtuelle Spur bezeichnet). Das Kompositionsobjekt kapselt dieses Verhalten und ermöglicht komplexe Übergänge. Beispielsweise kann ein Videoclip auf einen zweiten Clip zurückgelöscht werden, während der zusammengesetzte Clip (beide Clips plus das Zurücksetzungsvideo) zu einem dritten Clip verblasst.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit DirectShow-Bearbeitungsdiensten](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



