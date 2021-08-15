---
title: Windows Entwicklerhandbücher für Menübandframeworks
description: In den Themen in diesem Abschnitt werden bestimmte Aspekte des Windows Menübandframeworks beschrieben.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Windows Menüband, Framework
- Menüband, Framework
- Windows Menüband, Entwicklerhandbücher
- Menüband, Entwicklerhandbücher
- Entwicklerhandbücher für Windows Menüband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b30c5b2564dc918c6f9accfe5a5cb36a2d77222e3822a75a76332b1d3234cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850628"
---
# <a name="windows-ribbon-framework-developer-guides"></a>Windows Entwicklerhandbücher für Menübandframeworks

In den Themen in diesem Abschnitt werden bestimmte Aspekte des Windows Menübandframeworks beschrieben.

## <a name="basics"></a>Grundlagen

[Erstellen einer Menübandanwendung](windowsribbon-stepbystep.md)

Damit das Windows Menübandframework die Menüband-Markupdatei nutzen kann, muss die Markupdatei in eine Ressourcendatei im Binärformat kompiliert werden. Ein dedizierter Menübandmarkupcompiler, der UI COMMAND Compiler (UICC), ist zu diesem Zweck im Microsoft Windows Software Development Kit (SDK) (7.0 oder höher) enthalten. Zusätzlich zum Kompilieren der binären Version des Menübandmarkups generiert UICC eine ID-Definitionsheaderdatei (.h), die alle Markupelemente für die Menübandhostanwendung und eine Ressourcendatei (RC) verfügbar macht, mit der Image- und Zeichenfolgenressourcen zur Buildzeit mit der Hostanwendung verknüpft werden.

[Migrieren zum Windows Menübandframework](ribbon-migration.md)

Eine Anwendung, die auf herkömmlichen Menüs, Symbolleisten und Dialogen basiert, kann zur umfangreichen, dynamischen und kontextgesteuerten Benutzeroberfläche des Menübandframework-Befehlssystems migriert werden. Dies ist eine einfache und effektive Möglichkeit, die Anwendung zu modernisieren und zu beleben und gleichzeitig die Barrierefreiheit, Nutzbarkeit und Auffindbarkeit ihrer Funktionalität zu verbessern.

[Grundlegendes zu Befehlen und Steuerelementen](windowsribbon-commandscontrols.md)

Die Trennung von Logik und Präsentation ist die Entwurfskonzeption, die das Befehlspräsentationssystem des Menübandframeworks inspiriert– ein System, das auf einem Entwurfsmuster basiert, in dem Funktionalität und Verhalten unabhängig von den Steuerelementen implementiert werden, die diese Funktionalität verfügbar machen.

## <a name="user-interface"></a>Benutzeroberfläche

[Angeben von Menübandbildressourcen](windowsribbon-imageformats.md)

Als umfassendes Befehlspräsentationssystem ist das Menübandframework so konzipiert, dass Bildressourcen in der gesamten Menüband-Benutzeroberfläche umfassend unterstützt werden. Alle Bildressourcen werden im [Menübandmarkup](windowsribbon-schema.md) deklariert oder von einer Menübandhostanwendung abgefragt.

Für Windows 8 und höher unterstützt das Menübandframework die folgenden Grafikformate: 32-Bit-ARGB-Bitmapdateien (BMP) und PNG-Dateien (Portable Network Graphics) mit Transparenz.

Für Windows 7 und früher müssen Bildressourcen dem in Windows verwendeten BMP-Standardgrafikformat entsprechen.

[Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien](windowsribbon-templates.md)

Steuerelemente, die auf der Menübandbefehlsleiste gehostet werden, unterliegen Layoutregeln, die vom Menübandframework erzwungen werden und auf einer Kombination aus Standardverhalten und Layoutvorlagen (frameworkdefiniert und benutzerdefiniert) basieren, wie im Menübandmarkup deklariert. Diese Regeln definieren das adaptive Layoutverhalten des Menübandframeworks, das die Anpassung von Steuerelementen in der Befehlsleiste an verschiedene Menübandgrößen zur Laufzeit beeinflusst.

[Arbeiten mit Katalogen](ribbon-controls-galleries.md)

Das Menübandframework bietet Entwicklern ein stabiles und konsistentes Modell für die Verwaltung dynamischer Inhalte über eine Vielzahl von sammlungsbasierten Steuerelementen hinweg. Durch Anpassen und Neukonfigurieren der Menüband-Benutzeroberfläche ermöglichen diese dynamischen Steuerelemente dem Framework, sowohl in der Hostanwendung als auch im Menüband selbst auf Benutzerinteraktionen zu reagieren, und bieten die Flexibilität, verschiedene Laufzeitumgebungen zu verarbeiten.

[Anzeigen kontextabhängiger Registerkarten](ribbon-contextualtabs.md)

In einer Menübandframeworkanwendung ist eine [](windowsribbon-controls-tab.md) kontextbezogene Registerkarte ein ausgeblendetes Registerkartensteuerelement, das in der Registerkartenzeile angezeigt wird, wenn ein Objekt im Arbeitsbereich der Anwendung, z. B. ein Bild, ausgewählt oder hervorgehoben wird.

[Erneutes Konfigurieren des Menübands mit Anwendungsmodi](ribbon-applicationmodes.md)

Das Menübandframework unterstützt das dynamische Neukonfigurieren und Verfügbarmachen von Kernelementen der Menüband-Benutzeroberfläche zur Laufzeit basierend auf dem Zustand der Anwendung (auch als Kontext bezeichnet). Deklariert und bestimmten Elementen im Markup zugeordnet, werden die verschiedenen von einer Anwendung unterstützten Zustände als Anwendungsmodi bezeichnet.

[Anpassen von Menübandfarben](ribbon-color.md)

Das Menübandframework macht eine Reihe von Farbeigenschaften verfügbar, mit denen eine Anwendung die Darstellung verschiedener Elemente der Menübandbenutzeroberfläche zur Laufzeit anpassen kann.

[Anzeigen des Menübands](ribbon-visibility.md)

Das Menübandframework macht eine Reihe von Eigenschaften verfügbar, mit denen eine Anwendung angeben kann, wie die Benutzeroberfläche des Menübands zur Laufzeit angezeigt wird.

## <a name="management"></a>Verwaltung

[Beibehalten des Menübandzustands](ribbon-statepersistence.md)

Das Windows-Frameworks (Menüband) bietet die Möglichkeit, den Zustand einer Vielzahl von Benutzereinstellungen und -einstellungen über Anwendungssitzungen hinweg beizubehalten.

[Lauschen auf Menübandereignisse](listening-for-ribbon-events.md)

Das Menübandframework verwendet die [ETW-Infrastruktur (Event Tracing for Windows),](../etw/event-tracing-portal.md) damit Entwickler lernen können, wie Benutzer mit dem Menüband ihrer Anwendung interagieren.

## <a name="markup-compiler"></a>Markupcompiler

[Kompilieren von Menübandmarkup](windowsribbon-intentcl.md)

Damit das Menübandframework die [Menüband-Markupdatei](windowsribbon-schema.md) nutzen kann, muss die Markupdatei in eine Ressourcendatei im Binärformat kompiliert werden. Ein dedizierter Markupcompiler, der UI COMMAND Compiler (UICC), ist zu diesem Zweck im Microsoft Windows Software Development Kit (SDK) (7.0 oder höher) enthalten. Zusätzlich zum Kompilieren der binären Version des Markups generiert UICC eine ID-Definitionsheaderdatei (.h), die alle Markupelemente für die Menübandhostanwendung und eine Ressourcendatei (RC) verfügbar macht, mit der Image- und Zeichenfolgenressourcen zur Buildzeit mit der Hostanwendung verknüpft werden.

[Grundlegendes zu Markupcompilernachrichten](windowsribbon-compilationerrors.md)

Der Windows Menübandframework-Markupcompiler ,UI Command Compiler (UICC.exe) überprüft das Menübandmarkup anhand des Menübandschemas und eines zusätzlichen Regelsatzes, der vom Menübandframework definiert wird.

 

 