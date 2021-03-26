---
description: Das Koordinatensystem für ein Fenster basiert auf dem Koordinatensystem des Anzeige Geräts.
ms.assetid: 8590fc59-d7ad-4149-9a77-242037a11188
title: Fenster Koordinaten System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c69c5faa7359700af8a3bb04413fa9b25648b0cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755832"
---
# <a name="window-coordinate-system"></a>Fenster Koordinaten System

Das Koordinatensystem für ein Fenster basiert auf dem Koordinatensystem des Anzeige Geräts. Die grundlegende Maßeinheit ist die Geräteeinheit (in der Regel das Pixel). Die Punkte auf dem Bildschirm werden durch x-und y-Koordinatenpaare beschrieben. Die x-Koordinaten werden auf der rechten Seite vergrößert. y-Koordinaten werden von oben nach unten vergrößert. Der Ursprung (0, 0) für das System hängt vom Typ der verwendeten Koordinaten ab.

Das System und die Anwendungen geben die Position eines Fensters auf dem Bildschirm in *Bildschirm Koordinaten* an. Bei Bildschirm Koordinaten wird der Ursprung in der oberen linken Ecke des Bildschirms angezeigt. Die vollständige Position eines Fensters wird häufig durch eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur beschrieben, die die Bildschirm Koordinaten zweier Punkte enthält, die die oberen linken und unteren rechten Ecke des Fensters definieren.

Das System und die Anwendungen geben die Position der Punkte in einem Fenster mithilfe von *Client Koordinaten* an. Der Ursprung ist in diesem Fall die linke obere Ecke des Fensters oder des Client Bereichs. Mithilfe von Client Koordinaten wird sichergestellt, dass eine Anwendung während des Zeichnens im Fenster konsistente Koordinaten Werte verwenden kann, unabhängig von der Position des Fensters auf dem Bildschirm.

Die Abmessungen des Client Bereichs werden auch durch eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur beschrieben, die Client Koordinaten für den Bereich enthält. In allen Fällen ist die obere linke Koordinate des Rechtecks im Fenster-oder Client Bereich enthalten, während die Koordinate der unteren rechten Seite ausgeschlossen wird. Grafik Vorgänge in einem Fenster-oder Client Bereich werden vom rechten und unteren Rand des einschließenden Rechtecks ausgeschlossen.

Gelegentlich ist es erforderlich, dass Anwendungen in einem Fenster Koordinaten in einem anderen Fenster zuordnen. Eine Anwendung kann Koordinaten mithilfe der [**mapwindowpoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints) -Funktion zuordnen. Handelt es sich bei einem der Fenster um das Desktop Fenster, konvertiert die Funktion Bildschirm Koordinaten effektiv in Client Koordinaten und umgekehrt. das Desktop Fenster wird immer in Bildschirm Koordinaten angegeben.

 

 
