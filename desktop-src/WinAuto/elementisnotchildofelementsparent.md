---
title: Elementisnotchildofelementsparent
description: Elementisnotchildofelementsparent
ms.assetid: DFD5CC2A-B5F4-49F2-B3EF-2CD447A575E2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a3d62a6ae656bffffca442ed3cbb9b85be8dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388795"
---
# <a name="elementisnotchildofelementsparent"></a><span data-ttu-id="334ef-103">Elementisnotchildofelementsparent</span><span class="sxs-lookup"><span data-stu-id="334ef-103">ElementIsNotChildOfElementsParent</span></span>

## <a name="text"></a><span data-ttu-id="334ef-104">Text</span><span class="sxs-lookup"><span data-stu-id="334ef-104">Text</span></span>

<span data-ttu-id="334ef-105">Das Element ist kein untergeordnetes Element des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="334ef-105">Element is not a child of it's parent</span></span>

## <a name="type"></a><span data-ttu-id="334ef-106">type</span><span class="sxs-lookup"><span data-stu-id="334ef-106">Type</span></span>

<span data-ttu-id="334ef-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="334ef-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="334ef-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="334ef-108">Description</span></span>

<span data-ttu-id="334ef-109">Wenn [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) für das untergeordnete Element aufgerufen wird, das von " [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) " zurückgegeben wird (mithilfe der \_ Navigations Konstanten navDir firstChild oder navDir \_ LastChild), stimmt das zurückgegebene übergeordnete Element nicht mit dem übergeordneten Element identisch, das im **accNavigate** -Aufruf angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="334ef-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the child element returned by [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (using either the NAVDIR\_FIRSTCHILD or NAVDIR\_LASTCHILD navigation constants), the parent element returned does not match the parent element specified in the **accNavigate** call.</span></span>

<span data-ttu-id="334ef-110">Dieses Problem kann Navigationsprobleme bei automatisierten Tools verursachen, da das Durchlaufen von Elementen möglicherweise erratisch und unvorhersagbar ist.</span><span class="sxs-lookup"><span data-stu-id="334ef-110">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="334ef-111">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="334ef-111">Possible causes</span></span>

<span data-ttu-id="334ef-112">Eine falsche oder ungültige MSAA-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="334ef-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="334ef-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="334ef-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="334ef-114">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="334ef-114">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="334ef-115">**IAccessible:: get- \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="334ef-115">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




