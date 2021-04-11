---
title: Variantnotint (checkrole)
description: Variantnotint (checkrole)
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdca744468d863ff1ab95b66edf5b3ff1f40b48f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310151"
---
# <a name="variantnotint-checkrole"></a><span data-ttu-id="67a36-103">Variantnotint (checkrole)</span><span class="sxs-lookup"><span data-stu-id="67a36-103">VariantNotInt (CheckRole)</span></span>

## <a name="text"></a><span data-ttu-id="67a36-104">Text</span><span class="sxs-lookup"><span data-stu-id="67a36-104">Text</span></span>

<span data-ttu-id="67a36-105">Die von zurückgegebene Variante {0} sollte ein sein, {1} aber ist {2} .</span><span class="sxs-lookup"><span data-stu-id="67a36-105">The variant returned from {0} should be an {1} but is a {2}.</span></span>

## <a name="type"></a><span data-ttu-id="67a36-106">type</span><span class="sxs-lookup"><span data-stu-id="67a36-106">Type</span></span>

<span data-ttu-id="67a36-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="67a36-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="67a36-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67a36-108">Description</span></span>

<span data-ttu-id="67a36-109">Ein Element meldet eine ungültige MSAA-Rolle.</span><span class="sxs-lookup"><span data-stu-id="67a36-109">An element is reporting an invalid MSAA role.</span></span> <span data-ttu-id="67a36-110">Beispielsweise sollte die [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) -Methode, die zum Abrufen der MSAA-Rolle eines Elements verwendet wird, einen ganzzahligen Wert zurückgeben, der eine der MSAA-Rollen Konstanten darstellt, sondern stattdessen eine andere Variante zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="67a36-110">For example, the [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) method used to retrieve the MSAA role of an element should return an integer value that represents one of the MSAA role constants, but is returning another variant instead.</span></span>

<span data-ttu-id="67a36-111">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm und eine Tastatur für die Navigation verlassen, Probleme verursachen, da die Elemente für den Benutzer möglicherweise falsch identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="67a36-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because elements may be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="67a36-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="67a36-112">Possible causes</span></span>

<span data-ttu-id="67a36-113">Für das-Element oder das übergeordnete Element ist eine MSAA-Rolle inadäquat festgelegt.</span><span class="sxs-lookup"><span data-stu-id="67a36-113">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67a36-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67a36-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67a36-115">**IAccessible:: get- \_ Zugriffs Rolle**</span><span class="sxs-lookup"><span data-stu-id="67a36-115">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="67a36-116">**Objekt Rollen**</span><span class="sxs-lookup"><span data-stu-id="67a36-116">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




