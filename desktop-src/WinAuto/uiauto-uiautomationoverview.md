---
title: Übersicht über die Benutzeroberflächenautomatisierung
description: Microsoft Benutzeroberflächenautomatisierung ist ein Barrierefreiheitsframework für Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- Benutzeroberflächenautomatisierung, Informationen
- Benutzeroberflächenautomatisierung,Barrierefreiheit
- Benutzeroberflächenautomatisierung,Komponenten
- Benutzeroberflächenautomatisierung,Anbieter-API
- Benutzeroberflächenautomatisierung,Client-API
- Benutzeroberflächenautomatisierung,Headerdateien
- Benutzeroberflächenautomatisierung,Model
- components
- Barrierefreiheit
- Anbieter-API
- Client-API
- Headerdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3664866280d570f9fa5f07acc6245ca2b4c1bff7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470057"
---
# <a name="ui-automation-overview"></a>Übersicht über die Benutzeroberflächenautomatisierung

Microsoft Benutzeroberflächenautomatisierung ist ein Barrierefreiheitsframework für Windows. Sie bietet programmgesteuerten Zugriff auf die meisten Benutzeroberflächenelemente auf dem Desktop. Es ermöglicht Hilfstechnologieprodukten wie Sprachausgaben, Endbenutzern Informationen über die Benutzeroberfläche bereitzustellen und die Benutzeroberfläche mit anderen Mitteln als standardeingaben zu bearbeiten. Benutzeroberflächenautomatisierung ermöglicht auch die Interaktion automatisierter Testskripts mit der Benutzeroberfläche.

Benutzeroberflächenautomatisierung war erstmals in Windows XP als Teil der Microsoft .NET Framework verfügbar. Obwohl zu diesem Zeitpunkt auch eine nicht verwaltete C++-API veröffentlicht wurde, war die Nützlichkeit von Clientfunktionen aufgrund von Interoperabilitätsproblemen eingeschränkt. Für Windows 7 wurde die API im Component Object Model (COM) umgeschrieben.

> [!Note]  
> Obwohl die in der früheren Version von Benutzeroberflächenautomatisierung eingeführten Bibliotheksfunktionen noch dokumentiert sind, sollten sie nicht in neuen Anwendungen verwendet werden.

 

Benutzeroberflächenautomatisierung Clientanwendungen können mit der Zusicherung geschrieben werden, dass sie auf mehreren Microsoft Windows-Steuerungsframeworks funktionieren. Der Benutzeroberflächenautomatisierung Core maskiert alle Unterschiede in den Frameworks, die verschiedenen Teilen der Benutzeroberfläche zugrundeliegt. Beispielsweise werden die **Content-Eigenschaft** einer Windows Presentation Foundation-Schaltfläche (WPF), die **Caption-Eigenschaft** einer Microsoft Win32-Schaltfläche und die **ALT-Eigenschaft** eines HTML-Bilds einer einzelnen Eigenschaft **namens** in der Benutzeroberflächenautomatisierung-Ansicht zugeordnet.

Benutzeroberflächenautomatisierung bietet vollständige Funktionen in Windows Betriebssystemen XP, Windows Server 2003 und höher.

Benutzeroberflächenautomatisierung Anbieter sind Komponenten, die Benutzeroberflächenautomatisierung-Unterstützung für Steuerelemente implementieren und über einen integrierten Bridgingdienst Unterstützung für Microsoft Active Accessibility Clientanwendungen bieten.

> [!Note]  
> Benutzeroberflächenautomatisierung ermöglicht keine Kommunikation zwischen Prozessen, die von verschiedenen Benutzern über den Befehl **Ausführen als** gestartet werden.

 

Dieses Thema enthält folgende Abschnitte:

-   [Benutzeroberflächenautomatisierung-Komponenten](#ui-automation-components)
-   [Benutzeroberflächenautomatisierung Headerdateien](#ui-automation-header-files)
-   [Benutzeroberflächenautomatisierungs-Modell](#ui-automation-model)
-   [Zugehörige Themen](#related-topics)

## <a name="ui-automation-components"></a>Benutzeroberflächenautomatisierung-Komponenten

Benutzeroberflächenautomatisierung verfügt über vier Hauptkomponenten, wie in der folgenden Tabelle dargestellt.




| Komponente | BESCHREIBUNG | 
|-----------|-------------|
| Anbieter-API | Eine Reihe von COM-Schnittstellen, die von Benutzeroberflächenautomatisierung-Anbietern implementiert werden. Benutzeroberflächenautomatisierung-Anbieter sind Objekte, die Informationen zu Benutzeroberflächenelementen bereitstellen und auf programmgesteuerte Eingaben reagieren. | 
| Client-API | Eine Reihe von COM-Schnittstellen, mit denen Clientanwendungen Informationen über die Benutzeroberfläche abrufen und Eingaben an Steuerelemente senden können.<blockquote>[!Note]<br />Die in <a href="uiauto-entry-cpfunctions.md">Veraltete Steuerelementmusterfunktionen</a> und <a href="uiauto-entry-uianodefunctions.md">veraltete Knotenfunktionen beschriebenen</a> Funktionen sind veraltet. Stattdessen sollten Clientanwendungen die Benutzeroberflächenautomatisierung COM-Schnittstellen verwenden, die in <a href="uiauto-entry-uiautoclientinterfaces.md">Benutzeroberflächenautomatisierung Elementschnittstellen für Clients</a>beschrieben sind.</blockquote><br /> | 
| UIAutomationCore.dll | Die Laufzeitbibliothek, die manchmal als Benutzeroberflächenautomatisierung Core bezeichnet wird und die Kommunikation zwischen Anbietern und Clients übernimmt. | 
| Oleacc.dll | Die Laufzeitbibliothek für Microsoft Active Accessibility und die Proxyobjekte. Die Bibliothek stellt auch Proxyobjekte bereit, die vom Microsoft-Microsoft Active Accessibility zum Benutzeroberflächenautomatisierung Proxy zur Unterstützung von Win32-Steuerelementen verwendet werden. | 




 

Es gibt zwei Möglichkeiten, Benutzeroberflächenautomatisierung zu verwenden: zum Erstellen von Unterstützung für benutzerdefinierte Steuerelemente mithilfe der Anbieter-API und zum Erstellen von Clientanwendungen, die den Benutzeroberflächenautomatisierung Core verwenden, um mit Benutzeroberflächenelementen zu kommunizieren und Informationen darüber abzurufen. Abhängig von Ihren Schwerpunkten sollten Sie auf verschiedene Teile der Dokumentation zugreifen. Wenn Sie Unterstützung für benutzerdefinierte Steuerelemente erstellen müssen, lesen Sie [Benutzeroberflächenautomatisierung Anbieterprogrammiererhandbuch.](uiauto-providerportal.md) Wenn Sie mit Benutzeroberflächenelementen kommunizieren oder Informationen dazu abrufen müssen, lesen [Sie Benutzeroberflächenautomatisierung Clientprogrammiererhandbuch.](uiauto-clientportal.md)

## <a name="ui-automation-header-files"></a>Benutzeroberflächenautomatisierung Headerdateien

Die Benutzeroberflächenautomatisierung-API ist in mehreren verschiedenen C/C++-Headerdateien definiert, die im Windows Software Development Kit (SDK) enthalten sind. Die Benutzeroberflächenautomatisierung Headerdateien werden in der folgenden Tabelle beschrieben:



| Headerdatei           | BESCHREIBUNG                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UIAutomationClient.h  | Definiert die Schnittstellen und zugehörigen Programmierelemente, die von Benutzeroberflächenautomatisierung Clients verwendet werden.                                                                                                                                                                                           |
| UIAutomationCore.h    | Definiert die Schnittstellen und zugehörigen Programmierelemente, die von Benutzeroberflächenautomatisierung-Anbietern verwendet werden.                                                                                                                                                                                         |
| UIAutomationCoreApi.h | Definiert allgemeine Konstanten, GUIDs, Datentypen und Strukturen, die von Benutzeroberflächenautomatisierung Clients und Anbietern verwendet werden. Sie enthält auch Definitionen für die veralteten Knoten- und Steuerelementmusterfunktionen.                                                                                    |
| UIAutomation.h        | Schließt alle anderen Benutzeroberflächenautomatisierung Headerdateien ein. Da die meisten Benutzeroberflächenautomatisierung Anwendungen Elemente aus allen Benutzeroberflächenautomatisierung Headerdateien benötigen, ist es am besten, UIAutomation.h in Ihre Benutzeroberflächenautomatisierung Anwendungsprojekte einzuschließen, anstatt jede Datei einzeln einzuschließen. |



 

Wenn Sie eine Anwendung entwickeln, die die Benutzeroberflächenautomatisierung-API verwendet, sollten Sie UIAutomation.h in Ihr Projekt einschließen. Wenn Ihre Anwendung Microsoft Active Accessibility unterstützt, schließen Sie die Headerdatei Oleacc.h ein. Benutzeroberflächenautomatisierung Anwendungen, die GUIDs verwenden, ist auch die Headerdatei Initguid.h erforderlich. Bei Bedarf sollte "Initguid.h" vor UIAutomation.h eingefügt werden.

## <a name="ui-automation-model"></a>Benutzeroberflächenautomatisierungs-Modell

Benutzeroberflächenautomatisierung macht jedes Element der Benutzeroberfläche für Clientanwendungen als objekt verfügbar, das durch die [**IUIAutomationElement-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) dargestellt wird. Elemente sind in einer Baumstruktur, mit dem Desktop als Stammelement, enthalten. Clients können die „Rohdatenansicht“ der Struktur als „Steuerelementansicht“ oder „Inhaltsansicht“ filtern. Diese Standardansichten der Struktur können leicht [](inspect-objects.md) mithilfe der Inspect-Anwendung, die im Windows SDK enthalten ist, sichtbar sein. Anwendungen können auch benutzerdefinierte Ansichten erstellen.

Ein Benutzeroberflächenautomatisierung-Element macht Eigenschaften des Steuerelements oder ui-Elements verfügbar, das es darstellt. Eine dieser Eigenschaften ist der Steuerelementtyp, der die grundlegende Darstellung und Funktionalität des Steuerelements oder Ui-Elements als einzelne erkennbare Entität definiert, z. B. eine Schaltfläche oder ein Kontrollkästchen. Weitere Informationen zu Steuerelementtypen finden Sie unter [Benutzeroberflächenautomatisierung Control Types Overview](uiauto-controltypesoverview.md).

Darüber hinaus macht ein Benutzeroberflächenautomatisierung-Element ein oder mehrere Steuerelementmuster verfügbar. Ein Steuerelementmuster stellt eine Reihe von Eigenschaften bereit, die für einen bestimmten Steuerelementtyp spezifisch sind. Ein Steuerelementmuster macht auch Methoden verfügbar, mit denen Clientanwendungen weitere Informationen über das Element abrufen und dem Element Eingaben bereitstellen können. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

> [!Note]  
> Es gibt keine 1:1-Entsprechung zwischen Steuerelementtypen und Steuerelementmustern. Ein Steuerelementmuster kann von mehreren Steuerelementtypen unterstützt werden, und ein Steuerelement kann mehrere Steuerelementmuster unterstützen, von denen jedes einen anderen Aspekt des Verhaltens verfügbar macht. Ein Kombinationsfeld hat beispielsweise mindestens zwei Steuerelementmuster: eines mit der Fähigkeit zum Erweitern und Reduzieren und ein anderes, das den Auswahlmechanismus darstellt. Ein Steuerelement kann jedoch nur einen einzigen Steuerelementtyp aufweisen.

 

Benutzeroberflächenautomatisierung stellt Clientanwendungen über Ereignisse Informationen bereit. Im Gegensatz zu WinEvents basieren Benutzeroberflächenautomatisierung Ereignisse nicht auf einem Broadcastmechanismus. Benutzeroberflächenautomatisierung Clients registrieren sich für bestimmte Ereignisbenachrichtigungen und können anfordern, dass bestimmte Eigenschaften und Steuerelementmusterinformationen an ihre Ereignishandler übergeben werden. Darüber hinaus enthält ein Benutzeroberflächenautomatisierung -Ereignis einen Verweis auf das Element, das es ausgelöst hat. Anbieter können die Leistung verbessern, indem sie Ereignisse selektiv abhängig davon auslösen, ob Clients zuhören. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> </dl>

 

 





