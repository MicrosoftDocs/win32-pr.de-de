---
title: Qmgr-Schnittstellen
description: Verwenden Sie die folgenden qmgr-Schnittstellen (Queue Manager), um Dateien herunterzuladen und Aufträge in der Download Warteschlange zu überwachen
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cc571dcc5bbf182b3f715ee34bb6c3e94b5502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206301"
---
# <a name="qmgr-interfaces"></a>Qmgr-Schnittstellen

\[Queue Manager-Schnittstellen (qmgr) sind für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen eines Themas angegeben sind. In nachfolgenden Versionen wurde sie möglicherweise geändert oder entfernt. Verwenden Sie stattdessen die [Bits-Schnittstellen](bits-interfaces.md).\]

Verwenden Sie die folgenden qmgr-Schnittstellen (Queue Manager), um Dateien herunterzuladen und Aufträge in der Download Warteschlange zu überwachen



| Schnittstelle                                                                 | BESCHREIBUNG                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IBackgroundCopyCallback1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | Implementieren Sie, um Benachrichtigungen zu empfangen, wenn Ereignisse auftreten.<br/>                                                                                               |
| [**Ibackgroundcopygroup**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | Verwenden Sie, um die Gruppe zu verwalten. Fügen Sie z. b. der Gruppe einen Auftrag hinzu, legen Sie die Eigenschaften der Gruppe fest, und starten und starten Sie die Gruppe in der Download Warteschlange.<br/> |
| [**IBackgroundCopyJob1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | Verwenden Sie, um dem Auftrag Dateien hinzuzufügen und den Status des Auftrags abzurufen.<br/>                                                                                         |
| [**Ibackgroundcopyqmgr**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | Verwenden Sie, um eine neue Gruppe zu erstellen, eine vorhandene Gruppe abzurufen oder alle Gruppen in der Warteschlange aufzuzählen.<br/>                                                       |
| [**Ienumbackgroundcopygroups**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | Verwenden Sie, um eine Liste der Gruppen in der Download Warteschlange abzurufen.<br/>                                                                                            |
| [**IEnumBackgroundCopyJobs1**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | Verwenden Sie, um eine Liste der Aufträge in der Gruppe abzurufen.<br/>                                                                                                       |



 

 

 





