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
# <a name="accessing-spreadsheet-content"></a><span data-ttu-id="300cc-107">Zugreifen auf den Tabelleninhalt</span><span class="sxs-lookup"><span data-stu-id="300cc-107">Accessing Spreadsheet Content</span></span>

<span data-ttu-id="300cc-108">Ein Text [basiertes Steuerelement](uiauto-implementingspreadsheetitem.md) , das Tabelleninhalt enthält, kann Clients den Zugriff auf den Inhalt ermöglichen, indem er das [Tabellen Kalkulations](uiauto-implementingspreadsheet.md) Steuerelement-Steuerelement Muster unterstützt.</span><span class="sxs-lookup"><span data-stu-id="300cc-108">A text-based control that contains spreadsheet content can enable clients to access the content by supporting the [Spreadsheet](uiauto-implementingspreadsheet.md) and [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) control patterns.</span></span> <span data-ttu-id="300cc-109">In diesem Thema wird beschrieben, wie Microsoft UI Automation-Client Anwendungen auf den Inhalt einer Kalkulations Tabelle zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="300cc-109">This topic describes how Microsoft UI Automation client applications can access the content of a spreadsheet.</span></span>

<span data-ttu-id="300cc-110">Um zu ermitteln, ob ein textbasiertes Steuerelement das [Kalkulations Tabellen](uiauto-implementingspreadsheet.md) -und das [spreadsheetitem](uiauto-implementingspreadsheetitem.md) -Steuerelement Muster unterstützt, rufen Sie zuerst die [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle für das Steuer [Element](uiauto-obtainingelements.md)ab Aufrufen Sie als nächstes die [**iuiautomationelement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) -Methode, und geben Sie dabei den Steuerelement Muster Bezeichner [**UIA \_ spreadsheetpatternid**](uiauto-controlpattern-ids.md) oder [**UIA \_ spreadsheetitempatternid**](uiauto-controlpattern-ids.md)und eine Variante an, die true erhält, wenn das Steuerelement ein bestimmtes Steuerelement Muster unterstützt.</span><span class="sxs-lookup"><span data-stu-id="300cc-110">To determine whether a text-based control supports the [Spreadsheet](uiauto-implementingspreadsheet.md) and [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) control patterns, first retrieve the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface for the control (see [Obtaining UI Automation Elements](uiauto-obtainingelements.md).) Next, call the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method, specifying a control pattern identifier of [**UIA\_SpreadsheetPatternId**](uiauto-controlpattern-ids.md) or [**UIA\_SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md), and a variant that receives TRUE if the control supports the particular control pattern.</span></span>

<span data-ttu-id="300cc-111">Um auf den Tabelleninhalt zuzugreifen, rufen Sie die [**iuiautomationspreadsheetpattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) -Schnittstelle ab, indem Sie die [**iuiautomationelement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) -Methode aufrufen und [**UIA \_ spreadsheetpatternid**](uiauto-controlpattern-ids.md) als Steuerelement Muster Bezeichner angeben.</span><span class="sxs-lookup"><span data-stu-id="300cc-111">To access the spreadsheet content, retrieve the [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) interface by calling [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method and specifying [**UIA\_SpreadsheetPatternId**](uiauto-controlpattern-ids.md) as the control pattern identifier.</span></span> <span data-ttu-id="300cc-112">Verwenden Sie als nächstes die [**iuiautomationspreadsheetpattern:: GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) -Methode, um die [**iuiautomationspreadsheetitem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) -Schnittstelle für ein bestimmtes Tabellen Element (in der Regel eine Zelle) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="300cc-112">Next, use the [**IUIAutomationSpreadsheetPattern::GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) method to get the [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) interface for a particular spreadsheet item (typically a cell).</span></span> <span data-ttu-id="300cc-113">Verwenden Sie die Eigenschaften und Methoden der **iuiautomationspreadsheetitem** -Schnittstelle, um die Formel für die Zelle und alle Anmerkungen, die der Zelle zugeordnet sind, abzurufen.</span><span class="sxs-lookup"><span data-stu-id="300cc-113">Use the properties and methods of the **IUIAutomationSpreadsheetItem** interface to retrieve the formula for the cell, and any annotations associated with the cell.</span></span> <span data-ttu-id="300cc-114">Weitere Informationen zu Anmerkungen finden Sie unter Abrufen von Anmerkungen [.](uiauto-usingtextrangeobjects.md)</span><span class="sxs-lookup"><span data-stu-id="300cc-114">For more information about annotations, see [Retrieving Annotations.](uiauto-usingtextrangeobjects.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="300cc-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="300cc-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="300cc-116">Benutzeroberflächenautomatisierungs-Unterstützung für Textinhalte</span><span class="sxs-lookup"><span data-stu-id="300cc-116">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="300cc-117">Arbeiten mit Text basierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="300cc-117">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 