---
description: Ein Akkord ist ein Bereich, der durch die Schnittmenge einer Ellipse und eines als "Secant" bezeichneten Linien Segments begrenzt ist. Die folgende Abbildung zeigt einen mit der Funktion "Chord" gezeichneten Akkord.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: Informationen zu Akkorden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d6310c47a503766e61b9c7936816a5891da89a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527704"
---
# <a name="about-chords"></a>Informationen zu Akkorden

Ein *Akkord* ist ein Bereich, der durch die Schnittmenge einer Ellipse und eines als " *Sekans*" bezeichneten Linien Segments begrenzt ist. Die folgende Abbildung zeigt einen mit der Funktion " [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord) " gezeichneten Akkord.

![Abbildung einer Elipse, die zwei radiale, eine Secant und einen Akkord anzeigt](images/csfsh-02.png)

Beim Aufrufen von " [**Chord**](/windows/win32/api/wingdi/nf-wingdi-chord)" stellt eine Anwendung die Koordinaten der oberen linken und der unteren rechten Ecke des umgebenden Rechtecks der Ellipse sowie die Koordinaten von zwei Punkten bereit, die zwei radiale definieren. Ein radiales ist eine Linie, die aus der Mitte des umgebenden Rechtecks einer Ellipse bis zu einem Punkt auf der Ellipse gezeichnet wird.

Wenn das System den gekrümmten Teil des Akkords zeichnet, erfolgt dies mithilfe der aktuellen Bogen Richtung für den angegebenen Gerätekontext. Die Standard-Bogen Richtung ist gegen den Uhrzeigersinn. Sie können festlegen, dass die Anwendung die Bogen Richtung zurücksetzen soll, indem Sie die [**setarcdirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) -Funktion aufrufen.

 

 
