---
title: Übersicht über die Benutzeroberflächenautomatisierungs-Struktur
description: Hilfstechnologieprodukte und Testskripts navigieren in der Microsoft Benutzeroberflächenautomatisierung-Struktur, um Informationen zur Benutzeroberfläche und ihren Elementen zu sammeln.
ms.assetid: f3afe258-baa7-41b5-a27e-cdc94b467d73
keywords:
- Benutzeroberflächenautomatisierung,Strukturübersicht
- Benutzeroberflächenautomatisierung,Ansicht der Struktur
- Benutzeroberflächenautomatisierung,Rohansicht der Struktur
- Benutzeroberflächenautomatisierung,Steuerelementansicht der Struktur
- Benutzeroberflächenautomatisierung,Inhaltsansicht der Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e1b8776f86931882acc85e2fb974ff5d1db0be266be94e391ce242ff2a497e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570399"
---
# <a name="ui-automation-tree-overview"></a>Übersicht über die Benutzeroberflächenautomatisierungs-Struktur

Hilfstechnologieprodukte und Testskripts navigieren in der Microsoft Benutzeroberflächenautomatisierung-Struktur, um Informationen zur Benutzeroberfläche und ihren Elementen zu sammeln.

In der Benutzeroberflächenautomatisierung struktur ein Stammelement, das das Windows Desktopfenster darstellt und dessen untergeordnete Elemente Anwendungsfenster darstellen. Jedes dieser untergeordneten Elemente kann Elemente enthalten, die Teile der Benutzeroberfläche darstellen, z. B. Menüs, Schaltflächen, Symbolleisten und Listenfelder. Diese Elemente können Elemente enthalten, z. B. Listenelemente.

Die Benutzeroberflächenautomatisierung struktur ist keine feste Struktur. Es ist selten in seiner Gesamtanzahl zu sehen, da es Tausende von Elementen enthalten kann. Teile der Benutzeroberflächenautomatisierung werden so erstellt, wie sie von einem Client benötigt werden, und die Struktur der Struktur ändert sich, wenn Elemente hinzugefügt, verschoben oder entfernt werden.

Benutzeroberflächenautomatisierung-Anbieter unterstützen die Benutzeroberflächenautomatisierung Struktur, indem sie die Navigation zwischen Elementen in einem Fragment implementieren. Ein Fragment ist eine vollständige Teilstruktur von Elementen aus einem bestimmten Framework und verfügt über ein Stammelement (als Fragmentstamm *bezeichnet),* das in der Regel in einem Fenster gehostet wird.

Anbieter haben keine Sorge um die Navigation von einem Steuerelement zu einem anderen. Dies wird vom Benutzeroberflächenautomatisierung Core verwaltet, der Informationen von den Standardfensteranbietern verwendet.

Dieses Thema enthält folgende Abschnitte:

-   [Ansichten der Benutzeroberflächenautomatisierung Struktur](#views-of-the-ui-automation-tree)
    -   [Rohdatenansicht](#raw-view)
    -   [Steuerelementansicht](#control-view)
    -   [Inhaltsansicht](#content-view)
-   [Zugehörige Themen](#related-topics)

## <a name="views-of-the-ui-automation-tree"></a>Ansichten der Benutzeroberflächenautomatisierung Struktur

Die Benutzeroberflächenautomatisierung kann gefiltert werden, um Ansichten zu erstellen, die nur die Benutzeroberflächenautomatisierung enthalten, die für einen bestimmten Client relevant sind. Mit diesem Ansatz können Clients die Struktur anpassen, die durch Benutzeroberflächenautomatisierung ihren speziellen Anforderungen dargestellt wird.

Der Client kann die Ansicht anpassen, indem er bereichs- und filtert. Bereichsausschnitt definiert den Umfang der Ansicht, beginnend mit einem Basiselement. Die Anwendung möchte beispielsweise nur direkte untergeordnete Elemente des Desktops oder alle Nachfolger eines Anwendungsfensters finden. Beim Filtern werden die Typen von Elementen definiert, die in der Ansicht enthalten sind.

Benutzeroberflächenautomatisierung-Anbieter das Filtern durch Definieren von Eigenschaften für Elemente, einschließlich der [**Eigenschaften IUIAutomationElement::IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) und [**IUIAutomationElement::IsContentElement.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement)

Benutzeroberflächenautomatisierung bietet drei Standardansichten: rohe Ansicht, Steuerelementansicht und Inhaltsansicht. Diese Ansichten werden durch den Typ der ausgeführten Filterung definiert. Der Bereich einer Ansicht wird von der Anwendung definiert. Die Anwendung kann andere Filter auf Eigenschaften anwenden. Zum Beispiel, um nur aktivierte Steuerelemente in eine Steuerelementansicht ein include.

### <a name="raw-view"></a>Rohdatenansicht

Die rohe Ansicht der Benutzeroberflächenautomatisierung struktur ist die vollständige Struktur von Automatisierungselementen, für die der Desktop der Stamm ist. Die Unformatierungsansicht folgt eng der nativen programmgesteuerten Struktur einer Anwendung und ist die ausführlichste verfügbare Ansicht. Sie stellt gleichzeitig die Basis zum Erstellen anderer Ansichten der Struktur dar. Da diese Ansicht vom zugrunde liegenden Benutzeroberflächenframework abhängt, verfügt die unformatierten Ansicht einer Windows Presentation Foundation-Schaltfläche (WPF) über eine andere rohe Ansicht als eine Microsoft Win32-Schaltfläche.

Die Unformatierungsansicht wird durch Suchen nach Elementen ohne Angabe von Eigenschaften oder mithilfe von [**IUIAutomation::RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker) zum Erhalten einer [**IUIAutomationTreeWalker-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) zum Navigieren in der Struktur ermittelt.

### <a name="control-view"></a>Steuerelementansicht

Die Steuerelementansicht ist eine Teilmenge der Rohdatenansicht. Sie enthält nur die Benutzeroberflächenelemente, für die die [**IUIAutomationElement::IsControlElement-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) auf **TRUE festgelegt ist.**

Die Steuerelementansicht enthält die Benutzeroberflächenelemente, die dem Benutzer Informationen bereitstellen oder dem Benutzer das Ausführen einer Aktion ermöglichen. Dies sind die Benutzeroberflächenelemente, die für automatisierte Testanwendungen am interessantesten sind.

Die Steuerelementansicht enthält auch nichtinteraktive Ui-Elemente, die zur logischen Struktur der Benutzeroberfläche beitragen. Dazu gehören Elementcontainer wie Listenansichtsheader, Symbolleisten, Menüs und die Statusleiste. Andere nichtinteraktive Elemente, die in der Steuerelementansicht angezeigt werden, sind Grafiken mit Informationen und statischem Text in einem Dialogfeld.

Nichtinteraktive Elemente, die nur für Layout- oder deaktive Zwecke verwendet werden, z. B. Bereiche, die zum Layout von Steuerelementen in einem Dialogfeld verwendet werden, werden nicht in der Steuerelementansicht angezeigt.

Die Steuerelementansicht der Benutzeroberflächenautomatisierung struktur ist eng mit der Benutzeroberflächenstruktur verknüpft, die von einem Endbenutzer wahrgenommen wird. Dies erleichtert es dem Hilfstechnologieprodukt, die Benutzeroberfläche für den Endbenutzer zu beschreiben und diesen Endbenutzer bei der Interaktion mit der Anwendung zu unterstützen.

Die Steuerelementansicht wird durch Suchen nach Elementen, für die die [**IUIAutomationElement::IsControlElement-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) auf TRUE festgelegt ist, oder durch Verwenden von [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) zum Erhalten einer [**IUIAutomationTreeWalker-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) zum Navigieren in der Struktur ermittelt.

### <a name="content-view"></a>Inhaltsansicht

Die Inhaltsansicht der Benutzeroberflächenautomatisierung struktur ist eine Teilmenge der Steuerelementansicht. Es enthält nur die Benutzeroberflächenelemente, für die sowohl [**das IUIAutomationElement::IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) als auch die [**IUIAutomationElement::IsContentElement-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) auf **TRUE festgelegt ist.**

Die Inhaltsansicht enthält Benutzeroberflächenelemente, die die tatsächlichen Informationen in einer Benutzeroberfläche vermitteln, einschließlich Benutzeroberflächenelementen, die den Tastaturfokus erhalten können, und Text, der keine Bezeichnung für ein Benutzeroberflächenelement ist. Dies sind die Benutzeroberflächenelemente, die für eine Sprachausgabeanwendung am interessantesten sind. Beispielsweise werden die Werte in einem Dropdown-Kombinationsfeld in der Inhaltsansicht angezeigt, da die Werte Informationen darstellen, die von einem Endbenutzer verwendet werden.

In der Inhaltsansicht werden ein Kombinationsfeld und ein Listenfeld als Sammlung von Benutzeroberflächenelementen dargestellt, in denen ein oder mehrere Elemente ausgewählt werden können. Die Tatsache, dass ein Element immer geöffnet ist und ein Element erweitert und reduziert werden kann, ist in der Inhaltsansicht irrelevant, da es so konzipiert ist, dass die Daten oder Inhalte angezeigt werden, die dem Benutzer angezeigt werden.

Die Inhaltsansicht wird durch Suchen nach Elementen ermittelt, bei denen sowohl die [**IsControlElement-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) als auch [**die CurrentIsContentElement-Eigenschaft**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) auf **TRUE** festgelegt ist, oder indem [**IUIAutomation::ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) verwendet wird, um eine [**IUIAutomationTreeWalker-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) zum Navigieren in der Struktur zu erhalten.

Die folgenden Abbildungen zeigen die Unterschiede zwischen der Steuerelementansicht und der Inhaltsansicht. Die erste Abbildung zeigt ein einfaches Kombinationsfeld mit drei Elementen in der Dropdownliste. Die zweite Abbildung zeigt, wie die Benutzeroberflächenelemente des Kombinationsfelds in den Steuerelement- und Inhaltsansichten der UISpy.exe angezeigt werden.

![Screenshot eines einfachen Kombinationsfelds mit drei Dropdownelementen](images/combobox.png)

![Screenshot der uispy-Anwendung mit Steuerelement- und Inhaltsansichten von Kombinationsfeldelementen](images/treeviews.jpg)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Erstellen des CUIAutomation-Objekts](uiauto-creatingcuiautomation.md)
</dt> <dt>

[Abrufen von Benutzeroberflächenautomatisierungs-Elementen](uiauto-obtainingelements.md)
</dt> <dt>

[Grundlagen der Benutzeroberflächenautomatisierung](entry-uiautocore-overview.md)
</dt> </dl>

 

 




