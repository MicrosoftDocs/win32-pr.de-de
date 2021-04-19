---
description: WMI-C++-Klassen, die Teil des WMI-Anbieter-Frameworks sind, werden jetzt im Endzustand berücksichtigt.
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: Anbieter Framework-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1562d00e6b3b1563ece933ba7dd9361dd8a5d94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349459"
---
# <a name="provider-framework-classes"></a>Anbieter Framework-Klassen

\[WMI-C++ Klassen, die Teil des WMI-Anbieter-Frameworks sind, werden jetzt im Endzustand berücksichtigt, und für nicht sicherheitsrelevante Probleme, die diese Bibliotheken betreffen, stehen keine weiteren Entwicklungen, Verbesserungen oder Updates zur Verfügung. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Das Anbieter Framework implementiert die folgenden Klassen.



| Framework-Klasse                                | BESCHREIBUNG                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cframeworkquery**](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | Enthält Methoden für die Verarbeitung von Abfragen.                                                                                                                                                                              |
| [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)                 | Enthält Methoden zum Festlegen und Abrufen von Eigenschaften und ist eine Kapselung der [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Schnittstelle. Der Implementierer sollte nicht direkt auf die **IWbemClassObject** -Methoden zugreifen müssen. |
| [**Cthreadbase**](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | Eine Basisklasse, die die internen Thread Sicherheitsmechanismen für das WMI-Anbieter Framework bereitstellt.                                                                                                                    |
| [**Cwbemgluefactory**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | Teil des WMI-Anbieter-Frameworks. Das Anbieter Framework implementiert intern Methoden dieser Schnittstelle, um neue Instanzen von Klassen für den Anbieter zu erstellen.                                                     |
| [**Cwbemproviderglue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | Implementiert die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Methode und die-Methode, die das Laden und Entladen des frameworkanbieters steuern.                                                                             |
| [**Anbieter**](/windows/desktop/api/Provider/nl-provider-provider)                   | Enthält Hilfsfunktionen und stellt Standard Implementierungen der Methoden von [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)bereit.                                                                                            |



 

Beachten Sie, dass viele der frameworkmethoden [**chstring**](chstring.md) -Parameter verwenden. **Chstring** unterstützt viele der gleichen Methoden und Eigenschaften wie die Microsoft Foundation Classes (MFC), aber ohne den mehr Aufwand von MFC. Weitere Informationen zu " **chstring**" finden Sie unter " **chstring Class Reference**".

 

 
