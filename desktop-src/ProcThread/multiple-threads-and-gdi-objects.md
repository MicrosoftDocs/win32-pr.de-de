---
description: Um die Leistung zu verbessern, wird der Zugriff auf Grafikgeräte Schnittstellen-Objekte (z. b. Paletten, Geräte Kontexte, Regionen und ähnliches) nicht serialisiert.
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Mehrere Threads und GDI-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5822539248be5189f7a8e7fb15f4ef8a42ff1b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360533"
---
# <a name="multiple-threads-and-gdi-objects"></a>Mehrere Threads und GDI-Objekte

Um die Leistung zu verbessern, wird der Zugriff auf Grafikgeräte Schnittstellen-Objekte (z. b. Paletten, Geräte Kontexte, Regionen und ähnliches) nicht serialisiert. Dadurch entsteht eine potenzielle Gefahr für Prozesse, die über mehrere Threads verfügen, die diese Objekte gemeinsam nutzen. Wenn ein Thread z. b. ein GDI-Objekt löscht, während er von einem anderen Thread verwendet wird, sind die Ergebnisse unvorhersehbar. Diese Gefahr kann vermieden werden, indem GDI-Objekte nicht gemeinsam genutzt werden. Wenn die Freigabe unvermeidlich (oder wünschenswert) ist, muss die Anwendung eigene Mechanismen für die Synchronisierung des Zugriffs bereitstellen. Weitere Informationen zur Synchronisierung des Zugriffs finden Sie unter [Synchronisieren der Ausführung mehrerer Threads](synchronizing-execution-of-multiple-threads.md).

 

 



