---
title: Der Desktopfenster-Manager
description: .
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73167b762a9952eb508f09e70f3d4183b3b7a018
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309936"
---
# <a name="the-desktop-window-manager"></a>Der Desktopfenster-Manager

Vor Windows Vista würde ein Windows-Programm direkt auf den Bildschirm gezeichnet werden. Das Programm würde also direkt in den Speicherpuffer schreiben, der von der Grafikkarte angezeigt wird. Diese Vorgehensweise kann visuelle Artefakte verursachen, wenn sich ein Fenster nicht selbst ordnungsgemäß neu zeichnet. Wenn der Benutzer z. b. ein Fenster über ein anderes Fenster zieht und sich das Fenster unterhalb nicht schnell genug neu zeichnet, kann das oberste Fenster eine Spur hinterlassen:

![ein Screenshot mit repaint-Artefakten.](images/graphics04.png)

Der Pfad ist darauf zurückzuführen, dass beide Fenster in denselben Bereich des Arbeitsspeichers zeichnen. Wenn das oberste Fenster gezogen wird, muss das Fenster unterhalb des Fensters neu gezeichnet werden. Wenn das erneute zeichnen zu langsam ist, werden die in der vorherigen Abbildung gezeigten Artefakte verursacht.

Windows Vista hat grundlegend geändert, wie Windows gezeichnet wird, indem die Desktopfenster-Manager (DWM) eingeführt wird. Wenn die DWM aktiviert ist, wird ein Fenster nicht mehr direkt in den Anzeige Puffer gezeichnet. Stattdessen zeichnet jedes Fenster einen Offscreen-Speicherpuffer, auch als *Offscreen-Oberfläche* bezeichnet. Anschließend werden diese Oberflächen vom DWM auf den Bildschirm integriert.

![ein Diagramm, das zeigt, wie die DWM den Desktop integriert.](images/graphics05.png)

Die DWM bietet mehrere Vorteile gegenüber der alten Grafik Architektur.

-   Weniger Repaint-Nachrichten. Wenn ein Fenster von einem anderen Fenster behindert wird, muss sich das versperrte Fenster nicht selbst neu zeichnen.
-   Reduzierte Artefakte. Zuvor konnte das Ziehen eines Fensters wie beschrieben visuelle Artefakte erstellen.
-   Visuelle Effekte. Da die DWM für die Zusammensetzung des Bildschirms zuständig ist, kann Sie überflüssig und unscharfe Bereiche des Fensters darstellen.
-   Automatische Skalierung für hohe dpi-Informationen. Obwohl die Skalierung nicht die ideale Methode zur Verarbeitung von hohem dpi-Wert ist, ist Sie ein funktionierender Fall Back für ältere Anwendungen, die nicht für hohe DPI-Einstellungen entwickelt wurden. (Dieses Thema wird später im Abschnitt [dpi und Device-Independent Pixel](dpi-and-device-independent-pixels.md)zurückgegeben.)
-   Alternative Ansichten. Die DWM kann die Offscreen-Oberflächen auf verschiedene interessante Arten verwenden. Die DWM ist beispielsweise die Technologie hinter Windows Flip 3D, Miniaturansichten und animierten Übergänge.

Beachten Sie jedoch, dass die DWM nicht garantiert aktiviert ist. Die Grafikkarte unterstützt die Systemanforderungen des DWM-Systems möglicherweise nicht, und Benutzer können die DWM über die **System** Steuerung deaktivieren. Dies bedeutet, dass sich das Programm nicht auf das neuzeichnungs Verhalten der DWM verlassen sollte. Testen Sie das Programm mit deaktiviertem DWM, um sicherzustellen, dass es ordnungsgemäß neu zeichnet.

## <a name="next"></a>Nächste

[Modus für beibehaltene Modus und unmittelbarer](retained-mode-versus-immediate-mode.md)

 

 




