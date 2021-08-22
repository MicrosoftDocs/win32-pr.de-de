---
title: Zugreifen auf Tabellenkalkulationsinhalte
description: In diesem Thema wird beschrieben, Benutzeroberflächenautomatisierung Microsoft-Clientanwendungen auf den Inhalt einer Kalkulationstabelle zugreifen können.
ms.assetid: F32EFA46-222B-4A4E-9938-10DE0F6A2CA7
keywords:
- Clients,Zugreifen auf Tabelleninhalt
- Clients,textbasierte Steuerelemente
- Clients, Tabellenkalkulationssteuermuster
- clients,SpreadsheetItem-Steuerelementmuster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09d34aeb484da056920a2b77d47ca199e11c00c99832412e9bf007807c49563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052348"
---
# <a name="accessing-spreadsheet-content"></a>Zugreifen auf Tabellenkalkulationsinhalte

Ein textbasiertes Steuerelement, das Tabellenkalkulationsinhalte enthält, kann Clients den Zugriff auf den Inhalt ermöglichen, indem die Steuerelementmuster [Spreadsheet](uiauto-implementingspreadsheet.md) und [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) unterstützt werden. In diesem Thema wird beschrieben, Benutzeroberflächenautomatisierung Microsoft-Clientanwendungen auf den Inhalt einer Kalkulationstabelle zugreifen können.

Um zu bestimmen, ob ein textbasiertes Steuerelement die Steuerelementmuster [Spreadsheet](uiauto-implementingspreadsheet.md) und [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) unterstützt, rufen Sie zunächst die [**IUIAutomationElement-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) für das Steuerelement ab (siehe Abrufen von Benutzeroberflächenautomatisierung [Elements](uiauto-obtainingelements.md).) Rufen Sie als Nächstes die [**IUIAutomationElement::GetCurrentPattern-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) auf, und geben Sie dabei einen Steuerelementmusterbezeichner von [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) oder [**UIA \_ SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md)und eine Variante an, die TRUE empfängt, wenn das Steuerelement das bestimmte Steuerelementmuster unterstützt.

Um auf den Tabelleninhalt zu zugreifen, rufen Sie die [**IUIAutomationSpreadsheetPattern-Schnittstelle**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) ab, indem Sie die [**IUIAutomationElement::GetCurrentPattern-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) aufrufen und [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) als Steuerelementmusterbezeichner angeben. Verwenden Sie als Nächstes die [**IUIAutomationSpreadsheetPattern::GetItemByName-Methode,**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) um die [**IUIAutomationSpreadsheetItem-Schnittstelle**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) für ein bestimmtes Arbeitsblattelement (in der Regel eine Zelle) zu erhalten. Verwenden Sie die Eigenschaften und Methoden der **IUIAutomationSpreadsheetItem-Schnittstelle,** um die Formel für die Zelle und alle anmerkungen abzurufen, die der Zelle zugeordnet sind. Weitere Informationen zu Anmerkungen finden Sie unter [Abrufen von Anmerkungen.](uiauto-usingtextrangeobjects.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzeroberflächenautomatisierung Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Arbeiten mit textbasierten Steuerelementen](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 