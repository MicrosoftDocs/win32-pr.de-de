---
description: In der Regel stellt ein Anbieter Daten im Namen einer Anwendung bereit.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Kommunizieren mit Ihrer Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb696c0c12ed8de542b07067fe16e13c9c098cb712393975e82d948bc3238979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061228"
---
# <a name="communicating-with-your-application"></a>Kommunizieren mit Ihrer Anwendung

In der Regel stellt ein Anbieter Daten im Namen einer Anwendung bereit. Beispielsweise kann ein Server eine Leistungs-DLL erstellen, um die Leistungsindikatordaten bereitzustellen. Die Kommunikation zwischen einer Anwendung und ihrem Anbieter unterscheidet sich bei Anwendungen im Benutzer- und Kernelmodus. Anbieter werden im Benutzermodus ausgeführt. Aus diesem Grund können Benutzermodusanwendungen, z. B. Druck- und Anzeigeanwendungen, beliebige Verfahren für die prozessübergreifende Kommunikation verwenden, z. B. Named Pipes, Dateizuordnung oder RPC. Kernelmodusanwendungen müssen jedoch eine IOCTL-Schnittstelle bereitstellen, die die Leistungsdaten an den Anbieter zurückgibt.

> [!WARNING]
> Verwenden Sie COM nicht als IPC-Mechanismus. Das System kann den COM-Initialisierungsstatus des Threads, der die Schnittstelle aufruft, nicht garantieren. Daher kann die DLL COM möglicherweise nicht erfolgreich initialisieren und die Daten sammeln.

 

 

 



