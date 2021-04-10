---
title: Hilfe Schaltfläche
description: Die Schaltfläche Hilfe ist ein Steuerelement, auf das der Benutzer klicken kann, um das Anwendungs Hilfesystem anzuzeigen.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc44c9f9a03561f1627067849272509838d7a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948759"
---
# <a name="help-button"></a><span data-ttu-id="45213-103">Hilfe Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="45213-103">Help Button</span></span>

<span data-ttu-id="45213-104">Die Schaltfläche Hilfe ist ein Steuerelement, auf das der Benutzer klicken kann, um das Anwendungs Hilfesystem anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="45213-104">The Help Button is a control that the user can click to display the application help system.</span></span>

-   [<span data-ttu-id="45213-105">Details</span><span class="sxs-lookup"><span data-stu-id="45213-105">Details</span></span>](#details)
-   [<span data-ttu-id="45213-106">Hilfe-Schaltflächen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45213-106">Help Button Properties</span></span>](#help-button-properties)
-   [<span data-ttu-id="45213-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45213-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="45213-108">Details</span><span class="sxs-lookup"><span data-stu-id="45213-108">Details</span></span>

<span data-ttu-id="45213-109">Der folgende Screenshot veranschaulicht die Menüband-Hilfe Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="45213-109">The following screen shot illustrates the Ribbon Help Button.</span></span>

![Screenshot mit der Schaltfläche "Hilfe"](images/controls/helpbutton.png)

## <a name="help-button-properties"></a><span data-ttu-id="45213-111">Hilfe-Schaltflächen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45213-111">Help Button Properties</span></span>

<span data-ttu-id="45213-112">Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Hilfe Button-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="45213-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Help Button control.</span></span>

<span data-ttu-id="45213-113">In der Regel wird eine Hilfe Schaltflächen Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="45213-113">Typically, a Help Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="45213-114">Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.</span><span class="sxs-lookup"><span data-stu-id="45213-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="45213-115">Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="45213-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="45213-116">Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="45213-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="45213-117">In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="45213-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="45213-118">In der folgenden Tabelle werden die Eigenschaften Schlüssel aufgelistet, die dem Schaltflächen-Steuerelement "Hilfe" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="45213-118">The following table lists the property keys that are associated with the Help Button control.</span></span>



| <span data-ttu-id="45213-119">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="45213-119">Property Key</span></span>                                                                                     | <span data-ttu-id="45213-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="45213-120">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="45213-121">UI- \_ pkey- \_ KeyTip</span><span class="sxs-lookup"><span data-stu-id="45213-121">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="45213-122">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="45213-122">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="45213-123">UI- \_ pkey- \_ Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="45213-123">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="45213-124">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="45213-124">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="45213-125">UI- \_ pkey- \_ tooltipdescription</span><span class="sxs-lookup"><span data-stu-id="45213-125">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="45213-126">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="45213-126">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="45213-127">UI- \_ pkey- \_ ToolTipTitle</span><span class="sxs-lookup"><span data-stu-id="45213-127">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="45213-128">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="45213-128">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="45213-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45213-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45213-130">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="45213-130">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="45213-131">**HelpButton-Element**</span><span class="sxs-lookup"><span data-stu-id="45213-131">**HelpButton element**</span></span>](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 