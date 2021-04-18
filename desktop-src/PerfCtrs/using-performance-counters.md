---
description: Informationen zur Nutzung von Counter-Daten finden Sie unter Verwenden von Counter-Daten
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: Verwenden von Leistungsindikatoren
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: abc055a34f0937e056d1d983354fc0a3edf182a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351680"
---
# <a name="using-performance-counters"></a>Verwenden von Leistungsindikatoren

Leistungsindikatorenconsumer sind Softwarekomponenten, die Leistungsdaten des Leistungs **Zählers erfassen** und nutzen. Zu den von Microsoft bereitgestellten Beispiel Verbrauchern Gehören System Monitor (perfmon.exe), Ressourcenmonitor (resmon.exe), Protokoll-Manager (logman.exe) und typeperf.exe. Softwarekomponenten von Drittanbietern können auch Leistungsdaten über Leistungsdaten Sammlungs-APIs oder über WMI-Leistungs Leistungs Bestellungs Klassen sammeln.

Leistungsindikatorenanbieter sind Softwarekomponenten zum Veröffentlichen von Leistungsdaten.  Leistungsindikatoren können von Betriebssystemkomponenten, Gerätetreibern und Diensten bereitgestellt werden. Viele Leistungsindikatoren werden als Teil des Windows-Betriebssystems bereitgestellt. Zusätzliche Leistungsindikatoren können von Softwarekomponenten von Drittanbietern über die Leistungsindikator Anbieter-APIs bereitgestellt werden.

- Verwenden Sie [Leistungs Tool Tools](performance-counters-tools.md) , wenn Sie die Leistungsdaten eines Systems erfassen oder anzeigen möchten.
- Verwenden Sie Leistungswert- [Consumer-APIs](consuming-counter-data.md) , wenn Sie ein Programm zum Sammeln von Leistungsdaten aus dem lokalen System schreiben möchten.
- Verwenden Sie [WMI-Leistungs Leistungs Zählers](/windows/desktop/WmiSdk/monitoring-performance-data) , wenn Sie Leistungsdaten von einem lokalen System oder Remote System mithilfe von WMI sammeln möchten.
- Verwenden Sie [Leistungs Anbieter-APIs](providing-counter-data.md) , wenn Sie Leistungsdaten aus ihrer Softwarekomponente veröffentlichen möchten.

## <a name="see-also"></a>Siehe auch

[Informationen zu Leistungsindikatoren](about-performance-counters.md)

[Leistungsindikator Referenz](performance-counters-reference.md)
