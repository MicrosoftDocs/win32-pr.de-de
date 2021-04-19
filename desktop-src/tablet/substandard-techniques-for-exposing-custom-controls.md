---
description: Beschreibung der unter Standardtechniken zum verfügbar machen von benutzerdefinierten Steuerelementen.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Unter Standardtechniken zum verfügbar machen von benutzerdefinierten Steuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194614474596b55e0b1cf0530a07f9b3c411f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359193"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a><span data-ttu-id="e4991-103">Unter Standardtechniken zum verfügbar machen von benutzerdefinierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="e4991-103">Substandard Techniques for Exposing Custom Controls</span></span>

<span data-ttu-id="e4991-104">Wenn eine Anwendung Microsoft Active Accessibility nicht unterstützt, ist Sie möglicherweise nicht vollständig zugänglich.</span><span class="sxs-lookup"><span data-stu-id="e4991-104">If an application does not support Microsoft Active Accessibility, it may not be fully accessible.</span></span> <span data-ttu-id="e4991-105">Die folgenden Techniken zum Rendering von Steuerelementen sind teilweise kompatibel:</span><span class="sxs-lookup"><span data-stu-id="e4991-105">The following techniques render controls partially compatible:</span></span>

-   <span data-ttu-id="e4991-106">Gibt eine beschreibende Zeichenfolge zurück, wenn das Steuerelement mithilfe der WM-gettext-Nachricht abgefragt wird \_ .</span><span class="sxs-lookup"><span data-stu-id="e4991-106">Return a descriptive string when the control is queried by using the WM\_GETTEXT message.</span></span> <span data-ttu-id="e4991-107">Gestatten Sie z. b. einem benutzerdefinierten Äquivalent eines Schaltflächen-Steuer Elements mit der Bezeichnung "Print", die Zeichenfolge "Print Button" zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="e4991-107">For example, allow a custom equivalent of a button control labeled "Print" to return the string "Print button."</span></span> <span data-ttu-id="e4991-108">Dadurch werden sowohl der Steuerelement Typ als auch die Bezeichnung identifiziert</span><span class="sxs-lookup"><span data-stu-id="e4991-108">This identifies both control type and label.</span></span> <span data-ttu-id="e4991-109">Die gleiche Zeichenfolge eignet sich für eine Schaltfläche mit einer Bezeichnung, die etwas anderes als Text ist, z. b. eine Grafik eines Druckers.</span><span class="sxs-lookup"><span data-stu-id="e4991-109">The same string is appropriate for a button with a label that is something other than text, such as a graphic of a printer.</span></span> <span data-ttu-id="e4991-110">Gleichermaßen können Sie zulassen, dass ein benutzerdefiniertes Steuerelement, das sich wie ein Kontrollkästchen verhält, die Beschriftungs Zeichenfolge "Druck aktiviert" zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e4991-110">Similarly, allow a custom control that behaves like a check box to return the caption string "Printing Enabled check box, checked."</span></span>
-   <span data-ttu-id="e4991-111">Unterstützung der WM- \_ getdlgcode-Meldung, die die unterstützte Tastatureingabe identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e4991-111">Support the WM\_GETDLGCODE message, identifying the keyboard input that is supported.</span></span> <span data-ttu-id="e4991-112">Gestatten Sie z. b. einem benutzerdefinierten Äquivalent eines Bearbeitungs Steuer Elements, WM \_ getdlgcode zu behandeln, indem Sie dlgc \_ hassetsel zurückgeben, wenn Nachrichten zum Festlegen der Auswahl verarbeitet werden, dlgc \_ wantpfeile bei Verwendung von Pfeiltasten und dlgc- \_ wantchars, um anzugeben, dass es Zeichen Eingaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4991-112">For example, allow a custom equivalent of an edit control to handle WM\_GETDLGCODE by returning DLGC\_HASSETSEL if it handles messages to set the selection, DLGC\_WANTARROWS if it uses arrow keys, and DLGC\_WANTCHARS to indicate that it uses character input.</span></span>
    > [!Note]  
    > <span data-ttu-id="e4991-113">Nur Steuerelemente, die über eigene Fenster Handles verfügen, können auf die \_ Nachrichten WM gettext und WM \_ getdlgcode Antworten.</span><span class="sxs-lookup"><span data-stu-id="e4991-113">Only controls that have their own window handles can respond to the WM\_GETTEXT and WM\_GETDLGCODE messages.</span></span>

     

<span data-ttu-id="e4991-114">Um Kompatibilitätsprobleme mit Hilfen bei der Barrierefreiheit zu vermeiden, sollten Sie beim Entwerfen von benutzerdefinierten Steuerelementen genau Active Accessibility Richtlinien befolgen.</span><span class="sxs-lookup"><span data-stu-id="e4991-114">To avoid compatibility problems with accessibility aids, you should follow Active Accessibility guidelines closely when designing custom controls.</span></span> <span data-ttu-id="e4991-115">Weitere Informationen zum Vermeiden von Kompatibilitätsproblemen mit hilfshilfen finden Sie im Abschnitt zur [Barrierefreiheit](../accessibility/accessibility.md) .</span><span class="sxs-lookup"><span data-stu-id="e4991-115">For more information about how to avoid compatibility problems with accessibility aids, see the [Accessibility](../accessibility/accessibility.md) section.</span></span>

 

 
