---
title: Controlschuldhavevalue
description: Controlschuldhavevalue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b078712319ffcfde386df519837ba467ca2fcf4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206922"
---
# <a name="controlshouldhavevalue"></a><span data-ttu-id="a4b99-103">Controlschuldhavevalue</span><span class="sxs-lookup"><span data-stu-id="a4b99-103">ControlShouldHaveValue</span></span>

## <a name="text"></a><span data-ttu-id="a4b99-104">Text</span><span class="sxs-lookup"><span data-stu-id="a4b99-104">Text</span></span>

<span data-ttu-id="a4b99-105">Ein Steuerelement mit der Rolle {0} muss über einen Wert verfügen, aber get \_ accValue ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a4b99-105">A control with role of {0} should have a value but get\_accValue is not implemented</span></span>

## <a name="type"></a><span data-ttu-id="a4b99-106">type</span><span class="sxs-lookup"><span data-stu-id="a4b99-106">Type</span></span>

<span data-ttu-id="a4b99-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="a4b99-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="a4b99-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4b99-108">Description</span></span>

<span data-ttu-id="a4b99-109">Ein Element stellt auf der Grundlage der zugewiesenen MSAA-Rolle nicht erwartungsgemäß einen Wert bereit. Dies impliziert, dass das Element nicht über die [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) -Methode verfügt.</span><span class="sxs-lookup"><span data-stu-id="a4b99-109">An element does not supply a value as expected based on the assigned MSAA role, implying that the element does not have the [**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) method implemented.</span></span> <span data-ttu-id="a4b99-110">Die folgenden MSAA-Rollen sollten beispielsweise alle einen Wert bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a4b99-110">For example, the following MSAA roles should all supply a value.</span></span>

-   <span data-ttu-id="a4b99-111">Kombinations \_ Feld "Rollen System" \_</span><span class="sxs-lookup"><span data-stu-id="a4b99-111">ROLE\_SYSTEM\_COMBOBOX</span></span>
-   <span data-ttu-id="a4b99-112">Rollen \_ System- \_ IPAddress</span><span class="sxs-lookup"><span data-stu-id="a4b99-112">ROLE\_SYSTEM\_IPADDRESS</span></span>
-   <span data-ttu-id="a4b99-113">Rollen \_ System \_ Link</span><span class="sxs-lookup"><span data-stu-id="a4b99-113">ROLE\_SYSTEM\_LINK</span></span>
-   <span data-ttu-id="a4b99-114">Rollen \_ System \_ outlineitem</span><span class="sxs-lookup"><span data-stu-id="a4b99-114">ROLE\_SYSTEM\_OUTLINEITEM</span></span>
-   <span data-ttu-id="a4b99-115">Rollen \_ System- \_ ProgressBar</span><span class="sxs-lookup"><span data-stu-id="a4b99-115">ROLE\_SYSTEM\_PROGRESSBAR</span></span>
-   <span data-ttu-id="a4b99-116">\_ \_ Schieberegler für Rollen System</span><span class="sxs-lookup"><span data-stu-id="a4b99-116">ROLE\_SYSTEM\_SLIDER</span></span>
-   <span data-ttu-id="a4b99-117">\_SpinButton für Rollen System \_</span><span class="sxs-lookup"><span data-stu-id="a4b99-117">ROLE\_SYSTEM\_SPINBUTTON</span></span>
-   <span data-ttu-id="a4b99-118">Rollen \_ System- \_ Scrollleiste</span><span class="sxs-lookup"><span data-stu-id="a4b99-118">ROLE\_SYSTEM\_SCROLLBAR</span></span>
-   <span data-ttu-id="a4b99-119">Rollen \_ System \_ Text</span><span class="sxs-lookup"><span data-stu-id="a4b99-119">ROLE\_SYSTEM\_TEXT</span></span>

<span data-ttu-id="a4b99-120">Dieses Problem ist ein Problem für Personen, die sich auf einen Bildschirm und eine Tastatur für die Navigation verlassen, da ein Element mit einem systeminternen Wert in der Lage sein muss, diesen Wert an einen Benutzer zu melden.</span><span class="sxs-lookup"><span data-stu-id="a4b99-120">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because an element that has an intrinsic value must be able to report that value to a user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="a4b99-121">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="a4b99-121">Possible causes</span></span>

<span data-ttu-id="a4b99-122">Für das-Element oder das übergeordnete Element ist eine MSAA-Rolle inadäquat festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a4b99-122">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4b99-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4b99-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4b99-124">**IAccessible:: get- \_ Zugriffs Rolle**</span><span class="sxs-lookup"><span data-stu-id="a4b99-124">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="a4b99-125">**Objekt Rollen**</span><span class="sxs-lookup"><span data-stu-id="a4b99-125">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




