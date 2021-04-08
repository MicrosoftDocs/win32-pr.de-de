---
description: In der Regel stellt ein Anbieter Daten im Auftrag einer Anwendung bereit.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Kommunikation mit Ihrer Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6def58d3e03676f3b1b46ba3ebd756eb3adc6196
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865131"
---
# <a name="communicating-with-your-application"></a>Kommunikation mit Ihrer Anwendung

In der Regel stellt ein Anbieter Daten im Auftrag einer Anwendung bereit. Beispielsweise kann ein Server eine Leistungs-DLL erstellen, um die Leistungsdaten des Zählers bereitzustellen. Die Kommunikation zwischen einer Anwendung und Ihrem Anbieter unterscheidet sich für Anwendungen im Benutzermodus und im Kernel Modus. Anbieter werden im Benutzermodus ausgeführt. Aus diesem Grund können Benutzermodusanwendungen, wie z. b. Druck-und Anzeige Anwendungen, beliebige Verfahren für die prozessübergreifende Kommunikation verwenden, z. b. Named Pipes, Datei Zuordnung oder RPC. Kernelmodusanwendungen müssen jedoch eine ioctl-Schnittstelle bereitstellen, die die Leistungsdaten an den Anbieter zurückgibt.

> [!WARNING]
> Verwenden Sie com nicht als IPC-Mechanismus. Das System kann den com-Initialisierungs Status des Threads nicht garantieren, der die-Schnittstelle aufrufen. Daher ist die dll möglicherweise nicht in der Lage, com erfolgreich zu initialisieren und die Daten zu erfassen.

 

 

 



