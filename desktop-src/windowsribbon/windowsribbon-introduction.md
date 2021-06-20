---
title: Einführung in das Windows-Menübandframework
description: Zeigen Sie die Landing Page für das Windows-Menübandframework an, das eine Alternative zu den mehrstufigen Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows-Anwendungen darstellt.
ms.assetid: bc19d5eb-e3a4-4022-8051-512cb3a3e065
keywords:
- Windows-Menüband, Framework
- Menüband, Framework
- Windows-Menüband, Informationen
- Menüband, Informationen
- Windows-Menüband, Komponenten
- Menüband, Komponenten
- Windows-Menüband, Ansichten
- Menüband, Ansichten
- Windows-Menüband, Architektur
- Menüband, Architektur
- Windows-Menüband, APIs
- Menüband, APIs
- Windows-Menüband, Sicherheit
- Menüband, Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db15165b91708a85e5ae6237b66a15bf733e80a7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404393"
---
# <a name="introducing-the-windows-ribbon-framework"></a>Einführung in das Windows-Menübandframework

Das Windows-Menübandframework ist ein umfangreiches Befehlspräsentationssystem, das eine moderne Alternative zu den mehrstufigen Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows-Anwendungen bietet.

-   [Ein neues Befehlsparadigma](#a-new-command-paradigm)
-   [Ansichten](#views)
    -   [Menübandansicht](#the-ribbon-view)
    -   [Die ContextPopup-Ansicht](#the-contextpopup-view)
-   [Menübandarchitektur](#ribbon-architecture)
    -   [Menüband-APIs](#the-ribbon-apis)
    -   [Sicherheit und Datenschutz](#security-and-privacy)
    -   [Barrierefreiheit und Lokalisierung](#accessibility-and-localization)
-   [Zusammenfassung](#conclusion)
-   [Verwandte Themen](#related-topics)

## <a name="a-new-command-paradigm"></a>Ein neues Befehlsparadigma

Das Menübandframework ist eine Sammlung von Microsoft Win32-APIs, die eine Vielzahl neuer Benutzeroberflächenfunktionen für Windows-Entwickler unterstützen.

Dieses umfangreiche, moderne Ui-Befehlsframework bietet:

-   Einfache Implementierung für ganz neue Menübandframeworkanwendungen und einfache Migration vorhandener Win32-Anwendungen.
-   Konsistente Darstellung und einheitliches Verhalten für Menübandanwendungen.
-   Einhaltung der Windows-Ui-Richtlinien für eine erstklassige Windows-Erfahrung durch Barrierefreiheitsstandards, Unterstützung des visuellen Stils (Design), automatische Anpassungen des hohen Kontrasts und Berücksichtigung hoher Punkte pro Zoll (dpi).

Das Menübandframework besteht aus zwei Hauptkomponenten der Benutzeroberfläche:

-   Die Menübandbefehlsleiste, die aus der Schnellzugriffssymbolleiste (Quick Access Toolbar, QAT) besteht, die verschiedene Menübandbefehle wie vom Benutzer oder der Anwendung angegeben verfügbar macht und hervorhebt, sowie eine Registerkartenzeile, die das Anwendungsmenü, standard- oder kontextbezogene Registerkarten sowie eine Hilfeschaltfläche enthält.
-   Ein umfangreiches Kontextmenüsystem.

Eine Kombination aus deklarativem XML und nativen COM-Schnittstellen wird verwendet, um die Darstellung und Funktionalität dieser Komponenten zu entkoppeln.

## <a name="views"></a>Sichten

Die primären Benutzeroberflächenkomponenten des Menübandframeworks, die Menübandbefehlsleiste und das Kontextmenüsystem, werden strukturell durch *Ansichten* unterschieden. Das Framework unterstützt zwei Ansichten: die [**Menübandansicht**](windowsribbon-element-ribbon.md) und die [**ContextPopup-Ansicht.**](windowsribbon-element-contextpopup.md)

### <a name="the-ribbon-view"></a>Menübandansicht

Die Benutzeroberfläche der [**Menübandansicht**](windowsribbon-element-ribbon.md) ist das primäre Feature des Menübandframeworks und bietet die Benutzeroberfläche der nächsten Generation für die Darstellung von Befehlen in Windows-Anwendungen.

Das Menüband ist eine Befehlsleiste, die die Hauptfunktionen einer Anwendung über eine Reihe von Registerkarten am oberen Rand eines Anwendungsfensters verfügbar macht. Sie ähnelt der Funktionalität und darstellung der Microsoft Office 2007 Fluent UI. Das Menüband bietet einen intuitiven Gegenpunkt zum Test- und Fehlerprozess der Befehlsermittlung, der typisch für Windows-Standardmenüsysteme ist. Optimiert für Effizienz und Auffindbarkeit ermöglicht das Menüband das Suchen, Verstehen und Verwenden von Befehlen mit minimalen Mausklicks und Tastatureingaben über ein System von Standardsteuerelementen, Katalogen und Livevorschau.

Die folgende Abbildung veranschaulicht die Implementierung des Menübandframeworks in Paint für Windows 7.

![Screenshot der Menübandimplementierung in Paint für Windows 7.](images/overviews/screenshot-paint-win7transparency-mirror.png)

### <a name="the-contextpopup-view"></a>Die ContextPopup-Ansicht

Die [**ContextPopup-Ansicht**](windowsribbon-element-contextpopup.md) bietet über das [Kontext-Popup-Steuerelement](windowsribbon-controls-contextpopup.md) ein umfangreicheres Kontextmenüsystem als bei früheren Windows-Anwendungen verfügbar ist. Ein Kontext-Popup kann nur zur Unterstützung eines Menübands bereitgestellt werden. Ein eigenständiges Kontext-Popup wird vom Menübandframework nicht unterstützt.

## <a name="ribbon-architecture"></a>Menübandarchitektur

Im Gegensatz zum herkömmlichen steuerelementbasierten Windows UI-Entwicklungsmodell basiert die Entwicklung der Windows-Menüband-Framework-UI auf dem abstrakteren Konzept von Befehlen. Durch die Konzentration auf die Befehle, die Steuerelementen zugeordnet sind, und nicht auf die Steuerelemente selbst, kann das Framework die Benutzeroberfläche automatisch entsprechend den Anforderungen anpassen, die als Reaktion auf den Befehlsausführungsstatus erforderlich sind, der von der Menübandhostanwendung abgerufen wurde.

Eine Anwendung, die das Menübandframework verwendet, macht Befehle verfügbar, ohne mit den Details der Darstellung dieses Befehls in der Benutzeroberfläche belastet zu werden. Dies wird manchmal als absichtsbasiertes Benutzeroberflächenmodell bezeichnet. Der [**Befehlstyp**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype), seine Eigenschaften und seine Ressourcen definieren die Absicht des Befehls für die Anwendung. Beispielsweise können Mauseingaben, Tastatureingaben oder sogar das Schütteln eines Gyroskopierungsgeräts zur Ausführung desselben Befehls führen, den die Anwendung nur für die Ausführung des Befehls und nicht für deren Aufruf verwendet.

Das Menübandframework bietet diese Flexibilität, indem es Funktionen von der Darstellung mit zwei unterschiedlichen Entwicklungsstrukturen trennt: eine auf Extensible Application Markup Language (XAML) basierende Markupsprache zum Deklarieren von Steuerelementen und das visuelle Layout einer Menübandimplementierung und C++-COM-basierte Schnittstellen zum Initialisieren des Frameworks und Behandeln von Ereignissen zur Laufzeit. Diese Unterscheidung ermöglicht es Benutzeroberflächenentwicklern und Designern, allein für die Darstellung einer Menübandanwendung verantwortlich zu sein, während kernliche Funktionen die Domäne der Softwareentwickler bleiben.

Weitere Informationen finden Sie unter [Grundlegendes zu Befehlen und Steuerelementen.](windowsribbon-commandscontrols.md)

### <a name="the-ribbon-apis"></a>Menüband-APIs

Die Menüband-APIs stellen die erforderlichen Verbindungen zwischen einer Ansicht und der Menübandhostanwendung bereit. Diese APIs bestehen aus den folgenden Schnittstellen und Eigenschaftsschlüsseln:

-   Eine Reihe von COM-Schnittstellen, die vom Menübandframework zum Ausführen von Benutzeroberflächendiensten implementiert werden.

    

    | Schnittstelle                                                                        | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
    |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [IUIContextualUI](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)           | Definiert die Methoden für die Kernfunktionalität der [**ContextPopup-Ansicht.**](windowsribbon-element-contextpopup.md)                                                                                                                                                                                                                                                                                                                                                                                                                  |
    | [IUIFramework®](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                 | Definiert die Methoden, die die Kernfunktionen der [**Menüband-**](windowsribbon-element-ribbon.md) und [**ContextPopup-Ansichten**](windowsribbon-element-contextpopup.md) unterstützen.                                                                                                                                                                                                                                                                                                                                                     |
    | [IUIRibbon](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                       | Definiert die Methoden zum Angeben von Einstellungen und Eigenschaften für eine [**Menübandansicht.**](windowsribbon-element-ribbon.md)                                                                                                                                                                                                                                                                                                                                                                                                                   |
    | [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) | Definiert eine Methode zum Abrufen des werts, der durch einen Eigenschaftsschlüssel identifiziert wird. Diese Schnittstelle wird vom Menübandframework implementiert und auch von der Hostanwendung für jedes Element im [**IUICollection-Objekt**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) eines Elementkatalogs implementiert.<br/> Bei Implementierung durch die Hostanwendung wird die von dieser Schnittstelle definierte Methode verwendet, um einen Eigenschaftsschlüsselwert für das ausgewählte Element in der [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)abzurufen.<br/> |
    | [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)               | Definiert die Methoden zum dynamischen Bearbeiten sammlungsbasierter Steuerelemente, z. B. der Menüband-QAT und sammlungsbasierter [Kataloge](ribbon-controls-galleries.md)zur Laufzeit.                                                                                                                                                                                                                                                                                                                                                        |
    | [IUIImage](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                         | Definiert die Methode zum Abrufen eines Bilds für die Anzeige auf der Menübandbenutzeroberfläche.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
    | [IUIImageFromBitmap](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)     | Definiert die Factorymethode zum Erstellen eines [**IUIImage-Objekts.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                                                                                                                                                                                                                                                                                                                                                                                                                 |

    

     

-   Eine Reihe von COM-Schnittstellen, die von der Menübandhostanwendung implementiert werden, die das Framework als Reaktion auf Benutzeroberflächenänderungen aufruft.

    

    | Schnittstelle                                                                                  | Beschreibung                                                                                                  |
    |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
    | [IUIApplication](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | Definiert die Methoden für den Anwendungsrückrufeinstiegspunkt für das Menübandframework.                               |
    | [IUICommandHandler](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | Definiert die Methoden zum Sammeln von Befehlsinformationen und Behandeln von Befehlsereignissen aus dem Menübandframework. |
    | [IUICollectionChangedEvent](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | Definiert die Methode, die zum Verarbeiten von Änderungen an einer Auflistung zur Laufzeit erforderlich ist.                                   |

    

     

-   Ein Satz von Eigenschaftsschlüsseln, die definieren, welche Benutzeroberflächeneigenschaften die Anwendung programmgesteuerte Kontrolle hat.

    

    | Eigenschaftenschlüsseltyp                                                  | Beschreibung                                              |
    |--------------------------------------------------------------------|----------------------------------------------------------|
    | [Sammlung](windowsribbon-reference-properties-collection.md)    | Definiert Eigenschaften für menübandauflistungsbasierte Steuerelemente. |
    | [Farbauswahl](windowsribbon-reference-properties-colorpicker.md) | Definiert Eigenschaften für Steuerelemente der Menübandfarbauswahl.     |
    | [Schriftart](windowsribbon-reference-properties-fontcontrol.md)         | Definiert Eigenschaften für das FontControl-Menüband.           |
    | [Global](windowsribbon-reference-properties-framework.md)         | Definiert globale Eigenschaften für das Menübandframework.      |
    | [Ressource](windowsribbon-reference-properties-resource.md)        | Definiert Menüband-Ressourceneigenschaften.                      |
    | [Menüband](windowsribbon-reference-properties-ribbon.md)            | Definiert Eigenschaften der Menübandansicht.                          |
    | [State](windowsribbon-reference-properties-state.md)              | Definiert Eigenschaften für den Menüband-Steuerelementzustand oder -kontext.  |

    

     

### <a name="security-and-privacy"></a>Sicherheit und Datenschutz

Die Menübandframework-DLL (uiribbon.dll) wird prozessin Bearbeitung ausgeführt und verfügt über die gleichen Berechtigungen wie die Hostanwendung. Das Menüband akzeptiert nur das, was die Hostanwendung als Eingabe oder Benutzereingabe von streng eingeschränkten Steuerelementen wie dem Drehfeld und dem bearbeitbaren Kombinationsfeld bietet.

Darüber hinaus werden im Framework keine Informationen dauerhaft gespeichert, außer den Informationen, die von der Hostanwendung bereitgestellt oder (wie vom Endbenutzer autorisiert) über das optionale Windows-Programm zur Benutzerfreundlichkeit erfasst werden.

### <a name="accessibility-and-localization"></a>Barrierefreiheit und Lokalisierung

Um eine hoch zugängliche Benutzeroberfläche zu bieten, implementiert das Menübandframework Microsoft Active Accessibility. Durch das automatische Auf populieren relevanter Microsoft Active Accessibility-Eigenschaften mit gültigen und hilfreichen Informationen reduziert das Framework den Aufwand für Entwickler erheblich, für alle Benutzer eine inklusive Benutzererfahrung zu bieten.

Weitere Informationen zur Barrierefreiheit im Menübandframework finden Sie unter [Working with Active Accessibility in the 2007 Office Fluent Benutzeroberfläche](/previous-versions/office/developer/office-2007/bb404170(v=office.12)).

Darüber hinaus ist das Menübandframework ein Windows-Feature und daher für alle Sprachen lokalisiert, die Windows unterstützt. Entwickler sind jedoch dafür verantwortlich, ihre eigenen spezifischen Anwendungsressourcen zu lokalisieren.

## <a name="conclusion"></a>Zusammenfassung

Das Menüband ist eine neue und ansprechende Form der Befehlspräsentation, die Anwendungsentwickler, Architekten und Designer beim Entwerfen und Erstellen neuer Anwendungen oder beim Aktualisieren vorhandener Anwendungen berücksichtigen sollten.

Das [Windows-Forum für die Menübandentwicklung](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) ist verfügbar, um Themen zu besprechen und Fragen im Zusammenhang mit der Entwicklung von Anwendungen zu stellen, die das Windows-Menübandframework implementieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deklarieren von Befehlen und Steuerelementen mit Menübandmarkup](windowsribbon-schema.md)
</dt> <dt>

[Richtlinien für die Benutzerfreundlichkeit des Menübands](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Menübandentwurfsprozess](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

