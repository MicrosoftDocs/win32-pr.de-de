---
title: Kernelobjektnamespaces
description: Remotedesktopdienste verwendet mehrere Namespaces für Kernel Objekte. ein globaler Namespace wird hauptsächlich von Diensten in Client/Server-Anwendungen verwendet.
ms.assetid: 771e0bbf-bd73-4e87-aa1e-945c1287b517
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20680a32c8b35e3fa2f1ab15c732683d424550f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340933"
---
# <a name="kernel-object-namespaces"></a>Kernelobjektnamespaces

Ein Remotedesktopdienste Server verfügt über mehrere Namespaces für die folgenden benannten Kernel Objekte: Ereignisse, Semaphore, Mutexen, wabbare Timer, Datei Zuordnung und Auftrags Objekte. Es gibt einen globalen Namespace, der hauptsächlich von Diensten in Client-/Server-Anwendungen verwendet wird. Außerdem verfügt jede Client Sitzung über einen separaten Namespace für diese Objekte, z. b. in Windows Vista.

Die separaten clientsitzungsnamespaces ermöglichen es mehreren Clients, dieselben Anwendungen auszuführen, ohne sich gegenseitig zu stören. Für Prozesse, die unter einer Client Sitzung gestartet werden, verwendet das System standardmäßig den Sitzungs Namespace. Allerdings können diese Prozesse den globalen Namespace verwenden, indem dem Objektnamen das Präfix "Global" vorangestellt wird \\ . Der folgende Code ruft beispielsweise " [**kreateevent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) " auf und erstellt ein Ereignis Objekt mit dem Namen "csapp" im globalen Namespace:

> [!Note]  
> Der globale Namespace ist für Windows Store-Apps nicht verfügbar.

 

`CreateEvent( NULL, FALSE, FALSE, "Global\\CSAPP" );`

Dienst Anwendungen in einer Remotedesktopdienste Umgebung verwenden standardmäßig den globalen Namespace.

Sitzung Null wird nur für Hostingdienste verwendet, und im Gegensatz zu früheren Versionen von Windows gibt es keine Konsolen Sitzung.

Der globale Namespace ermöglicht die Kommunikation von Prozessen in mehreren Client Sitzungen mit einer-Dienst Anwendung. Beispielsweise kann eine Client/Server-Anwendung ein Mutex-Objekt für die Synchronisierung verwenden. Das Servermodul kann das Mutex-Objekt im globalen Namespace erstellen. Eine Client Sitzung kann dann das "Global \\ "-Präfix verwenden, um das Mutex-Objekt zu öffnen.

Eine weitere Verwendung des globalen Namespace ist für Anwendungen, die benannte Objekte verwenden, um zu erkennen, dass bereits eine Instanz der Anwendung im System über alle Sitzungen hinweg ausgeführt wird. Dieses benannte Objekt muss im globalen Namespace anstelle des Sitzungs spezifischen Namespace erstellt oder geöffnet werden. Der gängigste Fall, dass die Anwendung einmal pro Sitzung ausgeführt wird, wird standardmäßig unterstützt, da das benannte Objekt in einem pro-Sitzungs-Namespace erstellt wird.

Zusätzlich zum "globalen \\ " Präfix können Client Prozesse das Präfix "local" verwenden, \\ um explizit ein Objekt in seinem Sitzungs Namespace zu erstellen. Bei diesen Schlüsselwörtern wird Groß-/Kleinschreibung

Das \\ Präfix "Session" ist für die Verwendung durch das System reserviert und sollte nicht in Namen von Kernel Objekten verwendet werden.

Die schnelle Benutzerumschaltung wird mithilfe von Remotedesktopdienste Sitzungen implementiert. Der erste Benutzer, der sich anmelden soll, verwendet Sitzung 1, der nächste Benutzer, der sich anmelden möchte, verwendet Sitzung Two usw. Kernel Objektnamen müssen den für Remotedesktopdienste beschriebenen Richtlinien entsprechen, damit Anwendungen mehrere Benutzer unterstützen können.

Die Erstellung eines Datei Mapping-Objekts im globalen Namespace mit der Verwendung von "" von "" in einer [**Sitzung, die**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)keine Sitzung 0 (null) ist, ist ein privilegierter Vorgang. Aus diesem Grund muss für eine Anwendung, die in einer beliebigen Remotedesktop-Sitzungshost-Server Sitzung (RD-Sitzungshost) ausgeführt wird, " [SeCreateGlobalPrivilege](/windows/desktop/SecAuthZ/authorization-constants) " aktiviert sein, damit ein Datei Zuordnungs Objekt im globalen Namespace erfolgreich erstellt werden kann. Die Berechtigungsüberprüfung ist auf die Erstellung von Datei Zuordnungsobjekten beschränkt und gilt nicht für das Öffnen vorhandener Dateien. Wenn ein Dienst oder das System z. b. ein Datei Zuordnungsobjekt erstellt, kann jeder Prozess, der in einer beliebigen Sitzung ausgeführt wird, auf das Datei Zuordnungsobjekt zugreifen, sofern der Benutzer über die erforderlichen Zugriffsrechte verfügt.

 

 