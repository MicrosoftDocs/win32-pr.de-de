---
title: "\"Zu untergeordnete Elemente\""
description: "\"Zu untergeordnete Elemente\""
ms.assetid: BF667CDC-C1F9-44B2-B64C-CD7F085CA364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e0eee0c29d0d5ee4cdfe66ee5b61aef4b31b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206833"
---
# <a name="toomanychildren"></a><span data-ttu-id="48b49-103">"Zu untergeordnete Elemente"</span><span class="sxs-lookup"><span data-stu-id="48b49-103">TooManyChildren</span></span>

## <a name="text"></a><span data-ttu-id="48b49-104">Text</span><span class="sxs-lookup"><span data-stu-id="48b49-104">Text</span></span>

<span data-ttu-id="48b49-105">Suche nach weiteren neben geordneten Elementen nach dem Suchen nach neben geordneten Elementen beendet {0}</span><span class="sxs-lookup"><span data-stu-id="48b49-105">Stopped looking for additional siblings after finding {0} siblings.</span></span> <span data-ttu-id="48b49-106">Mögliche falsche Struktur</span><span class="sxs-lookup"><span data-stu-id="48b49-106">Possible incorrect tree</span></span>

## <a name="type"></a><span data-ttu-id="48b49-107">type</span><span class="sxs-lookup"><span data-stu-id="48b49-107">Type</span></span>

<span data-ttu-id="48b49-108">Warnung</span><span class="sxs-lookup"><span data-stu-id="48b49-108">Warning</span></span>

## <a name="description"></a><span data-ttu-id="48b49-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48b49-109">Description</span></span>

<span data-ttu-id="48b49-110">Die Elementstruktur kann zyklisch sein, und die Baum Tiefe ist unendlich.</span><span class="sxs-lookup"><span data-stu-id="48b49-110">The element tree might be cyclic and the tree depth infinite.</span></span>

<span data-ttu-id="48b49-111">Dieses Problem kann Navigationsprobleme bei automatisierten Tools verursachen, da Sie einen Zirkel Verweis oder eine Endlosschleife eingeben.</span><span class="sxs-lookup"><span data-stu-id="48b49-111">This issue can cause navigation problems for automated tools because they will enter what appears to be a circular reference or infinite loop.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="48b49-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="48b49-112">Possible causes</span></span>

-   <span data-ttu-id="48b49-113">Der Entwurf der Anwendung oder des Steuer Elements ist möglicherweise zu komplex.</span><span class="sxs-lookup"><span data-stu-id="48b49-113">Application or control design may be too complex.</span></span> <span data-ttu-id="48b49-114">Diese Warnung wird möglicherweise für Listenansicht-Steuerelemente angezeigt, die über eine große Anzahl von Elementen verfügen.</span><span class="sxs-lookup"><span data-stu-id="48b49-114">This warning might be reported for list-view controls that have a large number of items.</span></span> <span data-ttu-id="48b49-115">In diesen Fällen können Sie diese Warnung in der Regel ignorieren.</span><span class="sxs-lookup"><span data-stu-id="48b49-115">In these cases, you can typically ignore this warning.</span></span>
-   <span data-ttu-id="48b49-116">Eine falsche oder ungültige MSAA-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="48b49-116">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48b49-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48b49-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48b49-118">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="48b49-118">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




