---
title: Grundlegendes zum Text Objektmodell für die Benutzeroberflächen Automatisierung
description: In diesem Thema wird beschrieben, wie Microsoft UI Automation-Client Anwendungen auf den Text Inhalt eines textbasierten Steuer Elements zugreifen.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- Clients, Grundlegendes zum Textobjekt Modell der Benutzeroberflächen Automatisierung
- Clients, textbasierte Steuerelemente
- Clients, Textbereiche
- Clients, Text-Steuerelement Muster
- Clients, TextRange-Steuerelement Muster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6dae1fc5ca02af69ab3d5386461e6bd7a864d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709341"
---
# <a name="understanding-the-ui-automation-text-object-model"></a><span data-ttu-id="0918a-108">Grundlegendes zum Text Objektmodell für die Benutzeroberflächen Automatisierung</span><span class="sxs-lookup"><span data-stu-id="0918a-108">Understanding the UI Automation Text Object Model</span></span>

<span data-ttu-id="0918a-109">In diesem Thema wird beschrieben, wie Microsoft UI Automation-Client Anwendungen auf den Text Inhalt eines textbasierten Steuer Elements zugreifen.</span><span class="sxs-lookup"><span data-stu-id="0918a-109">This topic describes how Microsoft UI Automation client applications access the textual content of a text-based control.</span></span>

-   [<span data-ttu-id="0918a-110">Steuerelement spezifisches Objektmodell</span><span class="sxs-lookup"><span data-stu-id="0918a-110">Control-specific Object Model</span></span>](#control-specific-object-model)
-   [<span data-ttu-id="0918a-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0918a-111">Related topics</span></span>](#related-topics)

<span data-ttu-id="0918a-112">Text basierte Steuerelemente machen Textinhalte für Benutzeroberflächenautomatisierungs-Client Anwendungen über ein einfaches Textobjekt Modell verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0918a-112">Text-based controls expose textual content to UI Automation client applications through a simple text object model.</span></span> <span data-ttu-id="0918a-113">Client Anwendungen können über die [Text-und TextRange](uiauto-about-text-and-textrange-patterns.md) -Steuerelement Muster-Schnittstellen auf das Textobjekt Modell zugreifen, einschließlich [**iuiautomationtextpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) und [**iuiautomationtextrange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange).</span><span class="sxs-lookup"><span data-stu-id="0918a-113">Client applications have access to the text object model through the [Text and TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern interfaces, including [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange).</span></span> <span data-ttu-id="0918a-114">Client Anwendungen können diese Schnittstellen verwenden, um Textinhalte, Text Attribute und eingebettete Objekte wie Tabellen und Hyperlinks aus textbasierten Steuerelementen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0918a-114">Client applications can use these interfaces to retrieve textual content, text attributes, and embedded objects such as tables and hyperlinks from text-based controls.</span></span>

<span data-ttu-id="0918a-115">Steuerelement Typen, die das Objektmodell für die Benutzeroberflächen Automatisierung unterstützen, enthalten die Steuerelement Typen [Bearbeiten](uiauto-supporteditcontroltype.md) und [Dokument](uiauto-supportdocumentcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="0918a-115">Control types that support the UI Automation text object model include the [Edit](uiauto-supporteditcontroltype.md) and [Document](uiauto-supportdocumentcontroltype.md) control types.</span></span> <span data-ttu-id="0918a-116">Andere Steuerelement Typen, [](uiauto-supporttooltipcontroltype.md) z. b. QuickInfo und [Text](uiauto-supporttextcontroltype.md) , unterstützen möglicherweise auch das Text Objektmodell, sind jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0918a-116">Other control types such as [ToolTip](uiauto-supporttooltipcontroltype.md) and [Text](uiauto-supporttextcontroltype.md) might also support the text object model, but they are not required to.</span></span>

> [!Note]  
> <span data-ttu-id="0918a-117">Das Benutzeroberflächen Automatisierungs-Textobjekt Modell bietet keine Möglichkeit, Text einzufügen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0918a-117">The UI Automation text object model does not provide a means to insert or modify text.</span></span> <span data-ttu-id="0918a-118">Einige Steuerelemente ermöglichen es jedoch, Text entweder über die [**iuiautomationvaluepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) -Schnittstelle oder durch direkte Tastatureingaben einzufügen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0918a-118">However, some controls enable text to be inserted or modified either through the [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) interface, or through direct keyboard input.</span></span>

 

## <a name="control-specific-object-model"></a><span data-ttu-id="0918a-119">Steuerelement spezifisches Objektmodell</span><span class="sxs-lookup"><span data-stu-id="0918a-119">Control-specific Object Model</span></span>

<span data-ttu-id="0918a-120">Ein textbasiertes Steuerelement, das seinen eigenen Dokumentobjektmodell (DOM) implementiert, kann das DOM durch Implementieren des [ObjectModel](uiauto-implementingobjectmodel.md) -Steuerelement Musters verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="0918a-120">A text-based control that implements its own Document Object Model (DOM) can expose the DOM by implementing the [ObjectModel](uiauto-implementingobjectmodel.md) control pattern.</span></span> <span data-ttu-id="0918a-121">Wenn Sie das DOM verfügbar machen, können Client Anwendungen den Inhalt eines textbasierten Steuer Elements besser aufrufen und steuern.</span><span class="sxs-lookup"><span data-stu-id="0918a-121">Exposing the DOM can give client applications greater access to, and control over, the content of a text-based control.</span></span>

<span data-ttu-id="0918a-122">Eine Client Anwendung kann ermitteln, ob ein bestimmtes textbasiertes Steuerelement ein DOM durch Abrufen der [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle des Steuer Elements implementiert.</span><span class="sxs-lookup"><span data-stu-id="0918a-122">A client application can discover whether a particular text-based control implements a DOM by retrieving the control's [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="0918a-123">Anschließend können Sie die [**iuiautomationelement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) -Methode aufrufen und dabei den [**UIA- \_ isobjectmodelpatternavailablepropertyid**](uiauto-control-pattern-availability-propids.md) -Eigenschafts Bezeichner angeben und einen Variant-Wert, der true erhält, wenn das Steuerelement ein DOM implementiert.</span><span class="sxs-lookup"><span data-stu-id="0918a-123">Then, call the [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) method, specifying the [**UIA\_IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) property identifier, and a variant that receives TRUE if the control implements a DOM.</span></span>

<span data-ttu-id="0918a-124">Um auf das DOM zuzugreifen, müssen Sie die [**iuiautomationelement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) -Methode aufrufen und dabei den [**UIA \_ objectmodelpatternid**](uiauto-controlpattern-ids.md) -Steuerelement Muster Bezeichner und eine Variable, die die [**iuiautomationobjectmodelpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) -Schnittstelle empfängt, angeben.</span><span class="sxs-lookup"><span data-stu-id="0918a-124">To access the DOM, call the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method, specifying the [**UIA\_ObjectModelPatternId**](uiauto-controlpattern-ids.md) control pattern identifier and a variable that receives the [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) interface.</span></span> <span data-ttu-id="0918a-125">Rufen Sie die [**iuiautomationobjectmodelpattern:: getunderlyingobjectmodel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) -Methode auf, um die DOM-Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0918a-125">Call the [**IUIAutomationObjectModelPattern::GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) method to retrieve the DOM interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0918a-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0918a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0918a-127">Text-und TextRange-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="0918a-127">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="0918a-128">Benutzeroberflächenautomatisierungs-Unterstützung für Textinhalte</span><span class="sxs-lookup"><span data-stu-id="0918a-128">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="0918a-129">Arbeiten mit Text basierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="0918a-129">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




