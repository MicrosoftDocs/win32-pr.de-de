---
title: Tabbingnotzyklische
description: Tabbingnotzyklische
ms.assetid: F6BCC613-1EA1-438C-AC09-8A282870E021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08fd2e9f6613e07840f432b646c1bdc06a34b5f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039213"
---
# <a name="tabbingnotcyclic"></a><span data-ttu-id="bf93f-103">Tabbingnotzyklische</span><span class="sxs-lookup"><span data-stu-id="bf93f-103">TabbingNotCyclic</span></span>

## <a name="text"></a><span data-ttu-id="bf93f-104">Text</span><span class="sxs-lookup"><span data-stu-id="bf93f-104">Text</span></span>

<span data-ttu-id="bf93f-105">Die Tabstopps in dieser Anwendung sind nicht zyklisch.</span><span class="sxs-lookup"><span data-stu-id="bf93f-105">The tabbing in this application is not cyclic.</span></span> <span data-ttu-id="bf93f-106">Die vorwärts-oder rückwärts {0} zeitablaufzeiten werden nicht an dasselbe Steuerelement zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bf93f-106">Tabbing forwards or backwards {0} times doesn't come back to the same control.</span></span>

## <a name="type"></a><span data-ttu-id="bf93f-107">type</span><span class="sxs-lookup"><span data-stu-id="bf93f-107">Type</span></span>

<span data-ttu-id="bf93f-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="bf93f-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="bf93f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf93f-109">Description</span></span>

<span data-ttu-id="bf93f-110">Bei Verwendung der Standardtastatur Navigation (Tab oder UMSCHALT + TAB) ist es nicht möglich, die Elementstruktur des Überprüfungs Ziels zu durchlaufen, bis das Start Element zum Endelement (mit der gleichen Anzahl von Tastatureingaben) wird, indem die Richtung des Durchlaufs umgekehrt wird.</span><span class="sxs-lookup"><span data-stu-id="bf93f-110">When using standard keyboard navigation (Tab or Shift+Tab), it isn't possible to traverse the element tree of the verification target until the starting element becomes the ending element (using the same number of keystrokes) by reversing the direction of traversal.</span></span> <span data-ttu-id="bf93f-111">Wenn z. b. die x-Zeiten der Tabulator Taste (Tab) von Element a (0) zu Element a (x) und dann nach unten (UMSCHALT + TAB) x nicht angezeigt wird, führt das Element a (0) nicht zum Fokus.</span><span class="sxs-lookup"><span data-stu-id="bf93f-111">For example, tabbing forward (Tab) x times from element A(0) to element A(x) and then tabbing backward (Shift+Tab) x times does not result in element A(0) regaining focus.</span></span>

<span data-ttu-id="bf93f-112">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm oder eine Tastatur für die Navigation verlassen, Probleme verursachen, da es keine vorhersagbare Möglichkeit gibt, zu einem Steuerelement zurückzukehren, nachdem es besucht wurde.</span><span class="sxs-lookup"><span data-stu-id="bf93f-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because there is no predictable way to return to a control after it has been visited.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="bf93f-113">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="bf93f-113">Possible causes</span></span>

-   <span data-ttu-id="bf93f-114">Das Element oder das übergeordnete Element ist ein benutzerdefiniertes Steuerelement, das die Tabstopps nicht korrekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="bf93f-114">The element or its parent is a custom control that doesn't implement tabbing correctly.</span></span> <span data-ttu-id="bf93f-115">Beispielsweise ist die Eigenschaft MSAA State nicht ordnungsgemäß festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bf93f-115">For example, the MSAA State property isn't set correctly.</span></span>
-   <span data-ttu-id="bf93f-116">Einige Anwendungen, z. b. der Editor, weisen dieses Verhalten Innately auf.</span><span class="sxs-lookup"><span data-stu-id="bf93f-116">Some applications, such as the Notepad, exhibit this behavior innately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf93f-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bf93f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf93f-118">Richtlinien zur Gestaltung einer tastaturgesteuerten Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="bf93f-118">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 