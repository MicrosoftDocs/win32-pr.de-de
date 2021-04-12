---
title: ElementIsChildOfParentMulipleTimes
description: ElementIsChildOfParentMulipleTimes
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27c66027f7948dfa794c85dace015565d636c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207452"
---
# <a name="elementischildofparentmulipletimes"></a><span data-ttu-id="27436-103">ElementIsChildOfParentMulipleTimes</span><span class="sxs-lookup"><span data-stu-id="27436-103">ElementIsChildOfParentMulipleTimes</span></span>

## <a name="text"></a><span data-ttu-id="27436-104">Text</span><span class="sxs-lookup"><span data-stu-id="27436-104">Text</span></span>

<span data-ttu-id="27436-105">Das accParent-Element des Elements ist ( {0} ), das ursprüngliche Element ist jedoch eine untergeordnete {1} Zeit.</span><span class="sxs-lookup"><span data-stu-id="27436-105">Element's accParent is ({0}), but original element is a child {1} times</span></span>

## <a name="type"></a><span data-ttu-id="27436-106">type</span><span class="sxs-lookup"><span data-stu-id="27436-106">Type</span></span>

<span data-ttu-id="27436-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="27436-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="27436-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27436-108">Description</span></span>

<span data-ttu-id="27436-109">Wenn [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) für das Target-Element aufgerufen wird, meldet es sich mehrmals als untergeordnetes Element desselben übergeordneten Elements an.</span><span class="sxs-lookup"><span data-stu-id="27436-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the target element, it reports being a child of the same parent multiple times.</span></span>

<span data-ttu-id="27436-110">Dieses Problem kann Navigationsprobleme bei automatisierten Tools verursachen, da das Durchlaufen von Elementen möglicherweise erratisch und unvorhersagbar ist.</span><span class="sxs-lookup"><span data-stu-id="27436-110">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="27436-111">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="27436-111">Possible causes</span></span>

<span data-ttu-id="27436-112">Eine falsche oder ungültige MSAA-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="27436-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27436-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="27436-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27436-114">**IAccessible:: get- \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="27436-114">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




