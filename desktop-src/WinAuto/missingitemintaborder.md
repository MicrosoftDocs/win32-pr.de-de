---
title: Missingitemintaborder
description: Missingitemintaborder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9841ab71e9f5d40cf25454e737b9790ce27a04de
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727520"
---
# <a name="missingitemintaborder"></a><span data-ttu-id="d7280-103">Missingitemintaborder</span><span class="sxs-lookup"><span data-stu-id="d7280-103">MissingItemInTabOrder</span></span>

## <a name="text"></a><span data-ttu-id="d7280-104">Text</span><span class="sxs-lookup"><span data-stu-id="d7280-104">Text</span></span>

<span data-ttu-id="d7280-105">Dieses Element ist anscheinend Tabellen fähig, aber nicht in der Aktivier Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="d7280-105">This element appears to be tabbable but is not in the tab order.</span></span>

## <a name="type"></a><span data-ttu-id="d7280-106">type</span><span class="sxs-lookup"><span data-stu-id="d7280-106">Type</span></span>

<span data-ttu-id="d7280-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="d7280-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="d7280-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7280-108">Description</span></span>

<span data-ttu-id="d7280-109">Auf ein Fokussier bares Element kann nicht über die Standardtastatur Navigation (Tab oder UMSCHALT + TAB) zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="d7280-109">A focusable element is not accessible using standard keyboard navigation (Tab or Shift+Tab).</span></span> <span data-ttu-id="d7280-110">Beispielsweise wurde das-Element nicht als Tabstopp gekennzeichnet, oder es wurde ein Registerkarten Index zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d7280-110">For example, the element has not been marked as a tab stop or assigned a tab index.</span></span> <span data-ttu-id="d7280-111">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, folgende Probleme verursachen:</span><span class="sxs-lookup"><span data-stu-id="d7280-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because:</span></span>

-   <span data-ttu-id="d7280-112">Das Element kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d7280-112">The element is not discoverable.</span></span>
-   <span data-ttu-id="d7280-113">Wenn das Element ein untergeordnetes Element eines benutzerdefinierten Listen Steuer Elements ist, können die Hinweise, die angeben, dass das untergeordnete Element mithilfe des Pfeils oder der Seiten Tasten navigiert werden kann, fehlen</span><span class="sxs-lookup"><span data-stu-id="d7280-113">If the element is a child of a custom list control, cues indicating the child element can be navigated using the Arrow or Page keys may be missing.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="d7280-114">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="d7280-114">Possible causes</span></span>

-   <span data-ttu-id="d7280-115">Die MSAA-Rolle des Elements oder des übergeordneten Elements ist nicht ordnungsgemäß festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d7280-115">The MSAA role of the element or its parent is not set correctly.</span></span> <span data-ttu-id="d7280-116">Wenn z. b. alle Listenelemente in einem Listenansicht-Steuerelement nicht über MSAA als \_ ListItem-Rollen System verfügbar gemacht werden, tritt bei \_ der Überprüfung ein Fehler auf, da die Listenelemente nicht mithilfe der Tab-Taste aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="d7280-116">For example, if all list items in a list view control are not exposed through MSAA as a ROLE\_SYSTEM\_LISTITEM, the verification fails because the list items are not accessible using the Tab key.</span></span>
-   <span data-ttu-id="d7280-117">Das Element oder das übergeordnete Element ist ein benutzerdefiniertes Steuerelement, das die Tabstopps nicht korrekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="d7280-117">The element or its parent is a custom control that doesn't implement tabbing correctly.</span></span> <span data-ttu-id="d7280-118">Beispielsweise ist die Eigenschaft MSAA State nie auf State \_ System \_ focverwendbar festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d7280-118">For example, the MSAA State property is never set to STATE\_SYSTEM\_FOCUSABLE.</span></span>
-   <span data-ttu-id="d7280-119">Ein Element, das als Container für andere Elemente fungiert, wurde zur Überprüfung ausgewählt, unterstützt jedoch keine Tastaturnavigation.</span><span class="sxs-lookup"><span data-stu-id="d7280-119">An element that acts as a container for other elements was selected for verification but does not support keyboard navigation itself.</span></span> <span data-ttu-id="d7280-120">Beispielsweise können Sie mit der Tab-Taste auf eine Symbolleiste und deren untergeordnete Elemente nicht zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d7280-120">For example, a toolbar and its child elements are not accessible using the TAB key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7280-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7280-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7280-122">Richtlinien zur Gestaltung einer tastaturgesteuerten Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d7280-122">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 