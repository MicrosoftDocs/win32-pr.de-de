---
description: Eine Ellipse ist ein Bereich, der durch die Schnittmenge einer Ellipse und eines Liniensegments, das als Secant bezeichnet wird, gebunden ist. Die folgende Abbildung zeigt eine mithilfe der Chord-Funktion gezeichnete Akkorde.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: Informationen zu Chords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3bad0d17d34386ada7c7c3b46bb1bcc4db5f9a2ce572ce78c33f8f4b6af909
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400530"
---
# <a name="about-chords"></a>Informationen zu Chords

Eine *Ellipse* ist ein Bereich, der durch die Schnittmenge einer Ellipse und eines Liniensegments, das als secant bezeichnet *wird, umgebunden ist.* Die folgende Abbildung zeigt eine mithilfe der [**Chord-Funktion gezeichnete Akkorde.**](/windows/desktop/api/Wingdi/nf-wingdi-chord)

![Abbildung eines Auslassungsdiagramms mit zwei Radialen, einem Sekanten und einer Ader](images/csfsh-02.png)

Beim [**Aufrufen von Chord**](/windows/win32/api/wingdi/nf-wingdi-chord)stellt eine Anwendung die Koordinaten der oberen linken und unteren rechten Ecke des umgrenzenden Rechtecks der Ellipse sowie die Koordinaten von zwei Punkten zur Definition von zwei radialen Punkten zur Auswahl. Ein radiales ist eine Linie, die von der Mitte des umgebundenen Rechtecks einer Ellipse bis zu einem Punkt auf der Ellipse gezeichnet wird.

Wenn das System den gekrümmten Teil des Chord zeichnet, verwendet es die aktuelle Bogenrichtung für den angegebenen Gerätekontext. Die Standard arc-Richtung ist gegen den Uhrzeigersinn. Sie können ihre Anwendung die Richtung des Bogens zurücksetzen lassen, indem Sie die [**SetArcDirection-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) aufrufen.

 

 
