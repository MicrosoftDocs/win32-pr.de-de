---
title: Die Desktopfenster-Manager
description: Die Desktopfenster-Manager
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99585a75bf2b25b086f09a17a0d8d93391b1f94f5018c5d4f83f90937fde620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896880"
---
# <a name="the-desktop-window-manager"></a>Die Desktopfenster-Manager

Vor Windows Vista würde ein Windows direkt auf den Bildschirm zeichnen. Anders ausgedrückt: Das Programm schreibt direkt in den Speicherpuffer, der von der Grafikkarte angezeigt wird. Dieser Ansatz kann zu visuellen Artefakten führen, wenn sich ein Fenster nicht ordnungsgemäß neu anpaint. Wenn der Benutzer z. B. ein Fenster über ein anderes Fenster zieht und sich das fenster darunter nicht schnell genug neu anpaint, kann das fenster oben einen Pfad verlassen:

![Ein Screenshot, der neu gemalte Artefakte zeigt.](images/graphics04.png)

Der Pfad wird dadurch verursacht, dass beide Fenster in den gleichen Speicherbereich zeichnen. Wenn das oberste Fenster gezogen wird, muss das Fenster darunter neu gepaint werden. Wenn die Neupaintierung zu langsam ist, werden die in der vorherigen Abbildung gezeigten Artefakte verursacht.

Windows Vista hat die Art und Weise, wie Fenster gezeichnet werden, grundlegend geändert, indem das Desktopfenster-Manager (DWM) eingeführt wurde. Wenn dwm aktiviert ist, wird ein Fenster nicht mehr direkt in den Anzeigepuffer ge zeichnet. Stattdessen zeichnet jedes Fenster zu einem Offscreen-Speicherpuffer, der auch als *Offscreenoberfläche bezeichnet wird.* Das DWM kombiniert diese Oberflächen dann mit dem Bildschirm.

![Ein Diagramm, das zeigt, wie dwm den Desktop zusammengesetzt.](images/graphics05.png)

Das DWM bietet gegenüber der alten Grafikarchitektur mehrere Vorteile.

-   Weniger neu gepainte Nachrichten. Wenn ein Fenster von einem anderen Fenster blockiert wird, muss das blockierte Fenster nicht selbst neu gepaint werden.
-   Reduzierte Artefakte. Zuvor konnten durch Ziehen eines Fensters visuelle Artefakte erstellt werden, wie beschrieben.
-   Visuelle Effekte. Da das DWM für das Zusammenordnen des Bildschirms zuständig ist, kann es durchscheinende und unscharfe Bereiche des Fensters rendern.
-   Automatische Skalierung für hohe DPI-Leistung. Obwohl die Skalierung nicht die ideale Methode zum Verarbeiten hoher DPI-Daten ist, ist sie ein sinnvoller Fallback für ältere Anwendungen, die nicht für Einstellungen mit hohem DPI-Ziel entwickelt wurden. (Wir kehren später zu diesem Thema zurück, im Abschnitt [DPI und Device-Independent Pixel](dpi-and-device-independent-pixels.md).)
-   Alternative Ansichten. Das DWM kann die Offscreenoberflächen auf verschiedene interessante Weise verwenden. Beispielsweise ist das DWM die Technologie hinter Windows Flip 3D, Miniaturansichten und animierten Übergängen.

Beachten Sie jedoch, dass dwm nicht garantiert aktiviert ist. Die Grafikkarte unterstützt möglicherweise die DWM-Systemanforderungen nicht, und Benutzer können das DWM über die **Systemeigenschaften-Systemsteuerung** deaktivieren. Das bedeutet, dass Ihr Programm nicht auf das Neupaintingverhalten des DWM angewiesen sein sollte. Testen Sie das Programm mit deaktivierter DWM, um sicherzustellen, dass es ordnungsgemäß neu gepaint wird.

## <a name="next"></a>Nächste

[Beibehaltener Modus im Vergleich zum unmittelbaren Modus](retained-mode-versus-immediate-mode.md)

 

 




