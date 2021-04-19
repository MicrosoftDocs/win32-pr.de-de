---
description: Die Installation eines neuen Dienstanbieters ist hochgradig Geräte-und betriebssystemspezifisch, sodass die Details nicht in den Rahmen dieses SDK fallen.
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Installation und Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4391f8453d17cc70382d3ecb0dff65189b61c310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362683"
---
# <a name="installation-and-initialization"></a>Installation und Initialisierung

Die Installation eines neuen Dienstanbieters ist hochgradig Geräte-und betriebssystemspezifisch, sodass die Details nicht in den Rahmen dieses SDK fallen. Im Allgemeinen ist das Ziel der Installation die Konfiguration des Dienstanbieters für die aktuelle Kommunikationsumgebung. Dabei handelt es sich in der Regel um Registrierungseinträge und die Einstellung von Dienst Abhängigkeiten.

Die Initialisierung eines Telefoniedienstanbieters beginnt mit der Versions Aushandlung. Eine Erörterung der Versions Aushandlung und der aktuellen Version finden Sie unter [TSPI-Versions](tspi-versioning.md) Verwaltung.

TAPI ruft dann [**TSPI \_ providerinit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)auf, die dem Anbieter einen Zeiger auf eine Rückruffunktion übergibt, mit der der Fortschritt der asynchronen Funktionen gemeldet wird. Der TSP gibt die Anzahl der Zeilen-und Telefongeräte zurück, die mit dem aktuellen Geräte Bezeichner verknüpft sind.

In der Regel ist der nächste Schritt die Ressourcen Inventur, die von TAPI durchgeführt wird, indem [**TSPI \_ linegetdevcaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) und [**TSPI \_ linegetaddresscaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)aufgerufen werden. Der Dienstanbieter soll die Elemente der beteiligten Datenstrukturen ausfüllen, die sich auf die von ihm unterstützten Geräte-und Sitzungs Funktionen beziehen.

TAPI sammelt Informationen aus den verschiedenen Anwendungen bezüglich der Ereignis Benachrichtigungs Anforderungen und weist den TSP mit [**TSPI \_ linesetdefaultmediadetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) an, um anzugeben, welche Medientypen für eine Zeile und [**TSPI \_ linesetstatus-Meldungen**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) erkannt werden sollen, um anzugeben, welche Zeilen-und Adress Ereignisse gemeldet werden sollen.

 

 
