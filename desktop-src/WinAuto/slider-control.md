---
title: Schieberegler-Steuer Element (MSAA UI-Element Referenz)
description: Ein Schieberegler-Steuerelement, das auch als TrackBar-Steuerelement bezeichnet wird, ermöglicht Benutzern die Auswahl aus einem Wertebereich durch Verschieben eines Schiebereglers. Unter dem Betriebssystem Windows werden Schieberegler-Steuerelemente zum Einstellen der Lautstärke verwendet.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03c39d6638557b9dfff90740132d3e22a7e2511
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037534"
---
# <a name="slider-control-msaa-ui-element-reference"></a><span data-ttu-id="a99db-104">Schieberegler-Steuer Element (MSAA UI-Element Referenz)</span><span class="sxs-lookup"><span data-stu-id="a99db-104">Slider Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="a99db-105">In diesem Thema werden **Schieberegler-Steuer** Element Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a99db-105">This topic describes **Slider Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="a99db-106">Hier wird beschrieben, wie Sie **Schieberegler-Steuer** Element Objekte in verschiedenen Benutzeroberflächen-Frameworks erstellen.</span><span class="sxs-lookup"><span data-stu-id="a99db-106">How to create **Slider Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="a99db-107">Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.</span><span class="sxs-lookup"><span data-stu-id="a99db-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="a99db-108">Ein Schieberegler-Steuerelement, das auch als TrackBar-Steuerelement bezeichnet wird, ermöglicht Benutzern die Auswahl aus einem Wertebereich durch Verschieben eines Schiebereglers.</span><span class="sxs-lookup"><span data-stu-id="a99db-108">A slider control, also called a trackbar control, lets a user select from a range of values by moving a slider.</span></span> <span data-ttu-id="a99db-109">Unter dem Betriebssystem Windows werden Schieberegler-Steuerelemente zum Einstellen der Lautstärke verwendet.</span><span class="sxs-lookup"><span data-stu-id="a99db-109">The volume controls in the Windows operating system are slider controls.</span></span>

<span data-ttu-id="a99db-110">Der Fenster Klassenname für ein Schieberegler-Steuerelement ist TrackBar \_ Class, das in der Datei "commctrl. h" als "msctls \_ TrackBar" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a99db-110">The window class name for a slider control is TRACKBAR\_CLASS, which is defined as "msctls\_trackbar" in Commctrl.h.</span></span>

<span data-ttu-id="a99db-111">Der Inhalt der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften hängt davon ab, ob der Schieberegler vertikal oder horizontal ist und auf welchem der folgenden Teile des Schieberegler-Steuer Elements vom Client abgefragt wird:</span><span class="sxs-lookup"><span data-stu-id="a99db-111">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depend on whether the slider is vertical or horizontal and on which of the following parts of the slider control is queried by the client:</span></span>

-   <span data-ttu-id="a99db-112">Schieberegler-Fenster</span><span class="sxs-lookup"><span data-stu-id="a99db-112">Slider window</span></span>
-   <span data-ttu-id="a99db-113">Ziehpunkt</span><span class="sxs-lookup"><span data-stu-id="a99db-113">Slider thumb</span></span>
-   <span data-ttu-id="a99db-114">Schattierter Bereich oberhalb (oder bis</span><span class="sxs-lookup"><span data-stu-id="a99db-114">Shaded area above (or to</span></span>
-   <span data-ttu-id="a99db-115">Schattierter Bereich unterhalb des Schieberegler-Zieh Punkts (oder rechts von)</span><span class="sxs-lookup"><span data-stu-id="a99db-115">Shaded area below (or to the right of) the slider thumb</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="a99db-116">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="a99db-116">IAccessible Methods</span></span>

<span data-ttu-id="a99db-117">Ein Schieberegler-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="a99db-117">A slider control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="a99db-118">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="a99db-118">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="a99db-119">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="a99db-119">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="a99db-120">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="a99db-120">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="a99db-121">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="a99db-121">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="a99db-122">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a99db-122">IAccessible Properties</span></span>

<span data-ttu-id="a99db-123">Ein Schieberegler-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a99db-123">A slider control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   [<span data-ttu-id="a99db-124">**\_accChild erhalten**</span><span class="sxs-lookup"><span data-stu-id="a99db-124">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [<span data-ttu-id="a99db-125">**get \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="a99db-125">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [<span data-ttu-id="a99db-126">**get- \_ accdescription**</span><span class="sxs-lookup"><span data-stu-id="a99db-126">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [<span data-ttu-id="a99db-127">**\_accHelp erhalten**</span><span class="sxs-lookup"><span data-stu-id="a99db-127">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="a99db-128">**\_accHelpTopic erhalten**</span><span class="sxs-lookup"><span data-stu-id="a99db-128">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="a99db-129">[**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)– die **KeyboardShortcut** -Eigenschaft ist die Zugriffstaste des Schieberegler-Fensters, bei der es sich um ein unterstrichenes Zeichen im Text der Bezeichnung für den Schieberegler handelt.</span><span class="sxs-lookup"><span data-stu-id="a99db-129">[**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)—The **KeyboardShortcut** property is the slider window's access key, which is an underlined character in the text of the label for the slider.</span></span> <span data-ttu-id="a99db-130">Die zurückgegebene Zeichenfolge enthält das Zugriffsschlüssel Zeichen, das an die Zeichenfolge "alt +" angehängt wird.</span><span class="sxs-lookup"><span data-stu-id="a99db-130">The returned string contains the access key character appended to the string "Alt+".</span></span>
-   <span data-ttu-id="a99db-131">[**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)– die **Name** -Eigenschaft hängt von dem Teil des Schiebereglers ab, der abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="a99db-131">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The **Name** property depends on the part of the slider that is queried.</span></span>

    <span data-ttu-id="a99db-132">Die Teile eines vertikalen Schiebereglers haben die folgenden Namen:</span><span class="sxs-lookup"><span data-stu-id="a99db-132">The parts of a vertical slider have the following names:</span></span>

    

    | <span data-ttu-id="a99db-133">Schieberegler-Teil</span><span class="sxs-lookup"><span data-stu-id="a99db-133">Slider part</span></span>                    | <span data-ttu-id="a99db-134">Name</span><span class="sxs-lookup"><span data-stu-id="a99db-134">Name</span></span>                                |
    |--------------------------------|-------------------------------------|
    | <span data-ttu-id="a99db-135">Schieberegler-Fenster</span><span class="sxs-lookup"><span data-stu-id="a99db-135">Slider window</span></span>                  | <span data-ttu-id="a99db-136">Statisches Text Steuerelement, das als Bezeichnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a99db-136">Static text control used as a label</span></span> |
    | <span data-ttu-id="a99db-137">Ziehpunkt</span><span class="sxs-lookup"><span data-stu-id="a99db-137">Slider thumb</span></span>                   | <span data-ttu-id="a99db-138">Gebracht</span><span class="sxs-lookup"><span data-stu-id="a99db-138">"Position"</span></span>                          |
    | <span data-ttu-id="a99db-139">Schattierter Bereich oberhalb des Schiebereglers</span><span class="sxs-lookup"><span data-stu-id="a99db-139">Shaded area above slider thumb</span></span> | <span data-ttu-id="a99db-140">"Seite nach oben"</span><span class="sxs-lookup"><span data-stu-id="a99db-140">"Page up"</span></span>                           |
    | <span data-ttu-id="a99db-141">Schattierter Bereich unterhalb des Schiebereglers</span><span class="sxs-lookup"><span data-stu-id="a99db-141">Shaded area below slider thumb</span></span> | <span data-ttu-id="a99db-142">"Bild-ab"</span><span class="sxs-lookup"><span data-stu-id="a99db-142">"Page down"</span></span>                         |

    

     

    <span data-ttu-id="a99db-143">Die Teile eines horizontalen Schiebereglers haben die folgenden Namen:</span><span class="sxs-lookup"><span data-stu-id="a99db-143">The parts of a horizontal slider have the following names:</span></span>

    

    | <span data-ttu-id="a99db-144">Schieberegler-Teil</span><span class="sxs-lookup"><span data-stu-id="a99db-144">Slider part</span></span>                              | <span data-ttu-id="a99db-145">Name</span><span class="sxs-lookup"><span data-stu-id="a99db-145">Name</span></span>                                |
    |------------------------------------------|-------------------------------------|
    | <span data-ttu-id="a99db-146">Schieberegler-Fenster</span><span class="sxs-lookup"><span data-stu-id="a99db-146">Slider window</span></span>                            | <span data-ttu-id="a99db-147">Statisches Text Steuerelement, das als Bezeichnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a99db-147">Static text control used as a label</span></span> |
    | <span data-ttu-id="a99db-148">Ziehpunkt</span><span class="sxs-lookup"><span data-stu-id="a99db-148">Slider thumb</span></span>                             | <span data-ttu-id="a99db-149">Gebracht</span><span class="sxs-lookup"><span data-stu-id="a99db-149">"Position"</span></span>                          |
    | <span data-ttu-id="a99db-150">Schattierter Bereich auf der linken Seite des Schiebereglers</span><span class="sxs-lookup"><span data-stu-id="a99db-150">Shaded area to the left of slider thumb</span></span>  | <span data-ttu-id="a99db-151">"Seite Links"</span><span class="sxs-lookup"><span data-stu-id="a99db-151">"Page left"</span></span>                         |
    | <span data-ttu-id="a99db-152">Schattierter Bereich rechts vom Schieberegler-Ziehpunkt</span><span class="sxs-lookup"><span data-stu-id="a99db-152">Shaded area to the right of slider thumb</span></span> | <span data-ttu-id="a99db-153">"Page Right"</span><span class="sxs-lookup"><span data-stu-id="a99db-153">"Page right"</span></span>                        |

    

     

-   <span data-ttu-id="a99db-154">[**get- \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)– die **Parent** -Eigenschaft der Pfeil Schaltflächen, der Bild Lauf Thumb und der schattierte Bereich auf beiden Seiten des Zieh Punkts ist das Schieberegler-Fenster.</span><span class="sxs-lookup"><span data-stu-id="a99db-154">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The **Parent** property of the arrow buttons, scroll thumb, and the shaded area on either side of the thumb is the slider window.</span></span> <span data-ttu-id="a99db-155">Die **Parent** -Eigenschaft des Schieberegler-Fensters ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die **Name** -Eigenschaft und den Fenster Klassennamen aufweist.</span><span class="sxs-lookup"><span data-stu-id="a99db-155">The **Parent** property of the slider window is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name.</span></span>
-   <span data-ttu-id="a99db-156">[**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)– die **Role** -Eigenschaft hängt von dem Teil des Schiebereglers ab, der abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="a99db-156">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property depends on the part of the slider that is queried.</span></span> 

    | <span data-ttu-id="a99db-157">Schieberegler-Teil</span><span class="sxs-lookup"><span data-stu-id="a99db-157">Slider part</span></span>                                     | [<span data-ttu-id="a99db-158">Rolle</span><span class="sxs-lookup"><span data-stu-id="a99db-158">Role</span></span>](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="a99db-159">Schieberegler-Fenster</span><span class="sxs-lookup"><span data-stu-id="a99db-159">Slider window</span></span>                                   | [<span data-ttu-id="a99db-160">**\_ \_ Schieberegler für Rollen System**</span><span class="sxs-lookup"><span data-stu-id="a99db-160">**ROLE\_SYSTEM\_SLIDER**</span></span>](object-roles.md)         |
    | <span data-ttu-id="a99db-161">Ziehpunkt</span><span class="sxs-lookup"><span data-stu-id="a99db-161">Slider thumb</span></span>                                    | [<span data-ttu-id="a99db-162">**Rollen \_ System \_ Indikator**</span><span class="sxs-lookup"><span data-stu-id="a99db-162">**ROLE\_SYSTEM\_INDICATOR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="a99db-163">Schattierte Bereiche auf beiden Seiten des Schiebereglers</span><span class="sxs-lookup"><span data-stu-id="a99db-163">Shaded areas on either side of the slider thumb</span></span> | [<span data-ttu-id="a99db-164">**\_ \_ Schaltfläche "Rollen System"**</span><span class="sxs-lookup"><span data-stu-id="a99db-164">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |

    

     

-   <span data-ttu-id="a99db-165">die [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)–-[Werte](object-state-constants.md) für die **State** -Eigenschaft sind abhängig von dem Teil des Schiebereglers, der abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="a99db-165">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—[Values](object-state-constants.md) for the **State** property depend on the part of the slider that is queried.</span></span> 

    | <span data-ttu-id="a99db-166">Schieberegler-Teil</span><span class="sxs-lookup"><span data-stu-id="a99db-166">Slider Part</span></span>                                     | <span data-ttu-id="a99db-167">Mögliche Zustands Werte</span><span class="sxs-lookup"><span data-stu-id="a99db-167">Possible state values</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="a99db-168">Schieberegler-Fenster</span><span class="sxs-lookup"><span data-stu-id="a99db-168">Slider window</span></span>                                   | <span data-ttu-id="a99db-169">[**Status \_ System \_ unsichtbares**](object-state-constants.md) Zustands System mit Fokus Zustands System mit \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a99db-169">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span> |
    | <span data-ttu-id="a99db-170">Ziehpunkt</span><span class="sxs-lookup"><span data-stu-id="a99db-170">Slider thumb</span></span>                                    | <span data-ttu-id="a99db-171">NULL (0), d. h. das Objekt ist sichtbar [**, \_ \_ oder das**](object-state-constants.md) nicht verfügbare Zustands System ist nicht \| [**\_ \_ verfügbar**](object-state-constants.md) . \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a99db-171">Zero (0), which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                       |
    | <span data-ttu-id="a99db-172">Schattierte Bereiche auf beiden Seiten des Schiebereglers</span><span class="sxs-lookup"><span data-stu-id="a99db-172">Shaded areas on either side of the slider thumb</span></span> | <span data-ttu-id="a99db-173">NULL (0), d. h. das Objekt ist sichtbar [**, \_ \_ oder das**](object-state-constants.md) nicht verfügbare Zustands System ist nicht \| [**\_ \_ verfügbar**](object-state-constants.md) . \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a99db-173">Zero (0), which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                       |

    

     

-   <span data-ttu-id="a99db-174">[**get- \_ Wert**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)– die **value** -Eigenschaft für das Schieberegler-Fenster gibt die Position des Zieh Punkts an und ist eine Zeichenfolge, die eine ganze Zahl zwischen "0" und "100" enthält.</span><span class="sxs-lookup"><span data-stu-id="a99db-174">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The **Value** property for the slider window indicates the position of the thumb and is a string that contains an integer from "0" through "100".</span></span>

## <a name="related-topics"></a><span data-ttu-id="a99db-175">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a99db-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a99db-176">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a99db-176">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="a99db-177">**Scrollleiste**</span><span class="sxs-lookup"><span data-stu-id="a99db-177">**Scroll Bar**</span></span>](scroll-bar.md)
</dt> </dl>

 

 




