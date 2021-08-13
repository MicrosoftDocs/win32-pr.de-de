---
title: QMGR-Schnittstellen
description: Verwenden Sie die folgenden Queue Manager-Schnittstellen (QMGR), um Dateien herunterzuladen und Aufträge in der Downloadwarteschlange zu überwachen.
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17bd3c27fad81416b916b52b055bc879b44f251113d43b6118e179b609762fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679994"
---
# <a name="qmgr-interfaces"></a>QMGR-Schnittstellen

\[Warteschlangen-Manager-Schnittstellen (QMGR) stehen für die Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt Anforderungen eines Themas angegeben sind. In nachfolgenden Versionen wurde sie möglicherweise geändert oder entfernt. Verwenden Sie stattdessen die [BITS-Schnittstellen](bits-interfaces.md).\]

Verwenden Sie die folgenden Queue Manager-Schnittstellen (QMGR), um Dateien herunterzuladen und Aufträge in der Downloadwarteschlange zu überwachen.



| Schnittstelle                                                                 | Beschreibung                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IBackgroundCopyCallback1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | Implementieren Sie , um Benachrichtigungen zu empfangen, wenn Ereignisse auftreten.<br/>                                                                                               |
| [**IBackgroundCopyGroup**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | Verwenden Sie , um die Gruppe zu verwalten. Fügen Sie beispielsweise der Gruppe einen Auftrag hinzu, legen Sie die Eigenschaften der Gruppe fest, und starten und beenden Sie die Gruppe in der Downloadwarteschlange.<br/> |
| [**IBackgroundCopyJob1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | Verwenden Sie , um dem Auftrag Dateien hinzuzufügen und den Status des Auftrags abzurufen.<br/>                                                                                         |
| [**IBackgroundCopyQMgr**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | Verwenden Sie , um eine neue Gruppe zu erstellen, eine vorhandene Gruppe abzurufen oder alle Gruppen in der Warteschlange aufzählen.<br/>                                                       |
| [**IEnumBackgroundCopyGroups**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | Verwenden Sie , um eine Liste der Gruppen in der Downloadwarteschlange abzurufen.<br/>                                                                                            |
| [**IEnumBackgroundCopyJobs1**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | Verwenden Sie , um eine Liste der Aufträge in der Gruppe abzurufen.<br/>                                                                                                       |



 

 

 





