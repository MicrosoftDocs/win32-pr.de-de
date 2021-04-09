---
title: Entwickler Handbücher für Windows Ribbon Framework
description: Die in diesem Abschnitt enthaltenen Themen beschreiben bestimmte Aspekte des Windows-Menüband-Frameworks.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Windows-Menüband, Framework
- Menüband, Framework
- Windows-Menüband, Entwickler Handbücher
- Menüband, Entwickler Handbücher
- Entwickler Handbücher für Windows-Menüband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b6e88045efdd31384d99370fdd9bb9cb264598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102155"
---
# <a name="windows-ribbon-framework-developer-guides"></a>Entwickler Handbücher für Windows Ribbon Framework

Die in diesem Abschnitt enthaltenen Themen beschreiben bestimmte Aspekte des Windows-Menüband-Frameworks.

## <a name="basics"></a>Grundlagen

[Erstellen einer Menü Bandanwendung](windowsribbon-stepbystep.md)

Damit das Windows-Menüband-Framework die Menüband-Markup Datei verwendet, muss die Markup Datei in eine Ressourcen Datei im Binärformat kompiliert werden. Ein dedizierter Menüband-Markup Compiler, der UI-Befehls Compiler (UICC), ist zu diesem Zweck im Microsoft Windows Software Development Kit (SDK) (7,0 oder höher) enthalten. Neben der Kompilierung der Binärversion des Menüband-Markups generiert UICC eine ID-Definitions Header Datei (. h), die alle Markup Elemente für die Menüband-Host Anwendung und eine Ressourcen Datei (. RC) zur Verfügung stellt, mit der Bild-und Zeichen folgen Ressourcen zur Buildzeit mit der Host Anwendung verknüpft werden.

[Migrieren zum Windows-Menü Band Framework](ribbon-migration.md)

Eine Anwendung, die auf herkömmlichen Menüs, Symbolleisten und Dialogfeldern basiert, kann auf die umfangreiche, dynamische und Kontext gesteuerte Benutzeroberfläche (UI) des befehlssystems des Multifunktionsleisten-Frameworks migriert werden. Dies ist eine einfache und effektive Möglichkeit, um die Anwendung zu modernisieren und zu beleben und gleichzeitig die Barrierefreiheit, die Benutzerfreundlichkeit und die Auffindbarkeit ihrer Funktionalität zu verbessern.

[Grundlegendes zu Befehlen und Steuerelementen](windowsribbon-commandscontrols.md)

Die Trennung der Logik von der Präsentation ist die Entwurfs Philosophie, die das Befehls Präsentationssystem des Multifunktionsleisten-Frameworks inspiriert – ein System, das auf einem Entwurfsmuster basiert, in dem Funktionalität und Verhalten unabhängig von den Steuerelementen implementiert werden, die diese Funktionalität verfügbar machen.

## <a name="user-interface"></a>Benutzeroberfläche

[Angeben von Menüband-Bild Ressourcen](windowsribbon-imageformats.md)

Als umfassendes Befehls Präsentationssystem ist das Menüband-Framework für die Unterstützung von Bild Ressourcen in der Multifunktionsleisten-Benutzeroberfläche (UI) konzipiert. Alle Bild Ressourcen werden im [Menüband-Markup](windowsribbon-schema.md) deklariert oder von einer Menüband-Host Anwendung abgefragt.

Für Windows 8 und höher unterstützt das Menüband-Framework die folgenden Grafikformate: 32-Bit-ARGB-Bitmap-Dateien (BMP) und Portable Network Graphics-Dateien (PNG) mit Transparenz.

Für Windows 7 und früher müssen Bild Ressourcen dem standardmäßigen BMP-Grafikformat entsprechen, das in Windows verwendet wird.

[Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md)

Steuerelemente, die in der Multifunktionsleisten-Befehlsleiste gehostet werden, unterliegen Layoutregeln, die vom Menüband-Framework erzwungen werden, und basieren auf einer Kombination aus Standardverhalten und Layoutvorlagen (sowohl Framework-definiert als auch Benutzer definiert), wie im Menü Band Markup Diese Regeln definieren das Verhalten des adaptiven Layouts des Multifunktionsleisten-Frameworks, das beeinflussen, wie die Steuerelemente in der Befehlsleiste zur Laufzeit an verschiedene Menü Bandgrößen angepasst werden.

[Arbeiten mit Galerien](ribbon-controls-galleries.md)

Das Menüband-Framework bietet Entwicklern ein stabiles und konsistentes Modell für die Verwaltung dynamischer Inhalte über eine Vielzahl von Sammlungs basierten Steuerelementen. Durch das anpassen und Neukonfigurieren der Multifunktionsleisten-Benutzeroberfläche ermöglichen diese dynamischen Steuerelemente dem Framework, auf die Benutzerinteraktion sowohl in der Host Anwendung als auch auf dem Menüband selbst zu reagieren und die Flexibilität für verschiedene Laufzeitumgebungen zu bieten.

[Anzeigen kontextbezogener Registerkarten](ribbon-contextualtabs.md)

In einer Multifunktionsleisten-Framework-Anwendung ist eine Kontext Registerkarte ein ausgeblendetes [Register](windowsribbon-controls-tab.md) Karten-Steuerelement, das in der Registerkarten Zeile angezeigt wird, wenn ein Objekt im Anwendungs Arbeitsbereich (z. b. ein Bild) ausgewählt oder markiert

[Neukonfigurieren des Menübands mit Anwendungsmodi](ribbon-applicationmodes.md)

Das Menüband-Framework unterstützt die dynamische Neukonfiguration und das verfügbar machen von Kernelementen der Menüband-Benutzeroberfläche (User Interface, UI) zur Laufzeit basierend auf dem Zustand der Anwendung (auch als Kontext bezeichnet). Die verschiedenen Zustände, die von einer Anwendung unterstützt werden, werden als Anwendungsmodi bezeichnet und mit bestimmten Elementen im Markup verknüpft.

[Anpassen von Menü Band Farben](ribbon-color.md)

Das Menüband-Framework macht eine Reihe von Farbeigenschaften verfügbar, die es einer Anwendung ermöglichen, die Darstellung verschiedener Benutzeroberflächen Elemente der Multifunktionsleiste zur Laufzeit anzupassen.

[Anzeigen des Menübands](ribbon-visibility.md)

Das Menüband-Framework macht eine Reihe von Eigenschaften verfügbar, die es einer Anwendung ermöglichen, anzugeben, wie die Menüband-Benutzeroberfläche zur Laufzeit angezeigt wird.

## <a name="management"></a>Verwaltung

[Beibehalten des Multifunktionsleisten Status](ribbon-statepersistence.md)

Das Windows Ribon-Framework (Menüband) bietet die Möglichkeit, den Zustand einer Vielzahl von Benutzereinstellungen und-Einstellungen über Anwendungs Sitzungen hinweg beizubehalten.

[Lauschen auf Menü Band Ereignisse](listening-for-ribbon-events.md)

Das Menüband Framework verwendet die Infrastruktur der [Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw)](../etw/event-tracing-portal.md) , um Entwicklern zu ermöglichen, zu erfahren, wie Benutzer mit dem Menüband Ihrer Anwendung

## <a name="markup-compiler"></a>Markup Compiler

[Kompilieren von Menü Band Markup](windowsribbon-intentcl.md)

Damit das Menüband-Framework die [Menüband-Markup](windowsribbon-schema.md) Datei verwendet, muss die Markup Datei in eine Ressourcen Datei im Binärformat kompiliert werden. Ein dedizierter Markup Compiler, der UI-Befehls Compiler (UICC), ist zu diesem Zweck im Microsoft Windows Software Development Kit (SDK) (7,0 oder höher) enthalten. Zusätzlich zum Kompilieren der Binärversion des Markups generiert das UICC eine ID-Definitions Header Datei (. h), die alle Markup Elemente für die Menüband-Host Anwendung und eine Ressourcen Datei (. RC) verfügbar macht, mit der Bild-und Zeichen folgen Ressourcen zur Buildzeit mit der Host Anwendung verknüpft werden.

[Grundlegendes zu Markup Compiler-Meldungen](windowsribbon-compilationerrors.md)

Der Markup Compiler des Windows-Menüband-Frameworks (Menüband), der UI-Befehls Compiler (UICC.exe), überprüft das Menüband-Markup sowohl mit dem Menüband-Schema als auch mit einem zusätzlichen Regelsatz, der durch das Menüband

 

 