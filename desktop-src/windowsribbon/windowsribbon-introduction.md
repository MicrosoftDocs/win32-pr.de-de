---
title: Einführung in das Windows-Menü Band Framework
description: Das Windows-Menü Band Framework ist ein Funktions Reiches Befehls Präsentationssystem, das eine moderne Alternative zu den geschichteten Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows-Anwendungen bietet.
ms.assetid: bc19d5eb-e3a4-4022-8051-512cb3a3e065
keywords:
- Windows-Menüband, Framework
- Menüband, Framework
- Windows-Menüband, Info
- Multifunktionsleiste, Info
- Windows-Menüband, Komponenten
- Multifunktionsleiste, Komponenten
- Windows-Menüband, Ansichten
- Menüband, Ansichten
- Windows-Multifunktionsleiste, Architektur
- Multifunktionsleiste, Architektur
- Windows-Menüband, APIs
- Multifunktionsleiste, APIs
- Windows-Menüband, Sicherheit
- Multifunktionsleiste, Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ac5c3acccf1c48a54f93b1752729067e63e4c6
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104562653"
---
# <a name="introducing-the-windows-ribbon-framework"></a>Einführung in das Windows-Menü Band Framework

Das Windows-Menü Band Framework ist ein Funktions Reiches Befehls Präsentationssystem, das eine moderne Alternative zu den geschichteten Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows-Anwendungen bietet.

-   [Ein neues Befehls Paradigma](#a-new-command-paradigm)
-   [Ansichten](#views)
    -   [Die Menü Band Ansicht](#the-ribbon-view)
    -   [Die contextpopup-Ansicht](#the-contextpopup-view)
-   [Menüband-Architektur](#ribbon-architecture)
    -   [Die Menüband-APIs](#the-ribbon-apis)
    -   [Sicherheit und Datenschutz](#security-and-privacy)
    -   [Barrierefreiheit und Lokalisierung](#accessibility-and-localization)
-   [Zusammenfassung](#conclusion)
-   [Zugehörige Themen](#related-topics)

## <a name="a-new-command-paradigm"></a>Ein neues Befehls Paradigma

Das Menüband-Framework ist eine Sammlung von Microsoft-Win32-APIs, die eine Reihe neuer Benutzeroberflächen Funktionen für Windows-Entwickler unterstützen.

Dieses umfangreiche, moderne UI-Befehls Framework bietet Folgendes:

-   Einfache Implementierung für neue Menüband-Framework-Anwendungen und einfache Migration vorhandener Win32-Anwendungen.
-   Konsistente Darstellung und Verhalten von Multifunktionsleisten-Anwendungen.
-   Einhaltung von Windows-Benutzeroberflächen-Richtlinien für eine erstklassige Windows-Oberfläche durch Barrierefreiheits Standards, visuelle Stil Unterstützung (Themen Unterstützung), automatische hohe Kontrast Anpassungen und dpi-Informationen (High dots per inch).

Das Menüband-Framework besteht aus zwei Hauptkomponenten der Benutzeroberfläche:

-   Die Menüband-Befehlsleiste, die sich aus der Symbolleiste für den schnell Zugriff (QAT) zusammensetzt, die verschiedene vom Benutzer oder der Anwendung angegebene Menü Band Befehle verfügbar macht und hervorhebt, sowie eine Registerkarten Zeile, die das Anwendungsmenü, Standard-oder Kontext Registerkarten und eine Schaltfläche "Hilfe" enthält.
-   Ein umfangreiches Kontextmenü System.

Eine Kombination von deklarativem XML und systemeigenen COM-Schnittstellen wird verwendet, um die Darstellung und Funktionalität dieser Komponenten zu entkoppeln.

## <a name="views"></a>Sichten

Die primären Komponenten der Benutzeroberfläche des Menüband-Frameworks, die Menüband-Befehlsleiste und das Kontextmenü System werden strukturell durch *Ansichten* unterschieden. Das Framework unterstützt zwei Ansichten: die Menü [**Band**](windowsribbon-element-ribbon.md) Ansicht und die [**contextpopup**](windowsribbon-element-contextpopup.md) -Ansicht.

### <a name="the-ribbon-view"></a>Die Menü Band Ansicht

Die Benutzer [**Oberfläche der multifunktionsleistenansicht ist**](windowsribbon-element-ribbon.md) die primäre Funktion des Menüband-Frameworks und bietet die nächste Generation der Benutzeroberfläche für die Darstellung von Befehlen in Windows-Anwendungen.

Das Menüband ist eine Befehlsleiste, die die Hauptfunktionen einer Anwendung über eine Reihe von Registerkarten am oberen Rand eines Anwendungsfensters verfügbar macht. Die Funktionalität und Darstellung der Benutzeroberfläche von Microsoft Office 2007 ist ähnlich. Das Menüband bietet einen intuitiven gegen Punkt für den Test-und fehlerprozess der Befehls Ermittlung, der typisch für standardmäßige Windows-Menüsysteme ist. Das Menüband ist für Effizienz und Erkennbarkeit optimiert und ermöglicht das suchen, verstehen und Verwenden von Befehlen mit minimalen Mausklicks und Tastatureingaben durch ein System von Standard Steuerelementen, Galerien und der Live Vorschau.

Die folgende Abbildung veranschaulicht die Implementierung des Menüband-Frameworks in Paint für Windows 7.

![Screenshot mit der Multifunktionsleisten-Implementierung in Paint for Windows 7.](images/overviews/screenshot-paint-win7transparency-mirror.png)

### <a name="the-contextpopup-view"></a>Die contextpopup-Ansicht

Die [**contextpopup**](windowsribbon-element-contextpopup.md) -Ansicht, über das [Kontext-Popup](windowsribbon-controls-contextpopup.md) Steuerelement, bietet ein umfangreicheres Kontextmenü System als in früheren Windows-Anwendungen verfügbar ist. Ein Kontext-Popup kann nur zur Unterstützung einer Multifunktionsleiste bereitgestellt werden, ein eigenständiges Kontext-Popup wird vom Menüband-Framework nicht unterstützt.

## <a name="ribbon-architecture"></a>Menüband-Architektur

Im Gegensatz zum herkömmlichen Steuerelement basierten Entwicklungsmodell der Windows-Benutzeroberfläche basiert die Benutzeroberflächen Entwicklung für Windows-Menüband-Framework auf dem abstrakteren Konzept von Befehlen. Wenn Sie sich auf die Befehle konzentrieren, die Steuerelementen zugeordnet sind, und nicht auf die Steuerelemente selbst, kann das Framework die Benutzeroberfläche nach Bedarf automatisch anpassen, und zwar als Reaktion auf den Ausführungs Zustand des Befehls, der von der Ribbon-Host Anwendung abgerufen wurde.

Eine Anwendung, die das Multifunktionsleisten-Framework verwendet, macht Befehle verfügbar, ohne dass Sie mit den Details der Darstellung des Befehls in der Benutzeroberfläche belastet werden. Dies wird mitunter als Intent-basiertes UI-Modell bezeichnet. Der [**Befehlstyp**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype), seine Eigenschaften und seine Ressourcen definieren die Absicht des Befehls für die Anwendung. Wenn z. b. Maus Eingaben, Tastatureingaben oder sogar das Schütteln eines gyroskopischen Geräts zur Ausführung desselben Befehls führen, kann die Anwendung nur den Befehl ausführen, nicht aber die Art und Weise, wie Sie aufgerufen wurde.

Das Menüband-Framework bietet diese Flexibilität, indem es die Funktionalität von der Präsentation mit zwei unterschiedlichen Entwicklungsstrukturen trennt: eine Extensible Application Markup Language (XAML)-basierte Markup Sprache zum Deklarieren von Steuerelementen und das visuelle Layout einer multifunktionsleistenimplementierung und C++ COM-basierte Schnittstellen, um das Framework zu initialisieren und Ereignisse zur Laufzeit zu behandeln. Dieser Unterschied ermöglicht Entwicklern und Designern von Benutzeroberflächen die alleinige Verantwortung für das Aussehen einer Multifunktionsleistenanwendung, während die Kernfunktionalität die Domäne der Softwareentwickler ist.

Weitere Informationen finden Sie Untergrund Legendes zu [Befehlen und Steuerelementen](windowsribbon-commandscontrols.md).

### <a name="the-ribbon-apis"></a>Die Menüband-APIs

Die Menüband-APIs stellen die erforderlichen Verbindungen zwischen einer Ansicht und der Menüband-Host Anwendung bereit. Diese APIs bestehen aus den folgenden Schnittstellen und Eigenschafts Schlüsseln:

-   Eine Reihe von COM-Schnittstellen, die vom Multifunktionsleisten-Framework zum Ausführen von UI-Diensten implementiert werden

    

    | Schnittstelle                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
    |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [Iuicontextualui * * * *](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)           | Definiert die Methoden für die Kernfunktionalität der [**contextpopup**](windowsribbon-element-contextpopup.md) -Ansicht.                                                                                                                                                                                                                                                                                                                                                                                                                  |
    | [Iuiframework * * * *](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                 | Definiert die Methoden, die die Kernfunktionen der [**Multifunktionsleiste**](windowsribbon-element-ribbon.md) und der [**contextpopup**](windowsribbon-element-contextpopup.md) -Ansichten unterstützen.                                                                                                                                                                                                                                                                                                                                                     |
    | [Iuiribbon * * * *](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                       | Definiert die Methoden zum Angeben von Einstellungen und Eigenschaften für eine Menü [**Band**](windowsribbon-element-ribbon.md) Ansicht.                                                                                                                                                                                                                                                                                                                                                                                                                   |
    | [Iuisimplepropertyset * * * *](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) | Definiert eine Methode zum Abrufen des Werts, der durch einen Eigenschafts Schlüssel identifiziert wird. Diese Schnittstelle wird durch das Menüband-Framework implementiert und wird auch von der Host Anwendung für jedes Element im [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt eines Element Katalogs implementiert.<br/> Wenn Sie von der Host Anwendung implementiert wird, wird die durch diese Schnittstelle definierte Methode verwendet, um einen Eigenschafts Schlüsselwert für das ausgewählte Element in der [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)abzurufen.<br/> |
    | [Iuicollection * * * *](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)               | Definiert die Methoden für das dynamische manipulieren von Auflistungs basierten Steuerelementen, z. b. dem Menü Band-QAT und Sammlungs basierten [Katalogen, zur](ribbon-controls-galleries.md)Laufzeit.                                                                                                                                                                                                                                                                                                                                                        |
    | [Iuiimage * * * *](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                         | Definiert die Methode zum Abrufen eines Bilds für die Anzeige auf der Menüband-Benutzeroberfläche.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
    | [Iuiimagefrombitmap * * * *](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)     | Definiert die Factorymethode zum Erstellen eines [**iuiimage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) -Objekts.                                                                                                                                                                                                                                                                                                                                                                                                                                 |

    

     

-   Ein Satz von COM-Schnittstellen, die von der Menüband-Host Anwendung implementiert werden, die das Framework als Reaktion auf Änderungen der Benutzeroberfläche

    

    | Schnittstelle                                                                                  | BESCHREIBUNG                                                                                                  |
    |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
    | [Iuiapplication * * * *](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | Definiert die Einstiegspunkt Methoden für den Anwendungs Rückruf für das Menü Band Framework.                               |
    | [Iuicommandhandler * * * *](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | Definiert die Methoden zum Erfassen von Befehls Informationen und zum Behandeln von Befehls Ereignissen aus dem Menüband-Framework. |
    | [Iuicollectionchangede Vent * * * *](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | Definiert die Methode, die zum Verarbeiten von Änderungen an einer Auflistung zur Laufzeit erforderlich ist.                                   |

    

     

-   Ein Satz von Eigenschafts Schlüsseln, die definieren, welche Benutzeroberflächen Eigenschaften die Anwendung Programm gesteuert Steuern soll.

    

    | Eigenschafts Schlüsseltyp                                                  | BESCHREIBUNG                                              |
    |--------------------------------------------------------------------|----------------------------------------------------------|
    | [Sammlung](windowsribbon-reference-properties-collection.md)    | Definiert Eigenschaften für auf der Multifunktionsleiste Auflistungs basierte Steuerelemente. |
    | [Farbauswahl](windowsribbon-reference-properties-colorpicker.md) | Definiert Eigenschaften für Steuerelemente der Menüband-Farbauswahl.     |
    | [Schriftart](windowsribbon-reference-properties-fontcontrol.md)         | Definiert Eigenschaften für das Menüband FontControl.           |
    | [Global](windowsribbon-reference-properties-framework.md)         | Definiert globale Eigenschaften für das Menüband-Framework.      |
    | [Ressource](windowsribbon-reference-properties-resource.md)        | Definiert Menü Band Ressourcen Eigenschaften.                      |
    | [Menüband](windowsribbon-reference-properties-ribbon.md)            | Definiert Menü Band Ansichts Eigenschaften.                          |
    | [State](windowsribbon-reference-properties-state.md)              | Definiert Eigenschaften für den Zustand oder Kontext des Menüband-Steuer Elements.  |

    

     

### <a name="security-and-privacy"></a>Sicherheit und Datenschutz

Die Multifunktionsleisten-Framework-dll (uiribbon.dll) wird innerhalb des Prozesses ausgeführt und verfügt über dieselben Berechtigungen wie die Host Anwendung. Das Menüband akzeptiert nur das, was die Host Anwendung als Eingabe oder Benutzereingabe von streng eingeschränkten Steuerelementen bereitstellt, z. b. das Drehfeld Spinner und bearbeitbar.

Außerdem speichert das Framework keine Informationen, mit Ausnahme der von der Host Anwendung bereitgestellten oder vom Endbenutzer autorisierten Benutzer über das Windows-Programm zur Kundenfreundlichkeit.

### <a name="accessibility-and-localization"></a>Barrierefreiheit und Lokalisierung

Zum Bereitstellen einer Benutzeroberfläche mit hoher Verfügbarkeit implementiert das Menüband-Framework Microsoft-Active Accessibility. Durch Automatisches Auffüllen der relevanten Eigenschaften von Microsoft Active Accessibility mit gültigen und nützlichen Informationen verringert das Framework die Belastung der Entwickler erheblich, um für alle Benutzer ein inklusives Verhalten bereitzustellen.

Weitere Informationen zur Barrierefreiheit im Menüband-Framework finden Sie unter [Arbeiten mit Active Accessibility in der Benutzeroberfläche von 2007 Office-fließend](/previous-versions/office/developer/office-2007/bb404170(v=office.12)).

Außerdem ist das Menüband-Framework ein Windows-Feature und wird daher für alle Sprachen lokalisiert, die von Windows unterstützt werden. Entwickler sind jedoch für die Lokalisierung Ihrer eigenen spezifischen Anwendungs Ressourcen verantwortlich.

## <a name="conclusion"></a>Zusammenfassung

Das Menüband ist eine neue und ansprechende Form der Befehls Darstellung, die Anwendungsentwickler, Architekten und Designer beim Entwerfen und Erstellen neuer Anwendungen oder beim Aktualisieren vorhandener Anwendungen berücksichtigen sollten.

Das [Windows-Menüband-Entwicklungs Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) steht zur Erörterung von Themen und zum stellen von Fragen im Zusammenhang mit der Entwicklung von Anwendungen zur Verfügung, die das Windows

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup](windowsribbon-schema.md)
</dt> <dt>

[Multifunktionsleisten-Benutzeroberflächen Richtlinien](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Menüband-Entwurfsprozess](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

