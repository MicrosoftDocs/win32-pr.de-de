---
title: Incorrectroundtrip
description: Incorrectroundtrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f154c0ccc0fff9bb654b94ef9d0807aa459d4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207130"
---
# <a name="incorrectroundtrip"></a><span data-ttu-id="e6149-103">Incorrectroundtrip</span><span class="sxs-lookup"><span data-stu-id="e6149-103">IncorrectRoundTrip</span></span>

## <a name="text"></a><span data-ttu-id="e6149-104">Text</span><span class="sxs-lookup"><span data-stu-id="e6149-104">Text</span></span>

<span data-ttu-id="e6149-105">Rufen Sie auf, um zu über navigieren ((Klicken Sie auf "Wiederholen", um den Vorgang erneut auszuführen:), 1, navDir \_ Next), dann "accNavigate ((Open), 2, navDir \_ Previous"), sollte zurückgegeben werden, um wieder an Sie zu erinnern: (childID = 1)</span><span class="sxs-lookup"><span data-stu-id="e6149-105">Call to accNavigate((Click Snooze to be reminded again in:), 1, NAVDIR\_NEXT), then accNavigate((Open), 2, NAVDIR\_PREVIOUS), should have returned Click Snooze to be reminded again in:(ChildId=1), but returned Click Snooze to be reminded again in:</span></span>

## <a name="type"></a><span data-ttu-id="e6149-106">type</span><span class="sxs-lookup"><span data-stu-id="e6149-106">Type</span></span>

<span data-ttu-id="e6149-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="e6149-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="e6149-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6149-108">Description</span></span>

<span data-ttu-id="e6149-109">durch die Verwendung von [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) zum Durchlaufen der Elementstruktur des Überprüfungs Ziels wird das gleiche Start Element nicht zurückgegeben, wenn die Richtung der Traversierung umgekehrt wird.</span><span class="sxs-lookup"><span data-stu-id="e6149-109">using [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) to traverse the element tree of the verification target does not return the same starting element when the direction of traversal is reversed.</span></span>

![Beispiel für eine ungültige MSAA-Implementierung, die eine falsche Roundtrip-Navigation verursacht hat](images/accchecker-invalid-round-trip.png)

<span data-ttu-id="e6149-111">Dieses Problem kann Navigationsprobleme bei automatisierten Tools verursachen, da das Durchlaufen von Elementen möglicherweise erratisch und unvorhersagbar ist.</span><span class="sxs-lookup"><span data-stu-id="e6149-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="e6149-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="e6149-112">Possible causes</span></span>

<span data-ttu-id="e6149-113">Eine falsche oder ungültige MSAA-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="e6149-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6149-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6149-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6149-115">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="e6149-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




