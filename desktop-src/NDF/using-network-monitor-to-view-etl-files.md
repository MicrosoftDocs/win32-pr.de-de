---
title: Verwenden von Microsoft-Netzwerkmonitor zum Anzeigen von ETL-Dateien
description: Netzwerkmonitor 3,3 ermöglicht es Benutzern, eine ETL-Datei zu analysieren, zu filtern und anzuzeigen (unter Verwendung von Windows Vista oder höher).
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04120f860654f4859aa930f32a4711999682eaf8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "103961041"
---
# <a name="using-network-monitor-to-view-etl-files"></a>Verwenden von Microsoft-Netzwerkmonitor zum Anzeigen von ETL-Dateien

[Netzwerkmonitor 3,3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) ermöglicht es Benutzern, eine ETL-Datei zu analysieren, zu filtern und anzuzeigen (unter Verwendung von Windows Vista oder höher). (Wenn Sie Netzwerkmonitor 3,2 verwenden, müssen Sie zusätzliche Parser von [codeplex](https://www.codeplex.com/NMParsers) herunterladen und installieren, um die Netzwerk Ablauf Verfolgungs Ereignisse zu erzeugen.)

Korrelierte ETL-Dateien gruppieren die relevanten Ereignisse. Die unten stehende ScrollBar zeigt eine korrelierte Datei, die in Netzwerkmonitor geöffnet ist

![Screenshot, der die Netzwerkmonitor anzeigt, wobei Korrelierte Ereignisse im linken Fenster hervorgehoben werden und utevent in der Dropdown-Dropdown-Funktion hervorgehoben ist.](images/ut-netmon1.png)

Korrelierte Ereignisse werden nach Aktivität im linken Bereich gruppiert. Sie können ein Ereignis im Frame Zusammenfassungs Bereich auswählen und dann mit der rechten Maustaste klicken, um die Konversation auf der Netzwerk Ereignis Ebene auszuwählen. Dadurch wird eine verwandte Aktivität im linken Bereich angezeigt.

Wenn Sie im linken Bereich eine bestimmte Aktivität auswählen und Sie erweitern, wird die Liste der Anbieter für die korrelierten Ereignisse angezeigt.

![Screenshot, der die Netzwerkmonitor mit einer Aktivität anzeigt, die im linken Bereich ausgewählt ist, sowie Ereignisse, die diesem Ereignis im rechten Bereich entsprechen.](images/ut-netmon2.png)

Wenn Sie einen bestimmten Anbieter im linken Bereich auswählen, wird eine Liste der für diesen Anbieter und jede Aktivität spezifischen Ereignisse im Frame Zusammenfassungs Bereich angezeigt.

![Screenshot, der einen bestimmten Anbieter anzeigt, der im linken Bereich ausgewählt ist, sowie eine Liste der für den anbieterspezifischen Ereignisse, die im oberen rechten Bereich hervorgehoben sind.](images/ut-netmon3.png)

Filter können in Netzwerkmonitor angewendet werden, um die Anzeige und Suche nach den richtigen Ereignissen oder Paketen zu vereinfachen. Beispielsweise können Sie einen Filter auf ausgewählte Fehlerereignisse anwenden (z. b. **utevent. Header. Descriptor. Level = = 2**), um Sie in einer bestimmten Farbe anzuzeigen.

![Screenshot, der das Dialogfeld "Farb Filter bearbeiten" anzeigt.](images/ut-netmon4.png)

Filter können auch angewendet werden, um verschiedene Anbieter in unterschiedlichen Farben zu markieren, sodass die Ergebnisse leichter angezeigt werden können.

![Screenshot, der ein Beispiel für verschiedene Anbieter anzeigt, die in unterschiedlichen Farben gekennzeichnet sind.](images/ut-netmon5.png)

Um einen Filter anzuwenden, klicken Sie im Menü **Filter** auf **colorfilters** .

In der folgenden Tabelle sind einige Beispiele für nützliche Filter aufgeführt.



| Filtern                                                                        | BESCHREIBUNG                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| Utevent. Header. Descriptor. Level = = 2                                          | Filtert nur Fehlerereignisse.                                        |
| Utevent. Header. Descriptor. Level = = 3                                          | Filtert nur Warnungs Ereignisse.                                      |
| UTEvent.Header.Descriptor.ID = = 2001                                          | Filtert nur Ereignisse mit der Ereignis-ID 2001.                           |
| WLAN \_ microsoftwindowtauscht autoConfig                                          | Filtert nur Ereignisse aus dem WLAN-Dienst.                            |
| N802 \_ microsoftwindowsnwifi                                                   | Filtert nur Ereignisse des systemeigenen WiFi-Treibers.                  |
| WLAN \_ microsoftwindowswap-AutoConfig und UTEvent.Header.Descriptor.ID = = 2001 | Filtert nur Ereignisse mit der vom WLAN-Dienst ausgegebenen Ereignis-ID 2001. |



 

 

 




