---
title: Hohe DPI-Werte
description: Hohe DPI-Werte
ms.assetid: 476fe65c-2acd-4a7a-8a76-72d9f010b772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7c70e44c497f116348e7b42b260f056d593524
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114698"
---
# <a name="high-dpi"></a>Hohe DPI-Werte

Mit zunehmender Entwicklung der Anzeigetechnologien haben Hersteller die Anzahl von Pixeln erhöht, die von ihren Displays unterstützt werden. Text, Bilder und Benutzeroberflächenelemente sehen zwar viel schärfer und besser lesbar auf hochauflösenden Displays aus, das Betriebssystem muss jedoch hochskaliert werden, um die visuelle Benutzeroberfläche zu unterstützen. andernfalls sieht alles einfach kleiner aus.

Windows 7 unterstützt hohe *DPI-Anzeigen.* Marktdaten deuten darauf hin, dass die Bereitstellungen von Bildschirmen mit hohem *DPI-Wert* (120 bis 144 Punkte pro Zoll (dpi)) im Windows 7-Zeitrahmen zunehmen werden. Wenn sie native Auflösungen auf diesen Bildschirmen ausführen, werden viele Anwendungen sehr klein angezeigt, es sei denn, sie verwenden *hohe DPI-Auflösungen.* Einige Anwendungen (z. B. Windows Internet Explorer) verfügen über Features für die Schriftskalierung, die benutzern das Vergrößern und Verkleinern ermöglichen, aber viele Anwendungen nicht. High DPI feature in Windows 7 (Feature für hohe *DPI-Leistung* in Windows 7):

-   Stellt sicher, dass Windows- und Anwendungserfahrungen auf Standardhardware optimal sind *(DPI-Einstellungen* sind so optimiert, dass sie den Funktionen der Hardware entsprechen).
-   Ermöglicht es der Windows-Shell und anderen Windows-basierten Anwendungen, mit unterschiedlichen *DPI-Einstellungen* gut zu aussehen.
-   Beachtet *DPI-Standardeinstellungen* basierend auf Hardwarespezifikationen und -funktionen.
-   Ermöglicht Benutzern das Personalisieren von *DPI-Einstellungen* ohne Neustart.
-   Stellt sicher, dass der Bildschirm immer auf systemeigene Auflösung festgelegt ist.

Das *Windows-DPI-Skalierungsfeature* skaliert Schriftarten und Benutzeroberflächenelemente (z. B. Schaltflächen, Symbole und Eingabefelder) um einen berechneten Prozentsatz, wie in der *DPI-Einstellung* angegeben. Dies ist anders als die Skalierung, die auftritt, wenn die Anzeigeauflösung gesenkt wird. Im Fall der *DPI-Skalierung* stellt Windows Schriftarten und Benutzeroberflächenelemente bereit, die mit mehr Pixeln gezeichnet werden, was zu einer größeren, genaueren und schärferen Windows-Erfahrung führt. Windows-Anwendungen von Drittanbietern können High *DPI-Einstellungen* nutzen und die Benutzeroberfläche entsprechend anpassen, indem sie sich *selbst als "High DPI aware" deklarieren.* Anwendungsentwickler sollten nicht mehr davon ausgehen, dass 96 dpi die ideale Auflösung für alle Anwendungen ist.

Weitere Informationen zu *hohen DPI-Daten* und zum Schreiben von Anwendungen, die *hohe DPI-fähige* Daten enthalten, finden Sie unter [High DPI](../hidpi/high-dpi-desktop-application-development-on-windows.md).

 

 
