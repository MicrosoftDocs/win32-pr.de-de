---
description: Um die Leistung zu verbessern, wird der Zugriff auf GDI-Objekte (Graphics Device Interface) (z. B. Paletten, Gerätekontexte, Bereiche usw.) nicht serialisiert.
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Mehrere Threads und GDI-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a17c7edcf32341eb9b1eaff3546fbe7be219b5f924a85d4a1db1d584a0a5922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032330"
---
# <a name="multiple-threads-and-gdi-objects"></a>Mehrere Threads und GDI-Objekte

Um die Leistung zu verbessern, wird der Zugriff auf GDI-Objekte (Graphics Device Interface) (z. B. Paletten, Gerätekontexte, Bereiche usw.) nicht serialisiert. Dies führt zu einer potenziellen Gefahr für Prozesse, deren Objekte von mehreren Threads gemeinsam verwendet werden. Wenn beispielsweise ein Thread ein GDI-Objekt löscht, während es von einem anderen Thread verwendet wird, sind die Ergebnisse unvorhersehbar. Diese Gefahr kann vermieden werden, indem GDI-Objekte einfach nicht gemeinsam verwendet werden. Wenn die Freigabe unvermeidbar (oder wünschenswert) ist, muss die Anwendung eigene Mechanismen für die Synchronisierung des Zugriffs bereitstellen. Weitere Informationen zum Synchronisieren des Zugriffs finden Sie unter [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md)( Synchronisieren der Ausführung mehrerer Threads).

 

 



