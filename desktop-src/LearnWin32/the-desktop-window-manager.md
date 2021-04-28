---
title: Die Desktopfenster-Manager
description: Die Desktopfenster-Manager
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fca8550134ba0c1cdafe0bd5c349061ef900a9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103898"
---
# <a name="the-desktop-window-manager"></a>Die Desktopfenster-Manager

Vor Windows Vista zeichnete ein Windows-Programm direkt auf den Bildschirm. Anders ausgedrückt: Das Programm würde direkt in den Speicherpuffer schreiben, der von der Grafikkarte angezeigt wird. Dieser Ansatz kann visuelle Artefakte verursachen, wenn sich ein Fenster nicht ordnungsgemäß neu malt. Wenn der Benutzer beispielsweise ein Fenster über ein anderes Fenster zieht und sich das darunter liegende Fenster nicht schnell genug neu malt, kann das oberste Fenster einen Trail verlassen:

![Screenshot: Neupaintieren von Artefakten](images/graphics04.png)

Der Trail wird verursacht, weil beide Fenster in den gleichen Speicherbereich zeichnen. Wenn das oberste Fenster gezogen wird, muss das Fenster darunter neu strichen werden. Wenn das erneute Anstrichen zu langsam ist, führt dies zu den Artefakten, die in der vorherigen Abbildung gezeigt werden.

Windows Vista hat durch die Einführung des Desktopfenster-Manager (DWM) die Art und Weise, wie Fenster gezeichnet werden, grundlegend geändert. Wenn dwm aktiviert ist, wird ein Fenster nicht mehr direkt in den Anzeigepuffer geschaltet. Stattdessen zeichnet jedes Fenster zu einem Offscreen-Speicherpuffer, der auch als *Offscreenoberfläche* bezeichnet wird. Der DWM kombiniert diese Oberflächen dann mit dem Bildschirm.

![Ein Diagramm, das zeigt, wie dwm den Desktop zusammengesetzt.](images/graphics05.png)

Dwm bietet gegenüber der alten Grafikarchitektur mehrere Vorteile.

-   Weniger neu malte Nachrichten. Wenn ein Fenster durch ein anderes Fenster blockiert wird, muss sich das verdeckte Fenster nicht selbst neu malen.
-   Reduzierte Artefakte. Zuvor konnten durch Ziehen eines Fensters visuelle Artefakte erstellt werden, wie beschrieben.
-   Visuelle Effekte. Da der DWM für das Zusammenstellen des Bildschirms zuständig ist, kann er durchscheinende und unscharfe Bereiche des Fensters rendern.
-   Automatische Skalierung für hohe DPI-Daten. Obwohl die Skalierung nicht die ideale Methode zum Verarbeiten von hohen DPI-Daten ist, ist sie ein sinnvoller Fallback für ältere Anwendungen, die nicht für hohe DPI-Einstellungen konzipiert wurden. (Wir kehren später im Abschnitt [DPI und Device-Independent Pixels](dpi-and-device-independent-pixels.md)zu diesem Thema zurück.)
-   Alternative Ansichten. Der DWM kann die Offscreenoberflächen auf verschiedene interessante Weise verwenden. Der DWM ist beispielsweise die Technologie hinter Windows-Flip-3D, Miniaturansichten und animierten Übergängen.

Beachten Sie jedoch, dass die Aktivierung des DWM nicht garantiert ist. Die Grafikkarte unterstützt möglicherweise nicht die DWM-Systemanforderungen, und Benutzer können den DWM über die **Systemeigenschaften-Systemsteuerung** deaktivieren. Das bedeutet, dass sich Ihr Programm nicht auf das Neumalverhalten des DWM verlassen sollte. Testen Sie ihr Programm mit deaktivierter DWM, um sicherzustellen, dass es ordnungsgemäß neu malt.

## <a name="next"></a>Nächste

[Beibehaltener Modus im Vergleich zum unmittelbaren Modus](retained-mode-versus-immediate-mode.md)

 

 




