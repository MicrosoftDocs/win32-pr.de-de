---
title: Elementschildhasdifferenentparent
description: Elementschildhasdifferenentparent
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ea0f0ec7708f91d407f1fa7a55fa59a813234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311520"
---
# <a name="elementschildhasdifferentparent"></a><span data-ttu-id="3d5f2-103">Elementschildhasdifferenentparent</span><span class="sxs-lookup"><span data-stu-id="3d5f2-103">ElementsChildHasDifferentParent</span></span>

## <a name="text"></a><span data-ttu-id="3d5f2-104">Text</span><span class="sxs-lookup"><span data-stu-id="3d5f2-104">Text</span></span>

<span data-ttu-id="3d5f2-105">Das untergeordnete Element () des Elements {0} hat ein anderes {1} übergeordnetes Element () als Element</span><span class="sxs-lookup"><span data-stu-id="3d5f2-105">Element's child({0}) has different parent({1}) than element</span></span>

## <a name="type"></a><span data-ttu-id="3d5f2-106">type</span><span class="sxs-lookup"><span data-stu-id="3d5f2-106">Type</span></span>

<span data-ttu-id="3d5f2-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="3d5f2-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="3d5f2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d5f2-108">Description</span></span>

<span data-ttu-id="3d5f2-109">Dieser Fehler zeigt an, dass die untergeordneten Elemente, wenn [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) für die untergeordneten Elemente des Target-Elements aufgerufen wird, kein konsistentes übergeordnetes Element melden.</span><span class="sxs-lookup"><span data-stu-id="3d5f2-109">This error indicates that, when [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the children of the target element, the children do not report a consistent parent.</span></span>

![ein Beispiel für die untergeordneten Elemente eines Elements, das eine inkonsistente übergeordnete Meldung meldet](images/accchecker-inconsistent-parent.png)

<span data-ttu-id="3d5f2-111">Dieses Problem kann Navigationsprobleme bei automatisierten Tools verursachen, da das Durchlaufen von Elementen möglicherweise erratisch und unvorhersagbar ist.</span><span class="sxs-lookup"><span data-stu-id="3d5f2-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="3d5f2-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="3d5f2-112">Possible causes</span></span>

<span data-ttu-id="3d5f2-113">Eine falsche oder ungültige MSAA-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="3d5f2-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d5f2-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d5f2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d5f2-115">**Accessiblechildren**</span><span class="sxs-lookup"><span data-stu-id="3d5f2-115">**AccessibleChildren**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




