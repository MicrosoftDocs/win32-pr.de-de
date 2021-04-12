---
title: Variantnotint (CheckState)
description: Variantnotint (CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d951a51ae6aa3f4d9454fc95a56c76cfe30500c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206770"
---
# <a name="variantnotint-checkstate"></a><span data-ttu-id="410b7-103">Variantnotint (CheckState)</span><span class="sxs-lookup"><span data-stu-id="410b7-103">VariantNotInt (CheckState)</span></span>

## <a name="text"></a><span data-ttu-id="410b7-104">Text</span><span class="sxs-lookup"><span data-stu-id="410b7-104">Text</span></span>

<span data-ttu-id="410b7-105">Die von zurückgegebene Variante {0} sollte ein sein, {1} aber ist {2} .</span><span class="sxs-lookup"><span data-stu-id="410b7-105">The variant returned from {0} should be an {1} but is a {2}.</span></span>

## <a name="type"></a><span data-ttu-id="410b7-106">type</span><span class="sxs-lookup"><span data-stu-id="410b7-106">Type</span></span>

<span data-ttu-id="410b7-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="410b7-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="410b7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="410b7-108">Description</span></span>

<span data-ttu-id="410b7-109">Ein Element meldet einen ungültigen MSAA-Zustand.</span><span class="sxs-lookup"><span data-stu-id="410b7-109">An element is reporting an invalid MSAA state.</span></span> <span data-ttu-id="410b7-110">Beispielsweise sollte die [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) -Methode, die zum Abrufen des MSAA-Zustands eines Elements verwendet wird, einen ganzzahligen Wert zurückgeben, der eine der MSAA-Zustands Konstanten darstellt, sondern stattdessen eine andere Variante zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="410b7-110">For example, the [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) method used to retrieve the MSAA state of an element should return an integer value that represents one of the MSAA state constants, but is returning another variant instead.</span></span>

<span data-ttu-id="410b7-111">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme verursachen, da dem Benutzer ein falscher Element Zustand gemeldet werden könnte.</span><span class="sxs-lookup"><span data-stu-id="410b7-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an incorrect element state might be reported to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="410b7-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="410b7-112">Possible causes</span></span>

<span data-ttu-id="410b7-113">Für das-Element oder das übergeordnete Element ist ein MSAA-Zustand unpassend festgelegt.</span><span class="sxs-lookup"><span data-stu-id="410b7-113">The element or its parent has an MSAA state set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="410b7-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="410b7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="410b7-115">**IAccessible:: get- \_ accState**</span><span class="sxs-lookup"><span data-stu-id="410b7-115">**IAccessible::get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[<span data-ttu-id="410b7-116">**Objekt Zustands Konstanten**</span><span class="sxs-lookup"><span data-stu-id="410b7-116">**Object State Constants**</span></span>](object-state-constants.md)
</dt> </dl>

 

 




