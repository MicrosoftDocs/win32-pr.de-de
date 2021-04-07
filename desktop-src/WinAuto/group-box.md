---
title: Gruppenfeld (MSAA UI-Element Referenz)
description: Ein Gruppenfeld ist ein Rechteck, das einen Satz von Steuerelementen umgibt, z. b. Kontrollkästchen oder Options Felder, und einen Anwendungs definierten Text (Bezeichnung) enthält.
ms.assetid: c6cd81a1-76c0-41c5-bb7f-4796ea7e3114
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a105242aabd49d87241a2a49bdaca5c19edd350b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712570"
---
# <a name="group-box-msaa-ui-element-reference"></a><span data-ttu-id="2ff2d-103">Gruppenfeld (MSAA UI-Element Referenz)</span><span class="sxs-lookup"><span data-stu-id="2ff2d-103">Group Box (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="2ff2d-104">In diesem Thema werden **Gruppenfeld** Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-104">This topic describes **Group Box** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="2ff2d-105">Das Erstellen von **Gruppenfeld** Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-105">How to create **Group Box** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="2ff2d-106">Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="2ff2d-107">Ein Gruppenfeld ist ein Rechteck, das einen Satz von Steuerelementen umgibt, z. b. Kontrollkästchen oder Options Felder, und einen Anwendungs definierten Text (Bezeichnung) enthält.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-107">A group box is a rectangle that surrounds a set of controls, such as check boxes or radio buttons, and contains an application-defined text (label).</span></span>

<span data-ttu-id="2ff2d-108">Der einzige Zweck eines Gruppen Felds besteht darin, Steuerelemente zu organisieren, die durch einen gemeinsamen Zweck, angegeben durch die Bezeichnung, verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-108">The sole purpose of a group box is to organize controls related by a common purpose, indicated by the label.</span></span>

<span data-ttu-id="2ff2d-109">Der Fenster Klassenname für ein Gruppenfeld ist "Schaltfläche".</span><span class="sxs-lookup"><span data-stu-id="2ff2d-109">The window class name for a group box is "BUTTON".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="2ff2d-110">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="2ff2d-110">IAccessible Methods</span></span>

<span data-ttu-id="2ff2d-111">Ein Gruppenfeld unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="2ff2d-111">A group box supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="2ff2d-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="2ff2d-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="2ff2d-114">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-114">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="2ff2d-115">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2ff2d-115">IAccessible Properties</span></span>

<span data-ttu-id="2ff2d-116">Ein Gruppenfeld unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2ff2d-116">A group box supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="2ff2d-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2ff2d-117">Property</span></span>                                                                             | <span data-ttu-id="2ff2d-118">Kommentare</span><span class="sxs-lookup"><span data-stu-id="2ff2d-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ff2d-119">**get \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="2ff2d-120">Die **childCount** -Eigenschaft ist immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2ff2d-120">The **ChildCount** property is always zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="2ff2d-121">**\_Zugriffs Fokus erhalten**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-121">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="2ff2d-122">**\_accKeyboardShortcut erhalten**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-122">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="2ff2d-123">Gruppen Felder haben keine Tastenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-123">Group boxes do not have keyboard shortcuts.</span></span> <span data-ttu-id="2ff2d-124">Wenn der Fenster Text für das Feld Gruppe jedoch ein kaufmännisches und-Zeichen (&) enthält, gibt Microsoft Active Accessibility eine Zeichenfolge ungleich NULL als **KeyboardShortcut** -Eigenschaft zurück.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-124">However, if the window text for the group box contains an ampersand (&) character, Microsoft Active Accessibility returns a non-Null string as the **KeyboardShortcut** property.</span></span>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="2ff2d-125">**\_accName erhalten**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-125">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="2ff2d-126">Die **Name** -Eigenschaft wird aus dem Fenster Text (oder der Beschriftung) des Steuer Elements abgerufen, der mit dem Gruppenfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-126">The **Name** property is obtained from the control's window text (or caption), which is displayed with the group box.</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="2ff2d-127">**\_accParent erhalten**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="2ff2d-128">Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die gleiche **Name** -Eigenschaft und den Fenster Klassennamen wie das Steuerelement aufweist.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-128">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="2ff2d-129">**get- \_ Zugriffs Rolle**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-129">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="2ff2d-130">Die **Role** -Eigenschaft ist eine [**Rollen \_ System \_ Gruppierung**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2ff2d-130">The **Role** property is [**ROLE\_SYSTEM\_GROUPING**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="2ff2d-131">**\_accState erhalten**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-131">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="2ff2d-132">Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="2ff2d-132">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2ff2d-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2ff2d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ff2d-134">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2ff2d-134">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





