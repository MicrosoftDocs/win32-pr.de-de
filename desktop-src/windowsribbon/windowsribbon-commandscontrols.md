---
title: Grundlegendes zu Befehlen und Steuerelementen
description: Die Trennung der Logik von der Präsentation ist die Entwurfs Philosophie, die das Befehls Präsentationssystem von Windows Ribbon Framework \ 8212 inspiriert; ein System, das auf einem Entwurfsmuster basiert, in dem Funktionalität und Verhalten unabhängig von den Steuerelementen implementiert werden, die diese Funktionalität verfügbar machen.
ms.assetid: fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d
keywords:
- Fenster Multifunktionsleiste, Befehle (Übersicht)
- Menüband, Befehle (Übersicht)
- Fenster Multifunktionsleiste, Übersicht über Steuerelemente
- Menüband, Übersicht über Steuerelemente
- Befehlssystem für Windows-Menüband
- Steuerelemente für Windows-Menüband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2659da608a3d3e73f3f35ac1911946a6685c74e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104556722"
---
# <a name="understanding-commands-and-controls"></a>Grundlegendes zu Befehlen und Steuerelementen

Die Trennung der Logik von der Präsentation ist die Entwurfs Philosophie, die das Befehls Präsentationssystem des Windows-Menüband-Frameworks – ein System, das auf einem Entwurfsmuster basiert, bei dem Funktionalität und Verhalten unabhängig von den Steuerelementen implementiert werden, die diese Funktionalität verfügbar machen.

-   [Introduction (Einführung)](#introduction)
-   [Das Windows-Menüband-Befehls System](#the-windows-ribbon-command-system)
    -   [Steuerelemente](#understanding-commands-and-controls)
    -   [Befehle](#understanding-commands-and-controls)
    -   [Die Befehls Funktion in Aktion](#the-command-experience-in-action)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

In diesem Artikel wird das Design des befehlssystems des Menüband-Frameworks erläutert. Es beschreibt die Konzepte der Befehle und Steuerelemente und erläutert, wie diese zusammenarbeiten, um eine umfangreiche Befehls Oberfläche mit einer Reihe neuer Benutzeroberflächen Funktionen bereitzustellen.

## <a name="the-windows-ribbon-command-system"></a>Das Windows-Menüband-Befehls System

Im Menüband-Framework sind Befehle und Steuerelemente unabhängige Entitäten. Ein Befehl ist eine abstrakte Struktur ohne Präsentations Einschränkungen, die eine bestimmte Aufgabe oder Funktionsklasse darstellt. Ein Steuerelement hingegen ist ein konkretes Objekt, das Befehlsfunktionen über die Multifunktionsleisten-Benutzeroberfläche verfügbar macht.

Diese Unterscheidung bietet die Möglichkeit, Befehle zu definieren, für die keine Benutzeroberflächen Details verfügbar sind und die für eine Aktion ausgeführt werden können, ohne dass Sie die Art und Weise verwalten müssen, wie die Aktion aufgerufen wurde.

### <a name="controls"></a>Steuerelemente

Steuerelemente sind die für die Befehls Darstellung erforderlichen UI-Objekte. Sie werden zur Laufzeit durch das Framework basierend auf der Benutzerinteraktion und einem Satz inhärenter Eigenschaften und Verhalten gerendert und verwaltet.

Als Adaptive Layout bezeichnet die Framework-verwaltete Flexibilität der Benutzeroberfläche eine der großartigen Stärken der Multifunktionsleiste. Menüband-Steuerelemente können sich automatisch durch Framework-abhängige oder Entwickler definierte Layoutvorlagen neu konfigurieren, die auf verschiedene Lauf Zeitanforderungen reagieren können, ohne eine einzige Zeile von Präsentationscode schreiben zu müssen. Weitere Informationen finden Sie unter [Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md).

Neben den Vorteilen des adaptiven Layouts bieten mehrere komplexe Menüband-Steuerelemente eigenständige Lösungen für bestimmte Bereiche von Benutzeroberflächen Problemen. Durch die Bereitstellung eines ausgereiften Interaktions Modells bieten multifunktionsleistensteuerelemente, wie z. b. FontControl oder ColorPicker, die Möglichkeit, Daten in abstrakter Form durch Eigenschafts Behälter tatsächlicher Schriftart-oder Farb Attribute und nicht durch verschiedene untergeordnete Steuerelemente, Enumerationen und Indexwerte von standardmäßigen Windows-Steuerelementen zu manipulieren.

### <a name="commands"></a>Befehle

Wenn Sie locker an die Menüband-Steuerelemente gekoppelt sind, die ihre Funktionalität verfügbar machen, sind Befehls Implementierungen die Domäne der Host Anwendung und weisen die Form von Ereignislistenern, Befehls Handlern und verschiedenen Befehls Eigenschaften auf.

Befehle werden im Menüband-Markup mit einer eindeutigen ID deklariert, oder bei der Kompilierung wurde eine vom Markup Compiler generierte ID zugewiesen. Befehle sind mit Steuerelementen über einen Befehlsnamen verknüpft, aber im Gegensatz zu-Steuerelementen wird Ihre tatsächliche Funktionalität in Code definiert, in dem Sie über die Befehls-ID an bestimmte Befehls Handler gebunden werden.

> [!Note]  
> Bei der Kompilierung wird diese ID in einer ID-Definitions Header Datei gespeichert, die Befehle für die entsprechenden Befehls Handler in der Menüband-Host Anwendung verfügbar macht.

 

Jeder Befehl verfügt über einen zugrunde liegenden Befehlstyp, der in der [**UI \_ CommandType**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) -Enumeration aufgeführt ist.

### <a name="the-command-experience-in-action"></a>Die Befehls Funktion in Aktion

Die Funktionen dieses Befehls Modells werden von der Symbolleiste für den schnell Zugriff auf das Menüband (QAT) veranschaulicht. QAT bietet Endbenutzern die Möglichkeit, auf einfache Weise ihre eigenen Verknüpfungen für praktisch alle Steuerelemente in der Menüband-Benutzeroberfläche zu definieren. Der QAT wird zur Laufzeit dynamisch eine Verknüpfung hinzugefügt, wenn der Benutzer mit der rechten Maustaste auf ein Menüband-Steuerelement klickt und aus dem Kontextmenü die **Symbolleiste für den schnell Zugriff hinzufügen** auswählt.

Das folgende Bild zeigt die Befehle **Einfügen** und **Einfügen aus** , dargestellt durch ein [**SplitButton**](windowsribbon-element-splitbutton.md) -Steuerelement im Menüband von Windows 7 Paint.

![Bild der "SplitButton einfügen" im Microsoft Paint-Menüband.](images/overviews/paint-paste-splitbutton-ribbon.png)

Das folgende Bild zeigt die gleichen **Einfüge** -und **Einfüge Befehle von** Befehlen, die noch durch ein [**SplitButton**](windowsribbon-element-splitbutton.md) -Steuerelement dargestellt werden, im Menüband-QAT von Windows 7 Paint.

![Bild der "SplitButton einfügen" in Microsoft Paint QAT.](images/overviews/paint-paste-splitbutton-qat.png)

Wenn ein Steuerelement vom QAT gehostet wird, behält die neue Instanz des Steuer Elements die gesamte Funktionalität des ursprünglichen Steuer Elements bei, ohne dass zusätzliche Ereignislistener und Befehls Handler diese unterstützen müssen. Beide Steuerelemente werden über einen freigegebenen Befehls Bezeichner an denselben Menü Band Befehls Handler gebunden. Auf diese Weise behandelt das Framework beide Steuerelemente als eins, unabhängig davon, welches aufgerufen wird.

> [!Note]  
> Die gleichen Vorteile werden erkannt, wenn Befehle zur Entwurfszeit in ein [**contextpopup-Objekt**](windowsribbon-element-contextpopup.md) integriert werden. In diesem Fall können die Befehls Handler für das Einfügen verwendet werden, unabhängig davon, ob das [**SplitButton**](windowsribbon-element-splitbutton.md) -Steuerelement in der Multifunktionsleiste, in der QAT oder in **contextpopup** angezeigt wird.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einführung in das Windows-Menü Band Framework](windowsribbon-introduction.md)
</dt> <dt>

[Erstellen einer Menü Bandanwendung](windowsribbon-stepbystep.md)
</dt> <dt>

[Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup](windowsribbon-schema.md)
</dt> </dl>

 

 