---
title: Informationen zum Neustart-Manager
description: Der Hauptgrund für die Softwareinstallation und Updates ist, dass ein Systemneustart erforderlich ist, da einige der zu aktualisierenden Dateien derzeit von einer ausgeführten Anwendung oder einem Dienst verwendet werden.
ms.assetid: 9a1166d7-a0e1-4948-9077-278c84afccac
keywords:
- Neustart-Manager Restart Mgr , Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98003ff4193ce26eb4ed2a3bdab60db8d58adf86698c6b9369a80b8043458579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010298"
---
# <a name="about-restart-manager"></a>Informationen zum Neustart-Manager

Der Hauptgrund für die Softwareinstallation und Updates ist, dass ein Systemneustart erforderlich ist, da einige der zu aktualisierenden Dateien derzeit von einer ausgeführten Anwendung oder einem Dienst verwendet werden. Der Neustart-Manager ermöglicht das Herunterfahren und Neustarten aller wichtigen Anwendungen und Dienste bis auf . Dadurch werden die verwendeten Dateien freigegeben, und Installationsvorgänge können abgeschlossen werden. Es kann auch die Anzahl von Systemneustarts beseitigen oder verringern, die zum Abschließen einer Installation oder eines Updates erforderlich sind.

Der Neustart-Manager beendet Anwendungen in der folgenden Reihenfolge, und nachdem die Anwendungen aktualisiert wurden, werden Anwendungen, die für den Neustart registriert wurden, in umgekehrter Reihenfolge neu gestartet.

1.  GUI-Anwendungen
2.  Konsolenanwendungen
3.  Windows-Dienste
4.  Windows-Explorer

Neustart-Manager fährt Anwendungen oder Dienste nur herunter, wenn der Aufrufer dazu berechtigt ist. Beachten Sie, dass das sitzungsübergreifende Herunterfahren nicht unterstützt wird.

Anwendungen, die den [Windows Installer](/windows/desktop/Msi/windows-installer-portal) Version 4.0 für die Installation und Wartung verwenden, verwenden automatisch den Neustart-Manager, um Systemneustarts zu reduzieren. Benutzerdefinierte Installationsprogramme können auch so entworfen werden, dass sie die Restart Manager-API aufrufen, um Anwendungen und Dienste herunterzufahren und neu zu starten. In Fällen, in denen ein Systemneustart unvermeidlich ist, können Installationsprogramme die Restart Manager-API verwenden, um Neustarts so zu planen, dass die Unterbrechung des Arbeitsablaufs des Benutzers minimiert wird.

Informationen zur Verwendung der Restart Manager-API während der Installation und updates finden Sie unter [Verwenden von Restart Manager.](using-restart-manager.md)

Kritische Systemdienste können vom Neustart-Manager nicht ohne Systemneustart beendet und neu gestartet werden. Weitere Informationen zum Identifizieren kritischer Systemdienste finden Sie unter [Wichtige Systemdienste.](critical-system-services.md)

Ihre Anwendungen und Dienste sollten darauf vorbereitet sein, vom Neustart-Manager heruntergefahren zu werden und Benutzerdaten und Zustandsinformationen zu speichern, die für einen sauberen Neustart erforderlich sind. Weitere Informationen zum Vorbereiten Ihrer Anwendungen und Dienste für die Arbeit mit dem Neustart-Manager finden Sie unter [Richtlinien für Anwendungen und Dienste.](guidelines-for-applications-and-services.md)

Referenzinformationen zu den Enumerationen, Strukturen und Funktionen der Restart Manager-API finden Sie im Abschnitt Restart Manager Reference (Referenz zum [Neustart-Manager).](restart-manager-reference.md)

 

 