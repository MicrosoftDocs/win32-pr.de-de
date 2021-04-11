---
title: Hohe DPI-Werte
description: .
ms.assetid: 476fe65c-2acd-4a7a-8a76-72d9f010b772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adad7c986c7083ab2327f0c8de0bd2cace5ef20a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039394"
---
# <a name="high-dpi"></a>Hohe DPI-Werte

Wenn die Anzeigetechnologien fortgesetzt werden, haben die Hersteller die Anzahl der von ihren anzeigen unterstützten Pixel übersteigt. Obwohl Text, Bilder und Benutzeroberflächen Elemente viel schärfer und besser lesbar für hochauflösende anzeigen aussehen, muss das Betriebssystem zur Unterstützung der visuellen Darstellung zentral hochskaliert werden. Andernfalls ist alles nur kleiner.

Windows 7 unterstützt High *dpi* -Anzeige. Marktdaten deuten darauf hin, dass die bereit Stellungen hoher *dpi* -Bildschirme (120-144 Punkte pro Zoll (dpi)) im Windows 7-Zeitrahmen zunehmen. Wenn Sie Native Auflösungen auf diesen Bildschirmen ausführen, werden viele Anwendungen sehr klein angezeigt, es sei denn, Sie verwenden *High dpi*. Einige Anwendungen (z. b. Windows Internet Explorer) verfügen über Funktionen zur Schriftart Skalierung, die es Benutzern ermöglichen, ein-und auszuzoomen, aber viele Anwendungen nicht. Das *hohe dpi* -Feature in Windows 7:

-   Stellt sicher, dass die Windows-und Anwendungsumgebung auf Standard Hardware optimal ist (die *dpi* -Einstellungen sind entsprechend den Funktionen der Hardware optimiert).
-   Ermöglicht das Aussehen der Windows-Shell und anderer Windows-basierter Anwendungen mit unterschiedlichen *dpi* -Einstellungen.
-   Respektiert die Standard- *dpi* -Einstellungen basierend auf Hardware Spezifikationen und-Funktionen.
-   Ermöglicht es Benutzern, die *dpi* -Einstellungen ohne Neustart zu personalisieren.
-   Stellt sicher, dass der Bildschirm immer auf native Auflösung festgelegt ist.

Das Windows-Feature für die *dpi* -Skalierung skaliert Schriftarten und Benutzeroberflächen Elemente (z. b. Schaltflächen, Symbole und Eingabefelder) mit einem berechneten Prozentsatz, wie in der *dpi* -Einstellung angegeben. Dies unterscheidet sich von der Skalierung, die auftritt, wenn die Bildschirmauflösung verringert wird. Im Fall der *dpi* -Skalierung stellt Windows Schriftarten und Benutzeroberflächen Elemente bereit, die mit mehr Pixeln gezeichnet werden. Dies führt zu einer größeren, stärkeren Genauigkeit und einer stärkeren Windows-Darstellung. Windows-Anwendungen von Drittanbietern können *hohe dpi* -Einstellungen nutzen und die Benutzeroberfläche entsprechend anpassen, indem Sie eine *hohe dpi* -Unterstützung deklarieren. Anwendungsentwickler sollten nicht mehr davon ausgehen, dass 96 dpi die ideale Lösung für alle Anwendungen ist.

Weitere Informationen zu *hohen dpi* -Werten und zum Schreiben von Anwendungen, die *hoch dpi* -fähig sind, finden Sie unter [High dpi](../hidpi/high-dpi-desktop-application-development-on-windows.md).

 

 