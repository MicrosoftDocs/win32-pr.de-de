---
description: Wenn die Daten kohärent sind, werden die Daten auf dem Server und alle Clients synchronisiert. Eine Art von Softwaresystem, das Datenkonsistenz bereitstellt, ist ein Revisions Steuerungssystem (RCS).
ms.assetid: cd33d20e-bf25-4a50-9b20-344495554434
title: Datenkohärenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f300296ff0fdc807beb95e2c03662814957bedb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867699"
---
# <a name="data-coherency"></a>Datenkohärenz

Daten, die *kohärent* sind, sind Daten, die im gesamten Netzwerk identisch sind. Anders ausgedrückt: Wenn Daten kohärent sind, werden die Daten auf dem Server und allen Clients synchronisiert. Eine Art von Softwaresystem, das Datenkonsistenz bereitstellt, ist ein Revisions Steuerungssystem (RCS). Ein solches System ist in der Regel recht einfach, und nur ein Benutzer darf eine angegebene Datei gleichzeitig ändern. Andere Benutzer können die Datei lesen, aber nicht ändern.

Der Benutzer, der eine Datei ändern kann, hat ihn als ausgecheckt bezeichnet. Der Benutzer überprüft dann die geänderte Datei, damit andere Benutzer die Änderungen sehen können. Erst nachdem der Benutzer eine Datei wieder eingecheckt hat, kann er von einem anderen Benutzer ausgecheckt werden.

Eine RCS erfordert, dass der aktive Eingriff von Benutzern auf nützliche Weise funktioniert. Ein Dateisystem, das über ein Netzwerk betrieben wird, sollte das Problem automatisch behandeln.

Das lokale Zwischenspeichern von kohärenten Daten ist recht einfach, wenn ein Thread auf einem Client auf eine Datei im gesamten Netzwerk zugreift. In den meisten Fällen lesen viele verschiedene Threads auf einem oder mehreren Computern jedoch möglicherweise dieselbe Datei. Diese Situation ist immer noch recht unkompliziert. Da die Daten in der Datei statisch sind, kann jeder Client Computer über eine eigene lokale Kopie verfügen, ohne dass sich dies auf die Datenkohärenz auswirkt.

Eine allgemeinere Situation besteht darin, dass ein Thread die Datei ändert und viele andere Threads Sie lesen. In dem Moment, in dem ein Schreibvorgang stattfindet, sind alle lokalen Caches dieser Datei veraltet. Der Server muss jeden Client Benachrichtigen, damit der Cache abgebrochen wird. Alle nachfolgenden Lesevorgänge für die Datei müssen über das Netzwerk ausgeführt werden.

In einer anderen häufigen Situation könnten mehrere Threads auf einem oder mehreren Netzwerk Clients versuchen, in dieselbe Datei zu schreiben. Diese Situation ähnelt einer solchen Situation, in der mehrere RCS-Benutzer alle Änderungen an derselben Datei vornehmen möchten. Jeder Benutzer muss die Datei Auschecken, Änderungen vornehmen und die Datei dann wieder einchecken. Ebenso muss der Server in einem lokalen zwischen Speicherungs Schema die Berechtigung zum Schreiben in eine Datei an einen Client Thread gleichzeitig übergeben.

 

 



