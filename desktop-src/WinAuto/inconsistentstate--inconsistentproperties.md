---
title: Inkonsistentstate, inkonsistentproperties
description: Inkonsistentstate, inkonsistentproperties
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5522025eff8aecbdf0f4313c0052afebd4a17958
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708729"
---
# <a name="inconsistentstate-inconsistentproperties"></a><span data-ttu-id="be402-103">Inkonsistentstate, inkonsistentproperties</span><span class="sxs-lookup"><span data-stu-id="be402-103">InconsistentState, InconsistentProperties</span></span>

## <a name="text"></a><span data-ttu-id="be402-104">Text</span><span class="sxs-lookup"><span data-stu-id="be402-104">Text</span></span>

<span data-ttu-id="be402-105">Ein Steuerelement weist Zustände/Eigenschaften auf, {0} die inkonsistent sind. {1}</span><span class="sxs-lookup"><span data-stu-id="be402-105">A control has states/properties that are inconsistent {0} and {1}</span></span>

## <a name="type"></a><span data-ttu-id="be402-106">type</span><span class="sxs-lookup"><span data-stu-id="be402-106">Type</span></span>

<span data-ttu-id="be402-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="be402-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="be402-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be402-108">Description</span></span>

<span data-ttu-id="be402-109">Ein Element meldet inkonsistente oder widersprüchliche MSAA-Zustände oder Benutzeroberflächenautomatisierungs-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="be402-109">An element is reporting inconsistent or conflicting MSAA states or UI Automation properties.</span></span> <span data-ttu-id="be402-110">Wenn z. b. die [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) -Methode eine der folgenden Kombinationen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="be402-110">For example, when the [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) method returns any of the following combinations.</span></span>

-   <span data-ttu-id="be402-111">Zustands \_ System \_ erweitert und Zustands \_ System \_ reduziert</span><span class="sxs-lookup"><span data-stu-id="be402-111">STATE\_SYSTEM\_EXPANDED and STATE\_SYSTEM\_COLLAPSED</span></span>
-   <span data-ttu-id="be402-112">Status \_ System \_ ausgewählt und nicht Zustands \_ System \_ auswählbar</span><span class="sxs-lookup"><span data-stu-id="be402-112">STATE\_SYSTEM\_SELECTED and not STATE\_SYSTEM\_SELECTABLE</span></span>
-   <span data-ttu-id="be402-113">Zustands \_ System \_ fokussiert und nicht Zustands \_ fähig \_</span><span class="sxs-lookup"><span data-stu-id="be402-113">STATE\_SYSTEM\_FOCUSED and not STATE\_SYSTEM\_FOCUSABLE</span></span>

<span data-ttu-id="be402-114">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme verursachen, da dem Benutzer ein falscher Element Zustand gemeldet werden könnte.</span><span class="sxs-lookup"><span data-stu-id="be402-114">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an incorrect element state might be reported to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="be402-115">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="be402-115">Possible causes</span></span>

<span data-ttu-id="be402-116">Für das-Element oder das übergeordnete Element ist ein MSAA-Zustand unpassend festgelegt.</span><span class="sxs-lookup"><span data-stu-id="be402-116">The element or its parent has an MSAA state set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be402-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be402-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be402-118">**IAccessible:: get- \_ accState**</span><span class="sxs-lookup"><span data-stu-id="be402-118">**IAccessible::get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[<span data-ttu-id="be402-119">**Objekt Zustands Konstanten**</span><span class="sxs-lookup"><span data-stu-id="be402-119">**Object State Constants**</span></span>](object-state-constants.md)
</dt> <dt>

[<span data-ttu-id="be402-120">Zustände und Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="be402-120">States and Properties</span></span>](uiauto-msaa.md)
</dt> </dl>

 

 




