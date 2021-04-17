---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: AccNavigate- \_ rückkehrelement-withincorrectparent
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3bdff54c9c594cde4e6e57fe1886a900c913eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104559852"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a><span data-ttu-id="ce109-103">AccNavigate- \_ rückkehrelement-withincorrectparent</span><span class="sxs-lookup"><span data-stu-id="ce109-103">AccNavigate\_ReturnedElementWithIncorrectParent</span></span>

## <a name="text"></a><span data-ttu-id="ce109-104">Text</span><span class="sxs-lookup"><span data-stu-id="ce109-104">Text</span></span>

<span data-ttu-id="ce109-105">Aufrufen von accNavigate ((Live Search), 0, navDir \_ FirstChild), die (x-Gadget:///gadget.html) zurückgegeben haben, hat das falsche übergeordnete Element (null) zurückgegeben, \[ \] nicht (Live Suche)</span><span class="sxs-lookup"><span data-stu-id="ce109-105">Calling accNavigate((Live Search), 0, NAVDIR\_FIRSTCHILD) which returned (x-gadget:///gadget.html) returned the incorrect parent(\[NULL\]) and not (Live Search)</span></span>

## <a name="type"></a><span data-ttu-id="ce109-106">type</span><span class="sxs-lookup"><span data-stu-id="ce109-106">Type</span></span>

<span data-ttu-id="ce109-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="ce109-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="ce109-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce109-108">Description</span></span>

<span data-ttu-id="ce109-109">Wenn [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) für das untergeordnete Element aufgerufen wird, das von " [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) " zurückgegeben wird (mithilfe der \_ Navigations Konstanten navDir firstChild oder navDir \_ LastChild), stimmt das zurückgegebene übergeordnete Element nicht mit dem übergeordneten Element identisch, das im **accNavigate** -Aufruf angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ce109-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the child element returned by [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (using either the NAVDIR\_FIRSTCHILD or NAVDIR\_LASTCHILD navigation constants), the parent element returned does not match the parent element specified in the **accNavigate** call.</span></span>

![Beispiel für eine ungültige MSAA-Implementierung, die ein falsches übergeordnetes Element zurückgibt.](images/accchecker-invalid-msaa-parent.png)

<span data-ttu-id="ce109-111">Dieses Problem kann Navigationsprobleme bei automatisierten Tools verursachen, da das Durchlaufen von Elementen möglicherweise erratisch und unvorhersagbar ist.</span><span class="sxs-lookup"><span data-stu-id="ce109-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="ce109-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="ce109-112">Possible causes</span></span>

<span data-ttu-id="ce109-113">Eine falsche oder ungültige MSAA-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="ce109-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce109-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce109-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce109-115">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="ce109-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="ce109-116">**IAccessible:: get- \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="ce109-116">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




