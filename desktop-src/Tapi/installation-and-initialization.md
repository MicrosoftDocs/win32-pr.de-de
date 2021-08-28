---
description: Die Installation eines neuen Dienstanbieters ist geräte- und betriebssystemspezifisch, sodass die Details außerhalb des Bereichs dieses SDK liegen.
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Installation und Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b15dc5d9d93ce33ac13a04aec3abd7d49fec3ed2ece3cce691d47c0d617bacd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003538"
---
# <a name="installation-and-initialization"></a>Installation und Initialisierung

Die Installation eines neuen Dienstanbieters ist geräte- und betriebssystemspezifisch, sodass die Details außerhalb des Bereichs dieses SDK liegen. Im Allgemeinen ist das Ziel der Installation die Konfiguration des Dienstanbieters für die aktuelle Kommunikationsumgebung. Dies umfasst in der Regel Registrierungseinträge und die Einstellung von Dienstabhängigkeiten.

Die Initialisierung eines Telefoniedienstanbieters beginnt mit der Versionsaushandlung. Eine Erläuterung der Versionsaushandlung und der aktuellen Version finden Sie unter [TSPI-Versionierung.](tspi-versioning.md)

TAPI ruft dann [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)auf, der dem Anbieter einen Zeiger auf eine Rückruffunktion übergibt, die zum Melden des Fortschritts asynchroner Funktionen verwendet wird. Der TSP gibt die Anzahl der Zeilen- und Telefongeräte zurück, die dem aktuellen Gerätebezeichner zugeordnet sind.

In der Regel ist der nächste Schritt die Ressourceninventur, die von TAPI durchgeführt wird und [**tspi \_ lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) und [**TSPI \_ lineGetAddressCaps aufruft.**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps) Es wird erwartet, dass der Dienstanbieter die Elemente der beteiligten Datenstrukturen einfüllt, die sich auf die unterstützten Geräte- und Sitzungsfunktionen beziehen.

TAPI sammelt Informationen zu den Anforderungen an Ereignisbenachrichtigungen aus den verschiedenen Anwendungen und weist den TSP mit [**tspi \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) an, welche Medientypen für eine Zeile und [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) erkannt werden sollen, um anzugeben, welche Zeilen- und Adressereignisse gemeldet werden sollen.

 

 
