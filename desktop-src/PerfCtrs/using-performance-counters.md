---
description: Informationen zum Nutzen von Indikatordaten finden Sie unter Nutzen von Indikatordaten.
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: Verwenden von Leistungsindikatoren
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 18bb017a34fb23188c20e81bce28c171c50dcb4d43cd52d458e92be99b7d03a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033210"
---
# <a name="using-performance-counters"></a>Verwenden von Leistungsindikatoren

**Leistungsindikatorverbraucher** sind Softwarekomponenten, die Leistungsindikatordaten sammeln und nutzen. Beispiele für Consumer, die von Microsoft bereitgestellt werden, sind Leistungsmonitor (perfmon.exe), Ressourcenmonitor (resmon.exe), Log Manager (logman.exe) und typeperf.exe. Softwarekomponenten von Drittanbietern können auch Leistungsdaten über Leistungserfassungs-APIs oder WMI-Leistungsindikatorklassen sammeln.

**Leistungsindikatoranbieter** sind Softwarekomponenten, die Leistungsindikatordaten veröffentlichen. Leistungsindikatoren können von Betriebssystemkomponenten, Gerätetreibern und Diensten bereitgestellt werden. Viele Leistungsindikatoren werden als Teil des Windows Betriebssystems bereitgestellt. Zusätzliche Leistungsindikatoren können von Softwarekomponenten von Drittanbietern über die Leistungsindikatoranbieter-APIs bereitgestellt werden.

- Verwenden Sie [Leistungsindikatortools,](performance-counters-tools.md) wenn Sie die Indikatordaten eines Systems erfassen oder anzeigen möchten.
- Verwenden Sie [Leistungsindikator-Consumer-APIs,](consuming-counter-data.md) wenn Sie ein Programm schreiben möchten, das Indikatordaten aus dem lokalen System sammelt.
- Verwenden Sie [WMI-Leistungsindikatorklassen,](/windows/desktop/WmiSdk/monitoring-performance-data) wenn Sie Leistungsindikatordaten von einem lokalen oder Remotesystem mithilfe von WMI sammeln möchten.
- Verwenden Sie [Leistungsindikatoranbieter-APIs,](providing-counter-data.md) wenn Sie Leistungsindikatordaten aus Ihrer Softwarekomponente veröffentlichen möchten.

## <a name="see-also"></a>Siehe auch

[Informationen zu Leistungsindikatoren](about-performance-counters.md)

[Referenz zu Leistungsindikatoren](performance-counters-reference.md)
