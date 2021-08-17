---
title: Einführung in das Windows-Menübandframework
description: Zeigen Sie die Landing Page für das Windows-Menübandframework an. Dies ist eine Alternative zu den mehrschichtigen Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows Anwendungen.
ms.assetid: bc19d5eb-e3a4-4022-8051-512cb3a3e065
keywords:
- Windows Menüband, Framework
- Menüband, Framework
- Windows Menüband, Informationen
- Menüband, Informationen
- Windows Menüband, Komponenten
- Menüband, Komponenten
- Windows Menüband, Ansichten
- Menüband, Ansichten
- Windows Menüband, Architektur
- Menüband, Architektur
- Windows Menüband, APIs
- Menüband, APIs
- Windows Menüband, Sicherheit
- Menüband, Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65576d90abb68b0efddf850f4855633f4b362d8cb21ce6f6f85f7924085e8810
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850642"
---
# <a name="introducing-the-windows-ribbon-framework"></a>Einführung in das Windows-Menübandframework

Das Windows-Menübandframework ist ein umfangreiches Befehlspräsentationssystem, das eine moderne Alternative zu den mehrschichtigen Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows bietet.

-   [Ein neues Befehlsparadigma](#a-new-command-paradigm)
-   [Ansichten](#views)
    -   [Menübandansicht](#the-ribbon-view)
    -   [Die ContextPopup-Ansicht](#the-contextpopup-view)
-   [Menübandarchitektur](#ribbon-architecture)
    -   [Die Menüband-APIs](#the-ribbon-apis)
    -   [Sicherheit und Datenschutz](#security-and-privacy)
    -   [Barrierefreiheit und Lokalisierung](#accessibility-and-localization)
-   [Zusammenfassung](#conclusion)
-   [Zugehörige Themen](#related-topics)

## <a name="a-new-command-paradigm"></a>Ein neues Befehlsparadigma

Das Menübandframework ist eine Sammlung von Microsoft Win32-APIs, die eine Vielzahl neuer Benutzeroberflächenfunktionen für Windows unterstützen.

Dieses umfangreiche, moderne UI-Befehlsframework bietet Folgendes:

-   Einfache Implementierung für ganz neue Ribbon-Frameworkanwendungen und einfache Migration vorhandener Win32-Anwendungen.
-   Konsistente Darstellung und einheitliches Verhalten für Menübandanwendungen.
-   Einhaltung der Windows-Benutzeroberflächenrichtlinien für eine erstklassige Windows-Erfahrung durch Barrierefreiheitsstandards, Unterstützung visueller Stile (Design), automatische Anpassungen mit hohem Kontrast und DPI-Bewusstsein (High Dots per Inch).

Das Menübandframework besteht aus zwei primären Benutzeroberflächenkomponenten:

-   Die Menübandbefehlsleiste, die aus der Symbolleiste für den Schnellzugriff (Quick Access Toolbar, QAT) besteht, die verschiedene Menübandbefehle verfügbar macht und hebt, wie vom Benutzer oder der Anwendung angegeben, sowie eine Registerkartenzeile, die das Anwendungsmenü, standard- oder kontextbezogene Registerkarten und eine Hilfeschaltfläche enthält.
-   Ein umfangreiches Kontextmenüsystem.

Eine Kombination aus deklarativem XML und nativen COM-Schnittstellen wird verwendet, um die Darstellung und Funktionalität dieser Komponenten zu entkoppeln.

## <a name="views"></a>Sichten

Die hauptkomponenten der Benutzeroberfläche des Menübandframework, die Menübandbefehlsleiste und das Kontextmenüsystem, werden strukturell durch Ansichten *unterschieden.* Das Framework unterstützt zwei Ansichten: die [**Menübandansicht**](windowsribbon-element-ribbon.md) und die [**ContextPopup-Ansicht.**](windowsribbon-element-contextpopup.md)

### <a name="the-ribbon-view"></a>Menübandansicht

Die Benutzeroberfläche der [**Menübandansicht**](windowsribbon-element-ribbon.md) ist das primäre Feature des Menübandframework und bietet die Benutzeroberfläche der nächsten Generation zum Präsentieren von Befehlen in Windows Anwendungen.

Das Menüband ist eine Befehlsleiste, die die wichtigsten Funktionen einer Anwendung über eine Reihe von Registerkarten am oberen Ende eines Anwendungsfensters verfügbar macht. Sie ähnelt der Funktionalität und Darstellung der Microsoft Office 2007 Fluent Benutzeroberfläche. Das Menüband bietet einen intuitiven Gegenpunkt zum Test-und-Fehler-Prozess der Befehlsermittlung, der typisch für Standardmenüsysteme Windows ist. Optimiert für Effizienz und Auffindbarkeit, erleichtert das Menüband das Suchen, Verstehen und Verwenden von Befehlen mit minimalen Mausklicks und Tastatureingaben über ein System von Standardsteuerelementen, Katalogen und Livevorschau.

Die folgende Abbildung veranschaulicht die Implementierung des Menübandframework in Paint für Windows 7.

![Screenshot, der die Menübandimplementierung in Farbe für Windows 7 zeigt.](images/overviews/screenshot-paint-win7transparency-mirror.png)

### <a name="the-contextpopup-view"></a>Die ContextPopup-Ansicht

Die [**ContextPopup-Ansicht**](windowsribbon-element-contextpopup.md) stellt über das [Kontext-Popup-Steuerelement](windowsribbon-controls-contextpopup.md) ein umfangreiches Kontextmenüsystem bereit, als bei früheren Windows verfügbar ist. Ein Kontext-Popup kann nur zur Unterstützung eines Menübands bereitgestellt werden. Ein eigenständiges Kontext-Popup wird vom Menübandframework nicht unterstützt.

## <a name="ribbon-architecture"></a>Menübandarchitektur

Im Gegensatz zum herkömmlichen steuerelementbasierten entwicklungsmodell Windows-Benutzeroberfläche basiert Windows Entwicklung der Menübandframework-Benutzeroberfläche auf dem abstrakteren Konzept von Befehlen. Durch die Konzentration auf die Befehle, die Steuerelementen und nicht den Steuerelementen selbst zugeordnet sind, kann das Framework die Benutzeroberfläche als Reaktion auf den Befehlsausführungsstatus, der von der Menübandhostanwendung abgerufen wird, automatisch anpassen.

Eine Anwendung, die das Menübandframework verwendet, macht Befehle verfügbar, ohne sich mit den Details der Dargestelltheit dieses Befehls auf der Benutzeroberfläche zu indumeriert zu machen. Dies wird manchmal als absichtsbasiertes Benutzeroberflächenmodell bezeichnet. Der [**Befehlstyp**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype), seine Eigenschaften und seine Ressourcen definieren die Absicht des Befehls für die Anwendung. Beispielsweise können Mauseingaben, Tastatureingaben oder sogar das Shaking eines Gyroskopgeräts zur Ausführung desselben Befehls führen, für den die Anwendung nur die Ausführung des Befehls und nicht die Art des Aufrufs betrifft.

Das Menübandframework bietet diese Flexibilität, indem es Funktionen von der Präsentation mit zwei unterschiedlichen Entwicklungsstrukturen trennt: eine Extensible Application Markup Language(XAML)-basierte Markupsprache zum Deklarieren von Steuerelementen und das visuelle Layout einer Menübandimplementierung und C++-COM-basierte Schnittstellen, um das Framework zu initialisieren und Ereignisse zur Laufzeit zu behandeln. Diese Unterscheidung ermöglicht es Benutzeroberflächenentwicklern und -designern, allein für die Darstellung einer Menübandanwendung verantwortlich zu sein, während die Kernfunktionalität weiterhin der Bereich der Softwareentwickler bleibt.

Weitere Informationen finden Sie unter [Grundlegendes zu Befehlen und Steuerelementen.](windowsribbon-commandscontrols.md)

### <a name="the-ribbon-apis"></a>Die Menüband-APIs

Die Menüband-APIs stellen die erforderlichen Verbindungen zwischen einer Ansicht und der Menübandhostanwendung zur Verfügung. Diese APIs bestehen aus den folgenden Schnittstellen und Eigenschaftsschlüsseln:

-   Eine Reihe von COM-Schnittstellen, die vom Menübandframework implementiert werden, um Benutzeroberflächendienste durchzuführen.

    

    | Schnittstelle                                                                        | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
    |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)           | Definiert die Methoden für die Kernfunktionen der [**ContextPopup-Ansicht.**](windowsribbon-element-contextpopup.md)                                                                                                                                                                                                                                                                                                                                                                                                                  |
    | [IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                 | Definiert die Methoden, die die [](windowsribbon-element-ribbon.md) Kernfunktionen der Menüband- und [**ContextPopup-Ansichten**](windowsribbon-element-contextpopup.md) unterstützen.                                                                                                                                                                                                                                                                                                                                                     |
    | [IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                       | Definiert die Methoden zum Angeben von Einstellungen und Eigenschaften für eine [**Menübandansicht.**](windowsribbon-element-ribbon.md)                                                                                                                                                                                                                                                                                                                                                                                                                   |
    | [IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) | Definiert eine Methode zum Abrufen des durch einen Eigenschaftsschlüssel identifizierten Werts. Diese Schnittstelle wird vom Menübandframework implementiert und auch von der Hostanwendung für jedes Element im [**IUICollection-Objekt**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) eines Elementkatalogs implementiert.<br/> Bei der Umsetzung durch die Hostanwendung wird die von dieser Schnittstelle definierte Methode verwendet, um einen Eigenschaftsschlüsselwert für das ausgewählte Element in der [**IUICollection abzurufen.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)<br/> |
    | [IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)               | Definiert die Methoden zum dynamischen Bearbeiten sammlungsbasierter Steuerelemente, z. B. menübandbasierte QAT- und [sammlungsbasierte](ribbon-controls-galleries.md)Kataloge, zur Laufzeit.                                                                                                                                                                                                                                                                                                                                                        |
    | [IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                         | Definiert die Methode zum Abrufen eines Bilds für die Anzeige in der Menübandbenutzeroberfläche.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
    | [IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)     | Definiert die Factorymethode zum Erstellen eines [**IUIImage-Objekts.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                                                                                                                                                                                                                                                                                                                                                                                                                 |

    

     

-   Eine Reihe von COM-Schnittstellen, die von der Menübandhostanwendung implementiert werden, die das Framework als Reaktion auf Änderungen der Benutzeroberfläche aufruft.

    

    | Schnittstelle                                                                                  | Beschreibung                                                                                                  |
    |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
    | [IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | Definiert die Anwendungsrückruf-Einstiegspunktmethoden für das Menübandframework.                               |
    | [IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | Definiert die Methoden zum Sammeln von Befehlsinformationen und zum Behandeln von Befehlsereignissen aus dem Menübandframework. |
    | [IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | Definiert die Methode, die zum Behandeln von Änderungen an einer Auflistung zur Laufzeit erforderlich ist.                                   |

    

     

-   Ein Satz von Eigenschaftsschlüsseln, die definieren, welche Benutzeroberflächeneigenschaften die Anwendung programmgesteuerte Kontrolle hat.

    

    | Eigenschaftenschlüsseltyp                                                  | BESCHREIBUNG                                              |
    |--------------------------------------------------------------------|----------------------------------------------------------|
    | [Sammlung](windowsribbon-reference-properties-collection.md)    | Definiert Eigenschaften für auflistungsbasierte Steuerelemente des Menübands. |
    | [Farbauswahl](windowsribbon-reference-properties-colorpicker.md) | Definiert Eigenschaften für Steuerelemente der Menübandfarbauswahl.     |
    | [Schriftart](windowsribbon-reference-properties-fontcontrol.md)         | Definiert Eigenschaften für das FontControl-Menüband.           |
    | [Global](windowsribbon-reference-properties-framework.md)         | Definiert globale Eigenschaften für das Menübandframework.      |
    | [Ressource](windowsribbon-reference-properties-resource.md)        | Definiert Menüband-Ressourceneigenschaften.                      |
    | [Menüband](windowsribbon-reference-properties-ribbon.md)            | Definiert Menübandansichtseigenschaften.                          |
    | [State](windowsribbon-reference-properties-state.md)              | Definiert Eigenschaften für den Menüband-Steuerelementzustand oder -kontext.  |

    

     

### <a name="security-and-privacy"></a>Sicherheit und Datenschutz

Die Menübandframework-DLL (uiribbon.dll) wird prozessbearbeitend ausgeführt und verfügt über die gleichen Berechtigungen wie die Hostanwendung. Das Menüband akzeptiert nur das, was die Hostanwendung als Eingabe oder Benutzereingabe aus eng eingeschränkten Steuerelementen wie dem Spinner und dem bearbeitbaren Kombinationsfeld bereitstellt.

Darüber hinaus speichert das Framework keine Informationen dauerhaft, außer dem, was von der Hostanwendung bereitgestellt oder (wie vom Endbenutzer autorisiert) über das Programm zur nutzungsbasierten Windows gesammelt wird.

### <a name="accessibility-and-localization"></a>Barrierefreiheit und Lokalisierung

Um eine hoch zugängliche Benutzeroberfläche bereitzustellen, implementiert das Menübandframework Microsoft Active Accessibility. Durch das automatische Auffüllen relevanter Microsoft Active Accessibility Eigenschaften mit gültigen und hilfreichen Informationen reduziert das Framework die Belastung für Entwickler erheblich, eine inklusive Benutzeroberfläche für alle Benutzer bereitzustellen.

Weitere Informationen zur Barrierefreiheit im Menübandframework finden Sie unter [Working with Active Accessibility in the 2007 Office Fluent Benutzeroberfläche](/previous-versions/office/developer/office-2007/bb404170(v=office.12)).

Darüber hinaus ist das Menübandframework ein Windows-Feature und daher für alle Sprachen lokalisiert, die Windows unterstützt. Entwickler sind jedoch für die Lokalisierung ihrer eigenen spezifischen Anwendungsressourcen verantwortlich.

## <a name="conclusion"></a>Zusammenfassung

Das Menüband ist eine neue und ansprechende Form der Befehlspräsentation, die Anwendungsentwickler, Architekten und Designer beim Entwerfen und Erstellen neuer Anwendungen oder beim Aktualisieren vorhandener Anwendungen berücksichtigen sollten.

Das [Windows Menübandentwicklungsforum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) ist verfügbar, um Themen zu besprechen und Fragen im Zusammenhang mit der Entwicklung von Anwendungen zu stellen, die das Windows Menüband-Framework implementieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deklarieren von Befehlen und Steuerelementen mit Menübandmarkup](windowsribbon-schema.md)
</dt> <dt>

[Richtlinien für die Menübandbenutzerfreundlichkeit](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Menübandentwurfsprozess](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

