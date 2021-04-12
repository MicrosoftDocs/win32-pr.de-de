---
description: Die StretchBlt-Funktion skaliert eine Bitmap, indem eine Bitblock Übertragung von einem Rechteck in einem Quell Gerätekontext in ein Rechteck in einem Zielgeräte Kontext durchgeführt wird.
ms.assetid: 34390ff9-8d5f-497e-87aa-a1019d01bba6
title: Bitmapskalierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4011b06e6a7269be29e1834e90928c4f531b1023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130848"
---
# <a name="bitmap-scaling"></a>Bitmapskalierung

Die [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) -Funktion skaliert eine Bitmap, indem eine Bitblock Übertragung von einem Rechteck in einem Quell Gerätekontext in ein Rechteck in einem Zielgeräte Kontext durchgeführt wird. Anders als bei der [**BitBLT**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) -Funktion, mit der die Quell Rechteck Dimensionen im Ziel Rechteck dupliziert werden, kann eine Anwendung mithilfe von **StretchBlt** die Dimensionen der Quell-und Ziel Rechtecke angeben. Wenn die Ziel Bitmap kleiner ist als die Quell Bitmap, kombiniert das System Zeilen oder Spalten von Farbdaten (oder beides) vor dem Rendern des entsprechenden Bilds auf dem Anzeigegerät. Das System kombiniert die Farbdaten gemäß dem angegebenen streckungs Modus, der von der Anwendung durch Aufrufen der [**setstretchbltmode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) -Funktion definiert wird. Wenn die Ziel Bitmap größer als die Quell Bitmap ist, skaliert oder vergrößert das System jedes Pixel im resultierenden Bild entsprechend.

 

 



