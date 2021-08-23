---
title: Neustart-Manager-Funktionen
description: Die Restart Manager-API verwendet die in der folgenden Tabelle identifizierten Funktionen.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Restart Manager Restart Mgr , Referenz, Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d628fcd5c1f6488d69152340dd76ae59ac27ea93b2ca157179a052883a26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010198"
---
# <a name="restart-manager-functions"></a>Neustart-Manager-Funktionen

Die Restart Manager-API verwendet die in der folgenden Tabelle identifizierten Funktionen.



| Funktion                                           | BESCHREIBUNG                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | Ändert Aktionen zum Herunterfahren oder Neustarten.                                                                                                                                                        |
| [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | Startet eine neue Neustart-Manager-Sitzung.                                                                                                                                                        |
| [**RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | Verbindet den Prozess einer Anwendung mit einer vorhandenen Neustart-Manager-Sitzung.                                                                                                                  |
| [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | Beendet die Neustart-Manager-Sitzung.                                                                                                                                                            |
| [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | Registriert Ressourcen wie Dateinamen, Kurznamen von Diensten oder [**RM \_ UNIQUE \_ PROCESS-Strukturen**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) in einer Restart Manager-Sitzung.                                   |
| [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | Wird von Installationsprogrammen verwendet, um eine Liste aller Anwendungen, die von registrierten Ressourcen betroffen sind, und deren aktuellen Status zu erhalten.                                                                              |
| [**RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | Fragt den Status der Änderungen beim Herunterfahren und Neustarten ab, die bereits angewendet wurden.                                                                                                     |
| [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | Initiiert das Herunterfahren von Anwendungen und Diensten.                                                                                                                                        |
| [**RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | Entfernt änderungen am Herunterfahren und Neustarten, die bereits angewendet wurden.                                                                                                                   |
| [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | Startet Anwendungen und Dienste neu, die von der [**RmShutdown-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) heruntergefahren wurden und für den Neustart mit **RegisterApplicationRestart registriert wurden.** |
| [**RmCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | Bricht die aktuelle [**RmGetList-,**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) [**RmShutdown-**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)oder [**RmRestart-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) ab.                                                            |



 

 

 




