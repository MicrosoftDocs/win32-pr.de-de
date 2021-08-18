---
description: Erfahren Sie mehr über die WMI-C++-Klassen, die Teil des WMI-Anbieterframeworks sind und jetzt im endgültigen Zustand betrachtet werden.
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: Anbieterframeworkklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba5f8ec85eca2ea2413e176b104865c84ddc5de39aa9fd137b015d07c3e0592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130992"
---
# <a name="provider-framework-classes"></a>Anbieterframeworkklassen

\[WMI-C++-Klassen, die Teil des WMI-Anbieterframeworks sind, werden jetzt als endgültig betrachtet, und es sind keine weiteren Entwicklungen, Verbesserungen oder Updates für nicht sicherheitsrelevante Probleme verfügbar, die sich auf diese Bibliotheken auswirken. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle Neuentwicklungen verwendet werden.\]

Das Anbieterframework implementiert die folgenden Klassen.



| Framework-Klasse                                | Beschreibung                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CFrameworkQuery**](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | Enthält Methoden für die Abfrageverarbeitung.                                                                                                                                                                              |
| [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)                 | Enthält Methoden zum Festlegen und Abrufen von Eigenschaften und ist eine Kapselung der [**IWbemClassObject-Schnittstelle.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) Implementierer sollten nicht direkt auf **IWbemClassObject-Methoden** zugreifen müssen. |
| [**CThreadBase**](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | Eine Basisklasse, die die internen Threadsicherheitsmechanismen für das WMI-Anbieterframework zur Verfügung stellt.                                                                                                                    |
| [**CWbemGlueFactory**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | Teil des WMI-Anbieterframeworks. Das Anbieterframework implementiert intern Methoden dieser Schnittstelle, um neue Instanzen von Klassen für den Anbieter zu erstellen.                                                     |
| [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | Implementiert [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) und Methoden, die das Laden und Entladen des Frameworkanbieters steuern.                                                                             |
| [**Anbieter**](/windows/desktop/api/Provider/nl-provider-provider)                   | Enthält Hilfsfunktionen und stellt Standardimplementierungen der Methoden von [**IWbemServices bereit.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)                                                                                            |



 

Beachten Sie, dass viele der Frameworkmethoden [**CHString-Parameter**](chstring.md) verwenden. **CHString** unterstützt viele der gleichen Methoden und Eigenschaften wie die Microsoft Foundation Classes (MFC), jedoch ohne den Mehraufwand von MFC. Weitere Informationen zu **CHString** finden Sie unter **CHString-Klassenreferenz.**

 

 
