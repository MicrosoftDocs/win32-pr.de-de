---
title: Informationen zur Monitorkonfiguration
description: Informationen zur Monitorkonfiguration
ms.assetid: 66345021-41e8-429a-bbf7-a4aa72a57337
keywords:
- monitor,about
- Monitor, Farb kalibrieren
- Monitor,Anzeigebereich des Monitors anpassen
- Überwachen,Speichern von Monitoreinstellungen
- Überwachen,Wiederherstellen von Monitoreinstellungen
- Monitor,Anbieterfeatures
- Farb kalibrieren
- Anpassen des Anzeigebereichs des Monitors
- Speichern von Monitoreinstellungen
- Wiederherstellen von Monitoreinstellungen
- Anbieterfeatures
- Überwachen der Konfiguration, Farb kalibrieren
- Überwachen der Konfiguration,Informationen
- Monitorkonfiguration, Anpassen des Anzeigebereichs des Monitors
- Überwachen der Konfiguration,Speichern von Monitoreinstellungen
- Überwachen der Konfiguration,Wiederherstellen von Monitoreinstellungen
- Überwachen der Konfiguration, Anbieterfeatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5f3d8c56521c07d704fe586f486298d0e679d1bfc33e25a29d943aa92dd66e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146183"
---
# <a name="about-monitor-configuration"></a>Informationen zur Monitorkonfiguration

Zu den Verwendungsmöglichkeiten für die Monitorkonfigurationsfunktionen gehören:

-   Farberbung. Ein ordnungsgemäß kalibrierter Monitor reproduziert Farben ordnungsgemäß. In der Regel zeigt eine Farb kalibrierungsanwendung ein Testmuster an und verfügt über Steuerelemente zum Ändern einer Monitoreinstellung. Der Benutzer ändert die Einstellung, bis eine Bedingung erfüllt ist, und wiederholt diesen Vorgang für jede Monitoreinstellung, bis der Monitor kalibriert ist.
-   Anpassen des Anzeigebereichs des Monitors. Die Monitorkonfigurationsfunktionen können verwendet werden, um die Größe und Position des Anzeigebereichs eines Monitors zu ändern. Wenn z. B. ein MONITORS-Monitor über einen analogen Connector mit einem Computer verbunden ist, wird die beste Bildqualität erzielt, wenn eine 1:1-Zuordnung zwischen Pixeln im Framepuffer der Grafikkarte und Pixeln auf dem DISPLAY-Monitor besteht.
-   Speichern und Wiederherstellen von Monitoreinstellungen. Einige Benutzer benötigen mehrere Sätze von Monitoreinstellungen, da verschiedene Szenarien unterschiedliche Monitoreinstellungen erfordern. Monitoreinstellungen, die für Desktopanwendungen optimal sind, sind beispielsweise nicht optimal für die Fernsehsendung.
-   Verwenden anbieterspezifischer Monitorfeatures. Mithilfe der Monitorkonfigurationsfunktionen können Hersteller Anwendungen erstellen, die die herstellerspezifischen Features des Monitors verwenden.

Die Monitorkonfigurationsfunktionen sind in Funktionen auf hoher und niedriger Ebene unterteilt. Die Funktionen auf hoher Ebene sind einfacher zu verwenden als die Low-Level-Funktionen. Um die funktionen auf hoher Ebene verwenden zu können, müssen Sie nichts über die Display Data Channel Command Interface (DDC/CI) wissen. Die funktionen auf hoher Ebene bieten Ihnen jedoch keinen Zugriff auf anbieterspezifische Funktionen des Monitors.

Die Funktionen auf niedriger Ebene sind ein schlanker Wrapper um die DDC/CI-Befehle. Um die Low-Level-Funktionen verwenden zu können, müssen Sie mit dem DDC/CI-Standard und dem VESA Monitor Control Command Set (MCCS)-Standard vertraut sein. Im Allgemeinen sollten Sie die allgemeinen Funktionen verwenden, es sei denn, Sie müssen Features verwenden, die nur in den Low-Level-Funktionen verfügbar sind.

Die konfigurationsbasierten Monitorfunktionen auf hoher Ebene sind so konzipiert, dass eine Anwendung einen Monitor nicht in einen unbrauchbaren Zustand bringen kann. Die Funktionen auf niedriger Ebene können verwendet werden, um VCP-Codes an den Monitor zu senden. Beachten Sie jedoch, dass einige VCP-Codes wichtige Funktionen deaktivieren oder den Monitor in einen Zustand bringen können, in dem der Benutzer das Anzeigebild nicht sehen kann. Weitere Informationen finden Sie unter VESA Monitor Control Command Set (MCCS)-Standard.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachen der Konfiguration](monitor-configuration.md)
</dt> </dl>

 

 




