---
title: Dragpattern/dragdroppattern-Elemente benötigen einen Namen
description: Dragpattern/dragdroppattern-Elemente benötigen einen Namen
ms.assetid: DEF58FB2-5830-4162-87D0-40DEC1237529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc60eeca59f4754f9c160696cdfa2556c36a5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337135"
---
# <a name="dragpatterndragdroppattern-elements-requires-name"></a><span data-ttu-id="6ce1b-103">Dragpattern/dragdroppattern-Elemente benötigen einen Namen</span><span class="sxs-lookup"><span data-stu-id="6ce1b-103">DragPattern/DragDropPattern elements requires Name</span></span>

## <a name="text"></a><span data-ttu-id="6ce1b-104">Text</span><span class="sxs-lookup"><span data-stu-id="6ce1b-104">Text</span></span>

<span data-ttu-id="6ce1b-105">Für Elemente, die Drag & Drop unterstützen, muss ein gültiger Name festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="6ce1b-105">Elements that support Drag/Drop should have a valid 'Name' set</span></span>

## <a name="type"></a><span data-ttu-id="6ce1b-106">type</span><span class="sxs-lookup"><span data-stu-id="6ce1b-106">Type</span></span>

<span data-ttu-id="6ce1b-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="6ce1b-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="6ce1b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ce1b-108">Description</span></span>

<span data-ttu-id="6ce1b-109">Das Element unterstützt entweder [**iuiautomationdragpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) oder [**iuiautomationdroptargetpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), aber es ist kein gültiger Name festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6ce1b-109">The element supports either [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) or [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), but does not have a valid Name set.</span></span>

<span data-ttu-id="6ce1b-110">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm verlassen, Probleme haben.</span><span class="sxs-lookup"><span data-stu-id="6ce1b-110">This issue causes problems for people who rely on a screen-reader.</span></span> <span data-ttu-id="6ce1b-111">Der Benutzer kann nicht erkennen, was dieses Objekt ist, da der Bildschirm Lesevorgang keinen gültigen Namen ausliest, um zu unterscheiden, was dieses Element beim ziehen ist.</span><span class="sxs-lookup"><span data-stu-id="6ce1b-111">The user will not be able to tell what this object is since the screen read will not read out a valid name to distinguish what this element is when dragging.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="6ce1b-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="6ce1b-112">Possible causes</span></span>

-   <span data-ttu-id="6ce1b-113">Das Element oder das übergeordnete Element weist einen falsch zugewiesenen Namen oder eine Bezeichnung auf.</span><span class="sxs-lookup"><span data-stu-id="6ce1b-113">The element, or its parent, has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="6ce1b-114">Ein Entwickler weiß nicht, dass Bildschirm Sprachausgaben Namen und Steuerelement Typen lesen.</span><span class="sxs-lookup"><span data-stu-id="6ce1b-114">A developer is not aware that screen readers read names and control types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ce1b-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ce1b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ce1b-116">**IAccessible:: get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="6ce1b-116">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="6ce1b-117">Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6ce1b-117">Name Property</span></span>](name-property.md)
</dt> <dt>

[<span data-ttu-id="6ce1b-118">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="6ce1b-118">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="6ce1b-119">**Iuiautomationelement:: currentname**</span><span class="sxs-lookup"><span data-stu-id="6ce1b-119">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




