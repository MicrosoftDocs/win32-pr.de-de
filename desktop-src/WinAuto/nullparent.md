---
title: Nullparent
description: Nullparent
ms.assetid: F9563D73-66EF-4C66-8783-B034AA7A212E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 765217f8d2d46645358d590c5a93310b04da01b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309868"
---
# <a name="nullparent"></a><span data-ttu-id="3dd35-103">Nullparent</span><span class="sxs-lookup"><span data-stu-id="3dd35-103">NullParent</span></span>

## <a name="text"></a><span data-ttu-id="3dd35-104">Text</span><span class="sxs-lookup"><span data-stu-id="3dd35-104">Text</span></span>

<span data-ttu-id="3dd35-105">Das übergeordnete Element ist NULL.</span><span class="sxs-lookup"><span data-stu-id="3dd35-105">Elements parent is NULL</span></span>

## <a name="type"></a><span data-ttu-id="3dd35-106">type</span><span class="sxs-lookup"><span data-stu-id="3dd35-106">Type</span></span>

<span data-ttu-id="3dd35-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="3dd35-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="3dd35-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3dd35-108">Description</span></span>

<span data-ttu-id="3dd35-109">NULL wird zurückgegeben, wenn [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) für das Element aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3dd35-109">NULL is returned when [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the element.</span></span> <span data-ttu-id="3dd35-110">Die **get \_ accParent** -Methode sollte NULL nur zurückgeben, wenn Sie für das Stamm Element des Überprüfungs Ziels aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3dd35-110">The **get\_accParent** method should return NULL only when called on the root element of the verification target.</span></span>

<span data-ttu-id="3dd35-111">Dieses Problem kann Navigationsprobleme bei automatisierten Tools verursachen, da das Durchlaufen von Elementen möglicherweise erratisch und unvorhersagbar ist.</span><span class="sxs-lookup"><span data-stu-id="3dd35-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="3dd35-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="3dd35-112">Possible causes</span></span>

<span data-ttu-id="3dd35-113">Eine falsche oder ungültige MSAA-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="3dd35-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dd35-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3dd35-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dd35-115">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="3dd35-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="3dd35-116">**IAccessible:: get- \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="3dd35-116">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




