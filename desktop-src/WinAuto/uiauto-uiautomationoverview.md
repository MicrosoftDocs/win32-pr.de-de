---
title: Übersicht über die Benutzeroberflächenautomatisierung
description: Die Microsoft-Benutzeroberflächen Automatisierung ist ein Barrierefreiheits Framework für Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- Benutzeroberflächen Automatisierung, Informationen zu
- Benutzeroberflächen Automatisierung, Barrierefreiheit
- Benutzeroberflächen Automatisierung, Komponenten
- UI-Automatisierung, Anbieter-API
- Benutzeroberflächen Automatisierung, Client-API
- Benutzeroberflächen Automatisierung, Header Dateien
- UI-Automatisierung, Modell
- components
- Barrierefreiheit
- Anbieter-API
- Client-API
- Headerdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ea29b0abd4c6ed791ae3195f36a0f8184c8596
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389815"
---
# <a name="ui-automation-overview"></a>Übersicht über die Benutzeroberflächenautomatisierung

Die Microsoft-Benutzeroberflächen Automatisierung ist ein Barrierefreiheits Framework für Windows. Sie ermöglicht programmgesteuerten Zugriff auf die meisten Elemente der Benutzeroberfläche auf dem Desktop. Sie ermöglicht Hilfstechnologieprodukten, wie z. b. Bildschirm Sprachausgaben, Informationen zur Benutzeroberfläche für Endbenutzer bereitzustellen und die Benutzeroberfläche auf andere Weise als Standard Eingaben zu bearbeiten. Die Benutzeroberflächen Automatisierung ermöglicht außerdem die Interaktion von automatisierten Test Skripts mit der Benutzeroberfläche.

Die Benutzeroberflächen Automatisierung war erstmals in Windows XP als Teil des Microsoft .NET Frameworks verfügbar. Obwohl eine nicht verwaltete C++-API zu diesem Zeitpunkt ebenfalls veröffentlicht wurde, war die Nützlichkeit von Client Funktionen aufgrund von Interoperabilitätsproblemen eingeschränkt. Für Windows 7 wurde die API im Component Object Model (com) umgeschrieben.

> [!Note]  
> Obwohl die in der früheren Version der Benutzeroberflächen Automatisierung eingeführten Bibliotheksfunktionen weiterhin dokumentiert sind, sollten Sie in neuen Anwendungen nicht verwendet werden.

 

Benutzeroberflächenautomatisierungs-Client Anwendungen können mit der Gewissheit geschrieben werden, dass Sie an mehreren Microsoft Windows-Steuerelement-Frameworks funktionieren. Der Benutzeroberflächenautomatisierungs-Kern maskiert alle Unterschiede in den Frameworks, die verschiedene Teile der Benutzeroberfläche unterliegen. Beispielsweise werden die **Content** -Eigenschaft einer Windows Presentation Foundation (WPF)-Schaltfläche, die **Caption** -Eigenschaft einer Microsoft Win32-Schaltfläche und die **alt** -Eigenschaft eines HTML-Bilds alle einer einzelnen Eigenschaft ( **Name**) in der Benutzeroberflächenautomatisierungs-Ansicht zugeordnet.

Die Benutzeroberflächen Automatisierung bietet vollständige Funktionalität in den Betriebssystemen Windows XP, Windows Server 2003 und höher.

Benutzeroberflächenautomatisierungs-Anbieter sind Komponenten, die die Benutzeroberflächenautomatisierungs-Unterstützung für Steuerelemente implementieren und einige Unterstützung für Microsoft Active Accessibility-Client Anwendungen über einen integrierten Überbrückungs Dienst bieten.

> [!Note]  
> Die Benutzeroberflächen Automatisierung ermöglicht keine Kommunikation zwischen Prozessen, die von verschiedenen Benutzern durch den Befehl **Ausführen als** gestartet werden.

 

Dieses Thema enthält folgende Abschnitte:

-   [UI-Automatisierungskomponenten](#ui-automation-components)
-   [Benutzeroberflächenautomatisierungs-Header Dateien](#ui-automation-header-files)
-   [Benutzeroberflächenautomatisierungs-Modell](#ui-automation-model)
-   [Zugehörige Themen](#related-topics)

## <a name="ui-automation-components"></a>UI-Automatisierungskomponenten

Die Benutzeroberflächen Automatisierung verfügt über vier Hauptkomponenten, wie in der folgenden Tabelle gezeigt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Komponente</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Anbieter-API</td>
<td>Ein Satz von COM-Schnittstellen, die von Benutzeroberflächenautomatisierungs-Anbietern implementiert werden. Benutzeroberflächenautomatisierungs-Anbieter sind Objekte, die Informationen über Benutzeroberflächen Elemente bereitstellen und auf programmgesteuerte Eingaben reagieren.</td>
</tr>
<tr class="even">
<td>Client-API</td>
<td>Ein Satz von COM-Schnittstellen, mit denen Client Anwendungen Informationen über die Benutzeroberfläche abrufen und Eingaben an Steuerelemente senden können.
<blockquote>
[!Note]<br />
Die Funktionen, die in <a href="uiauto-entry-cpfunctions.md">veralteten Steuerelement Mustern</a> und Funktionen für <a href="uiauto-entry-uianodefunctions.md">Veraltete Knoten</a> beschrieben werden, sind veraltet. Stattdessen sollten Client Anwendungen die in Benutzeroberflächenautomatisierungs- <a href="uiauto-entry-uiautoclientinterfaces.md">Element Schnittstellen für Clients</a>beschriebenen Benutzeroberflächenautomatisierungs-com-Schnittstellen verwenden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>UIAutomationCore.dll</td>
<td>Die Lauf Zeit Bibliothek, die manchmal als Benutzeroberflächenautomatisierungs-Kern bezeichnet wird und die Kommunikation zwischen Anbietern und Clients behandelt.</td>
</tr>
<tr class="even">
<td>Oleacc.dll</td>
<td>Die Lauf Zeit Bibliothek für Microsoft Active Accessibility und die Proxy Objekte. Die Bibliothek stellt auch Proxy Objekte bereit, die vom Microsoft Microsoft Active Accessibility dem Benutzeroberflächenautomatisierungs-Proxy zur Unterstützung von Win32-Steuerelementen verwendet</td>
</tr>
</tbody>
</table>



 

Es gibt zwei Möglichkeiten zum Verwenden der Benutzeroberflächen Automatisierung: zum Erstellen von Unterstützung für benutzerdefinierte Steuerelemente mithilfe der Anbieter-API und zum Erstellen von Client Anwendungen, die den Benutzeroberflächenautomatisierungs-Kern zum kommunizieren mit und zum Abrufen von Informationen zu Benutzeroberflächen Elementen verwenden. Abhängig von Ihren Schwerpunkten sollten Sie auf verschiedene Teile der Dokumentation zugreifen. Wenn Sie Unterstützung für benutzerdefinierte Steuerelemente erstellen müssen, finden Sie weitere Informationen unter [Benutzeroberflächenautomatisierungs-Anbieter Handbuch](uiauto-providerportal.md). Informationen zu den Benutzeroberflächen Elementen finden Sie unter [Benutzeroberflächenautomatisierungs-Client Programmiererhandbuch](uiauto-clientportal.md).

## <a name="ui-automation-header-files"></a>Benutzeroberflächenautomatisierungs-Header Dateien

Die Benutzeroberflächenautomatisierungs-API ist in verschiedenen C/C++-Header Dateien definiert, die im Windows Software Development Kit (SDK) enthalten sind. Die Header Dateien für die Benutzeroberflächen Automatisierung werden in der folgenden Tabelle beschrieben:



| Headerdatei           | BESCHREIBUNG                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UIAutomationClient. h  | Definiert die von Benutzeroberflächenautomatisierungs-Clients verwendeten Schnittstellen und zugehörigen Programmier Elemente.                                                                                                                                                                                           |
| Uiautomationcore. h    | Definiert die Schnittstellen und zugehörigen Programmier Elemente, die von Benutzeroberflächenautomatisierungs-Anbietern verwendet werden                                                                                                                                                                                         |
| Uiautomationcoreapi. h | Definiert allgemeine Konstanten, GUIDs, Datentypen und Strukturen, die von Benutzeroberflächenautomatisierungs-Clients und-Anbietern verwendet werden. Sie enthält auch Definitionen für die veralteten Knoten-und Steuerelement Muster Funktionen.                                                                                    |
| Uiautomation. h        | Schließt alle anderen Header Dateien der Benutzeroberflächen Automatisierung ein. Da die meisten Benutzeroberflächenautomatisierungs-Anwendungen Elemente aus allen Header Dateien für die Benutzeroberflächen Automatisierung benötigen, empfiehlt es sich, "uiautomation. h" in Ihre Benutzeroberflächenautomatisierungs-Anwendungsprojekte einzubeziehen, anstatt jede Datei einzeln zu |



 

Wenn Sie eine Anwendung entwickeln, die die Benutzeroberflächenautomatisierungs-API verwendet, sollten Sie "uiautomation. h" in Ihr Projekt einschließen. Wenn Ihre Anwendung Microsoft Active Accessibility unterstützt, schließen Sie die Header Datei "Oleacc. h" ein. Benutzeroberflächenautomatisierungs-Anwendungen, die GUIDs verwenden, benötigen auch die Header Datei "Initguid. h". Bei Bedarf sollte Initguid. h vor "uiautomation. h" eingeschlossen werden.

## <a name="ui-automation-model"></a>Benutzeroberflächenautomatisierungs-Modell

Die Benutzeroberflächen Automatisierung macht alle Elemente der Benutzeroberfläche für Client Anwendungen als Objekt verfügbar, das von der [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle dargestellt wird. Elemente sind in einer Baumstruktur, mit dem Desktop als Stammelement, enthalten. Clients können die „Rohdatenansicht“ der Struktur als „Steuerelementansicht“ oder „Inhaltsansicht“ filtern. Diese Standard Sichten der Struktur können problemlos mithilfe der in der Windows SDK enthaltenen Anwendung "über [prüfen](inspect-objects.md) " angezeigt werden. Anwendungen können auch benutzerdefinierte Ansichten erstellen.

Ein Benutzeroberflächenautomatisierungs-Element macht Eigenschaften des Steuer Elements oder des Benutzeroberflächen Elements verfügbar, das es darstellt. Eine dieser Eigenschaften ist der Steuer Elementtyp, der die grundlegende Darstellung und die Funktionalität des Steuer Elements oder des Benutzeroberflächen Elements als einzelne erkennbare Entität definiert, z. b. eine Schaltfläche oder ein Kontrollkästchen. Weitere Informationen zu Steuerelement Typen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

Außerdem stellt ein Benutzeroberflächenautomatisierungs-Element ein oder mehrere Steuerelement Muster zur Verfügung. Ein-Steuerelement Muster stellt einen Satz von Eigenschaften bereit, die für einen bestimmten Steuerelement Typen spezifisch sind. Ein Steuerelement Muster macht auch Methoden verfügbar, mit denen Client Anwendungen Weitere Informationen über das Element erhalten und Eingaben für das Element bereitstellen können. Weitere Informationen zu Steuerelementmustern finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

> [!Note]  
> Es gibt keine eins-zu-eins-Entsprechung zwischen Steuerelement Typen und Steuerelement Mustern. Ein Steuerelementmuster kann von mehreren Steuerelementtypen unterstützt werden, und ein Steuerelement kann mehrere Steuerelementmuster unterstützen, von denen jedes einen anderen Aspekt des Verhaltens verfügbar macht. Ein Kombinationsfeld hat beispielsweise mindestens zwei Steuerelementmuster: eines mit der Fähigkeit zum Erweitern und Reduzieren und ein anderes, das den Auswahlmechanismus darstellt. Ein Steuerelement kann jedoch nur einen einzigen Steuerelement Typen aufweisen.

 

Die Benutzeroberflächen Automatisierung stellt mithilfe von Ereignissen Informationen für Client Anwendungen bereit. Im Gegensatz zu WinEvents basieren Benutzeroberflächenautomatisierungs-Ereignisse nicht auf einem Übertragungsmechanismus. Benutzeroberflächenautomatisierungs-Clients registrieren sich für bestimmte Ereignis Benachrichtigungen und können anfordern, dass bestimmte Eigenschaften und Steuerelement Muster Informationen an Ihre Ereignishandler übermittelt werden. Außerdem enthält ein Benutzeroberflächenautomatisierungs-Ereignis einen Verweis auf das Element, das es ausgelöst hat. Anbieter können die Leistung verbessern, indem sie Ereignisse selektiv abhängig davon auslösen, ob Clients zuhören. Weitere Informationen zu Ereignissen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> </dl>

 

 





