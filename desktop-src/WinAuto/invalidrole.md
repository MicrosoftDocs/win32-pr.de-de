---
title: Ungültig
description: Ungültig
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531aa9917bd68b615c2cd2457d7a24bfc4af336c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340818"
---
# <a name="invalidrole"></a><span data-ttu-id="85490-103">Ungültig</span><span class="sxs-lookup"><span data-stu-id="85490-103">InvalidRole</span></span>

## <a name="text"></a><span data-ttu-id="85490-104">Text</span><span class="sxs-lookup"><span data-stu-id="85490-104">Text</span></span>

<span data-ttu-id="85490-105">Der von Get accRole zurückgegebene int-Wert \_ ist keine gültige Rollen Konstante, d. h. das Rollen \_ System.\_\*</span><span class="sxs-lookup"><span data-stu-id="85490-105">The int returned from get\_accRole is not a valid role constant, ie ROLE\_SYSTEM\_\*</span></span>

## <a name="type"></a><span data-ttu-id="85490-106">type</span><span class="sxs-lookup"><span data-stu-id="85490-106">Type</span></span>

<span data-ttu-id="85490-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="85490-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="85490-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85490-108">Description</span></span>

<span data-ttu-id="85490-109">Ein Element meldet eine ungültige MSAA-Rolle.</span><span class="sxs-lookup"><span data-stu-id="85490-109">An element is reporting an invalid MSAA role.</span></span> <span data-ttu-id="85490-110">Beispielsweise gibt die [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) -Methode einen ganzzahligen Wert zurück, der keiner gültigen Objekt Rollen Konstante (z. b \_ . Role System \_ ListItem) zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="85490-110">For example, the [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) method returns an integer value that does not map to a valid object role constant (such as ROLE\_SYSTEM\_LISTITEM).</span></span>

<span data-ttu-id="85490-111">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm und eine Tastatur für die Navigation verlassen, Probleme verursachen, da die Elemente für den Benutzer möglicherweise falsch identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="85490-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because elements may be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="85490-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="85490-112">Possible causes</span></span>

<span data-ttu-id="85490-113">Für das-Element oder das übergeordnete Element ist eine MSAA-Rolle inadäquat festgelegt.</span><span class="sxs-lookup"><span data-stu-id="85490-113">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85490-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="85490-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85490-115">**IAccessible:: get- \_ Zugriffs Rolle**</span><span class="sxs-lookup"><span data-stu-id="85490-115">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="85490-116">**Objekt Rollen**</span><span class="sxs-lookup"><span data-stu-id="85490-116">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




