---
title: Übersicht über die Benutzeroberflächenautomatisierungs-Struktur
description: Hilfstechnologieprodukte und Test Skripts Navigieren in der Microsoft UI Automation-Struktur zum Sammeln von Informationen über die Benutzeroberfläche und deren Elemente.
ms.assetid: f3afe258-baa7-41b5-a27e-cdc94b467d73
keywords:
- UI-Automatisierung, Übersicht über die Struktur
- UI-Automatisierung, Strukturansicht
- Benutzeroberflächen Automatisierung, unformatierte Ansicht der Struktur
- UI-Automatisierung, Steuerelement Ansicht der Struktur
- UI-Automatisierung, Inhaltsansicht von Tree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76bc9aa6568a3f4d63194d35ff0c7d8f59510c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855939"
---
# <a name="ui-automation-tree-overview"></a>Übersicht über die Benutzeroberflächenautomatisierungs-Struktur

Hilfstechnologieprodukte und Test Skripts Navigieren in der Microsoft UI Automation-Struktur zum Sammeln von Informationen über die Benutzeroberfläche und deren Elemente.

In der Benutzeroberflächenautomatisierungs-Struktur ist ein Stamm Element, das das Windows-Desktop Fenster ("der Desktop") darstellt und dessen untergeordnete Elemente Anwendungsfenster darstellen. Jedes dieser untergeordneten Elemente kann Elemente enthalten, die Teile der Benutzeroberfläche darstellen, z. b. Menüs, Schaltflächen, Symbolleisten und Listenfelder. Diese Elemente können Elemente enthalten, wie z. b. Listenelemente.

Die Benutzeroberflächenautomatisierungs-Struktur ist keine Fixed-Struktur. Es ist selten in seiner Gesamtheit zu sehen, da es Tausende von Elementen enthalten kann. Teile der Benutzeroberflächenautomatisierungs-Struktur werden erstellt, wenn Sie von einem Client benötigt werden, und die Struktur der Struktur ändert sich, wenn Elemente hinzugefügt, verschoben oder entfernt werden.

Benutzeroberflächenautomatisierungs-Anbieter unterstützen die Benutzeroberflächenautomatisierungs-Struktur durch Implementieren der Navigation zwischen Elementen in einem Fragment Ein Fragment ist eine gesamte Unterstruktur von Elementen eines bestimmten Frameworks und verfügt über ein Stamm Element (das als *Fragmentstamm* bezeichnet wird), das in der Regel in einem-Fenster gehostet wird.

Die Navigation von einem Steuerelement zu einem anderen ist nicht von den Anbietern betroffen. Diese wird vom Benutzeroberflächenautomatisierungs-Kern verwaltet, der Informationen aus den Standardfenster Anbietern verwendet.

Dieses Thema enthält folgende Abschnitte:

-   [Ansichten der Benutzeroberflächenautomatisierungs-Struktur](#views-of-the-ui-automation-tree)
    -   [Rohdaten Ansicht](#raw-view)
    -   [Steuerelement Ansicht](#control-view)
    -   [Inhaltsansicht](#content-view)
-   [Zugehörige Themen](#related-topics)

## <a name="views-of-the-ui-automation-tree"></a>Ansichten der Benutzeroberflächenautomatisierungs-Struktur

Die Benutzeroberflächenautomatisierungs-Struktur kann gefiltert werden, um Ansichten zu erstellen, die nur die Benutzeroberflächen-Automatisierungselemente enthalten, die für einen bestimmten Client relevant sind. Dieser Ansatz ermöglicht es Clients, die Struktur, die über die Benutzeroberflächen Automatisierung dargestellt wird, an Ihre speziellen Anforderungen anzupassen.

Der Client kann die Ansicht anpassen, indem er den Bereich und die Filterung durch filtert. Die Bereichs Definition definiert den Umfang der Sicht, beginnend mit einem Basiselement. Die Anwendung kann z. b. nur direkt untergeordnete Elemente des Desktops oder alle nachfolgenden Elemente eines Anwendungsfensters suchen. Beim Filtern werden die Elementtypen definiert, die in der Sicht enthalten sind.

Benutzeroberflächenautomatisierungs-Anbieter unterstützen das Filtern, indem Sie Eigenschaften für Elemente definieren, einschließlich der Eigenschaften [**iuiautomationelement:: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) und [**iuiautomationelement:: IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) .

Die Benutzeroberflächen Automatisierung bietet drei Standardansichten: Rohdaten Ansicht, Steuerelement Ansicht und Inhaltsansicht. Diese Sichten werden durch den Typ der durchgeführten Filterung definiert. Der Gültigkeitsbereich einer beliebigen Ansicht wird von der Anwendung definiert. Die Anwendung kann andere Filter auf Eigenschaften anwenden. So können Sie beispielsweise nur aktivierte Steuerelemente in eine Steuerelement Ansicht einschließen.

### <a name="raw-view"></a>Rohdatenansicht

Die Rohdaten Ansicht der Benutzeroberflächenautomatisierungs-Struktur ist die vollständige Struktur der Automatisierungselemente, für die der Desktop das Stammverzeichnis ist. Die Rohdaten Ansicht folgt genau der systemeigenen programmgesteuerten Struktur einer Anwendung, und ist die ausführlichste verfügbare Sicht. Sie stellt gleichzeitig die Basis zum Erstellen anderer Ansichten der Struktur dar. Da diese Ansicht vom zugrunde liegenden UI-Framework abhängt, hat die unformatierte Ansicht einer Windows Presentation Foundation-Schaltfläche (WPF) eine andere unformatierte Ansicht als eine Microsoft Win32-Schaltfläche.

Die Rohdaten Ansicht wird abgerufen, indem nach Elementen gesucht wird, ohne Eigenschaften anzugeben, oder indem [**iuiautomation:: RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker) verwendet wird, um eine [**iuiautomationtreewalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) -Schnittstelle zum Navigieren in der Struktur zu erhalten.

### <a name="control-view"></a>Steuerelementansicht

Die Steuerelementansicht ist eine Teilmenge der Rohdatenansicht. Sie enthält nur die Elemente der Benutzeroberfläche, für die die [**iuiautomationelement:: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) -Eigenschaft auf **true** festgelegt ist.

Die Steuerelement Ansicht enthält die Benutzeroberflächen Elemente, die dem Benutzerinformationen zur Verfügung stellen oder dem Benutzer die Ausführung einer Aktion ermöglichen. Dies sind die Elemente der Benutzeroberfläche, die für automatisierte Testanwendungen am interessantesten sind.

Die Steuerelement Ansicht umfasst auch nicht interaktive Benutzeroberflächen Elemente, die zur logischen Struktur der Benutzeroberfläche beitragen. Dazu zählen Element Container wie Listen Ansichts Header, Symbolleisten, Menüs und die Statusleiste. Andere nicht interaktive Elemente, die in der Steuerelement Ansicht angezeigt werden, sind Grafiken mit Informationen und statischem Text in einem Dialogfeld.

Nicht interaktive Elemente, die nur für Layout oder dekorative Zwecke verwendet werden, z. b. Bereiche, die zum Anordnen von Steuerelementen in einem Dialogfeld verwendet werden, werden in der Steuerelement Ansicht nicht angezeigt.

Die Steuerelement Ansicht der Benutzeroberflächenautomatisierungs-Struktur ist der Benutzeroberflächen Struktur, die von einem Endbenutzer erkannt wird, eng zugeordnet. Dies erleichtert es dem Hilfstechnologieprodukt, die Benutzeroberfläche für den Endbenutzer zu beschreiben und den Endbenutzer bei der Interaktion mit der Anwendung zu unterstützen.

Die Steuerelement Ansicht wird abgerufen, indem Sie nach Elementen suchen, für die die [**iuiautomationelement:: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) -Eigenschaft auf true festgelegt ist, oder indem Sie [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) verwenden, um eine [**iuiautomationtreewalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) -Schnittstelle zum Navigieren in der Struktur zu erhalten.

### <a name="content-view"></a>Inhaltsansicht

Die Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur ist eine Teilmenge der Steuerelement Ansicht. Sie enthält nur die Elemente der Benutzeroberfläche, für die sowohl das [**iuiautomationelement:: IsControlElement-Element**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) als auch die [**iuiautomationelement:: IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) -Eigenschaft auf **true** festgelegt ist.

Die Inhaltsansicht enthält Elemente der Benutzeroberfläche, die die tatsächlichen Informationen in einer Benutzeroberfläche übermitteln, einschließlich Elemente der Benutzeroberfläche, die den Tastaturfokus erhalten können, sowie Text, der keine Bezeichnung für ein UI-Element ist. Dabei handelt es sich um die Benutzeroberflächen Elemente, die für eine Bildschirm Leseanwendung am interessantesten sind. Beispielsweise werden die Werte in einem Dropdown-Kombinations Feld in der Inhaltsansicht angezeigt, da die Werte Informationen darstellen, die von einem Endbenutzer verwendet werden.

In der Inhaltsansicht werden ein Kombinations Feld und ein Listenfeld als eine Auflistung von UI-Elementen dargestellt, bei denen mindestens ein Element ausgewählt werden kann. Die Tatsache, dass ein Element immer geöffnet ist und ein Element erweitert und reduziert werden kann, ist in der Inhaltsansicht irrelevant, da es so konzipiert ist, dass es die Daten oder Inhalte anzeigt, die dem Benutzer angezeigt werden.

Die Inhaltsansicht wird abgerufen, indem nach Elementen gesucht wird, für die sowohl das [**IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) -als [**auch das-Element auf**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) **true** festgelegt ist, oder indem [**iuiautomation:: ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) verwendet wird, um eine [**iuiautomationtreewalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) -Schnittstelle zum Navigieren in der Struktur zu erhalten.

Die folgenden Abbildungen zeigen die Unterschiede zwischen der Steuerelement Ansicht und der Inhaltsansicht. In der ersten Abbildung wird ein einfaches Kombinations Feld mit drei Elementen in der Dropdown Liste angezeigt. Die zweite Abbildung zeigt, wie die Kombinations Feld-UI-Elemente in den Steuerelement-und Inhalts Ansichten der UISpy.exe Anwendung angezeigt werden.

![Screenshot eines einfachen Kombinations Felds mit drei Dropdown Elementen](images/combobox.png)

![Screenshot der UISpy-Anwendung mit Steuerelement-und Inhalts Ansichten von Kombinations Feld Elementen](images/treeviews.jpg)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Erstellen des cuiautomation-Objekts](uiauto-creatingcuiautomation.md)
</dt> <dt>

[Abrufen von Benutzeroberflächenautomatisierungs-Elementen](uiauto-obtainingelements.md)
</dt> <dt>

[Grundlagen der Benutzeroberflächenautomatisierung](entry-uiautocore-overview.md)
</dt> </dl>

 

 




