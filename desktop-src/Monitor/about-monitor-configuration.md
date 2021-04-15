---
title: Informationen zur Monitor Konfiguration
description: Informationen zur Monitor Konfiguration
ms.assetid: 66345021-41e8-429a-bbf7-a4aa72a57337
keywords:
- überwachen, Informationen zu
- überwachen, Farbkalibrierung
- überwachen, Anpassen des Anzeige Bereichs des Monitors
- überwachen, Speichern von Monitoreinstellungen
- Überwachung, Wiederherstellen von Monitoreinstellungen
- Monitor, Hersteller Features
- Farbkalibrierung
- Anpassen des Anzeige Bereichs des Monitors
- Monitoreinstellungen werden gespeichert
- Überwachungs Einstellungen werden wieder hergestellt
- Hersteller Features
- Monitor Konfiguration, Farbkalibrierung
- Monitor Konfiguration, Informationen zu
- Monitor Konfiguration, Anpassen des Anzeige Bereichs des Monitors
- Überwachen der Konfiguration, Speichern von Monitoreinstellungen
- Überwachen der Konfiguration, Wiederherstellen von Monitoreinstellungen
- Monitor Konfiguration, Hersteller Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d8e2f3d463bc84acaf8b48f493f5a0118976ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515681"
---
# <a name="about-monitor-configuration"></a>Informationen zur Monitor Konfiguration

Folgende Verwendungsmöglichkeiten für die Überwachungs Konfigurationsfunktionen finden Sie unter:

-   Farbkalibrierung. Mit einem ordnungsgemäß kalibrierten Monitor werden Farben ordnungsgemäß wieder hergestellt. In der Regel zeigt eine farbkalibrierungsanwendung ein Testmuster an und verfügt über Steuerelemente, um eine Monitor Einstellung zu ändern. Der Benutzer ändert die Einstellung, bis eine Bedingung erfüllt ist, und wiederholt diesen Vorgang für jede Monitor Einstellung, bis der Monitor gekalibriert ist.
-   Der Anzeigebereich des Monitors wird angepasst. Mithilfe der Überwachungs Konfigurationsfunktionen können die Größe und Position des Anzeige Bereichs eines Monitors geändert werden. Wenn ein LCD-Monitor z. b. über einen analogen Connector mit einem Computer verbunden ist, wird die beste Bildqualität erzielt, wenn eine eins-zu-Eins-Zuordnung zwischen Pixeln im Frame Puffer der Grafikkarte und Pixel im LCD-Monitor vorhanden ist.
-   Die Monitoreinstellungen werden gespeichert und wieder hergestellt. Einige Benutzer benötigen mehrere Überwachungs Einstellungen, da für verschiedene Szenarien unterschiedliche Monitoreinstellungen erforderlich sind. Beispielsweise sind die Monitoreinstellungen, die für Desktop Anwendungen optimal sind, für die Überwachung des Fernseh Monitors nicht optimal.
-   Mithilfe Hersteller spezifischer Monitor Features. Mithilfe der Überwachungs Konfigurationsfunktionen können Hersteller Anwendungen erstellen, die die herstellerspezifischen Funktionen des Monitors verwenden.

Die Überwachungs Konfigurationsfunktionen sind in Funktionen auf hoher Ebene und auf niedriger Ebene unterteilt. Die Funktionen auf hoher Ebene sind einfacher zu verwenden als die Funktionen auf niedriger Ebene. Wenn Sie die Funktionen auf hoher Ebene verwenden möchten, müssen Sie nichts über die Anzeigedaten Kanal-Befehlsschnittstelle (DDC/CI) wissen. Die Funktionen auf hoher Ebene bieten Ihnen jedoch keinen Zugriff auf herstellerspezifische Features des Monitors.

Bei den Funktionen auf niedriger Ebene handelt es sich um einen schmalen Wrapper um die DDC/CI-Befehle. Um die Low-Level-Funktionen verwenden zu können, müssen Sie mit dem DDC/CI-Standard und auch mit dem VESA-Monitor Steuerungs Befehlssatz (MCCS) vertraut sein. Im Allgemeinen sollten Sie die Funktionen auf hoher Ebene verwenden, es sei denn, Sie müssen Funktionen verwenden, die nur in den Funktionen auf niedriger Ebene verfügbar sind.

Die Konfigurationsfunktionen auf hoher Ebene sind so konzipiert, dass eine Anwendung einen Monitor nicht in den unbrauchbar Zustand versetzen kann. Die Funktionen auf niedriger Ebene können zum Senden von VCP-Codes an den Monitor verwendet werden. Beachten Sie jedoch, dass einige VCP-Codes wichtige Funktionen deaktivieren oder den Monitor in einen Zustand versetzen können, in dem der Benutzer das Anzeige Bild nicht sehen kann. Weitere Informationen finden Sie unter VESA Monitor Control Command Set (MCCS) Standard.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Monitor Konfiguration](monitor-configuration.md)
</dt> </dl>

 

 




