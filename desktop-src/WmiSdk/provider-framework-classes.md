---
description: Erfahren Sie mehr über die WMI-C++-Klassen, die Teil des WMI-Anbieterframework sind und jetzt im enden Zustand betrachtet werden.
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: Anbieterframeworkklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf4ef94b25e51b7f012987552babd30a93e7792
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120445"
---
# <a name="provider-framework-classes"></a>Anbieterframeworkklassen

\[WMI-C++-Klassen, die Teil des WMI-Anbieterframework sind, werden jetzt als endgültig betrachtet, und es sind keine weiteren Entwicklungen, Erweiterungen oder Updates für nicht sich sicherheitsbezogene Probleme verfügbar, die sich auf diese Bibliotheken ausdrungen. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Das Anbieterframework implementiert die folgenden Klassen.



| Framework-Klasse                                | Beschreibung                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CFrameworkQuery**](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | Enthält Methoden für die Abfrageverarbeitung.                                                                                                                                                                              |
| [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)                 | Enthält Methoden zum Festlegen und Abrufen von Eigenschaften und ist eine Kapselung der [**IWbemClassObject-Schnittstelle.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) Implementer sollte nicht direkt auf **IWbemClassObject-Methoden** zugreifen müssen. |
| [**CThreadBase**](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | Eine Basisklasse, die die internen Threadsicherheitsmechanismen für das WMI-Anbieterframework bietet.                                                                                                                    |
| [**CWbemGlueFactory**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | Teil des WMI-Anbieterframework. Das Anbieterframework implementiert Methoden dieser Schnittstelle intern, um neue Instanzen von Klassen für den Anbieter zu erstellen.                                                     |
| [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | Implementiert [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) und -Methoden, die das Laden und Entladen des Frameworkanbieters steuern.                                                                             |
| [**Anbieter**](/windows/desktop/api/Provider/nl-provider-provider)                   | Enthält Hilfsfunktionen und stellt Standardimplementierungen der Methoden von [**IWbemServices zur Verfügung.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)                                                                                            |



 

Beachten Sie, dass viele framework-Methoden [**CHString-Parameter**](chstring.md) verwenden. **CHString** unterstützt viele der gleichen Methoden und Eigenschaften wie der Microsoft Foundation Classes (MFC), aber ohne den Mehraufwand von MFC. Weitere Informationen zu **CHString finden Sie unter** **CHString-Klassenreferenz.**

 

 
