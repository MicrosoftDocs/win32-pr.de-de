---
title: Zugreifen auf den Tabelleninhalt
description: In diesem Thema wird beschrieben, wie Microsoft UI Automation-Client Anwendungen auf den Inhalt einer Kalkulations Tabelle zugreifen können.
ms.assetid: F32EFA46-222B-4A4E-9938-10DE0F6A2CA7
keywords:
- Clients, Zugriff auf Tabelleninhalt
- Clients, textbasierte Steuerelemente
- Clients, Tabellen Steuerungs Muster
- Client, spreadsheetitem-Steuerelement Muster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31495086614f34aeff378a8565200fa03f2dad62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316232"
---
# <a name="accessing-spreadsheet-content"></a>Zugreifen auf den Tabelleninhalt

Ein Text [basiertes Steuerelement](uiauto-implementingspreadsheetitem.md) , das Tabelleninhalt enthält, kann Clients den Zugriff auf den Inhalt ermöglichen, indem er das [Tabellen Kalkulations](uiauto-implementingspreadsheet.md) Steuerelement-Steuerelement Muster unterstützt. In diesem Thema wird beschrieben, wie Microsoft UI Automation-Client Anwendungen auf den Inhalt einer Kalkulations Tabelle zugreifen können.

Um zu ermitteln, ob ein textbasiertes Steuerelement das [Kalkulations Tabellen](uiauto-implementingspreadsheet.md) -und das [spreadsheetitem](uiauto-implementingspreadsheetitem.md) -Steuerelement Muster unterstützt, rufen Sie zuerst die [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle für das Steuer [Element](uiauto-obtainingelements.md)ab Aufrufen Sie als nächstes die [**iuiautomationelement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) -Methode, und geben Sie dabei den Steuerelement Muster Bezeichner [**UIA \_ spreadsheetpatternid**](uiauto-controlpattern-ids.md) oder [**UIA \_ spreadsheetitempatternid**](uiauto-controlpattern-ids.md)und eine Variante an, die true erhält, wenn das Steuerelement ein bestimmtes Steuerelement Muster unterstützt.

Um auf den Tabelleninhalt zuzugreifen, rufen Sie die [**iuiautomationspreadsheetpattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) -Schnittstelle ab, indem Sie die [**iuiautomationelement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) -Methode aufrufen und [**UIA \_ spreadsheetpatternid**](uiauto-controlpattern-ids.md) als Steuerelement Muster Bezeichner angeben. Verwenden Sie als nächstes die [**iuiautomationspreadsheetpattern:: GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) -Methode, um die [**iuiautomationspreadsheetitem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) -Schnittstelle für ein bestimmtes Tabellen Element (in der Regel eine Zelle) abzurufen. Verwenden Sie die Eigenschaften und Methoden der **iuiautomationspreadsheetitem** -Schnittstelle, um die Formel für die Zelle und alle Anmerkungen, die der Zelle zugeordnet sind, abzurufen. Weitere Informationen zu Anmerkungen finden Sie unter Abrufen von Anmerkungen [.](uiauto-usingtextrangeobjects.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzeroberflächenautomatisierungs-Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Arbeiten mit Text basierten Steuerelementen](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 