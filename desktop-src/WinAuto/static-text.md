---
title: Statischer Text (MSAA UI-Element Referenz)
description: Statische Text Steuerelemente bieten eine bequeme Möglichkeit, Text in Dialogfeldern und anderen Fenstern anzuzeigen. Statische Text Steuerelemente dienen oft als Bezeichnungen für andere Steuerelemente.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f35581a9b305f28782d8faeac81105afb0d5147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856859"
---
# <a name="static-text-msaa-ui-element-reference"></a><span data-ttu-id="6b80d-104">Statischer Text (MSAA UI-Element Referenz)</span><span class="sxs-lookup"><span data-stu-id="6b80d-104">Static Text (MSAA UI Element Reference)</span></span>

<span data-ttu-id="6b80d-105">Statische Text Steuerelemente bieten eine bequeme Möglichkeit, Text in Dialogfeldern und anderen Fenstern anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6b80d-105">Static text controls provide a convenient way to display text on dialog boxes and other windows.</span></span> <span data-ttu-id="6b80d-106">Statische Text Steuerelemente dienen oft als Bezeichnungen für andere Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="6b80d-106">Static text controls often serve as labels for other controls.</span></span>

<span data-ttu-id="6b80d-107">Der Fenster Klassenname für ein statisches Text Steuerelement ist "static".</span><span class="sxs-lookup"><span data-stu-id="6b80d-107">The window class name for a static text control is "STATIC".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="6b80d-108">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="6b80d-108">IAccessible Methods</span></span>

<span data-ttu-id="6b80d-109">Statische Text Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="6b80d-109">Static text controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="6b80d-110">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="6b80d-110">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="6b80d-111">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="6b80d-111">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="6b80d-112">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="6b80d-112">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="6b80d-113">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="6b80d-113">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="6b80d-114">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b80d-114">IAccessible Properties</span></span>

<span data-ttu-id="6b80d-115">Statische Text Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6b80d-115">Static text controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="6b80d-116">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6b80d-116">Property</span></span>                                                                             | <span data-ttu-id="6b80d-117">Kommentare</span><span class="sxs-lookup"><span data-stu-id="6b80d-117">Comments</span></span>                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b80d-118">**\_accChild erhalten**</span><span class="sxs-lookup"><span data-stu-id="6b80d-118">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="6b80d-119">**get \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="6b80d-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="6b80d-120">Die **childCount** -Eigenschaft ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6b80d-120">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="6b80d-121">**get- \_ accdescription**</span><span class="sxs-lookup"><span data-stu-id="6b80d-121">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="6b80d-122">**\_Zugriffs Fokus erhalten**</span><span class="sxs-lookup"><span data-stu-id="6b80d-122">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="6b80d-123">**\_accHelp erhalten**</span><span class="sxs-lookup"><span data-stu-id="6b80d-123">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="6b80d-124">**\_accHelpTopic erhalten**</span><span class="sxs-lookup"><span data-stu-id="6b80d-124">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="6b80d-125">**\_accKeyboardShortcut erhalten**</span><span class="sxs-lookup"><span data-stu-id="6b80d-125">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="6b80d-126">Die **KeyboardShortcut** -Eigenschaft ist die Zugriffstaste, bei der es sich um das unterstrichene Zeichen im Text handelt, das das dem statischen Text zugeordnete Steuerelement aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6b80d-126">The **KeyboardShortcut** property is the access key, which is the underlined character in the text that activates the control associated with the static text.</span></span> <span data-ttu-id="6b80d-127">Die zurückgegebene Zeichenfolge enthält das Zugriffsschlüssel Zeichen, das an die Zeichenfolge "alt +" angehängt wird.</span><span class="sxs-lookup"><span data-stu-id="6b80d-127">The returned string contains the access key character appended to the string "Alt+".</span></span>                                           |
| [<span data-ttu-id="6b80d-128">**\_accName erhalten**</span><span class="sxs-lookup"><span data-stu-id="6b80d-128">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="6b80d-129">Die **Name** -Eigenschaft entspricht dem Text im statischen Text Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="6b80d-129">The **Name** property is the same as the text in the static text control.</span></span>                                                                                                                                                                                                                     |
| [<span data-ttu-id="6b80d-130">**\_accParent erhalten**</span><span class="sxs-lookup"><span data-stu-id="6b80d-130">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="6b80d-131">Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die gleiche **Name** -Eigenschaft und den Fenster Klassennamen wie das Steuerelement aufweist.</span><span class="sxs-lookup"><span data-stu-id="6b80d-131">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                   |
| [<span data-ttu-id="6b80d-132">**get- \_ Zugriffs Rolle**</span><span class="sxs-lookup"><span data-stu-id="6b80d-132">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="6b80d-133">Die **Role** -Eigenschaft ist [**role \_ System \_ StaticText**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="6b80d-133">The **Role** property is [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md).</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="6b80d-134">**\_accState erhalten**</span><span class="sxs-lookup"><span data-stu-id="6b80d-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="6b80d-135">Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): [**Zustands \_ \_**](object-state-constants.md) System Schreib geschütztes \| [**Zustands \_ System \_ unsichtbar**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="6b80d-135">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_READONLY**](object-state-constants.md) \| [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="6b80d-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b80d-136">Notes</span></span>

-   <span data-ttu-id="6b80d-137">Die Methode [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) gibt DISP \_ E \_ mitgliednotfound zurück, wenn Sie mit [**selflag \_ TakeFocus**](selflag.md) für ein statisches Textobjekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6b80d-137">The [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method returns DISP\_E\_MEMBERNOTFOUND when it is called with [**SELFLAG\_TAKEFOCUS**](selflag.md) on a static text object.</span></span>
-   <span data-ttu-id="6b80d-138">Statische Steuerelemente mit dem SS- \_ Symbolstil geben ungültige Daten in der **Name** -Eigenschaft zurück.</span><span class="sxs-lookup"><span data-stu-id="6b80d-138">Static controls with the SS\_ICON style return invalid data in the **Name** property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b80d-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b80d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b80d-140">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6b80d-140">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





