---
title: Windows-Menüband-Steuerelement Bibliothek
description: In den Themen in diesem Abschnitt wird der Satz von Steuerelementen beschrieben, die im Windows-Menü Band Framework enthalten sind. Die hier aufgeführten Steuerelemente sind die UI-Objekte in einem Menüband, die Befehls Funktionalität verfügbar machen.
ms.assetid: bda13e51-7e5f-4600-a6bd-9388bffd6ce2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840b07bafe0c43cb7ab148a4413657b9722c409b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341321"
---
# <a name="windows-ribbon-framework-control-library"></a>Windows-Menüband-Steuerelement Bibliothek

In den Themen in diesem Abschnitt wird der Satz von Steuerelementen beschrieben, die im Windows-Menü Band Framework enthalten sind. Die hier aufgeführten Steuerelemente sind die UI-Objekte in einem Menüband, die Befehls Funktionalität verfügbar machen.

-   [Introduction (Einführung)](#introduction)
-   [Die Steuerelemente](#windows-ribbon-framework-control-library)
    -   [Grundlegende Steuerelemente](#basic-controls)
    -   [Container Steuerelemente](#container-controls)
    -   [Spezialisierte Steuerelemente](#specialized-controls)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Das Menüband-Framework besteht aus Komponenten wie [Registerkarten](windowsribbon-controls-tab.md) und der [Symbolleiste für den schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md), die zusammenarbeiten, um eine umfangreiche Benutzeroberfläche bereitzustellen. Diese Komponenten stellen verschiedene Arten von Befehlen zur Verfügung, um Kunden eine strukturierte, vorhersagbare Darstellung für multifunktionsleistenanwendungen zu bieten. Beispielsweise macht jede Registerkarte Befehle verfügbar, die sich auf das Erstellen und bearbeiten bestimmter Teile des Inhalts im Anwendungs Arbeitsbereich beziehen, während das [Anwendungsmenü](windowsribbon-controls-applicationmenu.md) Funktionen bereitstellt, die mit einem vollständigen Projekt verknüpft sind, z. b. ein gesamtes Dokument, Bild oder Film.

Dieses Thema enthält eine umfassende Liste der Menüband-Steuerelemente und enthält eine kurze Beschreibung der einzelnen Steuerelemente, mit Links zu ausführlicheren Dokumentationen, soweit verfügbar.

## <a name="the-controls"></a>Die Steuerelemente

Das Menüband-Framework besteht aus zwei [Ansichten](windowsribbon-reference-elements-view.md): der Menü [**Band**](windowsribbon-element-ribbon.md) Ansicht und der [**contextpopup**](windowsribbon-element-contextpopup.md) -Ansicht. Jede Ansicht kann mehrere Komponenten hosten, die als Präsentations Container für alle Steuerelemente fungieren, die vom Framework gerendert und verwaltet werden.

Die [**Menüband**](windowsribbon-element-ribbon.md) -Ansicht hostet das Element [**applicationmenu**](windowsribbon-element-applicationmenu.md) , das [**quickaccesstoolbar**](windowsribbon-element-quickaccesstoolbar.md) -Element und die Menüband-Befehlsleiste, während die [**contextpopup**](windowsribbon-element-contextpopup.md) -Ansicht ein [**ContextMenu**](windowsribbon-element-contextmenu.md) -Element, ein [**MiniToolbar**](windowsribbon-element-minitoolbar.md) -Element oder beides hostet.

Jedes Framework-Steuerelement wird durch die Funktionalität unterschieden, die seinem [**Befehlstyp**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)zugeordnet ist.

### <a name="basic-controls"></a>Grundlegende Steuerelemente

Grundlegende Steuerelemente bestehen aus einer oder mehreren Schaltflächen, die per Mausklick aufgerufen werden können, um eine einfache Aktion auszuführen.

> [!Note]  
> Der [**Spinner**](windowsribbon-element-spinner.md) ist eine Ausnahme, da er ein Bearbeitungs Steuerelement enthält.

 

In der folgenden Tabelle sind die grundlegenden Steuerelemente im Menüband-Framework aufgeführt.



| Control                                                  | Markup-Element                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [Schaltfläche](windowsribbon-controls-button.md)              | [**Gedrückt**](windowsribbon-element-button.md)             |
| [Kontrollkästchen](windowsribbon-controls-checkbox.md)         | [**CheckBox**](windowsribbon-element-checkbox.md)         |
| [Hilfe Schaltfläche](windowsribbon-controls-helpbutton.md)     | [**HelpButton**](windowsribbon-element-helpbutton.md)     |
| [Spinner](windowsribbon-controls-spinner.md)            | [**Spinner**](windowsribbon-element-spinner.md)           |
| [UMSCHALT Fläche](windowsribbon-controls-togglebutton.md) | [**ToggleButton**](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a>Container Steuerelemente

Container Steuerelemente bestehen aus Gruppen von Steuerelementen, Menüs, Listen oder Element-und Befehls Sammlungen.

Das Framework unterscheidet zwischen zwei Arten von Containern, statisch und dynamisch.

### <a name="static-containers"></a>Statische Container

Statische Container werden zusammen mit allen zugeordneten Ressourcen in der Menüband-Markup Datei deklariert und aufgefüllt. Diese Steuerelemente können zur Laufzeit nicht geändert werden.

Zu den Vorteilen statischer Steuerelemente gehören die folgenden:

-   Schnelles Prototypen. Statische Steuerelemente ermöglichen das schnelle Erstellen eines Menüband-Mock-up, das einem abschließenden Menüband-Design ähnelt, das keinen komplizierten Code erfordert.
-   Einfache Änderungen. Die meisten Elemente, Attribute, Ressourcen und Layouts statischer Steuerelemente können im Markup geändert werden.
-   Konsistente Benutzeroberfläche. Gut entworfene Anwendungen bieten eine konsistente und stabile Benutzeroberfläche, mit der Änderungen an Menüs und Listen zur Laufzeit vermieden werden.

In der folgenden Tabelle werden die statischen Container-Steuerelemente im Menüband-Framework beschrieben.



| Control                                                        | Markup-Element                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [Anwendungsmenü](windowsribbon-controls-applicationmenu.md) | [**Applicationmenu**](windowsribbon-element-applicationmenu.md) |
| [Kontext-Popup](windowsribbon-controls-contextpopup.md)       | [**Contextpopup**](windowsribbon-element-contextpopup.md)       |
| [Dropdown Schaltfläche](windowsribbon-controls-dropdownbutton.md)  | [**DropDownButton**](windowsribbon-element-dropdownbutton.md)   |
| [Gruppieren](windowsribbon-controls-group.md)                      | [**Gruppe**](windowsribbon-element-group.md)                     |
| [Menü Gruppe](windowsribbon-controls-menugroup.md)             | [**MenuGroup**](windowsribbon-element-menugroup.md)             |
| [Trenn Schaltfläche](windowsribbon-controls-splitbutton.md)         | [**SplitButton**](windowsribbon-element-splitbutton.md)         |
| [TAB](windowsribbon-controls-tab.md)                          | [**Registerkarte**](windowsribbon-element-tab.md)                         |
| [Registerkarten Gruppe](windowsribbon-controls-tabgroup.md)               | [**TabGroup**](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a>Dynamische Container

Dynamische Container werden in der Menüband-Markup Datei deklariert. Sie verfügen über eine Gruppe von Elementen oder Befehlen, die zur Laufzeit erstellt oder geändert werden.

Eine Unterklasse dynamischer Container, die als Galerien bezeichnet werden, unterscheidet sich durch ihre Implementierung der [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Schnittstelle. Diese Schnittstelle ermöglicht es einem Steuerelement, seine Elemente oder Befehlsliste als Auflistung verfügbar zu machen und Aktualisierungen auf der Grundlage der Benutzerinteraktion und der Lauf Zeit Bedingungen zu unterstützen. Weitere Informationen finden Sie unter [Arbeiten mit Galerien](ribbon-controls-galleries.md).

In der folgenden Tabelle werden die dynamischen Container Steuerelemente im Menüband-Framework aufgelistet.



| Control                                                               | Markup-Element                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [Kombinations Feld](windowsribbon-controls-combobox.md)                      | [**ComboBox**](windowsribbon-element-combobox.md)                     |
| [Dropdown-Katalog](windowsribbon-controls-dropdowngallery.md)       | [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)       |
| [In-Ribbon-Katalog](windowsribbon-controls-inribbongallery.md)       | [**Inribbongallery**](windowsribbon-element-inribbongallery.md)       |
| [Symbolleiste für den Schnellzugriff](windowsribbon-controls-quickaccesstoolbar.md) | [**Quickaccesstoolbar**](windowsribbon-element-quickaccesstoolbar.md) |
| [Zuletzt verwendete Elemente](windowsribbon-controls-recentitems.md)                | [**"Recentitems"**](windowsribbon-element-recentitems.md)               |
| [Split Button-Katalog](windowsribbon-controls-splitbuttongallery.md) | [**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a>Spezialisierte Steuerelemente

Das Menüband-Framework enthält eine Reihe spezieller Steuerelemente für bestimmte UI-Funktionen.

In der folgenden Tabelle sind die spezialisierten Steuerelemente im Menüband-Framework aufgeführt.



| Control                                                                  | Markup-Element                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Dropdown-Farbauswahl](windowsribbon-controls-dropdowncolorpicker.md) | [**Dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md) |
| [Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)                   | [**FontControl**](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Befehlen und Steuerelementen](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 