---
title: Elementhasnoname
description: Elementhasnoname
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc9af7e1ad0a62f35edb88102b68bfa6de3d5c28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311525"
---
# <a name="elementhasnoname"></a><span data-ttu-id="bb18f-103">Elementhasnoname</span><span class="sxs-lookup"><span data-stu-id="bb18f-103">ElementHasNoName</span></span>

## <a name="text"></a><span data-ttu-id="bb18f-104">Text</span><span class="sxs-lookup"><span data-stu-id="bb18f-104">Text</span></span>

<span data-ttu-id="bb18f-105">Das Element hat keinen Namen.</span><span class="sxs-lookup"><span data-stu-id="bb18f-105">Element has no name</span></span>

## <a name="type"></a><span data-ttu-id="bb18f-106">type</span><span class="sxs-lookup"><span data-stu-id="bb18f-106">Type</span></span>

<span data-ttu-id="bb18f-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="bb18f-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="bb18f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb18f-108">Description</span></span>

<span data-ttu-id="bb18f-109">Ein Element hat keinen Namen.</span><span class="sxs-lookup"><span data-stu-id="bb18f-109">An element does not have a name.</span></span> <span data-ttu-id="bb18f-110">Beispielsweise ist für das-Element der accName nicht implementiert, und eine leere Zeichenfolge wird zurückgegeben, wenn die [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) -Methode verwendet wird, um den MSAA-Namen des Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bb18f-110">For example, the element does not have accName implemented and an empty string is returned when the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method is used to retrieve the MSAA name of the element.</span></span>

<span data-ttu-id="bb18f-111">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme verursachen, da ein Element für den Benutzer fälschlicherweise identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bb18f-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="bb18f-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="bb18f-112">Possible causes</span></span>

-   <span data-ttu-id="bb18f-113">Das Element oder das übergeordnete Element hat keinen Namen oder keine Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="bb18f-113">The element or its parent has no name or label.</span></span>
-   <span data-ttu-id="bb18f-114">Dem-Element wird eine [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) zugewiesen, die vorschlägt, dass das Element einen Namen hat.</span><span class="sxs-lookup"><span data-stu-id="bb18f-114">The element is assigned an [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) that suggests the element have a name.</span></span>
-   <span data-ttu-id="bb18f-115">Das Element, das den Fokus besitzt, sollte keinen Fokus erhalten.</span><span class="sxs-lookup"><span data-stu-id="bb18f-115">The element that has focus should not receive focus.</span></span> <span data-ttu-id="bb18f-116">Beispielsweise eine Bezeichnung oder ein deaktiviertes Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="bb18f-116">For example, a label or a disabled control.</span></span>
-   <span data-ttu-id="bb18f-117">Ein unsichtbares Steuerelement hat den Fokus erhalten.</span><span class="sxs-lookup"><span data-stu-id="bb18f-117">An invisible control has received focus.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb18f-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb18f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb18f-119">**IAccessible:: get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="bb18f-119">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="bb18f-120">Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bb18f-120">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




