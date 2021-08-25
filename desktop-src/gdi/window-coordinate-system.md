---
description: Das Koordinatensystem für ein Fenster basiert auf dem Koordinatensystem des Anzeigegeräts.
ms.assetid: 8590fc59-d7ad-4149-9a77-242037a11188
title: Fensterkoordinatensystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c5492aaa02e1b2b2ace7e0cb02a65caa1faad320eca11414707145066308e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717870"
---
# <a name="window-coordinate-system"></a>Fensterkoordinatensystem

Das Koordinatensystem für ein Fenster basiert auf dem Koordinatensystem des Anzeigegeräts. Die grundlegende Maßeinheit ist die Geräteeinheit (in der Regel das Pixel). Punkte auf dem Bildschirm werden durch X- und y-Koordinatenpaare beschrieben. Die x-Koordinaten werden nach rechts erhöht. y-Koordinaten erhöhen sich von oben nach unten. Der Ursprung (0,0) für das System hängt vom Typ der verwendeten Koordinaten ab.

Das System und die Anwendungen geben die Position eines Fensters auf dem Bildschirm in *Bildschirmkoordinaten an.* Bei Bildschirmkoordinaten ist der Ursprung die linke obere Ecke des Bildschirms. Die vollständige Position eines Fensters wird häufig durch eine [**RECT-Struktur**](/previous-versions//dd162897(v=vs.85)) beschrieben, die die Bildschirmkoordinaten von zwei Punkten enthält, die die oberen linken und unteren rechten Ecken des Fensters definieren.

Das System und die Anwendungen geben die Position von Punkten in einem Fenster mithilfe der *Clientkoordinaten an.* Der Ursprung ist in diesem Fall die linke obere Ecke des Fensters oder Clientbereichs. Clientkoordinaten stellen sicher, dass eine Anwendung beim Zeichnen im Fenster konsistente Koordinatenwerte verwenden kann, unabhängig von der Position des Fensters auf dem Bildschirm.

Die Dimensionen des Clientbereichs werden auch durch eine [**RECT-Struktur**](/previous-versions//dd162897(v=vs.85)) beschrieben, die Clientkoordinaten für den Bereich enthält. In allen Fällen ist die obere linke Koordinate des Rechtecks im Fenster- oder Clientbereich enthalten, während die untere rechte Koordinate ausgeschlossen wird. Grafikvorgänge in einem Fenster oder Clientbereich werden vom rechten und unteren Rand des umschließenden Rechtecks ausgeschlossen.

Gelegentlich müssen Anwendungen Koordinaten in einem Fenster denen eines anderen Fensters zuordnen. Eine Anwendung kann Koordinaten mithilfe der [**MapWindowPoints-Funktion**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints) zuordnen. Wenn eines der Fenster das Desktopfenster ist, konvertiert die Funktion Bildschirmkoordinaten effektiv in Clientkoordinaten und umgekehrt. das Desktopfenster wird immer in Bildschirmkoordinaten angegeben.

 

 
