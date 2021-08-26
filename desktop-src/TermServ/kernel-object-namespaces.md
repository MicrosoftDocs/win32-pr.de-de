---
title: Kernelobjektnamespaces
description: Remotedesktopdienste verwendet mehrere Namespaces für Kernelobjekte. ein globaler Namespace wird hauptsächlich von Diensten in Client-/Serveranwendungen verwendet.
ms.assetid: 771e0bbf-bd73-4e87-aa1e-945c1287b517
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82e1064638844039091dbe93aa1fedc75cb93f4aa1d012f8864e0154673c6cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989080"
---
# <a name="kernel-object-namespaces"></a>Kernelobjektnamespaces

Ein Remotedesktopdienste-Server verfügt über mehrere Namespaces für die folgenden benannten Kernelobjekte: Ereignisse, Semaphore, Mutexe, wartebare Timer, Dateizuordnungsobjekte und Auftragsobjekte. Es gibt einen globalen Namespace, der hauptsächlich von Diensten in Client-/Serveranwendungen verwendet wird. Darüber hinaus verfügt jede Clientsitzung über einen separaten Namespace für diese Objekte, z. B. in Windows Vista.

Die separaten Clientsitzungsnamespaces ermöglichen es mehreren Clients, dieselben Anwendungen ohne Beeinträchtigungen voneinander ausführen zu müssen. Für Prozesse, die unter einer Clientsitzung gestartet werden, verwendet das System standardmäßig den Sitzungsnamespace. Diese Prozesse können jedoch den globalen Namespace verwenden, indem dem Objektnamen das Präfix \\ "Global" vorangestellt wird. Der folgende Code ruft beispielsweise [**CreateEvent auf und**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) erstellt ein Ereignisobjekt namens CSAPP im globalen Namespace:

> [!Note]  
> Der globale Namespace ist nicht für Windows Store verfügbar.

 

`CreateEvent( NULL, FALSE, FALSE, "Global\\CSAPP" );`

Dienstanwendungen in einer Remotedesktopdienste-Umgebung verwenden standardmäßig den globalen Namespace.

Sitzung 0 wird nur zum Hosten von Diensten verwendet, und es gibt keine Konsolensitzung, im Gegensatz zu früheren Versionen von Windows.

Der globale Namespace ermöglicht es Prozessen in mehreren Clientsitzungen, mit einer Dienstanwendung zu kommunizieren. Beispielsweise kann eine Client-/Serveranwendung ein Mutex-Objekt für die Synchronisierung verwenden. Das Servermodul kann das Mutex-Objekt im globalen Namespace erstellen. Anschließend kann eine Clientsitzung das Präfix \\ "Global" verwenden, um das Mutex-Objekt zu öffnen.

Eine weitere Verwendung des globalen Namespace ist für Anwendungen, die benannte Objekte verwenden, um zu erkennen, dass bereits eine Instanz der Anwendung im System für alle Sitzungen ausgeführt wird. Dieses benannte Objekt muss im globalen Namespace erstellt oder geöffnet werden, anstatt im Sitzungsnamespace. Der häufigere Fall, dass die Anwendung einmal pro Sitzung ausgeführt wird, wird standardmäßig unterstützt, da das benannte Objekt in einem Namespace pro Sitzung erstellt wird.

Zusätzlich zum Präfix "Global" können Clientprozesse das Präfix "Local" verwenden, um explizit ein Objekt \\ \\ in ihrem Sitzungsnamespace zu erstellen. Bei diesen Schlüsselwörtern wird die Kleinschreibung beachtet.

Das Präfix "Session" ist für die Systemnutzung reserviert, und Sie sollten es nicht in Namen \\ von Kernelobjekten verwenden.

Schnelle Benutzerwechsel werden mithilfe von Remotedesktopdienste implementiert. Der erste Benutzer, der sich anmeldet, verwendet Sitzung 1, der nächste Benutzer, der sich anmeldet, verwendet Sitzung 2 und so weiter. Kernelobjektnamen müssen die richtlinien für die Remotedesktopdienste damit Anwendungen mehrere Benutzer unterstützen können.

Die Erstellung eines Dateizuordnungsobjekts im globalen Namespace mit [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)aus einer anderen Sitzung als Sitzung 0 ist ein privilegierter Vorgang. Aus diesem Grund muss für eine Anwendung, die in einer beliebigen Remotedesktop-Sitzungshost-Serversitzung (RD-Sitzungshost) ausgeführt wird, [SeCreateGlobalPrivilege](/windows/desktop/SecAuthZ/authorization-constants) aktiviert sein, damit ein Dateizuordnungsobjekt im globalen Namespace erfolgreich erstellt werden kann. Die Berechtigungsprüfung ist auf die Erstellung von Dateizuordnungsobjekten beschränkt und gilt nicht für das Öffnen vorhandener Objekte. Wenn beispielsweise ein Dienst oder das System ein Dateizuordnungsobjekt erstellt, kann jeder Prozess, der in einer Sitzung ausgeführt wird, auf dieses Dateizuordnungsobjekt zugreifen, vorausgesetzt, der Benutzer hat den erforderlichen Zugriff.

 

 