---
title: Hohe DPI-Werte
description: Hohe DPI-Werte
ms.assetid: 476fe65c-2acd-4a7a-8a76-72d9f010b772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5006d5bdf1c9e90745ef8e3571e64e729dbf5dff54338280789f39c6d0027e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118203961"
---
# <a name="high-dpi"></a>Hohe DPI-Werte

Mit zunehmender Anzahl von Anzeigetechnologien haben Hersteller die Anzahl der von ihren Displays unterstützten Pixel erhöht. Während Text-, Bilder- und Benutzeroberflächenelemente auf Bildschirmen mit hoher Auflösung deutlich schärfer und besser lesbar aussehen, muss das Betriebssystem hochskaliert werden, um die visuelle Darstellung zu unterstützen. Andernfalls sieht alles nur kleiner aus.

Windows 7 unterstützt hohe *DPI-Anzeigen.* Marktdaten deuten darauf hin, dass bereitstellungen mit hohen *DPI-Bildschirmen* (120-144 Punkte pro Zoll (dpi)) im zeitraum von Windows 7 erhöht werden. Wenn sie native Auflösungen auf diesen Bildschirmen ausführen, werden viele Anwendungen nur sehr klein angezeigt, wenn sie *hohe DPI-Daten* verwenden. Einige Anwendungen (z. B. Windows Internet Explorer) verfügen über Features für die Schriftskalierung, mit denen Benutzer die Anzeige vergrößern und verkleinern können, bei vielen Anwendungen jedoch nicht. Das Feature *"High DPI"* in Windows 7:

-   Stellt sicher, dass Windows und Anwendungserfahrungen auf Standardhardware optimal sind (*DPI-Einstellungen* sind für die Funktionen der Hardware optimiert).
-   Ermöglicht es der Windows Shell und anderen Windows-basierten Anwendungen, mit unterschiedlichen *DPI-Einstellungen* gut auszusehen.
-   Beachtet *DPI-Standardeinstellungen* basierend auf Hardwarespezifikationen und -funktionen.
-   Ermöglicht Es Benutzern, *DPI-Einstellungen* ohne Neustart zu personalisieren.
-   Stellt sicher, dass der Bildschirm immer auf native Auflösung festgelegt ist.

Die Windows *DPI-Skalierungsfunktion* skaliert Schriftarten und Benutzeroberflächenelemente (z. B. Schaltflächen, Symbole und Eingabefelder) um einen berechneten Prozentsatz, wie durch die *DPI-Einstellung* angegeben. Dies unterscheidet sich von der Skalierung, die auftritt, wenn die Anzeigeauflösung verringert wird. Im Fall der *DPI-Skalierung* stellt Windows Schriftarten und Benutzeroberflächenelemente bereit, die mit mehr Pixeln gezeichnet werden, was zu einer größeren, höheren Genauigkeit und schärferen Windows führt. Drittanbieteranwendungen Windows können *Hohe DPI-Einstellungen* nutzen und die Benutzeroberfläche entsprechend anpassen, indem sie sich selbst für *hohe DPI-fähige* Daten deklarieren. Anwendungsentwickler sollten nicht mehr davon ausgehen, dass 96 dpi die ideale Auflösung für alle Anwendungen ist.

Weitere Informationen zu *hohen DPI-Daten* und zum Schreiben von Anwendungen, die *hohe DPI-fähige* Daten enthalten, finden Sie unter [High DPI](../hidpi/high-dpi-desktop-application-development-on-windows.md).

 

 
