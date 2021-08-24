---
title: Verwenden von Microsoft-Netzwerkmonitor zum Anzeigen von ETL-Dateien
description: Netzwerkmonitor 3.3 ermöglicht Benutzern das Analysieren, Filtern und Anzeigen einer ETL-Datei (mit Windows Vista oder höher).
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc8c794b04837cc9d32b265eb81bfeb08fa47bdc1730672971ff6824b31c8ca0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685696"
---
# <a name="using-network-monitor-to-view-etl-files"></a>Verwenden von Microsoft-Netzwerkmonitor zum Anzeigen von ETL-Dateien

[Netzwerkmonitor 3.3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) ermöglicht Benutzern das Analysieren, Filtern und Anzeigen einer ETL-Datei (mit Windows Vista oder höher). (Wenn Sie Netzwerkmonitor 3.2 verwenden, müssen Sie zusätzliche Parser von [CodePlex](https://www.codeplex.com/NMParsers) herunterladen und installieren, um die Netzwerkablaufverfolgungsereignisse zu rendern.)

Korrelierte ETL-Dateien gruppieren die relevanten Ereignisse zusammen. Die unten gezeigte Unseigung zeigt eine korrelierte Datei, die in Netzwerkmonitor geöffnet ist, bei der die Konversation aktiviert ist.

![Screenshot: Netzwerkmonitor mit hervorgehobenen korrelierten Ereignissen im linken Fenster und hervorgehobenen UTEvent-Ereignissen in der Dropdownliste](images/ut-netmon1.png)

Korrelierte Ereignisse werden im linken Bereich nach Aktivität gruppiert. Sie können ein Ereignis im Bereich Framezusammenfassung auswählen und dann mit der rechten Maustaste klicken, um die Konversation auf Netzwerkereignisebene auszuwählen. Dadurch wird eine zugehörige Aktivität im linken Bereich angezeigt.

Wenn Sie eine bestimmte Aktivität im linken Bereich auswählen und erweitern, wird die Liste der Anbieter für die korrelierten Ereignisse angezeigt.

![Screenshot, der die Netzwerkmonitor mit einer im linken Bereich ausgewählten Aktivität und ereignissen zeigt, die diesem Ereignis im rechten Bereich entspricht.](images/ut-netmon2.png)

Wenn Sie im linken Bereich einen bestimmten Anbieter auswählen, wird im Bereich Framezusammenfassung eine Liste der ereignisse angezeigt, die für diesen Anbieter und die Aktivität spezifisch sind.

![Screenshot, der einen bestimmten Anbieter zeigt, der im linken Bereich ausgewählt wurde, und eine Liste der für den Anbieter spezifischen Ereignisse, die im oberen rechten Bereich hervorgehoben sind.](images/ut-netmon3.png)

Filter können in der Netzwerkmonitor, um das Anzeigen und Suchen der richtigen Ereignisse oder Pakete zu vereinfachen. Beispielsweise können Sie einen Filter auf ausgewählte Fehlerereignisse anwenden (z. B. **UTEvent.Header.Descriptor.Level == 2**), um sie in einer bestimmten Farbe anzuzeigen.

![Screenshot: Dialogfeld "Farbfilter bearbeiten"](images/ut-netmon4.png)

Filter können auch angewendet werden, um verschiedene Anbieter in unterschiedlichen Farben zu markieren, damit die Ergebnisse leichter angezeigt werden können.

![Screenshot: Beispiel für verschiedene Anbieter, die in unterschiedlichen Farben gekennzeichnet sind](images/ut-netmon5.png)

Um einen Filter anzuwenden, klicken Sie im Menü Filter **auf** **ColorFilters.**

Die folgende Tabelle enthält einige Beispiele für nützliche Filter.



| Filtern                                                                        | BESCHREIBUNG                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| UTEvent.Header.Descriptor.Level == 2                                          | Filtert nur Fehlerereignisse.                                        |
| UTEvent.Header.Descriptor.Level == 3                                          | Filtert nur Warnungsereignisse.                                      |
| UTEvent.Header.Descriptor.Id == 2001                                          | Filtert nur Ereignisse mit der Ereignis-ID 2001.                           |
| WLAN \_ MicrosoftWindowsWLANAutoConfig                                          | Filtert nur Ereignisse aus dem WLAN-Dienst.                            |
| N802 \_ MicrosoftWindowsNWiFi                                                   | Filtert nur Ereignisse aus dem Native Wifi-Treiber.                  |
| WLAN \_ MicrosoftWindowsWLANAutoConfig AND UTEvent.Header.Descriptor.Id == 2001 | Filtert nur Ereignisse mit der Ereignis-ID 2001, die vom WLAN-Dienst ausgegeben werden. |



 

 

 




