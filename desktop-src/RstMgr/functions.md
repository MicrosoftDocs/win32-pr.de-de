---
title: Neustart-Manager-Funktionen
description: Die Neustart-Manager-API verwendet die in der folgenden Tabelle identifizierten Funktionen.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Neustart-Manager Restart Mgr, Referenz, Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33187bff8522bfa347dc852f2cac157c2c3966a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855967"
---
# <a name="restart-manager-functions"></a>Neustart-Manager-Funktionen

Die Neustart-Manager-API verwendet die in der folgenden Tabelle identifizierten Funktionen.



| Funktion                                           | BESCHREIBUNG                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Rmaddfilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | Ändert das Herunterfahren oder Neustarten von Aktionen.                                                                                                                                                        |
| [**Rmstarzession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | Startet eine neue Neustart-Manager-Sitzung.                                                                                                                                                        |
| [**Rmjoinsession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | Fügt den Prozess einer Anwendung in eine vorhandene Restart Manager-Sitzung ein.                                                                                                                  |
| [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | Beendet die Neustart-Manager-Sitzung.                                                                                                                                                            |
| [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | Registriert Ressourcen, z. b. Dateinamen, Dienst Kurznamen [**oder \_ eindeutige \_ RM-Prozess**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) Strukturen, in einer Restart Manager-Sitzung.                                   |
| [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | Wird von Installationsprogrammen verwendet, um eine Liste aller von registrierten Ressourcen betroffenen Anwendungen und ihren aktuellen Status zu erhalten.                                                                              |
| [**Rmgetfilterlist**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | Fragt den Status des herunter Fahrens und Neustarts von Änderungen ab, die bereits angewendet wurden.                                                                                                     |
| [**Rmshutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | Initiiert das Herunterfahren von Anwendungen und Diensten.                                                                                                                                        |
| [**Rmremovefilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | Entfernt das Herunterfahren und Neustarten von Änderungen, die bereits angewendet wurden.                                                                                                                   |
| [**Rmrestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | Startet Anwendungen und Dienste, die durch die [**rmshutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) -Funktion heruntergefahren wurden und für den Neustart registriert wurden, mithilfe von **RegisterApplicationRestart** neu. |
| [**Rmcancelcurrenttask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | Bricht die aktuelle [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)-, [**rmshutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)-oder [**rmrestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) -Funktion ab.                                                            |



 

 

 




