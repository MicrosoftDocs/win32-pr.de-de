---
title: Accnameshouldnotcontainrole
description: Accnameshouldnotcontainrole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb91eeeb34d484c1f51cd0b7cd2d2947e86abda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714195"
---
# <a name="accnameshouldnotcontainrole"></a><span data-ttu-id="844eb-103">Accnameshouldnotcontainrole</span><span class="sxs-lookup"><span data-stu-id="844eb-103">AccNameShouldNotContainRole</span></span>

## <a name="text"></a><span data-ttu-id="844eb-104">Text</span><span class="sxs-lookup"><span data-stu-id="844eb-104">Text</span></span>

<span data-ttu-id="844eb-105">Der Name des Elements ( {0} ) darf nicht den Text der Rolle des Elements () enthalten. {1}</span><span class="sxs-lookup"><span data-stu-id="844eb-105">Element's Name ({0}) should not contain the text of the Element's Role ({1})</span></span>

## <a name="type"></a><span data-ttu-id="844eb-106">type</span><span class="sxs-lookup"><span data-stu-id="844eb-106">Type</span></span>

<span data-ttu-id="844eb-107">Warnung</span><span class="sxs-lookup"><span data-stu-id="844eb-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="844eb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="844eb-108">Description</span></span>

<span data-ttu-id="844eb-109">Der Name eines Elements enthält die MSAA-Rolle oder den UIA-Steuer Elementtyp.</span><span class="sxs-lookup"><span data-stu-id="844eb-109">The name of an element incorporates its MSAA role or UIA control type.</span></span> <span data-ttu-id="844eb-110">Diese Warnung kann z. b. auftreten, wenn die [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) -Methode –, die verwendet wird, um den MSAA-Namen eines Elements abzurufen – "role \_ System \_ ScrollBar" zurückgibt \_ \* .</span><span class="sxs-lookup"><span data-stu-id="844eb-110">For example, this warning can occur if the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method—which is used to retrieve the MSAA name of an element—returns "ROLE\_SYSTEM\_SCROLLBAR\_\*".</span></span>

<span data-ttu-id="844eb-111">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme haben, da die Rolle zweimal gelesen wird, oder Sie ist möglicherweise für Benutzer nicht erklärbar oder nicht intuitiv.</span><span class="sxs-lookup"><span data-stu-id="844eb-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because the role will be read twice, or it may be unpronounceable or non-intuitive for users.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="844eb-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="844eb-112">Possible causes</span></span>

-   <span data-ttu-id="844eb-113">Dem Element oder seinem übergeordneten Element ist ein falsch zugewiesener Name oder eine Bezeichnung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="844eb-113">The element or its parent has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="844eb-114">Das Element oder das übergeordnete Element verfügt über einen Standardnamen, der nicht auf einen anzeigen Amen überarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="844eb-114">The element or its parent has a default name that has not been revised to a friendly name.</span></span> <span data-ttu-id="844eb-115">Zum Beispiel: Button1.</span><span class="sxs-lookup"><span data-stu-id="844eb-115">For example, button1.</span></span>
-   <span data-ttu-id="844eb-116">Ein Entwickler weiß nicht, dass die Bildschirm Sprachausgaben Lese Namen haben.</span><span class="sxs-lookup"><span data-stu-id="844eb-116">A developer is not aware that screen readers read names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="844eb-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="844eb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="844eb-118">**IAccessible:: get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="844eb-118">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="844eb-119">Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="844eb-119">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




