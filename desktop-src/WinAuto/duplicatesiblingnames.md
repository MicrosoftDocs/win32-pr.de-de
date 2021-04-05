---
title: Dupligonesiblingnames
description: Dupligonesiblingnames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed5a7caeadc34519988fe8a4a1f12ec4e05ce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714513"
---
# <a name="duplicatesiblingnames"></a><span data-ttu-id="2d938-103">Dupligonesiblingnames</span><span class="sxs-lookup"><span data-stu-id="2d938-103">DuplicateSiblingNames</span></span>

## <a name="text"></a><span data-ttu-id="2d938-104">Text</span><span class="sxs-lookup"><span data-stu-id="2d938-104">Text</span></span>

<span data-ttu-id="2d938-105">Doppelter neben geordneter Name + Rolle \\ "" führt zu {0} \\ Mehrdeutigkeit zwischen Elementen.</span><span class="sxs-lookup"><span data-stu-id="2d938-105">Duplicate sibling Name+Role \\"{0}\\" will cause ambiguity between elements.</span></span>

## <a name="type"></a><span data-ttu-id="2d938-106">type</span><span class="sxs-lookup"><span data-stu-id="2d938-106">Type</span></span>

<span data-ttu-id="2d938-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="2d938-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="2d938-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d938-108">Description</span></span>

<span data-ttu-id="2d938-109">Ein Element hat denselben Namen und dieselbe Rolle bzw. diesen Typ wie ein anderes Element.</span><span class="sxs-lookup"><span data-stu-id="2d938-109">An element has the same Name and Role/ControlType as another element.</span></span>

<span data-ttu-id="2d938-110">Dieses Problem kann Verwirrung verursachen, da Sprachausgaben denselben Text für alle Elemente mit dem gleichen Namen und der gleichen Rolle bzw. dem gleichen "ControlType" lesen.</span><span class="sxs-lookup"><span data-stu-id="2d938-110">This issue can cause confusion because screen readers will read the same text for all the elements with the same Name and Role/ControlType.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="2d938-111">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="2d938-111">Possible causes</span></span>

-   <span data-ttu-id="2d938-112">Der Name des Elements enthält den Text Role/ControlType.</span><span class="sxs-lookup"><span data-stu-id="2d938-112">Element’s name contain Role/ControlType text.</span></span>
-   <span data-ttu-id="2d938-113">Der Name des Elements oder der Name des übergeordneten Elements ist nicht festgelegt oder falsch festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2d938-113">Element’s name or the name of its parent is not set or is set incorrectly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d938-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d938-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d938-115">**IAccessible:: get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="2d938-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="2d938-116">Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2d938-116">Name Property</span></span>](name-property.md)
</dt> <dt>

[<span data-ttu-id="2d938-117">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="2d938-117">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="2d938-118">**Iuiautomationelement. currentname**</span><span class="sxs-lookup"><span data-stu-id="2d938-118">**IUIAutomationElement.CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




