---
description: Die StretchBlt-Funktion skaliert eine Bitmap, indem sie eine Bitblockübertragung von einem Rechteck in einem Quellgerätekontext in ein Rechteck in einem Zielgerätekontext durchführt.
ms.assetid: 34390ff9-8d5f-497e-87aa-a1019d01bba6
title: Bitmapskalierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14975f884906fb95bf07fbf3ab5277b89c5cbfd2612864202eb64eedc5df646b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117699897"
---
# <a name="bitmap-scaling"></a>Bitmapskalierung

Die [**StretchBlt-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) skaliert eine Bitmap, indem sie eine Bitblockübertragung von einem Rechteck in einem Quellgerätekontext in ein Rechteck in einem Zielgerätekontext durchführt. Im Gegensatz zur [**BitBlt-Funktion,**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) die die Quellrechteckdimensionen im Zielrechteck dupliziert, ermöglicht **StretchBlt** einer Anwendung jedoch, die Dimensionen der Quell- und Zielrechtecke anzugeben. Wenn die Zielbitmap kleiner als die Quellbitmap ist, kombiniert das System Zeilen oder Spalten mit Farbdaten (oder beidem) in der Bitmap, bevor das entsprechende Bild auf dem Anzeigegerät gerendert wird. Das System kombiniert die Farbdaten gemäß dem angegebenen Stretchmodus, den die Anwendung durch Aufrufen der [**SetStretchBltMode-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) definiert. Wenn die Zielbitmap größer als die Quellbitmap ist, skaliert oder vergrößert das System jedes Pixel im resultierenden Bild entsprechend.

 

 



